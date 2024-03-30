- It is a non-rational document database that provides support for JSON-like storage. It is schemeless and highly scalable. It has databases which has collections and documents. We geta unique ID for each document, which is a unique identified ID/Unique identifier.
- Example : 
	- Employee --> COLLECTION (Column)
		{
			"name" : "Prakhar",
			"age" : "20",
			"city" : "Kanpur",
			"Identity" : {                                           |------------------------|
						"aadhar" : "123456789",   |     Example of a        |
						"pan" : "TUEF0123",          |  Nested Document   |
					 }                                           |------------------------|
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
- `load(myScript.js)` : Runs the JavaScript File


## CRUD operations : 
#### Create ->
- `db.coll.insertOne({name: "Prakhar"})` : Insert a single document into the collection "coll" with the field "name" set to "Prakhar".
- `db.coll.insertMany([{name: "Prakhar"}, {name:"Alex"}])`  : Insert multiple documents into the collection "coll" with the field "name" set to "Prakhar" and "Alex". The insertion is ordered, meaning if an error occurs, the operation will stop after the first error. Ordered bulk insert
- `db.coll.insertMany([{name: "Prakhar"}, {name:"Alex"}], {ordered: false})` : Insert multiple documents into the collection "coll" with the field "name" set to "Prakhar" and "Alex".The insertion is unordered, meaning if an error occurs, the operation will continue with the remaining documents. Unordered bulk insert
- `db.coll.insertOne({date: ISODate()})` : Insert a single document into the collection "coll" with the field "date" set to the current date and time in ISO format.
- `db.coll.insertOne({name: "Prakhar"}, {"writeConcern": {"w": "majority", "wtimeout": 5000}})` : Insert a single document into the collection "coll" with the field "name" set to "Prakhar". Specifies a write concern with the majority level and a timeout of 5000 milliseconds.

#### Read ->
- 


