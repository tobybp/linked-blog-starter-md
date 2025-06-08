[[Computing]]
#8/6/25
### **Key Definitions**

- **Entity**: An object, person, event, or thing of interest to record data about.
- **Attribute**: A property or detail of an entity.
- **Primary Key**: An attribute that uniquely identifies a record.
- **Composite Primary Key**: Two or more attributes used together to uniquely identify a record.
- **Foreign Key**: An attribute that creates a link between two tables by referencing a primary key in another table.
- **Relation**: A table in a relational database.
---
### **Example Entities in a Subscription System**

- **Customer (custID, title, firstname, surname, email)**
- **Product (productID, title, subject, level, price)**
- **Subscription (subID, startDate, endDate)**

---

### **Entity Descriptions**

Each entity must have a **Primary Key** (underlined in notation):

```
Customer (custID, title, firstname, surname, email) 
Product (productID, title, subject, level, price) 
Subscription (subID, startDate, endDate)
```
---

### **Entity Relationships**

- **Customer ↔ Subscription**: One-to-Many
- **Product ↔ Subscription**: One-to-Many

To model this:

```
Subscription (subID, startDate, endDate, custID, productID)
```

- `custID` and `productID` are **foreign keys** here.

---

### **Types of Relationships**

1. **One-to-One**: e.g. Husband ↔ Wife
    
2. **One-to-Many**: e.g. School ↔ Pupil
    
3. **Many-to-Many**: e.g. Actor ↔ Film (requires link table)
    

---

### **Database Structure**

- A **relation** is a table.

- Columns = Fields/Attributes
    
- Use prefix `tbl` for table names (e.g., `tblCustomer`, `tblProduct`)
    

---

### **Handling Many-to-Many Relationships**

- Cannot be implemented directly in tables.
    
- Require a **link table** (e.g. `Subscription`) containing foreign keys:
    
    plaintext
    
    CopyEdit
    
    `Subscription (subID, startDate, endDate, custID, productID)`
    

---

### **Best Practices**

- Always identify entities before designing a database.
    
- Avoid multiple fields (like `ProdID1`, `ProdID2`, etc.) for the same relationship.
    
- Use ERDs to clearly visualize relationships.