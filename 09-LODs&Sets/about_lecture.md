# What we'll do in today's session

## LODs
- Understand what Level of Detail (LoD) expressions are and why we need them when working with different levels of granularity in Tableau.
- Explore the different types of filters in Tableau and how they interact with LoDs.
- Create a detailed KPI map using `Fixed` and `Exclude` LoDs.
- Use filters in context to observe how results change depending on filter order.
- Explain the Tableau order of operations and where LoDs and filters fit into that flow.
- Get familiar with the `Include` LoD through the upcoming exercises.

## Definition
Level of Detail (LOD) expressions allow you to control the level at which Tableau aggregates data, independent of the view.  
They let you calculate values at a more granular or higher level than what is displayed.

## Purpose
- Compare individual values to overall totals or averages.
- Create metrics that remain fixed regardless of filters or visualization structure.
- Perform calculations across different levels of detail.

## Types of LOD Expressions
- **FIXED:** Calculates at a specific dimension level, ignoring the view’s structure.  
  ```tableau
  { FIXED [Customer Name] : SUM([Sales]) }```

- **INCLUDE** adds a lower level of granularity to a calculation than what is shown in the view.  It allows Tableau to calculate values at a more detailed level and then aggregate them back to the current view.

- **EXCLUDE**  removes one or more dimensions from the calculation, making it less granular than the current view.  
It calculates at a higher level of aggregation than what is displayed.


## Sets in Tableau

- understanding what sets are and how they’re different from groups or filters.
- Create a set for the **Top 10 States by Sales** and use it to split the view into top performers vs the rest.
- Group all states outside of the set into a single “Other” category using a calculated field.
- Make the Top N dynamic using a parameter so the user can adjust the threshold.
- Update the chart and title based on the parameter selection.


### Definition
Sets are custom fields that define a subset of data based on conditions or manual selection.  
They can be used to segment data dynamically in visualizations.

### Their Purpose
- Compare selected data vs. the rest.  
- Highlight, filter, or color specific groups.  
- Create dynamic cohort or category analyses.
- Sets can be used in filters, calculated fields, or on color/shape shelves.  
- They allow flexible, dynamic grouping in Tableau.

### Types
- **Fixed Set:** Manually select members.  
- **Conditional Set:** Defined by a condition or formula.  
- **Top/Bottom Set:** Select top or bottom members based on a measure.


All of this will be practiced hands-on and applied in your own visualizations during the exercises.
