
 
### Differentiate Report vs Dashboard. 

A **report** provides a detailed, static analysis of data, often with tables, charts, and narrative explanations. Shared periodically, reports give historical insights ideal for managers or analysts needing in-depth information on specific topics, like financials or compliance.

**Report Example 1**
![image](https://github.com/HarunMbaabu/Data-Analytics-Course-Resources/blob/main/assets/operations-dashboard-example.png)


A **dashboard** gives a high-level, real-time overview of key metrics through interactive visuals like charts and KPIs. Dashboards are ideal for quick decision-making, allowing users to adjust filters or drill into data for instant insights, making them popular for tracking ongoing performance. 

**Dashboard Example 1:**
![image](https://github.com/HarunMbaabu/Data-Analytics-Course-Resources/blob/main/assets/operations-dashboard-example.png)

### 1. Flat Files (CSV/Text)
- **Explanation**: Flat files, like CSV or text files, contain data in a single table without any built-in relationships. Think of them as simple spreadsheets where all data is in rows and columns, without links to other tables.
- **In Power BI**: Flat files are easy to import and ideal for small datasets or lists. When loading a CSV into Power BI, you’re pulling in a single table, so any relationships between tables need to be created manually in Power BI if you bring in additional files.

### 2. Relational Databases (SQL)
- **Explanation**: Relational databases, such as those using SQL, are structured collections of tables linked by relationships. These tables use unique keys (like IDs) to connect to each other, which helps manage large datasets with many related tables (e.g., customer, orders, and products tables).
- **In Power BI**: Power BI connects to relational databases to pull in multiple related tables at once. The relationships between tables are often recognized automatically, preserving the database structure, so you don’t have to manually link tables. This makes it easier to explore data across related categories.

### 3. Cloud Data (API/Web)
- **Explanation**: Cloud data comes from online sources and is often accessed through APIs (Application Programming Interfaces) or web services. This type of data is usually dynamic and frequently refreshed, so it provides the latest data without having to reload files manually.
- **In Power BI**: Power BI can connect to cloud data sources directly, allowing for live or scheduled data refreshes. This is great for up-to-date analytics, like tracking social media metrics, website data, or other online services that change in real time.





