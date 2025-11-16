# 🍕 Online Pizza Delivery (PHP & MySQL)

### 🛡️ Project Status & Context

| Status | Tech Stack | Type | Context |
| :--- | :--- | :--- | :--- |
| **Complete** | PHP, MySQL, Bootstrap, jQuery | Full-Stack Web App | **ISGA Academic Project** |

[![GitHub last commit](https://img.shields.io/github/last-commit/nveyounes/OnlinePizzaDelivery?style=for-the-badge&color=2ecc71)](https://github.com/nveyounes/OnlinePizzaDelivery)
[![License](https://img.shields.io/github/license/nveyounes/Online-Pizza-Delivery-PHP-MySQL-?style=for-the-badge&color=3498db)](LICENSE)
[![Repo Size](https://img.shields.io/github/repo-size/nveyounes/OnlinePizzaDelivery?style=for-the-badge&color=9b59b6)](https://github.com/nveyounes/OnlinePizzaDelivery)

---

## ⭐ Project Goal: Full-Stack Food Delivery Website

This repository contains a full-stack web application for an "Online Pizza Delivery" service. It was developed as a mini-project for ISGA to demonstrate database management and web development skills.

The project consists of two main parts:
1.  A **customer-facing website** where users can browse products, add items to a cart, and place orders.
2.  A password-protected **admin panel** for managing the entire website, including products, orders, users, and site settings.

### 📌 Key Features

**🧑‍💻 Client-Side (Website):**
* **Browse Menu:** View all available pizzas, sorted by category.
* **Shopping Cart:** Add/remove items and manage item quantities.
* **Checkout:** Place an order by providing delivery details.
* **Payment Options:** Supports multiple payment methods, including "Cash on Delivery" and PayPal.
* **Order Tracking:** Users can view the status of their orders.
* **Contact Form:** A functional "Contact Us" page.

**🔐 Admin-Side (Admin Panel):**
* **Secure Login:** The admin panel is protected by a username and password.
* **Dashboard:** A home page with at-a-glance statistics.
* **User Management:** View all registered users.
* **Category Management:** Add, edit, and delete food categories.
* **Menu Management:** Add, edit, and delete pizza items (including name, price, description, and image).
* **Order Management:** View and update the status of all customer orders (e.g., "Order Placed," "In Delivery," "Delivered").
* **Contact Management:** View and reply to customer messages.
* **Site Management:** Update system-wide details like the site name and contact info.

---

## 🛠️ Technology Stack

This project is a classic "LAMP" stack application, built with PHP and a MySQL database.

| Category | Technology | Purpose | Icon |
| :--- | :--- | :--- | :--- |
| **Backend** | PHP | Primary server-side language for all logic. | ![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=php&logoColor=white) |
| **Database** | MySQL | All data storage (users, orders, products). | ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white) |
| **Web Server** | Apache | (Via XAMPP) To serve the PHP files. | ![Apache](https://img.shields.io/badge/Apache-D22128?style=flat-square&logo=apache&logoColor=white) |
| **Frontend** | Bootstrap | CSS framework for UI and responsiveness. | ![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?style=flat-square&logo=bootstrap&logoColor=white) |
| **Frontend** | jQuery | JavaScript library for DOM manipulation and events. | ![jQuery](https://img.shields.io/badge/jQuery-0769AD?style=flat-square&logo=jquery&logoColor=white) |
| **DB Tool** | phpMyAdmin | Used to design and manage the database. | ![phpMyAdmin](https://img.shields.io/badge/phpMyAdmin-6C78AF?style=flat-square&logo=phpmyadmin&logoColor=white) |

---

## 📂 Architecture & Database

### 1. Architecture
The project uses a standard modular PHP structure.
* **`partials/`:** Contains reusable "include" files like the database connection (`_dbconnect.php`), header (`_nav.php`), and footer (`_footer.php`).
* **`admin/partials/`:** A separate set of includes for the admin panel.
* Logic for handling form submissions (login, signup, cart management) is contained in handler files (e.t., `_handleLogin.php`, `_manageCart.php`).

### 2. Database Schema
The complete database schema is provided in the **`opd.sql`** file. The database consists of 10 tables:

* `categories`: Stores food categories (e.g., "Vegetarian", "Non-Veg").
* `pizza`: Stores all individual pizza details (name, price, description, category ID).
* `users`: Stores customer and admin information (username, password, email, `userType`).
* `orders`: Contains high-level order information (user ID, address, phone, total amount, payment mode, status).
* `orderitems`: A junction table linking `orders` and `pizza` (stores which pizzas and what quantity are in each order).
* `viewcart`: Manages items currently in a user's cart.
* `contact`: Stores messages from the customer contact form.
* `contactreply`: Stores admin replies to customer messages.
* `deliverydetails`: Stores information about the delivery (e.g., delivery person, time).
* `sitedetail`: A key-value table for storing system settings like the site name and email.

---

## 📸 Screenshots

*(This is a perfect place to add screenshots of your running application!)*

| Client: Home Page | Client: View Pizza | Client: Cart | Admin: Login | Admin: Dashboard |
| :---: | :---: | :---: | :---: | :---: |
|  |  |  |  |  |

---

## 🚀 Getting Started

### Prerequisites
You need a local server environment that runs PHP and MySQL. The easiest way is to install **XAMPP**.
* [XAMPP](https://www.apachefriends.org/index.html) (or WAMP/MAMP)

### Installation & Usage

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/nveyounes/OnlinePizzaDelivery.git](https://github.com/nveyounes/OnlinePizzaDelivery.git)
    ```
2.  **Move Project:**
    * Move the entire `OnlinePizzaDelivery` folder into your XAMPP `htdocs` directory.
    * (e.g., `C:\xampp\htdocs\OnlinePizzaDelivery`)

3.  **Start Services:**
    * Open your XAMPP Control Panel.
    * Start the **Apache** and **MySQL** services.

4.  **Import Database:**
    * Open your browser and go to `http://localhost/phpmyadmin`.
    * Click on the **"Databases"** tab.
    * Create a new database. Name it `opd`.
    * Click on the new `opd` database in the left sidebar.
    * Click on the **"Import"** tab.
    * Click "Choose File" and select the `opd.sql` file from this project.
    * Click "Go" at the bottom of the page to import the schema and data.

5.  **Run the Application:**
    * **Client Website:** Go to `http://localhost/OnlinePizzaDelivery`
    * **Admin Panel:** Go to `http://localhost/OnlinePizzaDelivery/admin/login.php`
        * **Username:** `admin`
        * **Password:** `admin`

---

## 👥 Authors & Acknowledgements

This was an academic project for **ISGA (EDVANTIS Higher Education Group)**.

* **Farhat**
* **Bellmaine**
* **Iskazian**

### Supervised By:
* **Mr. Safsouf Yassine**
