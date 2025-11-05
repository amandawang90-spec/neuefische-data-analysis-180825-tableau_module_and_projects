## What we’ll cover in today's session

- Understand and manage **data types** in Tableau (e.g. decimals, whole numbers, geographic roles)
- Organize fields using **folders** for a cleaner data structure
- Build and customize **map visualizations**:
  - Use size and color to encode data (e.g. Sales and Profit by State)
  - Explore different **mark types** (circle, shape, density, map)
  - Use **background maps**, **map layers**, and map interaction settings
- Create **custom groups** for data classification (e.g. U.S. regions)
- Apply and configure **filters**:
  - Time filters and category filters
  - **Top N filters**
  - Use **context filters** to control filter execution order


- Create and use **calculated fields**:
  - Add a “Profitability” label using conditional logic
  - Compute **Profit Ratio** and format it as a percentage

- Refine visuals with titles, labels, axis formatting, and color schemes

### Calculated Fields in Tableau

#### Definition
Calculated fields are custom fields created using formulas to perform operations on existing data. They allow you to create new insights beyond what is directly available in the dataset.

#### Purpose
- Create new measures or dimensions (e.g., Profit Ratio, Sales Category).
- Apply conditional logic using IF statements.
- Aggregate or transform data dynamically.

#### Example
```tableau
[Profit] / [Sales]