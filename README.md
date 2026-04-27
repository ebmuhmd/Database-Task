# Database-Task|
# 🍽️ Restaurant Management System - SRD

## System Description

This system is designed to manage restaurant operations including customer orders, staff handling, table assignments, payments, menu items, and inventory usage.

---

##  Customers

Each customer is identified by a unique **Customer ID (CID)** and has attributes such as name, phone number, and address (street and city).

A customer can place multiple orders, but each order is placed by exactly one customer.

---

## Staff

Each staff member is identified by a unique **Staff ID (SID)** and has attributes including name, role, phone number, address, and salary.

A staff member can handle multiple orders, but each order is handled by exactly one staff member.

Additionally, staff members have a recursive relationship where one staff member (manager) can manage multiple other staff members.

---

## Orders

Each order is identified by a unique **Order ID (OID)** and includes attributes such as order date, status, and order type (dine-in, takeaway, or delivery).

The **Total Price** of an order is a derived attribute calculated as the sum of:

> (Menu Item Price × Quantity)

Each order:

* is placed by one customer
* is handled by one staff member
* may optionally be assigned to a table
* can have multiple payments
* must contain one or more order items

---

## Tables

Each table is identified by a unique **Table Number** and includes attributes such as capacity and status.

Tables may be assigned to orders in the case of dine-in orders. However, not all orders require a table (e.g., delivery or takeaway).

---

## Payments

Each payment is identified by a unique **Payment ID** and includes attributes such as date and amount.

An order can have multiple payments, but each payment belongs to exactly one order.

---

## Menu Items

Menu items represent meals offered by the restaurant.

Each menu item is identified by a unique **Menu Item ID** and includes attributes such as name, price, and description.

A menu item can appear in multiple orders.

---

## Order Items

Order items represent the relationship between orders and menu items.

Each order item:

* belongs to exactly one order
* refers to exactly one menu item
* includes a quantity

Order items are identified by a **composite primary key** consisting of:

* Order ID
* Menu Item ID

---

## Products

Products represent raw ingredients used in preparing menu items.

Each product is identified by a unique **Product ID** and includes attributes such as name, category, and unit of measurement (e.g., grams, liters).

---

## Product Composition

Menu items are composed of one or more products.

This is a many-to-many relationship between **Menu Items** and **Products**, with an associated attribute:

* Quantity (amount of product used in a menu item)

A product can be used in multiple menu items, and each menu item can include multiple products.

---
