# Inventory Database Project

## Tech Stack

* Node.js
* Express.js
* SQLite (SQL Database)

---

##  Database Schema

### Suppliers Table

* id (Primary Key)
* name
* city

### Inventory Table

* id (Primary Key)
* supplier_id (Foreign Key)
* product_name
* quantity
* price

Relationship:
One supplier → many inventory items

---

##  APIs

POST /supplier
Add new supplier

POST /inventory
Add inventory (valid supplier required)

GET /inventory
Fetch all inventory

GET /inventory/grouped
Grouped by supplier and sorted by total value

---

##  Validation Rules

* Quantity ≥ 0
* Price > 0
* supplier_id must exist

---

##  Why SQL

SQL is used because:

* Structured relational data
* Easy foreign key relationship
* Supports grouping and aggregation queries

---

##  Optimization

* Add index on supplier_id for faster joins and queries

---

## ▶️ Run Locally

npm install
node server.js

Server:
http://localhost:5000
