# Question 1: Tableau Extension exercise: Work on sankey
- Replace `Sales` with `Profit` to compare flows.
- Try different combinations of categorical levels (e.g., `Segment`, `Ship Mode`, `Category`).
- Discuss use cases: When would a Sankey diagram be more informative than a bar chart?

# Question 2: Tableau Dashboard Extension Exercise – Dynamic sunburst (Superstore)
A dynamic sunburst chart shows hierarchical data (like categories → subcategories → items) as concentric rings, where each ring level represents a hierarchy level — and it updates interactively based on filters or selections.

**Lets show Profit distribution across hierarchy**
- Create a new worksheet(profit by location).
   - `Country/Region`, `Region`, and `State/Province`(SKIP AREA) to the columns
   - `Profit` to the rows
   - You can use a time filter for months or years if you want
   - Go the dashboards and add the new sheet to the dashboard. 
   - On the left side under `Objects` find Extension
   - Search for Dynamic Sunburst and add it into the dashboard.
   - Select the sheet(profit by location)
   - Select `Profit`
   - your dynamic sunburst is ready.
   - Each ring segment’s size is proportional to the selected measure (Profit in your case).

# Question 3: (Optional)
- Use the extensions to create a funnel chart.
- Click on the extensions in a new worksheet and search for funnel chart.
- It asks for your email address to provide a code(therefore optional)
- give the code and activate
- add `Segment` into the dimensions
- Add `Sales` to the measurements

# Question 4: Reading
Learn and Explore more viz extension options [here](https://www.tableau.com/blog/your-guide-tableau-viz-extensions)

# Question 5: Row-Level Security (RLS) Exercise
We are going to try to simulate RLS principles without connecting to the server. Parameter is going to help us to mimic the USERNAME in the server.

## Prepare Your Files
- Create the following two CSV files on your computer:
### a) `spicefish_data.csv`

| Name        | Region | Email           | Sales |
|-------------|--------|------------------|--------|
| Dill Corp   | East   | dill@xyz.com     | 9000   |
| Pepper LLC  | West   | pepper@xyz.com   | 8500   |
| Zahtar Inc  | East   | zahtar@xyz.com   | 4000   |
| Salmon Inc  | South  | salmon@xyz.com   | 2000   |

### b) `user_access.csv`

| Username            | Region |
|---------------------|--------|
| spicy@example.com   | East   |
| neue@company.com    | West   |
| fische@firm.org     | South  |

- Save both files locally and remember the folder path.
- Open a new workbook in **Tableau Desktop**
- Choose **"Connect" → "Text File"**.
- Connect to `spicefish_data.csv`.
- In the **Data Source** tab, click **"Add"** → connect to `user_access.csv`.
- Create an **inner join** between `Region` fields.
- Your joined table should now include:
    - Name, Email, Sales (from `spicefish_data`)
    - Username (from `user_access`)
    - Only matching regions from both tables will remain.

- Create a parameter(this part will mimic the server permission):
    - name it `Simulate User`
    - choose string and list
    - add all the email addresses you have in your data

- Right-click in the **Data Pane** → *Create Calculated Field*.
- Name it: `Access Filter`
- Paste this formula:

```tableau
[Simulate User] = [Username]
```

- Go to a new worksheet.
- Drag `Name` to **Rows**.
- Drag `Sales` to **Columns**.
- (Optional) Drag `Region` to **Color** to differentiate regions visually.
- You should see a simple bar chart showing sales by name.
- Show the parameter `Simulate User`
- Locate the `Access Filter` calculated field in the Data Pane.
- Drag it onto the **Filters Shelf**.
- In the dialog that appears, check only `True`, then click OK.(do not show filter, we are only seeing if it is true)
- This filter now hides any rows where the logged-in user does not match the username in the permissions table.

# Question 6: More Viz: 
## Exercise 1: Dumbell Chart
**Let's explore Sales over time by Region and Category.**
This Dumbell chart highlights trends in sales, showing both the total trend (line) and the individual yearly values (circles) for each region and category. It helps identify peaks, dips, and overall performance.

- Create a new worksheet.
- Drag `Sales` to Columns.
- Drag `Region` and `Category` to Rows.
- Change the chart type to **Line**.
- Drag `Order Date` to Path (this defines the line order along the timeline, we used it in the funnel chart).
- Drag `Year(Order Date)` to Filters → select Years, and enable First and Last Year in your dataset.
- Drag `Sales` again to Columns → in the Marks card, select Circle for this second measure.
- Combine both charts into a dual-axis chart (Synchronize axes if necessary.)
- Drag `Year(Order Date)` to Color in the circle card under marks.
- analyze the chart


## Exercise 2: Alternative for the Dumbell Chart
You previously created a dual-axis chart (line + circles) to visualize sales trends by Region and Category over time.(showing the first and last year)
Explore an alternative way to visualize the same data using bar graph instead of lines and circles.

Hint:
- Use `Order Date`, `Sales`, `Region` and `Category` in rows or columns
- Use `Order Date` as filter to show only first and last year. 



