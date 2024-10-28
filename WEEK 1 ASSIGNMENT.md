# WEEK 1 ASSIGNMENT

## Tasks

### 1. Data Entry and Formatting
- **Formatting:**
  - Apply bold and color to the headers and increase their font size.
  - Adjust column sizes.
  - Use conditional formatting for:
    - Export values exceeding $200,000 in bold blue.
    - Rainfall levels exceeding 15mm in green.
  - Format Export Value and GDP Contribution columns to show USD currency, and Rainfall to one decimal place.
  - Highlight High Unemployment: Use conditional formatting to highlight cells in red in the Unemployment Rate column where the unemployment rate exceeds 20%.

### 2. Basic Formulas and Functions
1. **Calculate Total Export Value:**
   - Use `SUM` to calculate the total Export Value across all months and regions in a cell below the Export Value column.
   
2. **Average Temperature and Rainfall:**
   - Use `AVERAGE` to calculate average values for Temperature and Rainfall across all data.

3. **GDP Contribution by Product:**
   - Use `SUMIF` or `COUNTIF` to calculate the total GDP Contribution from each product (Livestock, Bananas, Fish) in a separate table to the right of your main data.

4. **Total Export Value:**
   - Calculate the total export value for each year and region.
   - Formula Example: Use `SUMIF` to total by year or region.

5. **Average Metrics:**
   - Calculate the average monthly temperature, rainfall, unemployment, and literacy rates for each region over the year.
   - Formula Example: Use `AVERAGEIF` to filter data by region.

### 3. Sorting and Filtering
1. **Sort by Export Value:**
   - Sort the dataset in descending order to identify months with the highest export values.

2. **Filter by Region:**
   - Use filters to show data for only Mogadishu, and identify months with an unemployment rate under 18%.

### 4. Conditional Functions (20 points)
1. **Unemployment Analysis:**
   - Use `IF` to label each month’s unemployment rate as:
     - “High” if above 20%,
     - “Moderate” if between 15%-20%,
     - “Low” if below 15%.
   - Place this in a new column labeled “Employment Status.”

2. **Literacy Rate Threshold:**
   - Use `COUNTIF` to calculate the number of months where literacy rates were above 50%.

3. **Export Threshold:**
   - Use `SUMIF` to total the Export Value for each region if exports are above $100,000.

### 5. Date Functions
1. **Current Date:**
   - In a cell labeled “Report Generated On,” use the `TODAY` function to display the current date.

2. **Data Entry Timestamp:**
   - Use the `NOW` function to show the date and time when the dataset was last updated.

### 6. Text Functions
1. **Product-Region Labels:**
   - Create a new column called “Export Label” and use the `CONCAT` function to combine Product Exported and Region columns, separated by a hyphen (e.g., “Livestock-Mogadishu”).

2. **Region Formatting:**
   - Use `PROPER` in a new column to format all region names in title case.

### 7. Advanced Summary and Presentation
1. **Summary Table:**
   - Create a table summarizing key metrics:
     - Total Export Value for each region,
     - Highest and Lowest Temperature values for the year,
     - Months with Export Value above $200,000.

2. **Formatting:**
   - Apply borders and shading to the summary table.
   - Add a title at the top of the worksheet, “Somalia Economic & Climate Analysis,” in a larger, bold font.

## Submission Requirements
- Submit the completed Excel workbook with:
  - Cleaned data (with errors annotated where corrected).
  - Formulas applied for calculations as instructed.
  - Conditional formatting rules set as instructed.
  - Correctly formatted and labeled charts.
- Name your workbook as your name followed by week 1 assignment, e.g., “Ali Hussein week 1 assignment”.
- Submit your assignment by Sunday 27th October 2024, 7PM.
