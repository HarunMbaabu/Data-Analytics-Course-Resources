### 2. Connecting to Data Sources
**Objective**: Learn how to import data from various sources, understand different data types, and perform hands-on data imports.

#### Get Data
1. **Home > Get Data**: Select the appropriate source. Common options include:
   - **Excel**: Widely used for structured datasets.
   - **CSV/Text**: Common format for flat files without complex relationships.
   - **SQL Server**: Often used for enterprise databases with relational data.
   - **Web**: Useful for scraping data directly from a URL.
2. **Navigator Window**: Once you’ve selected a source (e.g., Excel), Power BI opens the Navigator window to preview the tables or sheets. Select specific tables or all data, then click Load to import.

#### Understanding Data Types
- **Flat Files (CSV/Text)**: Single tables without relationships.
- **Relational Databases (SQL)**: Structured with multiple tables linked by relationships.
- **Cloud Data (API/Web)**: Pulls from online sources, often dynamic and refreshed.

**Example**:
1. Go to **Home > Get Data > Excel**.
2. Select a sample Excel file (e.g., sales data) with sheets named Customers and Sales.
3. In the Navigator, select both sheets and click Load to bring data into Power BI.
4. The loaded data appears in the Fields pane, where each table and column is listed.

### 3. Data Transformation with Power Query
**Objective**: Use Power Query to clean and shape data for analysis, making it ready for accurate visualizations and reports.

#### Opening Power Query Editor
- Go to **Home > Transform Data** to open the Power Query Editor.
- Power Query Editor provides a robust set of tools for manipulating and transforming data.

#### Power Query Editor Basics
- **Query Pane**: Lists all tables and applied transformation steps for each table.
- **Data View**: Shows the selected table with transformation options available in the ribbon.
- **Applied Steps Pane**: Lists each action applied to a table, allowing you to edit or remove steps.

#### Data Cleaning
1. **Removing Unnecessary Columns**
   - Select the column, right-click, and choose Remove. This streamlines data by focusing on relevant fields.
   - **Example**: Remove the Address column if it’s unnecessary for the analysis.
  
2. **Renaming Columns**
   - Double-click the column name to rename it for clarity.
   - **Example**: Rename “Cust_ID” to “Customer ID” to make the dataset more understandable.
  
3. **Filtering Rows**
   - Click on a column header filter icon to remove irrelevant rows.
   - **Example**: Filter out rows where Sales has null values to ensure accurate summaries.

### Handling Missing Values
- Use Replace Values to fill missing data.
- **Example**: Replace null values in the Sales column with 0 or an average, depending on the business logic.

#### Transformations
1. **Merging Queries**
   - Use **Home > Merge Queries** to join tables based on common fields.
   - **Example**: Merge Customers and Sales tables using Customer ID as the key to create a more comprehensive dataset.
  
2. **Appending Queries**
   - Use **Home > Append Queries** to stack tables with similar columns.
   - **Example**: Append data from multiple months into a single table for time-based analysis.
  
3. **Pivoting and Unpivoting Data**
   - **Pivot**: Turns row values into columns.
   - **Unpivot**: Turns columns into rows.
   - **Example**: Unpivot month columns to create a Month field for each row, enabling monthly trend analysis.

4. **Changing Data Types**
   - Ensure each column has the correct data type for calculations and analysis. Right-click the column, select Change Type, and choose the appropriate type.
   - **Example**: Set Sales to Decimal Number and Order Date to Date for accurate date-based filtering and analysis.

### Practical Exercise
- **Goal**: Practice cleaning and transforming a dataset for analysis.
- **Example**:
  1. **Import**: Import a Sales dataset.
  2. **Remove**: Delete irrelevant columns like Customer Address.
  3. **Rename**: Update column names for readability, e.g., changing “Sales_ID” to “Sales ID”.
  4. **Filter**: Exclude records with null Sales Amount values.
  5. **Unpivot**: Unpivot monthly columns to make Month a separate field.
  6. **Merge**: Merge Sales and Customer tables on Customer ID.
  7. **Change Type**: Set Sales Amount as a Decimal Number and Order Date as Date.

### Key Takeaways for Day 1
- Familiarity with Power BI’s interface and basic functions for data loading.
- Confidence in navigating Power Query Editor for data transformation.
- Experience in performing essential data-cleaning actions such as removing columns, renaming, filtering rows, and merging tables.

### Practice Work
- Import a new dataset, perform basic transformations, and create a clean, ready-to-use dataset.
- Experiment with merging and appending tables to practice data consolidation.

Day 1 provides the foundational skills for data preparation and transformation in Power BI. You'll apply these skills when modeling data on Day 2.
