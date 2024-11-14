**WEEK 4, DAY 4 GUIDE:** Today we will build on top of where we left yesterday, we will import data, and learn how to build relationships, create calculated columns and measures, optimize our model, and finally create visualizations in Power BI.

### **Step 1: Import Data Files.**

1. Open **Power BI Desktop**.
2. Go to **Home > Get Data > Text/CSV** and load each of your CSV files (**Customers.csv** and **Orders.csv**).
3. Preview the data, ensuring columns like `customer_id` and `transaction_amount` load correctly.
4. Once imported, Power BI displays these tables in the **Fields pane** on the right side, ready for modeling.

## Step 2: Data Modeling and Building Relationships

### Identifying Primary and Foreign Keys

1. In **Model view** (the icon looks like two linked tables), you can see both tables visually.
2. **Identify Primary Keys**:
   - Look at the **Customers** table and confirm `customer_id` as the primary key (unique identifier for each customer).
   - The **Orders** table should also have a `customer_id` column, which serves as the foreign key.

>> A primary key is a unique identifier for each record in a database table. It ensures that each row in the table can be uniquely identified, which is crucial for maintaining data integrity and establishing relationships between tables in a relational database.

>> A foreign key is a field (or collection of fields) in a database table that establishes a link between data in two tables by referencing the primary key of another table. Foreign keys are fundamental to relational databases because they allow you to create relationships between tables, ensuring that the data remains organized and interconnected.

>> A foreign key column in one table refers to a primary key column in another table, establishing a relationship between the two.

### Create Relationships

1. To set up a relationship between **Customers** and **Orders**, click and drag the `customer_id` column from **Customers** onto the `customer_id` column in **Orders**.
2. Power BI should automatically detect this as a **One-to-Many** relationship, where one customer can have multiple orders.
3. If needed, check the relationship properties by double-clicking the connecting line to ensure the **Cross filter direction** is set to **Single**, which typically optimizes performance.

#### 1. One-to-One (1:1) Relationship

**Definition**: In a one-to-one relationship, each record in one table is associated with exactly one record in another table, and vice versa.

**Usage**: This type of relationship is less common and is typically used to separate data into two tables when you have optional data or for security and performance reasons.

**Example**: A `Person` table and a `Passport` table could have a one-to-one relationship, where each person has only one passport, and each passport is assigned to only one person.

---

#### 2. One-to-Many (1:N) Relationship

**Definition**: In a one-to-many relationship, each record in the "parent" table can relate to multiple records in the "child" table, but each record in the child table is associated with only one record in the parent table.

**Usage**: This is the most common type of relationship in databases and is used to model hierarchical data, where one entity (like a customer) can be linked to multiple related entries (like orders).

**Example**: In a `Customers` and `Orders` table, each customer can have multiple orders, but each order is linked to only one customer.

---

#### 3. Many-to-Many (M:N) Relationship

**Definition**: In a many-to-many relationship, each record in one table can relate to multiple records in another table, and each record in the second table can also relate to multiple records in the first table.

**Implementation**: Direct many-to-many relationships are usually implemented using a *junction table* (or *bridge table*) that contains foreign keys referencing both related tables, turning the many-to-many relationship into two one-to-many relationships.

**Example**: In a `Students` table and a `Courses` table, students can enroll in multiple courses, and each course can have


## Step 3: Create Calculated Columns and Measures Using DAX

### Calculated Columns

Calculated columns allow you to add new data fields to each table based on existing data.

#### Creating a Calculated Column

1. Go to the **Data view** (second icon in the left sidebar) and select the **Orders** table.
2. Go to the **Modeling** tab at the top and click **New Column**.
3. Use a DAX formula to create a calculated column.

#### Example: Calculating Transaction Fee Percentage

```DAX
Transaction Fee % = DIVIDE(Orders[fee_amount], Orders[transaction_amount], 0)
