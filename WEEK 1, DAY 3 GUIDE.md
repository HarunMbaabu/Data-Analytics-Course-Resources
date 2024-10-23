### Topic: Data Formatting and Organizing Data

#### Objective
By the end of this session, students should understand how to apply advanced formatting to data, organize data using sorting and filtering, and manage worksheet structures.

### 2. Advanced Data Formatting

#### 2.1 Number Formatting
Excel provides several number formats that help present your data correctly.

- **General Format**: This is the default format for any cell. Numbers are displayed exactly as entered.
- **Number Format**: Displays numbers with commas and decimal points.  
  Example: `1000` becomes `1,000.00`.  
  - To apply this, select the cells you want to format, go to the **Home** tab, and click the dropdown in the **Number** section, then choose **Number**.
- **Currency Format**: This adds a currency symbol (like $ or €) and decimal points.  
  Example: `500` becomes `$500.00`.  
  - To apply this, select the cells, then click the **Currency** option in the **Number** dropdown.
- **Percentage Format**: Converts numbers to percentages.  
  Example: `0.5` becomes `50%`.  
  - To apply this, select the cells and click the **Percentage** button on the **Home** tab.
- **Date Format**: Changes the appearance of dates. Excel recognizes several date formats such as `10/22/2024` or `October 22, 2024`.  
  - To apply this, select the cells, click the dropdown in the **Number** section, and choose **Short Date** or **Long Date**.

#### 2.2 Custom Number Formatting
Excel allows you to create custom number formats for special cases.

- Example: To display a number with units (e.g., `1000` as `1,000 units`), you can use custom number formatting. Right-click the cell, select **Format Cells**, choose **Custom**, and enter a format like `#,##0 "units"`.

### 3. Managing Worksheets

#### 3.1 Inserting and Deleting Worksheets
- To insert a new worksheet, click the plus icon next to the existing sheet tabs at the bottom of your workbook. Alternatively, right-click a sheet tab and choose **Insert**.
- To delete a worksheet, right-click the sheet tab and choose **Delete**. Be careful, as deleting a sheet permanently removes its data!

#### 3.2 Renaming Worksheets
- Double-click the worksheet tab (e.g., Sheet1) and type a new name, such as "Sales Data" or "Q1 Report."

#### 3.3 Moving or Copying Worksheets
- To move a worksheet, click and drag the sheet tab to a new position.
- To copy a worksheet, right-click the sheet tab, select **Move or Copy**, then choose where to place the copy. Be sure to check the box for **Create a copy**.

#### 3.4 Grouping Worksheets
- If you need to apply the same changes to multiple sheets, you can group them. Hold **Ctrl** and click the tabs of the sheets you want to group.
- While grouped, any changes you make will apply to all selected sheets.

### 4. Sorting and Filtering Data

#### 4.1 Sorting Data
Sorting helps you organize data in a meaningful way. You can sort data alphabetically, numerically, or by date.

- **Sort A to Z**: For text, this arranges data alphabetically.  
  Example: Sorting names from A to Z.  
  - Select the column of data you want to sort, then in the **Data** tab, click **Sort A to Z**.
  
- **Sort Z to A**: This arranges data in reverse alphabetical order.  
  Example: Sorting names from Z to A.  
  - Use the **Sort Z to A** option from the **Data** tab.
  
- **Sort Smallest to Largest**: This arranges numerical data in ascending order.  
  Example: Sorting ages from youngest to oldest.  
  - Select the column with numbers, and choose **Sort Smallest to Largest**.
  
- **Sort Largest to Smallest**: This sorts numbers in descending order.  
  Example: Sorting sales figures from highest to lowest.  
  - Use the **Sort Largest to Smallest** option from the **Data** tab.

**Custom Sorting**:  
- Sometimes you need to sort based on multiple criteria. For example, you may want to first sort by "Region" and then by "Sales" within each region.  
  - Select your data, go to the **Data** tab, and click **Sort**. In the dialog box, you can add multiple levels of sorting.

#### 4.2 Filtering Data
Filtering allows you to view only the data that meets certain criteria. This is particularly useful for large datasets.

- To apply a filter, select the header row of your data (e.g., row 1), go to the **Data** tab, and click **Filter**.
- Small dropdown arrows will appear in each header cell. Click on these arrows to filter the data.  
  Example: In a list of cities, you can filter to show only rows where the city is "New York."

- **Advanced Filtering**: Use the **Text Filters**, **Number Filters**, or **Date Filters** options to filter data more precisely.  
  Example: You can filter numbers to show only values greater than 100.

**Hands-On Practice**:
1. Sort a list of employee names alphabetically and then by their hire date.
2. Apply filters to a dataset to show only rows where the sales are greater than $1,000 or the city is "New York."

### 5. Conditional Formatting

#### 5.1 Introduction to Conditional Formatting
Conditional formatting allows you to automatically apply formatting (like color-coding) to cells based on the data they contain. This helps highlight important information quickly.

- To apply conditional formatting, select the data range, go to the **Home** tab, click **Conditional Formatting**, and choose a rule.

#### 5.2 Examples of Conditional Formatting
- **Highlight Cells Rules**: You can highlight cells based on specific criteria.  
  Example: Highlight cells greater than 100 in red.
  
- **Top/Bottom Rules**: Highlight the top 10 values, the bottom 10 values, or those above or below average.  
  Example: Highlight the top 10% of sales figures in green.
  
- **Data Bars**: Add bars to visually represent data within the cells.  
  Example: Apply data bars to a column of sales numbers to show higher values with longer bars.
  
- **Color Scales**: Apply a gradient of colors to represent the range of values.  
  Example: Apply a color scale where lower values are red and higher values are green.

**Managing Conditional Formatting**:
- To edit or remove rules, go to **Conditional Formatting** > **Manage Rules**.

### 6. Wrap-Up and Review

#### Key Takeaways
- **Advanced Formatting**: You can format numbers as currency, percentages, or dates, and even create custom formats.
- **Managing Worksheets**: You can insert, rename, move, and group worksheets to better organize your data.
- **Sorting and Filtering**: Sorting helps you organize data, while filtering allows you to focus on specific parts of your dataset.
- **Conditional Formatting**: This helps highlight important data visually, making patterns and outliers easier to spot.
