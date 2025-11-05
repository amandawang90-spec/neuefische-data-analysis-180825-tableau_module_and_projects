# Question 1- Exercise Map Options
1. Create a map based on `State\Province`  
2. Change style to Dark 
3. Add `Terrain` and `Coastline`
4. Adjust controls to hide Zoom

# Question 2- Add a Custom Mapbox Map to Your Tableau Visualization
Use a custom Mapbox map in your Superstore dataset to enhance geographic visualizations.
- Go to [https://account.mapbox.com](https://account.mapbox.com) and sign up or log in.
- Once logged in, copy your default public access token from the dashboard.
- In Mapbox Studio, choose a default style or create a custom one.
- Copy the **Style URL** for the map you want to use.
- Create a map based on your preference.
- Go to `Map` > `Background Maps` > `Map Services`.
- Click `Add` > `Mapbox Maps`.
- Give your map a name, paste the **Style URL**, and enter the **Access Token**.
- Click OK and apply your new background map.
- Your Tableau map should now use the custom Mapbox design.

# Question 3 - Adding a filter
- Sales by categories and regions - improving the existing visual:
    - Apply time filter.
    - Try to find the option for 'apply to worksheets'(use it and see what happens, after that apply it only current one).


# Question 4 - Practice calculated field: Calculating Costs
- Create a new worksheet.
- Create a new calculated field to calculate *Costs*.
- Drag Sub-Category to Columns.
- Drag Costs and Sales to Rows.
- Change to dual axis and synchronize axis.
- Change Costs to bars (Sales can stay as Circle).
- Drag Profit to Colors in the Sales Marks Card.
- Edit colors in a meaningful way.
- Optional: Change the Format of Costs, Sales and Profit to Currency (English (United States)).


# Question 5 - Practice calculated field: My Sub-Categories
- Imagine you are working for the company and you are responsible for some specific sub categories.
- Create a calculated field that will create "my sub categories" which are arts and bookcases and the "other".
- Create a worksheet and show as a bar graph sales and profit for "my sub categories" and "other".


# Question 6 - Practice Product Grouping

- Create a bar chart showing sales across different sub-categories.
- Identify a few sub-categories from different categories that show relatively high sales values.
- Group them together and give the group a meaningful name based on their performance or shared traits.
- Do the same for a few sub-categories with noticeably lower sales.
- Rename your groups appropriately and replace the original sub-category field with your grouped version in the view.
- Add color or labels to visualize how the groups compare.
- Think about how grouping changed the insight you can get from this chart.

> Optional: Bring in other fields like `Sub-Category` or `Profit` to add more context to your groupings.

