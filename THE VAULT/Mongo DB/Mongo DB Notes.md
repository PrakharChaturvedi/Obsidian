- It is a non-rational document database that provides support for JSON-like storage. It is schemeless and highly scalable. It has databases which has collections and documents. We geta unique ID for each document, which is a unique identified ID/Unique identifier.
- Example : 
	- Employee --> COLLECTION (Column)
		{
			`"name" : "Prakhar"`,
			`"age" : "20"`,
			`"city" : "Kanpur"`,
			`"Identity"` : {                                           | -----------------------, |
						`"aadhar" : "123456789"`,   |      Example of a         |
						`"pan" : "TUEF0123"`,          |   Nested Document    |
					 }                                             | -----------------------, |
		} 

- Case : 
	- If in a new entry, additional fields are required then we can just add the fields in the above.
	- Collection remains the same while the document changes.
	- It has less relations hence faster, and data is stored together.

- BSON :
	- Binary Structure encodes type and length information, which allows it to be traversed much more quickly compared to JSON.

## Some basic commands for monogsh shell :
- `show dbs` : Shows all the databases, displays a list of all the available databases.
- `use database_name` : The command creates a new database if it doesn't exists, otherwise it will return the existing database.
- `show collections` : The command creates a new collection if it doesn't exists, otherwise it will return the existing collection in the specific dbs.
- `load(myScript.js)` : Runs the JavaScript File.
- `db.coll.drop()` : Removes the collection and its index definitions.
- `db.dropDatabase()` : Double check that you are *NOT* on the PROD cluster. 
- Collection functions :
	- `db.coll.stats()`
	- `db.coll.storageSize()`
	- `db.coll.totalIndexSize()`
	- `db.coll.totalSize()`
	- `db.coll.validate({full: true})`
	- `db.coll.renameCollection("new_coll", true)`: 2nd parameter to drop the target collection if exists.
- Create Collection :
	- ```db.createCollection("contacts", {
	   validator: {$jsonSchema: {
	      bsonType: "object",
	      required: ["phone"],
	      properties: {
	         phone: {
	            bsonType: "string",
	            description: "must be a string and is required"
	         },
	         email: {
	            bsonType: "string",
	            pattern: "@mongodb\.com$",
	            description: "must be a string and match the regular expression pattern"
	         },
	         status: {
	            enum: [ "Unknown", "Incomplete" ],
	            description: "can only be one of the enum values"
	         }
	      }
	   }}
	})``` : Create collection with a $jsonschema
## CRUD operations : 
#### <font color="#ffc000">Create</font> 
- `db.coll.insertOne({name: "Prakhar"})` : Insert a single document into the collection "coll" with the field "name" set to "Prakhar".
- `db.coll.insertMany([{name: "Prakhar"}, {name:"Alex"}])`  : Insert multiple documents into the collection "coll" with the field "name" set to "Prakhar" and "Alex". The insertion is ordered, meaning if an error occurs, the operation will stop after the first error. Ordered bulk insert
- `db.coll.insertMany([{name: "Prakhar"}, {name:"Alex"}], {ordered: false})` : Insert multiple documents into the collection "coll" with the field "name" set to "Prakhar" and "Alex".The insertion is unordered, meaning if an error occurs, the operation will continue with the remaining documents. Unordered bulk insert
- `db.coll.insertOne({date: ISODate()})` : Insert a single document into the collection "coll" with the field "date" set to the current date and time in ISO format.
- `db.coll.insertOne({name: "Prakhar"}, {"writeConcern": {"w": "majority", "wtimeout": 5000}})` : Insert a single document into the collection "coll" with the field "name" set to "Prakhar". Specifies a write concern with the majority level and a timeout of 5000 milliseconds.

#### <font color="#ffc000">Read</font>
-> <font color="#00b050">db.collection.find(query, projection, options)</font>
- `db.coll.findOne()` : Find a single document from the collection "coll". 
- `db.coll.find()` : Find all documents in the collection "coll" and return a cursor. Display up to 20 results. Use "it" to display more results.
- `db.coll.find().pretty()` : Find all documents in the collection "coll" and display them in a formatted way.
- `db.coll.find({name: "Prakhar", age: 32})` : Find documents in the collection "coll" where the "name" field is "Max" and the "age" field is 32. Implicit logical "AND".
- `db.coll.find({date: ISODate("2020-09-25T13:57:17.180Z")})` : Find documents in the collection "coll" where the "date" field matches the specified ISO date.
- `db.coll.find({name: "Prakhar", age: 32}).explain("executionStats")` : Provide execution statistics for the query matching documents where "name" is "Max" and "age" is 32.
- `db.coll.distinct("name")` : Find distinct values of the "name" field in the collection "coll".
------------ 
- COUNT
	- `db.coll.countDocuments({age: 32})` : Count documents in the collection "coll" where the "age" field is 32. Uses an aggregation pipeline for an accurate count.
	- `db.coll.estimatedDocumentCount()` : Estimate the count of documents in the collection "coll" based on collection metadata.
