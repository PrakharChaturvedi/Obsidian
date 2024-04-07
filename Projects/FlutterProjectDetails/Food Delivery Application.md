##### File Structure of Food App :
``` markdown-tree File Structure
Client (Flutter Application) => 
	 lib :
		 Controllers
			 popular_product_repo.dart
		 Data
			 API
				 api_client.dart
			Repository 
				popular_product_repo.dart
		 Helper
			 Dependencies.dart
		 Models
			 product_model.dart
		 Pages
			 Food
				 popular_food_details.dart
				 recommended_food.dart
			 Home
				 food_page_body.dart
				 main_food_page.dart
		 Routes
			 route_helper.dart
		 Testing_Servers
			 testing_api.dart
		 Utils   
			 app_constants.dart
			 colors.dart
			 dimensions.dart
		Widgets 
			app_column.dart
			app_icon.dart
			big_text.dart
			expandable_text.dart
			icon_and_text_widget.dart
			small_text.dart
	main.dart


Server (Node.js)
	Node.js

Database (MongoDB)
	Products [Table 1 stores prduct details]
```


##### Application Information - How MVC (model view controller) is working 
- The `ApiClient` class handles API requests, the `PopularProductRepo` acts as a repository for fetching and handling data, and the `PopularProductController` manages the application logic related to popular products. The `Product` and `ProductModel` classes represent the structure of the data being handled in the application. 

###### Features 
- Home page
- Sign in and Sign up
- Shopping Cart
- Local cart history page
- Server cart history page
- Profile Page
- Popular Food Page
- Recommended Food Page
- Order more function
- Go to Sign in page
- Address page
- Google map page
- Search Address
- Backend (Backend shows users orders, total orders, users' info, payment info, etc...)
- Creating new items
- UPI Payment page with database sync 




