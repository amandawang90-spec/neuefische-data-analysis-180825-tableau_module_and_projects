# Question 1: Creating a Custom Continuous Color Palette in Tableau
- Go to a color palette website like [Coolors](https://coolors.co/) or [Color Hunt](https://colorhunt.co/) to find a gradient palette you like (look for 3–5 harmonious colors).
- Copy the HEX codes of your selected colors. For a smooth continuous effect, pick colors that transition well.
- Open your **My Tableau Repository** folder
- Locate and open the file named `Preferences.tps` with a text editor as we did during the lecture (e.g., Notepad, VSCode). 
-  Inside the `<preferences>` tag, add a new **continuous** color-palette entry like the one we added but this time not regular!!

```xml
<workbook>
  <preferences>
    <color-palette name="give it a Name" type="ordered-sequential">
    .....
```
- save it and restart your workbook
- change the continues colors with the palette you have just created in a proper viz.
- you can also practice creating another `type="ordered-diverging">`

# Question 2: Create a scatterplot with animation
- Use `Sales` and `Profit` 
- You can use `Sub-Category` as Detail and Color.
- Use the Pages control to cycle through each `Quarter/year(continuos)`.
- Observe how marks move and update dynamically.(it is not going to be a pretty animation unfortunately, it is only for practice)
- Instead of order date you can also use region and add both animations into one dashboard and connect them with each other. 
- Drag both worksheets (line chart and scatter plot) into the dashboard.
- Add filter actions between views or enable filters in the dashboard.
- Interact with filters or Pages to observe smooth transitions.

# Question 3: Netflix Practice Exercise in Tableau

This exercise is inspired from Tableau Business Intelligence Analyst Professional Certificate course notes. The datasets appear to be custom-prepared practice datasets modeled on real Netflix metadata (Kaggle). Then, they were intentionally split into multiple sheets/files/tables

This exercise will guide you through integrating multiple Netflix-related data sources using Tableau. You'll apply concepts like joins, relationships, unions, and blending.

## Practice Joins 
- Connect to the **Netflix Titles** data source.
- Drag the **Titles** table onto the canvas.
- Collapse the metadata grid for clarity.
- Double-click the Titles table to enter the physical layer.
- Drag the **Details** table next to Titles.
- Edit the join clause to match:
  - `Titles.Show ID` with `Details.Show`
- Ensure an **Inner Join** is used to avoid nulls.
- Hide duplicate or unnecessary fields (e.g., redundant `Show` field).

## Create Relationships 
- Back in the logical layer, drag:
  - **Categories** table → relate using `Show ID`
  - **Countries** table → relate using `Show ID`
- Confirm relationships were detected correctly using the metadata grid.

> *Tip: Use the data preview panel to verify that categories or countries may contain multiple entries per show ID.*

## Connect to New Data Source
- Click `Add` > `To a File` > `More`.
- Load **Netflix Cast and Descriptions**.
- Double-click the main table area to enter the physical layer.
- Drag the **Descriptions** table to the canvas.
- Join it to the previously joined Titles/Details table using `Show ID`.
- Hide any duplicate `Show ID` field after joining.

## Create a Relationship with Cast
- Back in the logical layer, drag the **Cast** table.
- Set up a relationship using `Show ID`.
- Resolve any linking field warnings by matching `Show ID` from Cast with the main table.
- go next to the title and give the source project the name `Netflix` and click on the arrow next to the title/database logo to follow the next instructions

## Add Third Data Source – Directors
- Click `New Data Source`
- Load **Netflix Directors**.
- Rename the source for clarity (e.g., "Netflix Directors").

## Union Directors Tables
- First check the [unions](https://help.tableau.com/current/pro/desktop/en-us/union.htm)
- Drag `Directors 2` onto the canvas.
- Drop it onto `Directors` to initiate a **Union**.
- Hide the table name field (used to track which table rows came from).

## Blend Data Between Sources
- Add a worksheet and observe that both data sources are available.(There should be two data source projects, `Netflix` and `Netflix Directors`)
- Drag `Title` (from Netflix Titles source) to Rows.
- Drag `Cast` (from Netflix Cast source) to Detail or Tooltip.
- Click on the **broken link icon** next to `Show ID` in the secondary source (e.g., Netflix Directors).
- Activate the link to establish the connection.
- Now drag `Director` to the view — it should blend properly.

---

## Summary

You have now:
- Joined tables across the same source
- Created relationships to avoid duplication
- Used unions to stack similar tables
- Blended data across multiple sources
