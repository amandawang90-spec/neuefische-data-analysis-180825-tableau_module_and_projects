# Question 1 Keep exloring different chart types:  Waterfall chart using table calculations

- Research examples of waterfall charts.
- Create a waterfall chart that shows the development of Profit for each Month throughout the year.
- Hints:
    - You can filter for only one year so it’s more visible (add Year to filter and then show the filter).
    - Add additional filter and so you can explore the data even more (e.g. Category).
    - Try using the Gantt Bar mark type to represent the data.
    - The bars need to grow downwards, so we need to use a negative sum.
        - How could we achieve that?
        - Spoiler: https://www.youtube.com/watch?v=nKzdKGcXnv0
          and https://evolytics.com/blog/tableau-201-make-waterfall-chart/
    - Maybe you want to edit the Tooltip in the end.

# Question 2 Hands on Box Plot Exercise
## What is a Box Plot?
A box plot is a graphical representation that summarizes data distribution through five key metrics: minimum, first quartile (Q1), median, third quartile (Q3), and maximum. It helps you understand the spread and identify potential outliers in your data.

*Note:* We have covered box plots multiple times in previous sessions. Please review those if you need a refresher.

- Create a new worksheet.
- Drag `Category` to the Columns shelf.
- Drag `Sales` to the Rows shelf.
- Drag `Manufacturer` or `Sub catgory` into the Details.
- Change it to circles under marks and make the size of the circles smaller
- click on the y axis and select add reference line
- from the window select box plot
- Observe the box plots for each `Category`
   - Notice the median line inside the box.
   - Look at the spread between Q1 and Q3 (the box).
   - Identify any outliers (points outside the whiskers).

# Question 3 Explore a new chart type: Circle Timeline Chart
We use circle timeline charts to analyze trends over time. We can also check correlation between 2 measures.
- `Order Date` to the column(quarter -> continuous)
- `Sub categories` to the rows
- `Sales` to the size
- In marks change viz type to circles
- `Sales` to the color(you can also use profit in the color to have more granularity on your viz)
- Go to color and change the opacity
- you can also get rid of the headers.

