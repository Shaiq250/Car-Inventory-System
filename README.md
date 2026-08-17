# Car Inventory System

![PHP](https://img.shields.io/badge/PHP-v7.4+-777BB4?style=for-the-badge&logo=php)
![MySQL](https://img.shields.io/badge/MySQL-Database-4479A1?style=for-the-badge&logo=mysql)
![XAMPP](https://img.shields.io/badge/Setup-XAMPP-orange?style=for-the-badge)

A web-based **Car Inventory System** (also referred to as "Non PTA PakWheels") allowing users to browse car listings, view details, and inquire about vehicles. It includes an Admin Panel for managing brands, categories, car listings, and user inquiries.

## ⚙️ Prerequisites

To run this project, you need a local web server environment like **XAMPP**, **WAMP**, or **MAMP** that supports PHP and MySQL.

*   [Download XAMPP](https://www.apachefriends.org/download.html)

## 🚀 Installation & Setup Guide

Follow these steps to deploy the project locally using XAMPP:

### Step 1: Extract Files
1.  Download and unzip the project folder.
2.  Copy the folder `DB_Car_Inventory_Project` to your XAMPP `htdocs` directory.
    *   Path: `C:\xampp\htdocs\DB_Car_Inventory_Project`

### Step 2: Database Setup
1.  Open the **XAMPP Control Panel** and start **Apache** and **MySQL**.
2.  Open your browser and navigate to **PHPMyAdmin**: `http://localhost/phpmyadmin`.
3.  Click **New** to create a new database.
4.  Name the database: **`vehicle_db`** (or check `classes/SystemSettings.php` if different, likely matches the import).
    *   *Note: Based on default configurations, ensure the DB name matches your connection string.*
5.  Select the new database and click the **Import** tab.
6.  Choose the file `database/project.sql` from the project folder and click **Go**.

### Step 3: Configure Connection (If needed)
If you use a password for your local MySQL root user, update:
*   File: `classes/DBConnection.php` or `initialize.php`
*   Set `DB_USERNAME` and `DB_PASSWORD` accordingly.
*   *Default XAMPP credentials:* User: `root`, Password: `` (empty).

### Step 4: Run the Website
*   **Public/User View**:
    `http://localhost/DB_Car_Inventory_Project/`
*   **Admin Panel**:
    `http://localhost/DB_Car_Inventory_Project/admin/`

## 🔑 Default Credentials

Use these accounts to access the Admin Panel:

| Role | Username | Password |
| :--- | :--- | :--- |
| **Administrator** | `admin` | `admin123` |
| **Staff** | `cblake` | `cblake123` |

## 📁 Project Structure

*   **`admin/`**: Backend admin interface source code.
*   **`classes/`**: PHP classes for DB connection (`DBConnection.php`) and system settings.
*   **`database/`**: Contains the SQL dump file (`project.sql`).
*   **`uploads/`**: Stores uploaded car images and brand logos.
*   **`inc/`**: Page headers, navigation bars, and reusable components.

## 🛠️ Features
*   **Dashboard**: Overview of inventory and status.
*   **Brand Management**: Add/Edit/Delete car brands (Toyota, Honda, etc.).
*   **Car Listings**: Detailed inventory with specs (Engine, Mileage, Price).
*   **Inquiries**: View customer messages sent from the public site.
*   **User Management**: Manage system users (Admin/Staff).
