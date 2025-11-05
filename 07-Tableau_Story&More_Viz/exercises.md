# Question 1: mirrored Funnel
- create a calculated field(number of customers)
```
COUNTD([Customer Name])
```
- duplicate the same calculated field
- add minus at the beginning
- measure values to the column
- leave only 2 calculated fields there we created
- use sorting -> field -> descending
- change the chart type to line in the marks
- press control/cmd and drag measure values in the column to the column again(this will duplicate measure values in the column )
- under marks select the second graph and drag measure names to the path
- go to the second measure values in the columns and choose dual axis
- you can play with choosing area or putting ship mode as a color.
- What are the limitations of this chart comparing the bar chart based simple one?
- If you would like to improve your funnel chart, please watch this [video](https://www.youtube.com/watch?v=2ndtx5ricOw)
- after the tableau extensions part we will see some ready templates to use without needing to prepare those calculated fields.



# Question 2: Create a sparkline (analyze trends over time)
**What is a Sparkline?**
A sparkline is a small, simple line chart that shows a trend over time. They’re compact and useful for dashboards to compare multiple trends at a glance.

## Let's create a Sparkline chart
- Drag  `Region` to Rows (This will create a separate line for each category.)
- Drag  `Sales` to rows
- Drag `Order Date`(choose Month or Quarter) to Columns and make it continuous
- Change Marks Type to Line(if not already)
- Right-click on axis → Hide Header.
- Optionally, remove gridlines for a cleaner sparkline look.
- (optional)Drag Category to Color to differentiate lines.


# Question 3: Bump Chart

This is an alternative to the dumbbell chart where you can use table calculations and create a different visualisation. As in the dumbell chart, we want to see sales in different region, but this time their rankings. Try to create a bump chart for the sales in different regions this time from the start year until the last year in the same workbook (for a more granular visualisation, you filter for one year and use month).

Check some examples [here](https://datavizproject.com/data-type/bump-chart-2/)


# Question 4: Review Stories
Check the tableau documentation about stories. Here is the [link](https://help.tableau.com/current/pro/desktop/en-us/story_create.htm)

Create a new story points based on the story you would like to tell based on what you prepared so far.
