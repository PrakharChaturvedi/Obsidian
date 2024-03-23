### Back End Information - How MVC (model view controller) is working 
- The `ApiClient` class handles API requests, the `PopularProductRepo` acts as a repository for fetching and handling data, and the `PopularProductController` manages the application logic related to popular products. The `Product` and `ProductModel` classes represent the structure of the data being handled in the application. 

### In which file I have what?
- main.dart -> Mail file of the whole project
- MainFoodPage.dart -> Main screen of application 
	- Calls the following
		- _FoodPageBody.dart -> Has page view container for both Recommended and product list of dishes or items.
		- AppColumn.dart -> Has rating and details about the items/products. 
- 