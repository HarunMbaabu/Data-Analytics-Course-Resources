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

### Create Relationships

1. To set up a relationship between **Customers** and **Orders**, click and drag the `customer_id` column from **Customers** onto the `customer_id` column in **Orders**.
2. Power BI should automatically detect this as a **One-to-Many** relationship, where one customer can have multiple orders.
3. If needed, check the relationship properties by double-clicking the connecting line to ensure the **Cross filter direction** is set to **Single**, which typically optimizes performance.

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
