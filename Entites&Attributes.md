## Entities as Tables (Matching ERD Exactly)

### Customer

| Attribute   | Description                        |
| ----------- | ---------------------------------- |
| CID (PK)    | Unique customer identifier         |
| Name        | Customer name                      |
| PhoneNumber | Customer phone                     |
| Address     | Composite attribute (Street, City) |

---

### Staff

| Attribute   | Description             |
| ----------- | ----------------------- |
| SID (PK)    | Unique staff identifier |
| Name        | Staff name              |
| Role        | Job role                |
| PhoneNumber | Staff phone             |
| Address     | Staff address           |
| Salary      | Staff salary            |

---

### Order

| Attribute  | Description                   |
| ---------- | ----------------------------- |
| OID (PK)   | Unique order identifier       |
| OrderDate  | Date of the order             |
| Status     | Order status                  |
| OrderType  | dine-in / takeaway / delivery |
| TotalPrice | Derived attribute             |

---

### Table

| Attribute   | Description          |
| ----------- | -------------------- |
| Number (PK) | Table number         |
| Capacity    | Number of seats      |
| Status      | available / occupied |

---

### Payment

| Attribute      | Description               |
| -------------- | ------------------------- |
| PaymentID (PK) | Unique payment identifier |
| Date           | Payment date              |
| Amount         | Paid amount               |

---

### Menu Item

| Attribute   | Description                 |
| ----------- | --------------------------- |
| mealID (PK) | Unique menu item identifier |
| Name        | Item name                   |
| Price       | Item price                  |
| Description | Item description            |

---

### OrderItem

| Attribute    | Description          |
| ------------ | -------------------- |
| OrderID (PK) | References Order     |
| MealID (PK)  | References Menu Item |
| ItemQuantity | Number of items      |

---

### Product

| Attribute           | Description               |
| ------------------- | ------------------------- |
| Product_ID (PK)     | Unique product identifier |
| Name                | Product name              |
| Category            | Product category          |
| Unit of Measurement | Unit used (g, ml, etc.)   |