- ------------ 
- COMPARISION
	- `db.coll.find({"year": {$gt: 1970}})` : Find documents in the collection "coll" where the "year" field is greater than 1970.
	- `db.coll.find({"year": {$gte: 1970}})` : Find documents in the collection "coll" where the "year" field is greater than or equal to 1970.
	- `db.coll.find({"year": {$lt: 1970}})` : Find documents in the collection "coll" where the "year" field is less than 1970.
	- `db.coll.find({"year": {$lte: 1970}})` :   Find documents in the collection "coll" where the "year" field is less than or equal to 1970.
	- `db.coll.find({"year": {$ne: 1970}})` : Find documents in the collection "coll" where the "year" field is not equal to 1970.
	- `db.coll.find({"year": {$in: [1958, 1959]}})` : Find documents in the collection "coll" where the "year" field is in the specified array.
	- `db.coll.find({"year": {$nin: [1958, 1959]}})` : Find documents in the collection "coll" where the "year" field is not in the specified array.
------------ 
- LOGICAL 
	- `db.coll.find({name:{$not: {$eq: "Prakhar"}}})` : Find documents in the collection "coll" where the "name" field is not equal to "Max".
	- `db.coll.find({$or: [{"year" : 1958}, {"year" : 1959}]})` :  Find documents in the collection "coll" where the "year" field is 1958 or 1959.
	- `db.coll.find({$nor: [{price: 1.99}, {sale: true}]})` : Find documents in the collection "coll" where neither "price" is 1.99 nor "sale" is true.
	- ````db.coll.find({
		  $and: [
		    {$or: [{qty: {$lt :10}}, {qty :{$gt: 50}}]},
		    {$or: [{sale: true}, {price: {$lt: 5 }}]}
		  ]
		})```` : Find documents in the collection "coll" based on multiple logical conditions.
------------ 
- ELEMENT
	- `db.coll.find({name: {$exists: true}})` : Find documents in the collection "coll" where the "name" field exists. 
	- `db.coll.find({"zipCode": {$type: 2 }})` : Find documents in the collection "coll" where the "zipCode" field has the type 2 (string).
	- `db.coll.find({"zipCode": {$type: "string"}})` : Find documents in the collection "coll" where the "zipCode" field has the type "string".

-------------------
- AGGREGATION PIPELINE
	- ````db.coll.aggregate([
	  {$match: {status: "A"}},
	  {$group: {_id: "$cust_id", total: {$sum: "$amount"}}},
	  {$sort: {total: -1}}
	])```` : Perform an aggregation pipeline to match documents with status "A", group them by "cust_id", and calculate the total amount.
-----------------
- Text search with a "text" index
	- `db.coll.find({$text: {$search: "cake"}}, {score: {$meta: "textScore"}}).sort({score: {$meta: "textScore"}})` :  Perform a text search for "cake" using a "text" index, sorting by text score.
------------------
-  REGEX
	- `db.coll.find({name: /^Prakhar/})` : Find documents in the collection "coll" where the "name" field starts with "Max".
	- `db.coll.find({name: /^Prakhar$/i})` : Find documents in the collection "coll" where the "name" field is "Max", case insensitive.
------------------
- ARRRAY
	- `db.coll.find({tags: {$all: ["Realm", "Charts"]}})` : Find documents in the collection "coll" where all specified tags are present in the "tags" array. 
	- `db.coll.find({field: {$size: 2}})` : Find documents in the collection "coll" where the "field" array has a size of 2. Not recommended to index, prefer storing the size of the array and update it.
	- `db.coll.find({results: {$elemMatch: {product: "xyz", score: {$gte: 8}}}})` : Find documents in the collection "coll" where at least one element in the "results" array matches the specified conditions.
-------------
- PROJECTIONS
	- `db.coll.find({"x": 1}, {"actors": 1})` : Retrieve documents from the collection "coll" including only the "actors" field along with the default "_id" field. 
	- `db.coll.find({"x": 1}, {"actors": 1, "_id": 0})` : Retrieve documents from the collection "coll" excluding the "_id" field and including only the "actors" field. 
	- `db.coll.find({"x": 1}, {"actors": 0, "summary": 0})` : Retrieve documents from the collection "coll" excluding both "actors" and "summary" fields.
