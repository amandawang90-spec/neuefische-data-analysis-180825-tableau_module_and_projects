# Question 1: Tableau Extension exercise: Work on sankey
- Replace `Sales` with `Profit` to compare flows.
- Try different combinations of categorical levels (e.g., `Segment`, `Ship Mode`, `Category`).
- Discuss use cases: When would a Sankey diagram be more informative than a bar chart?

# Question 2: Tableau Dashboard Extension Exercise – Dynamic sunburst (Superstore)
A dynamic sunburst chart shows hierarchical data (like categories → subcategories → items) as concentric rings, where each ring level represents a hierarchy level — and it updates interactively based on filters or selections.

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


# Question 3: Row-Level Security (RLS) Exercise

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
- Right-click in the **Data Pane** → *Create Calculated Field*.
- Name it: `Access Filter`
- Paste this formula:

```tableau
USERNAME() = [Username]
```

- Go to a new worksheet.
- Drag `Name` to **Rows**.
- Drag `Sales` to **Columns**.
- (Optional) Drag `Region` to **Color** to differentiate regions visually.
- You should see a simple bar chart showing sales by name.
- Locate the `Access Filter` calculated field in the Data Pane.
- Drag it onto the **Filters Shelf**.
- In the dialog that appears, check only `True`, then click OK.
- This filter now hides any rows where the logged-in user does not match the username in the permissions table.

# Question 4: Workaround for Trying Ask Data with Superstore:
- create a new workbook and connect with superstore data
- you can create 1-2 vizs to test(additional)
- Go to Server > Publish Data Source.
- Publish it to your Tableau Cloud or Server site.
- Once published, go to your browser → navigate to the data source → click “Ask Data”.
- Now you can ask:
    - “Show sales by region in 2024”
    - “Top 5 products by profit”

# Question 5: Synonyms
- Go to Ask Data > Data tab > Manage Synonyms.
- Add synonyms for some fields. For example:
    - "Sales" → add "revenue"
    - "Profit" → add "earnings" or "net income"
    - "Region" → add "area"
- Test whether Ask Data recognizes these synonyms in new queries.

# Question 6: Understand how field visibility impacts user experience with Ask Data
- Hide irrelevant fields (like Row ID or Lat/Long) or reorder fields logically.
- Republish the data source.
- Use Ask Data again and notice how suggestions or search results improve.

# Question 7: Use Ask Data to Build a Viz and Save to a Workbook
- Ask a question (e.g., “sales by category in 2023”).
- Refine the chart using Ask Data’s visual editor (change chart type, filter).
- Click “Save As” → create a new worksheet or dashboard from it.
- Try to build the same view manually in Tableau Desktop.
- Compare the results and formatting. Is there any difference?
- enable Data Stories.
- Read the automatically generated narrative and verify if it matches the data.
