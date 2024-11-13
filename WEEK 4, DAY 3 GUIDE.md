### **Question 1: You would like to extract the first 2 characters from a column in your Power BI table. How can you achieve this?**

Answer: Click through Transform --> Extract --> First Characters

---

### **Joining Data (Using Merge Queries) in Power BI with Customer and Order Tables.**

### Step-by-Step Guide

#### 1. Load Your Tables
- Go to **Home > Get Data** to import both the **Customer** and **Order** tables into Power BI.

#### 2. Open Power Query Editor
- Once both tables are loaded, go to **Home > Transform Data** to open the Power Query Editor.

#### 3. Merge Queries
- In the Power Query Editor, select the **Order** table (this is the table you want to enrich with customer details).
- Go to **Home > Merge Queries**.
- In the Merge dialog box, select the **Customer** table as the second table to join with **Order**.
- Join on the **CustomerID** field in both tables by clicking on the **CustomerID** column in each table.

#### 4. Choose the Join Type
- Select the join type based on your needs:
  - **Left Outer join** (most common) will keep all rows from the **Order** table, adding matching data from the **Customer** table.
  - **Inner join** will keep only rows that have a match in both tables.
  - **Right Outer** or **Full Outer** joins are less common for customer-order joins but are available if needed.

#### 5. Expand Columns
- After merging, a new column will appear in the **Order** table with the name **Customer** (or **Customer Table**).
- Click the expand icon next to this column to see a list of columns from the **Customer** table.
- Select the columns you want to bring over from the **Customer** table, such as **CustomerName**, **Email**, and **Country**.
- Click **OK**.

#### 6. Finalize the Join
- After expanding the columns, your **Order** table will now contain additional details from the **Customer** table.
- Click **Close & Apply** to save the changes and load the transformed data into Power BI.

---
### **Example Scenario for Appending Data.**

You have three tables: **JanuaryOrders**, **FebruaryOrders**, and **MarchOrders**. Each table contains orders for a specific month, with the same structure (same columns).

### Columns in Each Monthly Orders Table

Each table might have these columns:
- **OrderID**: Unique identifier for each order.
- **CustomerID**: Identifier for the customer who placed the order.
- **OrderDate**: Date when the order was placed.
- **ProductID**: Identifier for the ordered product.
- **Quantity**: Quantity of the product ordered.
- **TotalAmount**: Total amount for each order.
- **Status**: Status of the order (e.g., "Shipped," "Processing," "Delivered").

### Step-by-Step Guide to Appending Data in Power BI

#### 1. Load Each Monthly Dataset
- Go to **Home > Get Data** and load the **JanuaryOrders**, **FebruaryOrders**, and **MarchOrders** tables into Power BI.

#### 2. Open Power Query Editor
- Once all tables are loaded, go to **Home > Transform Data** to open the Power Query Editor.

#### 3. Append Queries
- In the Power Query Editor, select one of the monthly order tables, for example, **JanuaryOrders**.
- Go to **Home > Append Queries > Append Queries as New**.
- In the Append Queries dialog:
  - Select **Three or More Tables** (since we’re appending multiple monthly tables).
  - Select **JanuaryOrders**, **FebruaryOrders**, and **MarchOrders** as the tables to append.
  - Click **OK**. This will create a new combined table containing rows from all selected tables.

#### 4. Rename the Appended Table
- The new table will appear in the Power Query Editor, likely with a default name like *Append1*.
- Rename this table to something more descriptive, such as **AllOrders**.

#### 5. Review and Close
- Double-check that all rows from each monthly table have been added to **AllOrders**.
- Click **Close & Apply** to save your changes and load the combined dataset into Power BI.



  ---
### **Step-by-Step Instructions to Unpivot Columns in Power BI.**

#### 1. Open Power BI and Load Your Data:
- Open **Power BI Desktop**.
- Go to the "Home" tab and select **Get Data > Excel**.
- Choose your file (**transactions.xlsx**) and load it into Power BI.

#### 2. Open Power Query Editor:
- Once the data is loaded, go to **Home > Transform Data**. This opens the Power Query Editor.

#### 3. Select Columns to Unpivot:
- In the Power Query Editor, locate your data table on the left.
- Select the columns you want to unpivot. In your case, you would select **Deposit** and **Withdrawal**.

#### 4. Unpivot Columns:
- With the **Deposit** and **Withdrawal** columns selected, go to the **Transform** tab in the menu.
- Click **Unpivot Columns**.

#### 5. Rename the Unpivoted Columns:
- After unpivoting, you’ll see two new columns created:
  - **Attribute**: This column will show the original column names (e.g., "Deposit" or "Withdrawal").
  - **Value**: This column contains the transaction amounts.
- Rename the **Attribute** column to **Transaction Type** by double-clicking on its header and typing the new name.

#### 6. Close and Apply:
- Once your columns are renamed, go to the **Home** tab in Power Query Editor.
- Click **Close & Apply** to save the changes and load the transformed data into Power BI.

