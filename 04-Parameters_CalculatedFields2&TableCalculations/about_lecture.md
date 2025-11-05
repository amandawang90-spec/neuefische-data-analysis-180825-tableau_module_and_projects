# What we'll cover in today's session:

- Build on the **same workbook** from the previous day to continue exploring calculated fields and start using parameters effectively.
- Understand how to use **parameters** to create interactive visuals, e.g., allowing users to switch between measures like Sales and Profit.
- Deep dive into **logical functions** (`IF`, `CASE`, `CONTAINS`, `DATEDIFF`) to categorize, flag, and segment data more dynamically.
- Learn how to **visually implement** logical functions into dashboards using clear, real-world examples (e.g., State Region or Shipping Priority).
- Begin using **table views** and learn how to enhance them using color, hierarchies, and formatting for effective storytelling.
- Discover how to apply **table calculations** like running totals or percent differences directly in visual tables.


Each part includes hands-on practice so you can apply what you’ve learned immediately.


## Table Calculations
Table calculations are computations applied **after** Tableau aggregates the data in a view.  
They work on the **visible results** of your visualization rather than the underlying data source.

### Common Uses
- Calculating running totals, ranks, or moving averages.
- Finding percent of total or difference from previous values.

### Example
```tableau
RUNNING_SUM(SUM([Sales]))
```

## Parameters in Tableau
- Parameters are dynamic input values that allow users to control aspects of a Tableau visualization.  
- They can replace constants in calculations, filters, or reference lines to make dashboards more interactive.

### Purpose
- Let users choose which measure, category, or date range to display.
- Enable "what-if" or scenario analysis.
- Allow switching between different views or metrics.