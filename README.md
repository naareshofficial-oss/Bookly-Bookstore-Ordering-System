# Bookly -- Online Bookstore Management System

## Project Overview

Bookly is a PHP-based online bookstore management system that allows
customers to browse books, add products to a shopping cart, place
orders, and contact the store. It also provides an administration area
for managing products, users, customer orders, and messages.

This project uses PHP for server-side functionality and MySQL for
database management.

## Technologies Used

-   **Frontend:** HTML, CSS, JavaScript
-   **Backend:** PHP
-   **Database:** MySQL
-   **Local Development Environment:** XAMPP (Apache and MySQL)
-   **Icons:** Font Awesome

## Features

### Customer Features

-   User registration and login
-   Browse available books
-   Search and view products
-   Add books to a shopping cart
-   Update cart quantities and remove items
-   Checkout and place orders
-   View order information
-   Send messages through the contact page
-   View the About page

### Admin Features

-   Admin login and dashboard
-   View dashboard statistics
-   Add, update, and delete books
-   Manage registered users
-   View and manage customer orders
-   Update order payment status
-   View customer contact messages

## Project Structure

``` text
phpscript/
├── about.php
├── add_to_cart.php
├── admin_contacts.php
├── admin_header.php
├── admin_orders.php
├── admin_page.php
├── admin_products.php
├── admin_users.php
├── cart.php
├── checkout.php
├── config.php
├── contact.php
├── footer.php
├── header.php
├── home.php
├── login.php
├── logout.php
├── orders.php
├── register.php
├── search_page.php
├── shop.php
├── shop_db.sql
├── css/
│   ├── admin_style.css
│   └── style.css
├── images/
├── js/
│   ├── admin_script.js
│   └── script.js
└── uploaded_img/
```

## Installation and Setup

Follow these steps to run the project on your computer.

### 1. Install XAMPP

Download and install [XAMPP](https://www.apachefriends.org/).

Start the following services from the XAMPP Control Panel: - Apache -
MySQL

### 2. Copy the Project Folder

1.  Extract or copy the `phpscript` project folder.
2.  Move it into the XAMPP `htdocs` directory.

Example:

``` text
C:\xampp\htdocs\phpscript
```

### 3. Create the Database

1.  Open your browser.
2.  Visit <http://localhost/phpmyadmin>.
3.  Create a database named `shop_db`.
4.  Select the newly created database.
5.  Click the **Import** tab.
6.  Choose the `shop_db.sql` file from the project folder.
7.  Click **Import** or **Go** to import the database tables.

### 4. Configure the Database Connection

Open `config.php` and check the database connection settings:

``` php
$conn = mysqli_connect('localhost', 'root', '', 'shop_db');
```

The default settings above are suitable for a typical local XAMPP
installation. Change the host, username, password, or database name if
your local MySQL configuration is different.

### 5. Run the Project

Open your browser and visit:

``` text
http://localhost/phpscript/
```

The application should now be available locally.

## Database Information

The project uses a MySQL database named `shop_db`.

Main database tables:

  Table        Description
  ------------ ----------------------------------------------------
  `users`      Stores customer and admin account information
  `products`   Stores bookstore product information
  `cart`       Stores shopping cart items
  `orders`     Stores customer order details
  `message`    Stores messages submitted through the contact page

## Admin Account Setup

The SQL file creates the database tables but does not provide a
ready-made admin account.

After registering an account through the application, you can assign
admin access through phpMyAdmin:

1.  Open the `shop_db` database.
2.  Open the `users` table.
3.  Find your registered account.
4.  Change its `user_type` value from `user` to `admin`.
5.  Save the changes and log in again.

Only do this on your own local development database.

## Important Notes

-   This project is intended to run in a PHP and MySQL environment.
-   The database must be imported before using the application.
-   Product images are stored in the `uploaded_img/` directory, while
    other website images are stored in `images/`.
-   The database connection settings in `config.php` may need to be
    changed for another computer or hosting provider.
-   Do not upload real passwords, private credentials, or production
    database information to a public GitHub repository.
-   Before deploying publicly, review and improve security, including
    password hashing, SQL query handling, input validation, and session
    management.

## Author

**Project:** Bookly -- Online Bookstore Management System

------------------------------------------------------------------------

*This README describes the project structure and functionality based on
the supplied source files.*
