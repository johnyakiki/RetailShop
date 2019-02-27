# RetailShop

1- Create two tables:
	retail_user    : user_id, first_name, last_name, level_id, join_date
	retail_product : product_id, product_type, prodcut_desc, product_price

level_id : indicate if the user is an employee of the store, affiliate of the store or customer.
product_type : indicate if the product is grocerie or not.

2- Create Retail Shop using netBeans:

Create new web application, new java application and new EJB.

3- Create a login jsp :

user will login using username and password to the retail shop in the login.jsp
When login button is clicked it will submit the form and go to the VerifyLogin servlet where we check if the user entered 
correct data.

If right data entered needed paramters ( username , password ) will be passed to the ejb that contains the method 
getUserInfo that will select user_id and level_id and set them in the session for further use and return to ShopMenu.jsp using 
RequestDispatcher.

4- Create ShopMenu.jsp :

Here the user will choose desired product to purchase . When purchase button is clicked it will submit the form and go to 
the servlet PurchaseOrder.
level_id, user_id, product_type, product_price will be passed to the method 
PurchaseOrder(String level_id, String user_id, int product_type, int product_price ) where level_id will be checked and related 
discount will be applied.
