### Class Notes: Freezing Panes and Splitting Windows
#### Objective:
Understand how to use Excel's freezing panes and window-splitting functions to navigate large datasets effectively.

### Freezing Panes
Freezing panes in Excel is a feature that locks specific rows and/or columns in place, so they stay visible while scrolling through a large dataset. This is particularly useful when working with headers or row labels, as it keeps them accessible at all times.

#### Steps for Freezing Panes:
1. **Freezing the Top Row (for header visibility):**
   - Go to the View tab.
   - Click on Freeze Panes in the toolbar.
   - Select Freeze Top Row. This locks the top row so it stays visible as you scroll down.

2. **Freezing the First Column (for category labels):**
   - Go to the View tab.
   - Click Freeze Panes and select Freeze First Column to keep the first column visible when scrolling horizontally.

3. **Freezing Both Row and Column:**
   - Select the cell below the row you want to freeze and to the right of the column you want to freeze (e.g., click B2 to freeze row 1 and column A).
   - Go to View > Freeze Panes > Freeze Panes.
   - This freezes both row 1 and column A, which is useful for both header and label navigation.

4. **Unfreezing Panes:**
   - If you need to unlock the frozen rows/columns, go to View > Freeze Panes > Unfreeze Panes.

### Splitting Windows
The Split function divides the Excel window into separate, scrollable panes. This is helpful when comparing data from different parts of a large dataset.

#### Steps for Splitting Windows:
1. **Splitting the Window Horizontally:**
   - Click on the row where you want the split to occur (e.g., row 5).
   - Go to the View tab and click Split.
   - This will create a horizontal split at the top of row 5, allowing you to scroll each section independently.

2. **Splitting the Window Vertically:**
   - Click on the column where you want the split to occur (e.g., column C).
   - Go to the View tab and click Split.
   - This will create a vertical split on the left of column C, letting you scroll each section independently.

3. **Splitting the Window Both Ways:**
   - Click on a cell where you want both horizontal and vertical splits (e.g., C5).
   - Go to View > Split.
   - You’ll now have four separate panes, each scrollable independently.

4. **Removing Splits:**
   - Go to View > Split again to turn off the split view.

### Day 9: Pivot Tables and Pivot Charts

### Pivot Tables and Pivot Charts
#### Objectives:
- To create and customize pivot tables to summarize data.
- To use pivot charts for data visualization.

### 8.1 Introduction to Pivot Tables
A pivot table is a powerful tool in Excel for summarizing, analyzing, and exploring large datasets. It allows you to reorganize and group data quickly, providing a dynamic way to see trends or comparisons.

#### Creating a Pivot Table: Steps
1. **Select the Dataset:**
   - Click anywhere in your dataset.
   - Go to the Insert tab and select PivotTable.

2. **Choose PivotTable Location:**
   - In the dialog box, choose to place the pivot table on a new worksheet or in the existing sheet.
   - Click OK.

3. **Configuring the Pivot Table:**
   - You’ll see a PivotTable Field List on the right side of the screen.
   - Drag fields (column headers) to Rows, Columns, Values, or Filters areas.
   - For example, drag Region to Rows and Sales to Values to summarize sales by region.

#### Hands-On Activity:
1. Create a pivot table summarizing mental health cases by region (or other categories).
2. Experiment with moving fields to different sections to observe changes in data organization.

### 8.2 Pivot Chart Creation
A pivot chart is a visual representation of a pivot table, making it easier to understand data summaries and patterns.

#### Creating a Pivot Chart from a Pivot Table
1. **Select the Pivot Table:**
   - Click on any cell in the pivot table.

2. **Insert the Pivot Chart:**
   - Go to the PivotTable Analyze tab.
   - Click PivotChart and select the chart type (e.g., bar chart, line chart).

3. **Customize the Pivot Chart:**
   - Modify the chart’s layout, colors, and titles as needed.
   - Use the Filter options on the chart to adjust displayed data dynamically.

#### Hands-On Activity:
1. Using your pivot table from the previous activity, create a pivot chart to visualize data by region or case type.
2. Customize the chart with colors, labels, and filters.

### 8.3 Advanced Pivot Table Options
Grouping Data, Adding Slicers, and Using Calculated Fields

#### Grouping Data by Month or Category:
- To group dates or categories in your pivot table, right-click on a date field in the pivot table and select Group.
- Choose options like Months to summarize data monthly.

#### Using Slicers for Filtering:
- Click on the PivotTable Analyze tab, then Insert Slicer.
- Select fields (e.g., Region, Category) for filtering.
- Slicers act as interactive buttons to filter data visually.

#### Adding Calculated Fields:
- Go to PivotTable Analyze > Fields, Items & Sets > Calculated Field.
- Define calculations based on existing fields (e.g., `=[Sales]*0.1` for a 10% tax estimate).

#### Hands-On Activity:
1. Group data by Month in your pivot table.
2. Add slicers for interactive data exploration.
3. Create a calculated field, if applicable, for additional insights.

### Wrap-Up and Q&A
Pivot tables and charts offer powerful ways to analyze data efficiently. Take time to explore these tools to enhance your data insights.
