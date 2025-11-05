# Analytics Deep Dive with Tableau:

- Create a **scatter plot** to visualize sales vs profit by product category.
- Learn how to annotate key insights or outliers on your visuals.
- Build and customize **clusters** to group products based on sales and profit similarity, and understand why clusters don’t always match predefined categories.
- Create a **forecast** on sales over time using Tableau’s forecasting features.
- (Exercises coming up) Explore more advanced visuals such as box plots, candlestick charts, and waterfall charts to deepen your understanding of analytics capabilities.


## Scatter Plot
- A scatter plot displays the relationship between two measures, such as Sales and Profit, for different product categories or subcategories.  
- It helps identify patterns, correlations, and outliers.

### Example
- X-axis: Sales  
- Y-axis: Profit  
- Color or shape: Category  

This view reveals which products are most profitable and which have high sales but low profit.

---

## Annotations
Annotations are notes or callouts added directly to a visualization to highlight key insights, trends, or anomalies.  
They make dashboards easier to interpret by explaining important data points.

- **Mark Annotation:** Adds a note to a single data point.  
- **Point Annotation:** Marks a specific location on the view.  
- **Area Annotation:** Highlights a region of interest.

---

## Clusters
- Clustering groups similar data points automatically based on selected measures, such as Sales and Profit.  
- Tableau uses statistical algorithms (k-means) to identify natural groupings.
- Clusters reveal hidden relationships in data.
- They may not align with predefined business categories.
- You can adjust the number of clusters for different levels of detail.

---

## Forecasting
- Forecasting in Tableau projects future values based on historical data trends.  
- It uses exponential smoothing models to predict future sales or other metrics.
- Can be applied to time-based measures such as monthly or yearly sales.
- Tableau automatically generates confidence intervals to show prediction uncertainty.
- Useful for planning and performance tracking.
