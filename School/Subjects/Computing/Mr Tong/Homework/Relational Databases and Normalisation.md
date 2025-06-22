[[Computing]]
#22/6/25 

| Term                  | Description                                                                                     |
| --------------------- | ----------------------------------------------------------------------------------------------- |
| Foreign Key           | An attribute which is the primary key in one table, and creates a join between two tables.      |
| Attribute             | A property of an entity.                                                                        |
| Entity Relationship   | A graphical way of representing the relationships between entities.                             |
| Entity                | A category of object, person, event or thing of interest about which data needs to be recorded. |
| Primary Key           | An attribute which uniquely identifies a record.                                                |
| Composite Primary Key | Two or more attributes that uniquely define a record.                                           |
| Relationship          | A link between entities.                                                                        |

- **Example: Mother and Child Entities**
    - **Notation:** `Tablename (keyfield, Attribute1, Attribute2, …)
    - `
**Relational Database Design:**
- Data is held in tables, also known as relations.
- One row in a table holds one record.
- Each column represents one attribute.
- Each relation should hold data about a single entity.
- **Problem with Flat File Approach (Example: Gym Members & Classes):**
    - The relationship between members and classes is many-to-many.
    - A single flat file leads to repeating groups of attributes and data duplication. For example, a member's details would be repeated for each class they enrol in, and class details would be repeated for each member in that class.

**Normalisation:**
- A process used to achieve the best possible design for a database.
- Aims to organise tables to avoid data duplication within and across tables.
- The structure should facilitate complex queries.
- There are three stages: First Normal Form (1NF), Second Normal Form (2NF), and Third Normal Form (3NF).

**First Normal Form (1NF):**
- A table is in 1NF if it contains no repeating attributes or groups of attributes.
- All attributes must be _atomic_ (single data item).
    - Example: Separating "firstname" and "surname" into individual attributes is necessary for 1NF, as it makes sorting by surname easier.
- The example flat file for gym members and classes is **not** in 1NF due to repeating groups of attributes, specifically because of the many-to-many relationship between Member and Class entities.
- **Achieving 1NF for Gym Member/Class Data:**
    - An extra table is needed in the middle to resolve the many-to-many relationship.
    - This results in three tables:
        - `tblMember (MemberID, MSurname, MFirstName)`
        - `tblClass (ClassID, CName, Day)`
        - `tblEnrolment (MemberID, ClassID)`
- **Composite Primary Key:** The `tblEnrolment` table uses `MemberID` and `ClassID` together as a composite primary key. Both of these fields also act as foreign keys, linking back to `tblMember` and `tblClass` respectively.
- At this stage, the tables are in 1NF.

**Second Normal Form (2NF):**
- A table is in 2NF if it is in 1NF and contains no _partial dependencies_.
- Partial dependencies can only occur if the primary key is a composite key.
- In the example of `tblEnrolment (MemberID, ClassID)`, if an attribute like `ClassSize` were added to `tblEnrolment`, and `ClassSize` only depended on `ClassID` (part of the composite key) and not `MemberID`, then it would be a partial dependency, and the table would not be in 2NF.
- The current `tblEnrolment` (with just `MemberID` and `ClassID`) has no fields dependent on only part of the key, so it is in 2NF.

**Third Normal Form (3NF):**
- A table is in 3NF if it is in 2NF and contains no _non-key dependencies_.
- This means "All attributes are dependent on the key, the whole key and nothing but the key."
- **Example (Illustrating non-key dependency):** If `tblClass` had `InstID`, `InstFirstname`, and `InstSurname`:
    - `InstFirstname` and `InstSurname` depend on `InstID`.
    - `InstID` itself is not the primary key of `tblClass` (which is `ClassID`). This is a non-key dependency.
    - To achieve 3NF, the `Instructor` information should be moved to its own table:
        - `tblInstructor (InstID, InstFirstname, InstSurname)`
        - `tblClass` would then only contain `ClassID`, `CName`, `Day`, and `InstID` (as a foreign key).
- There are now four entities in the database, each with its own table: Member, Enrolment, Class, and Instructor.

**Importance of Normalisation:**
- **Easier to maintain and change:** Updates are made in a single place.
    - Example: Changing an instructor's surname is done only in `tblInstructor`.
- **No unnecessary duplication of data:** Saves storage space.
- **Data integrity is maintained:**
    - Ensures consistency (e.g., a person doesn't have two different addresses).
    - Referential integrity can prevent deletion of records if they are referenced by foreign keys in other tables (e.g., an instructor record cannot be deleted if classes are still linked to that instructor).
- **Faster searches:** Smaller tables with fewer fields improve search performance.
- **Flexibility for adding fields:** If a new attribute is needed (e.g., class duration), only one relevant table needs modification.