# Question 1: Working with Dates in Tableau
Please check the **Date Functions Cheat Table** below for detailed usage.
## 📚 Date Functions Cheat Table (Tableau)

| Function           | Example                                         | Description                                                       |
|--------------------|-------------------------------------------------|-------------------------------------------------------------------|
| `TODAY()`          | `TODAY()`                                       | Returns the current date                                          |
| `NOW()`            | `NOW()`                                         | Returns current date and time                                     |
| `DATE()`           | `DATE("2025-06-25")`                            | Converts a string or number to a date                             |
| `DATENAME()`       | `DATENAME('month', [Order Date])`              | Returns the name (e.g. "January") of the date part                |
| `DATEPART()`       | `DATEPART('weekday', [Order Date])`            | Returns the numeric part of a date (e.g. 1 for Sunday)            |
| `DATEDIFF()`       | `DATEDIFF('day', [Order Date], TODAY())`       | Returns number of units (e.g. days) between two dates             |                   
| `YEAR()`           | `YEAR([Order Date])`                            | Extracts the year                                                 |
| `MONTH()`          | `MONTH([Order Date])`                           | Extracts the month (1–12)                                         |
| `DAY()`            | `DAY([Order Date])`                             | Extracts the day of the month                                     |

**Tip:** Use `DATENAME()` when you want labels (like "March"), and `DATEPART()` when you want numbers (like 3).

Let's have a small exercise with it 
- Create a **new worksheet**.
- Drag `Order Date` to Rows → right-click → choose **Exact Date**.
- Create a new **calculated field**: `Weekday Number`
     ```tableau
     DATEPART('weekday', [Order Date])
     ```
- Drag `Weekday Number` to Columns.
- click on the pill and choose discrete
- Drag `Sales` to Rows.
- Explore the sales performance by day of the week.
- you can also add years filter if you like

  
# Question 2: Dynamic time grouping
Using parameters and calculated fields we would like to have an option to show how to switch between different ways of grouping dates (years / months / quarters, etc.)
For this one we can use the hierarchy while creating the visual. However when we present our findings in a dashboard, we need a dropdown menu to be able to choose years / months / quarters, etc.

- Create a parameter with year , month , quarter, week options(choose list, string) and name it as `Order Date Group`

- Use the syntax below and create the calculated field.

```
if[Order Date Group] = 'quarter' then datename('year', [Order Date]) + datename('quarter', [Order Date])
elseif [Order Date Group] = 'year' then datename('year', [Order Date])
elseif [Order Date Group] = 'month' then datename('year', [Order Date]) + datename('month', [Order Date])
else datename('year', [Order Date]) + datename('week', [Order Date])
end
```
- Drag the calculated field `Dynamic Date Group` to Columns(discrete, dimension)
- Drag `Sales` to Rows
- Show the `Order Date Group` parameter control to allow switching between time groupings

# Question 3: Detect Keywords in Product Names

- Open a new worksheet using the Superstore dataset.
- Bring in `Product Name` and `Sales`.
- Create a **calculated field** to check whether the product name mentions a specific word (e.g. `"office"`).
- Use a text function to detect if the word is part of the name, regardless of capitalization.
- Label the records based on whether they **contain** the keyword.
   - For example: `"Mentions Office"` vs `"No Mention"`.
- Visualize this with a bar chart showing `Sales` for each group.
- Bonus: Try using other keywords like `"chair"` or `"phone"` to build similar logic.



# Question 4: Customer Names and Data Protection:
- Sensitive data and GDPR. What do you think we could do to make this data more anonymous? (In this exercise we will reduce the first name to only the first letter but a better idea would be to give the customers their unique idea so we don't work with the names at all).
- You can duplicate the worksheet "sales by customers" and try it there.
- "Create a calculated field that will be the last name plus the first letter from the first name (an approach for anonimizing the data)"
- **HINT:** please check the `left` & `split`on the [link](https://help.tableau.com/current/pro/desktop/en-us/functions_functions_string.htm) for string functions in tableau


# Question 5: Create a table for categories and subcategories vs segment

- How high is the percentage of individual sub-categories in the various segments?
- The idea is having a table for the percentage sale of the different subcategories in different segments.
- Calculate the percentage of each Subcategory's sales within its Segment using quick table calculations.

# Question 6: 100% stacked bar plot
- What kind of barplots do you know?
- What do you know about the idea behind 100% stacked bar plot? (https://www.perceptualedge.com/blog/?p=2239)
- Make some research (and discuss with your classmates).
- Make a 100% stacked bar plot which represents the share of categories (in terms of sales) in each year
- Outcome: 4 differrent bars, representing each year, all of them are stacked bars, however showing the 100%. Each category should be represented with different colors.

# Question 7: Create a treemap with subcategories

- Use the subcategories to make a treemap(Explore Show Me on the toolbar)
- You can decide either to focus on sales or profit.
- Making your treemap even more granular, you can focus on segment or shipmode.

# Question 8:
How do calculated fields differ from table calculations in Tableau? Can you provide examples of when to use each?

# Question 9: 
For more detailed knowledge about aggregated and non-aggregated calculated fields, please check the [link](https://www.theinformationlab.nl/2022/06/13/difference-between-aggregated-and-non-aggregated-calculations-in-tableau/)
