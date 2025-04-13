# PLP-DB-group-work
PLP-DB group work
This repository contains a database schema and related SQL scripts for a **Bookstore Management System**. The database is designed to manage various aspects of a bookstore, including customers, orders, books, authors, and shipping methods.

## Database Overview

The database is named `bookstoredb` and contains the following tables and some columns on the tables(**NB** this are not all the tables but just a preview of some of them):

### 1. **Address**
- **`address`**: Stores customer addresses along with references to country.
- **`address_status`**: Tracks the status of addresses (e.g., active, inactive).

### 2. **Customer**
- **`customer`**: Holds details about customers (e.g., names, email, phone numbers).
- **`customer_address`**: Links customers to their addresses and address statuses.

### 3. **Book**
- **`book`**: Contains information about books, including title, price, publisher, and language.
- **`author`**: Stores details about authors such as name and email.
- **`book_author`**: Links books to their authors.
- **`book_language`**: Defines the languages in which books are available.
- **`publisher`**: Contains information about publishers.

### 4. **Order**
- **`cust_order`**: Manages customer orders and links to shipping methods and statuses.
- **`order_line`**: Represents individual items in an order.
- **`order_status`**: Tracks the status of orders (e.g., pending, shipped, delivered).
- **`order_history`**: Logs changes in order statuses over time.

### 5. **Shipping_method**
- **`shipping_method`**: Stores available shipping methods and their costs.

### 6. **Country**
- **`country`**: Stores country names for address management.

## Features

- **Relational Design**: The schema uses foreign keys to maintain relationships between tables.
- **Normalization**: Tables are normalized to avoid redundancy and ensure data integrity.
- **Scalability**: Designed to handle a large number of books, customers, and orders efficiently.

## Prerequisites

To use this database schema, you need:
- A MySQL Server (version 8.0.41 or later is recommended).
- A MySQL client or any tool to execute SQL scripts (e.g., MySQL Workbench, phpMyAdmin).
