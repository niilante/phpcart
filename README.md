# Documentation of phpcart 


I've built this shopping cart after completing the google form where I had to completely answer your interview questions. This project includes the php cart you asked for

This is a proof-of-concept and is not intended to replace any existing server-side techniques. 

Bear in mind that there are a few things you need to change on the main `index.php` file, namely:

* Adding Products  to Shopping Cart

First, I created the product catalog page by listing products from the database. The following code retrieves the list of products from the database and displays them in a grid view. Each product has the ‘Add to cart’ option to place it into the cart.

On clicking the ‘Add to cart’ button, I added the selected product id and its quantity into the shopping cart. I used PHP SESSION to store the cart items. The following code shows a switch case used for adding products to the cart. When I then added the same product multiple times in the cart, the cart item quantity will be incremented.

* Removing or Clearing Cart Item

In this test phase, I allow users to remove each item from the cart by using the ‘Remove Item’ link in each row. Also, I allow the users to clear the whole cart by using ‘Empty Cart’ option. On clicking ‘Remove Item’, we call remove action with the reference of the item code to clear the particular item of the cart session. We use PHP unset() to clear the cart session.

* Import the following SQL script for creating a product table and   load your own data to show in your catalog page.

  `CREATE TABLE IF NOT EXISTS `tblproduct` (
  `id` int(8) NOT NULL AUTO_INCREMENT,
  `name` varchar(255) NOT NULL,
  `code` varchar(255) NOT NULL,
  `image` text NOT NULL,
  `price` double(10,2) NOT NULL,
  PRIMARY KEY (`id`),
  UNIQUE KEY `product_code` (`code`)
)`


NB: All these goes down in your phpmyadmin panel

Hope you find this useful.
