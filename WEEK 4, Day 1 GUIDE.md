### Class Notes for Week 4, Day 1: Power BI - Data Transformation, Data Modeling, and Interactive Reports

---

#### Data Transformation with Power Query

Data transformation in Power Query involves cleaning and restructuring raw data to make it suitable for analysis. This is crucial for ensuring reliable insights and accurate reporting.

##### Handling Missing Data
1. **Replace Null Values**:
   - Replace missing values in columns like `transaction_amount` with 0 to ensure calculations include all data.
   - In Power Query, select the `transaction_amount` column, choose **Replace Values**, and set null values to 0.

2. **Filter Out Rows with Missing Key Information**:
   - Fields like `customer_id` and `account_number` are essential for identifying transactions. Rows missing these should be removed.
   - Select `customer_id`, then choose **Remove Empty** to keep only records with this identifier.

##### Removing Duplicates
- Duplicate rows can lead to overcounting. Use `transaction_id` as a unique identifier:
  - In Power Query, select `transaction_id` and click **Remove Duplicates** to keep only the first occurrence of each transaction.

##### Standardizing Formatting
1. **Date Formatting**: Convert `transaction_date` to a Date type for accurate time-based analysis.
2. **Number Formatting**: Set `transaction_amount` and `account_balance` as Decimal Number types.
3. **Text Case Standardization**: Format fields like branch names consistently for easy filtering, using **Capitalize Each Word** for the branch column.

##### Combining Data (Joins and Appends)
1. **Joining Data**:
   - Join tables using fields like `branch`. For example, use **Merge Queries** to bring in additional branch details.

2. **Appending Data**:
   - Append rows from multiple datasets with the same columns, such as monthly transaction sheets, into a single dataset.

##### Advanced Transformations
1. **Unpivoting Data**: Converts multiple columns into a single column format. For example, unpivot columns for “Deposit” and “Withdrawal” into a single `Transaction Type` column.
2. **Data Splitting**: Splits information within a column, such as splitting `branch` into City and Branch Name.

##### Automating with Power Query M Language
- Use the M Language for automated transformations.
  - **Example M Code for Replacing Null Values**:
    ```M
    Table.ReplaceValue(#"Previous Step", null, 0, Replacer.ReplaceValue, {"transaction_amount"})
    ```
---

#### Data Modeling in Power BI

Data modeling structures data into tables and defines relationships, enabling efficient analysis and advanced calculations.

##### Building Table Relationships
1. **Primary and Foreign Keys**:
   - Use fields like `customer_id` in the Customers table as primary keys and link them to related tables.

2. **One-to-Many Relationships**:
   - A one-to-many relationship lets one record in a table relate to multiple records in another. For example, a single `customer_id` can link to multiple `transaction_id` records.

##### Calculated Columns and Measures with DAX
1. **Calculated Columns**:
   - Create new columns in tables using DAX formulas.
   - **Example**: To calculate `Transaction Fee Percentage`:
     ```DAX
     Transaction Fee % = [fee_amount] / [transaction_amount]
     ```

2. **Measures**:
   - Measures are dynamic calculations that adjust based on context.
   - **Examples**:
     - Total Transaction Amount:
       ```DAX
       Total Transaction Amount = SUM(data[transaction_amount])
       ```
     - Average Account Balance:
       ```DAX
       Average Account Balance = AVERAGE(data[account_balance])
       ```

3. **Custom Calculations**:
   - Example: Calculate total fees by branch.
     ```DAX
     Total Fees by Branch = CALCULATE(SUM(data[fee_amount]), ALLEXCEPT(data, data[branch]))
     ```

##### Model Optimization
1. **Remove Unnecessary Columns**: For efficiency, remove unused columns like `account_number`.
2. **Set Summarization Options**: Set columns like `transaction_amount` and `fee_amount` to default to Sum for aggregation.

---

#### Creating Interactive Reports

Interactive reports enable users to explore data independently with filters and visual interactions.

##### Visual Selection and Design
1. **Bar Chart**: Compare totals by categories (e.g., `transaction_amount` by branch).
2. **Line Chart**: Ideal for trend analysis, such as tracking `account_balance` over time.
3. **Map**: Display branch locations if geographic data is available.

##### Adding Interactivity
1. **Filters**: Apply a `transaction_date` filter to limit data by period.
2. **Slicers**: Use slicers for fields like branch and `customer_id` to allow focused analysis.
3. **Drill-Throughs**: Enable drill-throughs on branches to view transaction-level details for a specific branch.

