[[Computing]]
#24/6/25
#### Creating and Altering Tables with SQL

- **CREATE TABLE**: Used to define and create a new table. 
    - Example:    
        ```SQL
        CREATE TABLE tblProduct
        (
        ProductID CHAR(4) NOT NULL, PRIMARY KEY,
        Description VARCHAR(20) NOT NULL,
        Price CURRENCY
        )
        ```    
    - `NOT NULL` ensures the field cannot be left blank.
    - `PRIMARY KEY` defines the primary key for the table.    
- **Common Data Types**:
    - `CHAR(n)`: Fixed-length character string of length `n`. Example: `ProductCode CHAR(6)`.
    - `VARCHAR(n)`: Variable-length character string with a maximum length of `n`. Example: `Surname VARCHAR(25)`.
    - `BOOLEAN`: Stores `TRUE` or `FALSE`. Example: `ReviewComplete BOOLEAN`.
    - `INTEGER`, `INT`: Stores whole numbers. Example: `Quantity INTEGER`.
    - `FLOAT`: Stores numbers with a floating decimal point. Example: `Length FLOAT (10,2)` (10 total digits, 2 after decimal).
    - `DATE`: Stores Day, Month, Year. Example: `HireDate DATE`.
    - `TIME`: Stores Hour, Minute, Second. Example: `RaceTime TIME`.
    - `CURRENCY`: Formats numbers in the regional currency. Example: `EntryFee CURRENCY`.
- **ALTER TABLE**: Used to add, delete, or modify columns in an existing table.
    - **Add a new column**: `ALTER TABLE tblProduct ADD QtyInStock INTEGER`
    - **Delete a column**: `ALTER TABLE tblProduct DROP QtyInStock`
    - **Change data type of a column**: `ALTER TABLE tblProduct MODIFY COLUMN Description VARCHAR (30) NOT NULL`
- **Defining Linked Tables**:
    - Tables can be linked using `FOREIGN KEY` constraints.
    - Example of `ProductComponent` table linking `Product` and `Component` tables:
        ```SQL
        CREATE TABLE ProductComponent
        ( ProductID CHAR(4) NOT NULL,
        CompID CHAR(6) NOT NULL,
        Quantity INTEGER
        FOREIGN KEY ProductID REFERENCES Product(ProductID)
        FOREIGN KEY CompID REFERENCES Component(CompID)
        PRIMARY KEY (ProductID, CompID) )
        ```
#### Manipulating Data with SQL
- **INSERT INTO**: Used to add new records into a table.
    - Example: `INSERT INTO Product (ProductID, Description, Price) VALUES (“A345”, “Pink Rabbit”, 7.50)`
    - Field names can be omitted if inserting data into all fields in order.
- **UPDATE**: Used to modify existing records in a table.
    - The `WHERE` clause specifies which records to update.
    - Example: `UPDATE Product SET Description = “Blue Rabbit”, Price = 8.25 WHERE ProductID = “A345”`
- **DELETE FROM**: Used to remove records from a table.
    - The `WHERE` clause specifies which records to delete.
    - Example: `DELETE FROM Product WHERE ProductID = “A345”`
#### Client-Server Database Systems
- **Definition**: A client-server database system allows multiple clients to simultaneously access a database.
- **How it works**: Database Management System (DBMS) software on the server processes client requests (e.g., from individual workstations).
- **Advantages**:
    - Database consistency is maintained as there is only one copy.
    - Resources of a powerful computer are available to many users.
    - Centralised management of access rights and security.
    - Centralised backup and recovery.
#### Concurrent Access Control
- **Potential Problem**: Multiple users trying to access and modify the same data concurrently can lead to data inconsistencies or lost updates. (e.g., several people booking the last few airline seats).
- **Record Locking**:
    - Prevents simultaneous access to database objects to avoid lost updates or data inconsistencies.
    - When a user retrieves a record for editing, it is locked, denying access to others until the transaction is complete or cancelled.
    - Without locking, User B's changes might be lost if User A saves their changes to the same record later.
- **Serialisation and Timestamp Ordering**:
    - **Serialisation**: Ensures transactions do not overlap in time.        
    - **Timestamp Ordering**:
        - Every database object has a read and write timestamp, updated upon access.
        - If a user tries to save an update and the read timestamp is different from when they started, it indicates another user accessed the object.
        - The transaction is cancelled, and an "Update unsuccessful" message is sent.
- **Commitment Ordering**:
    - Another serialisation technique to prevent lost transactions when multiple clients update the same record.
    - Transactions are ordered based on their dependencies and initiation time.
    - Can prevent deadlock by blocking one request until another finishes.