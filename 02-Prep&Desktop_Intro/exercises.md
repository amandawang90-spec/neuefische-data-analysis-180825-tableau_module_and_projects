# Question 1- Dirty Data
Although the exact definitions of dirty data types are not necessarily widely agreed upon we can still use some kind a definitions. Keeping in mind that classifying the type of dirty data is not nearly as important as to spot and fix the dirty data please review the classifications below to answer the question.

- **Invalid data**: Values that are not possible.  
  *Example*: A temperature of 300°C for a room environment.

- **Incorrect data**: Values that are possible but not accurate.  
  *Example*: A customer’s birth year listed as 2028.

- **Outdated information**: Data that was once correct but is no longer accurate.  
  *Example*: An employee's job title listed from 3 years ago.

- **Inconsistent data**: Same value written in different ways.  
  *Example*: “NYC”, “New York”, and “New York City” for the same city.

- **Inconsistent data types**: Same value using different formats.  
  *Example*: “$100”, “100.00”, and “one hundred” in a Price field.

- **Duplicate data**: Same data recorded more than once.  
  *Example*: The same transaction ID appearing in multiple rows.

- **Missing or incomplete data**: Data is partially or fully absent.  
  *Example*: “Spain” listed in a Country column, but no City provided.

Please take a look at the data below and try to spot!

| Order ID       | Name           | Order Date    | Quantity | Ship Mode  |
|----------------|----------------|---------------|----------|------------|
| TX-2021-098765 | Saffron        | 03/15/21      | 8        | Express    |
| NY-2019-123456 | Cod            | 2019-07-22    | -2       | Standard   |
| CA-2020-654321 | Basil          | 15-Aug-2020   | Three    | 2nd Class  |
| FL-2022-456789 | Mackerel       | 2022/05/30    | 5        |            |
| TX-2018-112233 | Turmeric       | June 12 2018  | 1        | First      |
| WA-2021-667788 | Salmon         | 04/01/21      | Two      | Express    |
| NY-2019-123456 | Cod            | 2019-07-22    | -2       | Standard   |
| FL-2022-456789 | Mackerel       | 2022/05/30    | 5        | Priority   |


# Question 2
For a deep dive check the video about [Data Interpreter](https://www.youtube.com/watch?v=Tt6lb1B1C6A)

# Question 3
**data prep exercise**
We will use another dataset for this exercise.
- check `fishspice_daily.csv` in a text editor(vs code)to see the data(we will do the data prep with tableau)
- create a new workbook in tableau(DO NOT continue with the same workbook where we worked with superstore!!)
- connect `fishspice_daily.csv`
- how can we fix the extra header problem with tableau interpreter?
- change the column names if necessary.
- Do you see any problem with prices? Can we solve it here using tableau interpreter? Why?
- Pivot the weekday columns (Monday–Friday) into two columns: one for the `Day`, and one for the `Prices`.(highlight all the day columns and say pivot, then you need to change the field names accordingly)
- This structure enables us to analyze sales by day or category.
- create a new worksheet
- make a bar plot using `Day` and `Prices`
- add `Category` to the colors for more detail.
- Is the visual showing correct Prices? Why not? 
- save the workbook with the proper format.

# Question 4
**sales by category and region implementation**
- Create a new worksheet in the same workbook.
- This bar plot visualisation should show different sales for:
    - Category and 
    - Region 
- Each bar should represent different sales amounts by category and region.
- You can make the bar plot more granular by adding profit.
    - Think about how to add profit to this example.
- Is it also possible to show subcategories in this visualisation? Try to explore!
- Give the worksheet a descriptive name (Sales by Categories and Regions)
- Save the updated workbook.

# Question 5
**Sales by Year and Ship Mode**
- create a new worksheet
- create a bar chart that shows total sales for each year.
- think about how can we see how different shipping methods contribute to annual sales.
- Also add region to the view to compare sales across different regions.
- also change the colors according to your taste