##### Storytelling with Visuals
1. **Dynamic Titles**: Titles that change based on user selections, such as branch names.
2. **Custom Themes**: Apply a theme consistent with company branding.
3. **Tooltips**: Use tooltips to show additional details when hovering over visuals (e.g., transaction amount and fee percentage).

---

#### Practical Exercise
- **Data Transformation**: Import and clean data with Power Query, standardize it, and handle missing data.
- **Data Modeling**: Establish table relationships, add calculated columns, and create custom measures with DAX.
- **Report Creation**: Design an interactive report with visuals, slicers, and drill-throughs for exploring data by branch and customer.

---

#### Key Takeaways
- **Data Transformation**: Ensures data quality, foundational for reliable analysis.
- **Data Modeling**: Organizes data for effective use, while DAX enables advanced calculations.
- **Interactive Reports**: Facilitate a dynamic user experience for deeper insights.



### Data Analysis Expressions (DAX)

DAX, short for Data Analysis Expressions, is a powerful formula language used in Power BI, Power Pivot in Excel, and Analysis Services. DAX is designed for creating calculations and analyzing data within tabular data models, allowing users to perform complex calculations and derive new insights from their datasets.

#### Key Characteristics of DAX

1. **Column-Based Language**: DAX operates on columns of data rather than individual cells, which makes it suitable for large datasets and efficient for database operations.
2. **Relational Model Awareness**: DAX works with data models that define relationships between tables, allowing you to pull related data for calculations without explicitly joining tables.
3. **Dynamic Context-Based Calculations**: DAX can automatically adapt calculations based on filters or slicers applied in reports, adjusting values as the context changes.

#### Why DAX Is Important

DAX allows you to go beyond basic data aggregation by enabling powerful calculations that help in:
- Creating dynamic measures and metrics.
- Calculating percentages, rankings, cumulative totals, and year-to-date values.
- Defining custom columns and measures that allow for more sophisticated analysis.

DAX enhances Power BI’s interactivity by allowing real-time calculations that change based on user-selected filters or time periods, making reports more insightful and flexible.

#### How DAX Differs from Excel Formulas

- **Context-Based**: Unlike Excel formulas, which calculate at the cell level, DAX works at the row and filter level, making calculations adapt based on report filters.
- **Data Model Focused**: DAX is tightly integrated with the data model, allowing for table relationships to impact results automatically.
- **Performance-Oriented**: Designed for database efficiency, DAX calculations are optimized for large datasets, making it suitable for enterprise-level data analysis.

DAX’s functionality enhances Power BI by providing dynamic and powerful tools for data manipulation and analysis, allowing users to build complex calculations that drive deeper insights and enable more interactive and responsive reporting.

---

### Basic DAX Concepts

1. **Calculated Columns**
   - Calculated columns create new data in a table by defining formulas. These columns store results in the data model and can be used in relationships or as filters in reports.
   - **Example**: Creating a column for net amount after fees:
     ```DAX
     Net Amount = data[transaction_amount] - data[fee_amount]
     ```

2. **Measures**
   - Measures are calculations created using DAX that generate results dynamically, based on the context in which they are used (e.g., the filters or visualizations applied). Unlike calculated columns, measures do not store results in the data model.
   - **Example**: Calculating a dynamic total transaction amount:
     ```DAX
     Total Transaction Amount = SUM(data[transaction_amount])
     ```

3. **Row Context vs. Filter Context**
   - **Row Context**: When creating calculated columns, DAX evaluates formulas on a row-by-row basis.
   - **Filter Context**: When using measures, DAX evaluates formulas based on filters applied in the visualization, allowing calculations to change as users interact with reports.

---

### Common DAX Functions

1. **Basic Aggregations**
   - **Total Transaction Amount**: Calculates the sum of all transactions in the `transaction_amount` column.
     ```DAX
     Total Transaction Amount = SUM(data[transaction_amount])
     ```
   - **Total Fees**: Calculates the total of all fees in the `fee_amount` column.
     ```DAX
     Total Fees = SUM(data[fee_amount])
     ```
   - **Average Transaction Amount**: Calculates the average transaction amount.
     ```DAX
     Average Transaction Amount = AVERAGE(data[transaction_amount])
     ```
   - **Total Account Balance**: Gives the sum of all account balances in the `account_balance` column.
     ```DAX
     Total Account Balance = SUM(data[account_balance])
     ```

