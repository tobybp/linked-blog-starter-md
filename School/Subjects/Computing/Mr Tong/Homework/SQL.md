[[Computing]]
#22/6/25
## **SQL Basics**

- **SQL (Structured Query Language)**
    - Declarative language used to interact with relational databases.
    - Allows:
        - Data retrieval.
        - Table creation and updates.
        - Integration with other programming languages.

---
## 🔍 **SQL Syntax: SELECT…FROM…WHERE…ORDER BY**

- **SELECT**: Choose the fields to display.
- **FROM**: Identify the table(s) where the data is stored.
- **WHERE**: Apply search criteria.
- **ORDER BY**: Sort the results (ascending by default, descending with `DESC`).
### Example:
```SQL
SELECT productID, productName, subject, price 
FROM tblProduct 
WHERE level = 4 
ORDER BY productName;
```

---
## **Ordering Results**
- Use `ORDER BY` to sort results:
    - Default: Ascending (ASC)
    - To sort in descending order: `DESC`
### Example:
```SQL
ORDER BY price DESC, productName ASC;
```

---
## **Using Wildcards**

- **Asterisk (*)**: Selects all fields.
- **LIKE**: Used to search for patterns.
- Example:
```SQL
SELECT * 
FROM tblProduct 
WHERE subject 
LIKE "Comp*";
```
_(Finds subjects starting with "Comp")_

---
## **Operators in the WHERE Clause**
- Comparison Operators:
    - `=`, `<>` (not equal), `>`, `<`, `>=`, `<=`
- Logical Operators:
    - `AND`, `OR`, `NOT`
- Range & List Operators:
    - `BETWEEN`: Selects values within a range (inclusive)
    - `IN`: Selects values that match any value in a list
### Example:
```SQL
SELECT * 
FROM tblProduct 
WHERE price BETWEEN 5.00 AND 10.00;
```

---
## **Using Multiple Tables**
- Relational databases often require linking tables using key fields.
- **Example database:**
    - `tblCustomer` (custID, firstname, surname, etc.)
    - `tblSubscription` (subID, custID, productID, startDate, endDate)
    - `tblProduct` (productID, productName, subject, price)
### Example Query:
```SQL
SELECT tblCustomer.custID, surname, tblProduct.productID, productName 
FROM tblCustomer, tblProduct, tblSubscription 
WHERE tblSubscription.custID = tblCustomer.custID 
AND tblSubscription.productID = tblProduct.productID;
```

---
## **Using the JOIN Keyword**

- JOIN is an alternative to the WHERE clause for linking tables.
- Example:
```SQL
SELECT tblPlayer.surname, tblPlayer.firstname, tblTeam.teamName 
FROM tblTeam 
JOIN tblPlayer ON tblTeam.teamID = tblPlayer.teamID 
WHERE tblTeam.teamName = "Binham";
```

---
## **SQL Notes**

- Some databases require **semicolon (;)** at the end of SQL statements.
- Semicolons **separate** SQL statements (not used at the end of each line).