-------------
- SORT, SKIP, LIMIT
	- `db.coll.find({}).sort({"year": 1, "rating": -1}).skip(10).limit(3)` : Find all documents in the collection "coll", sort them by "year" ascending and "rating" descending, skip 10 documents, and limit to 3 documents. 
-------------
- READ CONCERN 
	- `db.coll.find().readConcern("majority")` : Specify a read concern of "majority" for the query operation. 

#### <font color="#ffc000">Update</font>
- ARRAY
	- `db.coll.updateOne({"_id": 1}, {$push :{"array": 1}})` : Add the value 1 to the "array" field in the document with "_id" equal to 1.
	- `db.coll.updateOne({"_id": 1}, {$pull :{"array": 1}})` : Remove the value 1 from the "array" field in the document with "_id" equal to 1.
	- `db.coll.updateOne({"_id": 1}, {$addToSet :{"array": 2}})` : Add the value 2 to the "array" field if it does not already exist in the document with "_id" equal to 1.
	- `db.coll.updateOne({"_id": 1}, {$pop: {"array": 1}})` : Remove the last element from the "array" field in the document with "_id" equal to 1.
	- `db.coll.updateOne({"_id": 1}, {$pop: {"array": -1}})` : Remove the first element from the "array" field in the document with "_id" equal to 1.
	- `db.coll.updateOne({"_id": 1}, {$pullAll: {"array" :[3, 4, 5]}})` : Remove multiple specified values from the "array" field in the document with "_id" equal to 1.
	- `db.coll.updateOne({"_id": 1}, {$push: {"scores": {$each: [90, 92]}}})` : Add multiple values to the "scores" array field in the document with "_id" equal to 1.
	- `db.coll.updateOne({"_id": 2}, {$push: {"scores": {$each: [40, 60], $sort: 1}}})` : Add multiple values to the "scores" array field in the document with "_id" equal to 2, sorting the array.
	- `db.coll.updateOne({"_id": 1, "grades": 80}, {$set: {"grades.$": 82}})` : Update the value within the "grades" array where the value is 80 to 82 in the document with "_id" equal to 1.
	- `db.coll.updateMany({}, {$inc: {"grades.$[]": 10}})` : Increment all values within the "grades" array in all documents.
	- `db.coll.updateMany({}, {$set: {"grades.$[element]": 100}}, {multi: true, arrayFilters: [{"element": {$gte: 100}}]})` : Set all values greater than or equal to 100 within the "grades" array to 100 in all documents.
	-------------
- FINDONEANDUPDATE
	- `db.coll.findOneAndUpdate({"name": "Max"}, {$inc: {"points": 5}}, {returnNewDocument: true})` : Find a document with the name "Max" and increment the "points" field by 5. Return the updated document.
	-------------
- UPSERT
	- `db.coll.updateOne({"_id": 1}, {$set: {item: "apple"}, $setOnInsert: {defaultQty: 100}}, {upsert: true})` : Update a document with "_id" equal to 1 by setting the "item" field to "apple" and setting the "defaultQty" field to 100 on insert if the document does not exist.
-------------
- REPLACE
	- `db.coll.replaceOne({"name": "Max"}, {"firstname": "Maxime", "surname": "Beugnet"})` : Replace a document with the name "Max" with a new document containing the fields "firstname" set to "Maxime" and "surname" set to "Beugnet".
-------------
- WRITE CONCERN
	- `db.coll.updateMany({}, {$set: {"x": 1}}, {"writeConcern": {"w": "majority", "wtimeout": 5000}})` : Update all documents in the collection by setting the field "x" to 1, with a write concern of "majority" and a timeout of 5000 milliseconds.

#### <font color="#ffc000">Delete</font> 
- DELETE ONE
  - `db.coll.deleteOne({name: "Max"})` : Delete a single document from the collection "coll" where the "name" field is "Max".
- DELETE MANY
	- `db.coll.deleteMany({name: "Max"}, {"writeConcern": {"w": "majority", "wtimeout": 5000}})` : Delete multiple documents from the collection "coll" where the "name" field is "Max", specifying a write concern of "majority" and a timeout of 5000 milliseconds.
	- `db.coll.deleteMany({})` : WARNING! Deletes all documents from the collection "coll" but does not delete the collection itself and its index definitions.
- FIND-ONE-AND-DELETE
	- `db.coll.findOneAndDelete({"name": "Max"})` : Find a document with the name "Max" and delete it. Returns the deleted document.




## 