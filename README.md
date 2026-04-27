# Database-Task|
# 🍽️ Restaurant Management System

##  Overview

This project represents a database design for a Restaurant Management System using ERD and Mapping.

---

## Entities

### Customer

* Customer ID (PK)
* Name
* Phone Number
* Address (Street, City)

### Staff

* Staff ID (PK)
* Name
* Role
* Phone Number
* Address
* Salary

### Order

* Order ID (PK)
* Order Date
* Status
* Order Type (dine-in, takeaway, delivery)
* Total Price (Derived)

### Table

* Table Number (PK)
* Capacity
* Status

### Payment

* Payment ID (PK)
* Date
* Amount

### Product

* Product ID (PK)
* Name
* Category
* Unit of Measurement

### Menu Item

* Menu Item ID (PK)
* Name
* Price
* Description

### OrderItem (Weak Entity)

* Order ID (PK, FK)
* Menu Item ID (PK, FK)
* Quantity

---

##  Relationships

* A Customer places multiple Orders (1:N)
* A Staff member handles multiple Orders (1:N)
* An Order may be assigned to a Table (M:1, optional)
* An Order can have multiple Payments (1:N)
* An Order contains multiple OrderItems (1:N)
* Each OrderItem refers to one Menu Item (N:1)
* Menu Items are composed of Products (M:N) with Quantity
* Staff manages other staff (recursive 1:N)

---

##  Notes

* Total Price is derived from Order Items
* OrderItem uses a composite primary key
* Table assignment is optional (only for dine-in)

---

