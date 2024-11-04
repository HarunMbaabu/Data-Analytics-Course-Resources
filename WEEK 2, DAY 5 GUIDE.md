### Class Notes: Day 9 - Advanced Excel Techniques

#### Objective
Today’s session will cover advanced Excel features essential for handling, analyzing, and visualizing large datasets efficiently. By the end, students will understand how to apply these features to streamline data workflows, create insightful visuals, and conduct complex analyses.

1. **Introduction**
   - **Context:** We’ll be working with the agriculture dataset, which includes columns like Crop Name, Region, Total Yield, Revenue, and other metrics.
   - **Goal:** Learn advanced Excel tools to manage, analyze, and visualize data effectively.

2. **Freezing Panes and Splitting Windows**
   - **Freezing Panes**  
     Freezing panes keeps specific rows or columns visible as you scroll through large datasets.
     - **Example:** Freeze the header row in the agriculture dataset to always display column titles (e.g., Crop Name, Region, Total Yield).
     - **Steps:**
       1. Select the row below the headers (e.g., Row 2).
       2. Go to `View > Freeze Panes > Freeze Top Row`.
   - **Splitting Windows**  
     Split windows allow you to view different sections of the worksheet simultaneously.
     - **Steps:**
       1. Go to `View > Split`.
       2. Excel will split the window at your current selection, enabling you to scroll different sections independently.
   - **Hands-On Task:** Freeze the header row and split windows to view multiple parts of the dataset.

3. **Array Formulas and Dynamic Arrays**
   - **FILTER Function**  
     FILTER allows you to view specific entries that match certain criteria.
     - **Example:** Extract data for all rows where Region is “East”.
     - **Steps:**
       1. Click on an empty cell where you want the filtered data to appear.
       2. Enter the formula: `=FILTER(B2:F401, B2:B401="East")`
       3. Press Enter to view all rows with “East” in the Region column.
   - **UNIQUE Function**  
     UNIQUE helps identify distinct entries in a column, which is useful for summarizing data.
     - **Example:** List all unique Crop Names.
     - **Steps:**
       1. Select a blank cell.
       2. Enter the formula: `=UNIQUE(A2:A401)`
       3. Press Enter, and Excel will display each unique crop name.
   - **Hands-On Task:** Use FILTER to find entries with Region as “North” and UNIQUE to display distinct values in the Crop Name column.

4. **Advanced Lookup Functions (VLOOKUP, HLOOKUP, and XLOOKUP)**
   - **VLOOKUP**  
     VLOOKUP searches for a specific value in the leftmost column of a range and returns a value in the same row from another column.
     - **Example:** Find the Total Yield for “Wheat”.
     - **Steps:**
       1. Select an empty cell (e.g., G2).
       2. Enter the formula: `=VLOOKUP("Wheat", A2:D401, 3, FALSE)`
          - "Wheat": The crop name we’re searching for.
          - A2: The table range.
          - 3: Column index for Total Yield.
          - FALSE: Ensures an exact match.
       3. Press Enter. If “Wheat” is found, the Total Yield value will appear.
   - **HLOOKUP**  
     HLOOKUP works like VLOOKUP but searches horizontally across the first row.
     - **Example:** Suppose the dataset is transposed, and we want to find the Revenue for “Wheat” in the first row.
     - **Steps:**
       1. Select a cell (e.g., H2).
       2. Use: `=HLOOKUP("Wheat", A1:Z2, 2, FALSE)`
   - **XLOOKUP**  
     XLOOKUP is more flexible, allowing searches both horizontally and vertically, with additional error-handling options.
     - **Example:** Find the Revenue for “Maize” in the Region "West".
     - **Steps:**
       1. Select a blank cell (e.g., H2).
       2. Enter the formula: `=XLOOKUP("Maize", A2:A401, D2:D401, "Not Found")`
          - "Maize": Crop name to look for.
          - A2: Column to search within.
          - D2: Column containing values to return.
       3. Press Enter.
   - **Hands-On Task:** Use VLOOKUP to find the Total Yield for “Rice” and XLOOKUP to retrieve Revenue for “Barley”.

5. **Goal Seek for Analysis**
   - Goal Seek determines the input value needed to achieve a specific target result.
   - **Example:** If you want to know how much Total Yield needs to increase to achieve a certain average yield.
   - **Steps:**
     1. In a new cell, calculate the current yield average: `=AVERAGE(C2:C401)`.
     2. Go to `Data > What-If Analysis > Goal Seek`.
     3. Set Set Cell to the cell with the average formula.
     4. To Value: Enter your target average.
     5. By Changing Cell: Select a cell in the Total Yield column.
   - **Hands-On Task:** Use Goal Seek to set a target Total Yield average.

6. **Advanced Visualizations**
   - **Waterfall Chart**  
     A waterfall chart shows the progression of values over time, useful for seeing changes in Total Yield.
     - **Steps:**
       1. Select the data for Date and Total Yield.
       2. Go to `Insert > Waterfall Chart`.
   - **Combo Chart**  
     A combo chart combines two chart types, allowing side-by-side comparisons.
     - **Example:** Compare Total Yield and Revenue over time.
     - **Steps:**
       1. Select both columns (Total Yield and Revenue).
       2. Go to `Insert > Combo Chart`.
       3. Customize the series to display one as a column chart and the other as a line chart.
   - **Hands-On Task:** Create a combo chart showing Total Yield and Revenue.

7. **Advanced Pivot Table Features**
   - **Calculated Fields**  
     Calculated fields add custom formulas within pivot tables, useful for scenario analysis.
     - **Example:** Increase Total Yield by 10% to project possible yield improvements.
     - **Steps:**
       1. Insert a pivot table.
       2. Go to `PivotTable Analyze > Fields, Items & Sets > Calculated Field`.
       3. Enter the formula: `=Total_Yield*1.1` and press OK.
   - **Slicers**  
     Slicers filter pivot tables dynamically, making data exploration more interactive.
     - **Steps:**
       1. Click on your pivot table.
       2. Go to `PivotTable Analyze > Insert Slicer`.
       3. Select fields to add filters.
   - **Hands-On Task:** Create a calculated field to increase revenue by 15% and add slicers for Crop Name and Region.

8. **Wrap-Up and Q&A**
   - **Summary:** Today we covered navigation (freezing panes and splits), lookup functions, Goal Seek, data cleaning with Power Query, and advanced visualizations.
   - **Assignment:** Use today’s skills to create a report including:
     - One visualization (e.g., combo chart)
     - A formula (e.g., VLOOKUP or XLOOKUP)
     - A pivot table with slicers
