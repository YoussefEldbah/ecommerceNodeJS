# E-Commerce Backend API

This repository contains the backend code for an e-commerce platform, providing user authentication, product management, cart functionality, order processing, and more. Built with Node.js, Express, and MongoDB, this API is designed to handle essential e-commerce operations efficiently and securely.

## Features

* **User Authentication & Role-Based Access:**
  Register, login, and manage users with secure password hashing and JWT authentication. Supports both `admin` and `user` roles.

* **Password Recovery:**
  Secure password reset via email with token expiration and a one-time link for resetting the password.

* **Product Management:**
  CRUD operations for managing products, including product details like title, price, category, and stock.

* **Category Management:**
  Create, read, and manage product categories.

* **Shopping Cart Management:**
  Add, remove, and view products in the cart. Cart is tied to each user, and quantities are updated accordingly.

* **Order Management:**
  Create and update orders, including stock updates when an order is placed. Admin can change order status to track the progress of orders.

* **Email Integration:**
  Sends email notifications for password resets and other user-related actions using Nodemailer.

## Technologies

* **Backend:**
  Node.js, Express.js, MongoDB, JWT, Bcrypt, Crypto, Nodemailer, dotenv

* **Database Models:**
  User, Product, Category, Cart, Order

## Endpoints

### User Authentication

* `POST /register`: Register a new user
* `POST /login`: User login
* `POST /forgotPassword`: Send password reset email
* `PUT /resetPassword`: Reset the user’s password

### Cart Management

* `POST /cart/add`: Add a product to the cart
* `POST /cart/remove`: Remove a product from the cart
* `GET /cart`: Get the current user's cart

### Product & Category Management

* `POST /products`: Create a new product
* `GET /products`: Get all products
* `PUT /products/:id`: Update product details
* `DELETE /products/:id`: Delete a product
* `POST /categories`: Create a new category
* `GET /categories`: Get all categories

### Order Management

* `POST /orders`: Create a new order
* `PUT /orders/:id`: Update order status (e.g., 'pending', 'completed')
* `GET /orders`: Get all orders (admin only)
* `GET /orders/user`: Get orders for a specific user

## Setup

1. Clone the repository:

   ```bash
   git clone <repo-url>
   cd <repo-directory>
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Configure environment variables:

   * `.env` file containing the following:

     ```
     JWT_SECRET=<your-secret-key>
     EMAIL=<your-email>
     PASSWORD=<your-email-password>
     ```

4. Start the server:

   ```bash
   npm start
   ```

## Conclusion

This API serves as the backend for a fully functional e-commerce platform, providing essential features such as user authentication, cart management, order processing, and product management. The API is secure, scalable, and easy to extend for additional features.