2. **Conditional Calculations**
   - **Transaction Count (Filtered)**: Counts the transactions where `transaction_type` is "Deposit."
     ```DAX
     Deposit Transaction Count = COUNTROWS(FILTER(data, data[transaction_type] = "Deposit"))
     ```
   - **Transaction Amount for Withdrawals**: Sums up only the transactions where `transaction_type` is "Withdrawal."
     ```DAX
     Total Withdrawals = CALCULATE(SUM(data[transaction_amount]), data[transaction_type] = "Withdrawal")
     ```

3. **Percentage Calculations**
   - **Transaction Fee Percentage**: Calculates the percentage of `fee_amount` relative to `transaction_amount` for each transaction.
     ```DAX
     Transaction Fee % = DIVIDE(data[fee_amount], data[transaction_amount], 0)
     ```
   - **Percentage of Total Transaction Amount by Branch**: Calculates each branch’s contribution to the overall transaction amount.
     ```DAX
     % of Total Transaction Amount = DIVIDE(SUM(data[transaction_amount]), [Total Transaction Amount], 0)
     ```

4. **Time-Based Calculations**
   - **Monthly Total Transactions**: Sums transactions month-by-month.
     ```DAX
     Monthly Total Transactions = CALCULATE(SUM(data[transaction_amount]), DATESMTD(data[transaction_date]))
     ```
   - **Year-to-Date (YTD) Total Transactions**: Sums transactions from the beginning of the year to the current date.
     ```DAX
     YTD Total Transactions = CALCULATE(SUM(data[transaction_amount]), DATESYTD(data[transaction_date]))
     ```
   - **Previous Month’s Transaction Total**: Compares the current month’s transactions to the previous month.
     ```DAX
     Previous Month Transactions = CALCULATE(SUM(data[transaction_amount]), DATEADD(data[transaction_date], -1, MONTH))
     ```

---

### Advanced Calculations

1. **Custom Measures with Calculations**
   - **Average Transaction Amount by Branch**: Calculates the average transaction amount specifically for each branch.
     ```DAX
     Avg Transaction by Branch = AVERAGEX(VALUES(data[branch]), CALCULATE(SUM(data[transaction_amount])))
     ```
   - **Total Fees by Branch**: Sums the fees for each branch individually.
     ```DAX
     Total Fees by Branch = CALCULATE(SUM(data[fee_amount]), ALLEXCEPT(data, data[branch]))
     ```

2. **Count Calculations**
   - **Distinct Customer Count**: Counts the unique customers in the `customer_id` column.
     ```DAX
     Distinct Customer Count = DISTINCTCOUNT(data[customer_id])
     ```
   - **Transaction Count by Branch**: Counts the number of transactions for each branch.
     ```DAX
     Transactions per Branch = CALCULATE(COUNT(data[transaction_id]), ALLEXCEPT(data, data[branch]))
     ```

3. **Row-Level Calculations with Calculated Columns**
   - **Net Transaction Amount**: Creates a calculated column for each transaction showing the net amount after fees.
     ```DAX
     Net Transaction Amount = data[transaction_amount] - data[fee_amount]
     ```
   - **Transaction Month**: Extracts the month from `transaction_date` for grouping transactions by month.
     ```DAX
     Transaction Month = FORMAT(data[transaction_date], "MMMM")
     ```

4. **Cumulative Totals**
   - **Cumulative Transaction Amount**: Running total of the transaction amount across time.
     ```DAX
     Cumulative Transaction Amount = CALCULATE(SUM(data[transaction_amount]), FILTER(ALL(data), data[transaction_date] <= MAX(data[transaction_date])))
     ```
   - **Cumulative Fees by Branch**: Cumulative total of fees for each branch.
     ```DAX
     Cumulative Fees by Branch = CALCULATE(SUM(data[fee_amount]), FILTER(ALL(data), data[branch] = EARLIER(data[branch]) && data[transaction_date] <= EARLIER(data[transaction_date])))
     ```

5. **Ranking Calculations**
   - **Rank by Transaction Amount**: Ranks branches based on their total transaction amount.
     ```DAX
     Rank by Transaction Amount = RANKX(ALL(data[branch]), CALCULATE(SUM(data[transaction_amount])), , DESC)
     ```
   - **Top 5 Branches by Transaction Count**: A measure for dynamic ranking where you could use this measure to filter only the top 5.
     ```DAX
     Top 5 Branches by Transactions = IF([Rank by Transaction Amount] <= 5, 1, 0)
     ```
