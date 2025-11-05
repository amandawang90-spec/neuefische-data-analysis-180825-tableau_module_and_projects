# Question 1: Include LoDs

- please check this article about "the include LoDs
" to be able to understand the concept. 
https://help.tableau.com/current/pro/desktop/en-us/calculations_calculatedfields_lod_include.htm

- and try to create the same logic in your workbook  on the same map that we work with LODs but for `avg sales per customer in states`


# Question 2: Create a dashboard called 'KPIs dashboard'
  - add title
  - add the map

- create a KPIs Story
  - add kpis dashboard to the story


# Question 3: Subcategories for Different Segments - Percent of Total

- Create a table with subcat, segment and Sales.
- Verify the Quick Table Calculation on `SUM(Sales)` is set to `Percent of Total` with *Compute Using* set to `Table (down)`.
- Click on *Chairs* and use **Keep Only**; then revert.
- Create a calculated field using a FIXED LOD expression for segment sales.
- Create another calculated field to calculate the ratio of sales over the segment total.
- Place this field on **Text** and format it as a percentage.
- Filter to *Chairs* again and observe the difference.

---

# Question 4: New vs Recurring Customers Visualization

- Create a new worksheet.
- Use `Order Date` (year) on Columns and `Sales` on Rows.
- Change Marks to Bar and apply a Quick Table Calculation of `Percent of Total` (compute using table down) on `SUM(Sales)`.
- Create a calculated field with FIXED LOD to find each customer’s first order date.
- Add this field to Color.
- Add `Sales` to Label and apply the same table calculation.
- Analyze the sales proportions for new vs recurring customers.



# Question 5: Combined sets

- create 2 sets 
- one, representing top 100 customers by sales 
- second, representing customers that are generating negative profit. 
- Check if there are any customers that are in both of the groups 
- create a 3rd set which is a combination of the two Visualize the results in a preferable way


