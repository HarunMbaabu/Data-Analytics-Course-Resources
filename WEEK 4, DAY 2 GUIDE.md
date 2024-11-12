TODOs: 

- Understand power bi features.
  
- Learn the different parts we can load data from.
  
- Understand different ways of loading data.
  
        - Understand how to get json, excel and csv data(Files were shared in the WhatsApp group).
  
        - Learn how to load data from web and sql server.
  
                    **Example:**
                               (i) Olympics data 2020: https://en.wikipedia.org/wiki/2020_Summer_Olympics_medal_table.
                               (ii) Staock data for Apple, Google and Microsoft : https://vincentarelbundock.github.io/Rdatasets/csv/Stat2Data/TechStocks.csv


  ##**Features of power query:**
  ![features of power query](https://k21academy.com/wp-content/uploads/2021/04/img4.png)

- **Queries Pane**: A new query tab named **TachStocks** (our dataset's name) has been created.

- **Name Section (Query Settings)**: Displays the name of the query currently in use.

- **Menu**: This ribbon provides various functions and operations we can apply to the dataset.

- **Column Names**: Shows the names of the dataset columns along with symbols that indicate each column's datatype. There’s also an arrow button to select entire columns and perform column operations.

- **Applied Steps Section (Query Settings)**: Lists all transformation steps applied to the query. Although we’ve only performed a simple query by importing the dataset, the Power Editor has automatically applied some initial steps, including:
   - Setting column names as headers (Promoted Headers)
   - Assigning datatypes to all columns (Changed Datatype)

   By clicking on any query step, we can view the dataset in its transformed state up to that specific step. For example:
   - Selecting the **Promoted Headers** step displays the dataset with headers as column names, but without assigned datatypes.
   - The **Changed Datatype** step shows the dataset after all query steps have been applied, including datatype assignments.

- **Formula Tab**: When on the **Changed Datatype** step, this tab shows the M-Language code snippet executed in the backend to apply the transformation.



**Complete the examples from week 4, day 1 on Power BI Power Query and DAX((Data Analysis Expressions).** 
