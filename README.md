# Brainwave_Task_2
Online Store Database Management System
This project involves designing a relational database for an online store, including customer management, product catalog, orders, and payment processing. The system is implemented using Microsoft SQL Server and contains tables for managing orders, products, customers, and payments.

Features
Customer Management: Add, update, and manage customer information.
Product Management: Store product details, including price and available stock.
Order Management: Track orders placed by customers, including product details.
Payment Processing: Store payment information for completed orders.
Stock Management: Update product stock after an order is placed.
Database Structure
The database consists of the following tables:

Customers: Stores customer information such as name, email, phone number, and address.
Products: Stores product details such as name, description, price, and stock quantity.
Orders: Stores order information for each customer, including the total amount and order status.
OrderDetails: Stores details for each product in an order, such as quantity and price.
Payments: Stores payment information for completed orders.
SQL Scripts
This repository includes SQL scripts to:

Create tables
Insert sample data
Query the database (e.g., retrieve customer order history and product details)
Example SQL Query
Here is an example of a query to retrieve a customer's order history:

sql
Copy
Edit
SELECT 
    o.order_id, 
    o.order_date, 
    o.total_amount, 
    o.status, 
    c.first_name + ' ' + c.last_name AS customer_name
FROM Orders o
JOIN Customers c ON o.customer_id = c.customer_id
ORDER BY o.order_date DESC;
Getting Started
To run this project, you need:

Microsoft SQL Server installed.
A tool like SQL Server Management Studio (SSMS) or Azure Data Studio to run the SQL scripts.
Steps to Set Up:
Clone this repository to your local machine.

bash
Copy
Edit
git clone https://github.com/wehypothetical/Brainwave_Task_2/blob/main/Online_Store
Open SQL Server Management Studio (SSMS) and connect to your database instance.

Run the SQL scripts in the following order:

Create_Tables.sql: Creates the tables in your database.
Insert_Sample_Data.sql: Adds sample data for customers, products, and orders.
Queries.sql: Run sample queries to test the database.
Once the tables are created and data is inserted, you can start querying the database and managing orders, customers, and products.

Sample Data
The project includes sample customers, products, and orders for testing:

Customers:
Alisa Smith
John Doe
Sarah Johnson
James Williams
Products:
Wireless Headphones
Smartphone
Laptop
Smartwatch
Orders:
Alisa placed an order for 2 Wireless Headphones.
John placed an order for 1 Smartphone.
Sarah placed an order for 1 Laptop.
James placed an order for 2 Smartwatches.
Contributing
Feel free to fork this repository, contribute new features, or submit bug fixes. Follow these steps to contribute:

Fork the repository.
Create a new branch (git checkout -b feature-branch).
Commit your changes (git commit -m 'Add new feature').
Push to the branch (git push origin feature-branch).
Open a pull request.
