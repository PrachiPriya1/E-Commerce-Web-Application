# 🛍️ E-Commerce Web Application

An e-commerce web application built with PHP, MySQL, HTML, CSS, JavaScript, and Bootstrap. The application offers a smooth shopping experience with features like user authentication, product catalog, cart management, checkout with address selection, order tracking, and profile management.

![E-Commerce Banner](https://via.placeholder.com/1200x300?text=E-Commerce+Web+Application) <!-- Replace this URL with an actual banner image URL -->

## 🔥 Features

- **🔑 User Authentication**: Register, log in, and manage user sessions.
- **👤 Profile Management**: View and update profile details, change passwords, and manage user information.
- **🛒 Cart Management**: Add products to the cart, adjust quantities, and view the cart summary.
- **📦 Checkout with Address Selection**: Choose a saved address, add a new address, or edit an existing one before checkout.
- **📜 Order Tracking**: Track orders with a list view and see details for each placed order.

## 📂 Database Structure

### `users` Table

| Field        | Type           | Key | Description          |
| ------------ | -------------- | --- | -------------------- |
| `id`         | `int(11)`      | PK  | User ID              |
| `name`       | `varchar(100)` |     | User's full name     |
| `email`      | `varchar(100)` | UNI | User's email address |
| `password`   | `varchar(255)` |     | Hashed password      |
| `created_at` | `timestamp`    |     | Creation timestamp   |

### `orders` Table

| Field        | Type            | Key | Description                                       |
| ------------ | --------------- | --- | ------------------------------------------------- |
| `id`         | `int(11)`       | PK  | Order ID                                          |
| `user_id`    | `int(11)`       | FK  | User who placed the order                         |
| `total`      | `decimal(10,2)` |     | Total amount of the order                         |
| `status`     | `enum`          |     | Order status (`pending`, `completed`, `canceled`) |
| `created_at` | `timestamp`     |     | Order creation timestamp                          |

### `order_items` Table

| Field        | Type            | Key | Description                  |
| ------------ | --------------- | --- | ---------------------------- |
| `order_id`   | `int(11)`       | FK  | Order ID from `orders` table |
| `product_id` | `int(11)`       | FK  | ID of the ordered product    |
| `quantity`   | `int`           |     | Quantity ordered             |
| `price`      | `decimal(10,2)` |     | Price of each unit           |

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Abhiroux/ecommerce-application.git
cd ecommerce-application
```

### Step 2: Set Up the Database

1. **Import the `database.sql` file** to create tables and insert sample data.
2. **Update `db.php`** with your MySQL database credentials to connect the application to the database.

### Step 3: Run the Application

- Use a local server like **XAMPP**, **MAMP**, or **WAMP** to host the application.
- Point the server to this project folder and start exploring!

---

## 🖥️ Usage Guide

- **🏠 Home Page**: Explore the product catalog, view details, and add items to the cart.
- **🛒 Cart Page**: View items in the cart and adjust quantities.
- **💳 Checkout Page**: Select or add a shipping address before placing an order.
- **📜 Orders Page**: Track your order history and view order details.
- **👤 Profile Page**: Update profile information, view past orders, and change your password.

---

## 🛠️ Technologies Used

- **Frontend**: HTML, CSS, JavaScript, Bootstrap
- **Backend**: PHP (with PDO for database handling), MySQL

---

## 📸 Screenshots

1. **Home Page**: Product catalog with details.
2. **Cart Page**: Shows items in the cart and allows adjustments.
3. **Profile Page**: Edit profile information and change password.
4. **Orders Page**: View your past orders and track order status.

> 📌 **Note**: Adding screenshots for each of these sections will make this README more illustrative and engaging.

---

## 🔄 Future Enhancements

- **💳 Payment Integration**: Add a payment gateway for secure transactions.
- **📊 Admin Dashboard**: A dedicated section for product and order management.
- **💡 Enhanced UI**: Make the interface more dynamic and responsive for all device sizes.

---

## 📄 License

This project is open-source and available under the **MIT License**.

---

## 👤 Author

**Abhishek Kumar**  
[GitHub](https://github.com/Abhiroux)

---

💖 _Thank you for checking out this project! Happy coding!_ 😊
