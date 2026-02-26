# Tour de France
For this recap project/exercise you will analyze **Tour de France** data. The steps below will guide you through preparing the data in Tableau Desktop and applying concepts you have learned. At the end of this project you should have one dashboard published on [tableau public](https://www.tableau.com/community/public).
(Click the links to read more on Tableau’s official documentation.). Let's start!

- Create a new workbook in Tableau Desktop and connect the dataset(excel file)
- Check the metadata, understand the fields, check the datatypes

-Because this exercise requires extensive data preparation, you will create calculated fields in the **Data Source area** (recommended for cleaning) using tableau desktop [interpreter](https://help.tableau.com/current/pro/desktop/en-us/data_interpreter.htm).   You can do it with right clicking in the table preview go on top of the field, right click and select create -> calculated field without going to the worksheet.(You may also create calculated fields in worksheets — both methods work.)


## Split Coordinate Data
- In the dataset we have `Start/Finish City Coordinates` field which has all the lat and long data for the start and finish. We need to split that data to be able to use it in our visualisations. For this we can use [String Functions](https://help.tableau.com/current/pro/desktop/en-us/functions_functions_string.htm)

- Create a calculated field to split the coordinates and call it **Finish City Coordinates**

```SPLIT([Start/Finish City Coordinates], " - ", 2)
```
- Create a second calculated field to split the coordinates and call it **Start City Coordinates**

```SPLIT([Start/Finish City Coordinates], " - ", 1)
```
- You can hide `Start/Finish City Coordinates` since we do not need this field anymore

- Let's get the Lat and Long separetly. Create a calculated field **Start Long**

```SPLIT([Start City Coordinates], ", ", 2)
```
- Now we need to get **Start Lat**

```SPLIT([Start City Coordinates], ", ", 1)
```
- You can hide `Start City Coordinates`.
- Change the data type to numerical decimal and then add geographical roles.
- Repeat the steps for creating `Finish Long` and `Finish Lat`
- Hide `Finish City Coordinates`

## Clean Date Fields
- Now we need to clean the dates using SPLIT

**Start Date**
```
SPLIT([Start/Finish Dates], ' - ',1)
```

**Finish Date**
```
SPLIT([Start/Finish Dates], " - ", 2)
```
-After splitting the start and finish dates, we also need a column which gives us only year as a seperate column. We will get help from [Date Functions](https://help.tableau.com/current/pro/desktop/en-us/functions_functions_date.htm)

**Year**
Let's get all the years when the Tour took place
```YEAR[(Start Date)]```

## Identify Other Fields to Clean

Ask yourself:
- Are there columns that contain multiple values in one field?
- Would splitting them make analysis easier?
- What new insights can we gain after splitting?


## Data Visualisation
Here are some suggested analysis steps and visualisation ideas to help you build strong insights from the Tour de France dataset.

### EDA
-start date year(continuous), number of states to the columns(avg)
-start date year(continuous), total distance to the columns

- check the winners with adding winner to the row, Date to the details, Sort the winner by descending by clicking on it(by field)
- Do you see the max winner's name is not visible. right click on that and say `change alias` and type: `Lance Armstrong`


### Did the Tour de France take place every year?
- Return to the **Year vs Total Distance** line chart.
- Right-click the **Year** pill in Columns → **Show Missing Values**.
- The gaps in the timeline will display.
- Discuss: *Why were certain years missing?* 

### % Finished
- Check the fields and think about how can we calculate the rate of the finishers like % Finished


### French vs Non-french
The Tour has a strong French identity. Consider which Tableau feature can help separate winners into **French** and **Non-French**: How can you adapt it into a viz?


### Riders with Multiple Victories
- Please review the [Sets](https://help.tableau.com/current/pro/desktop/en-us/sortgroup_sets_create.htm)
- Go to the Winner column and right click and select create set
- Go to the condition and write the formula:

```COUNTD([Year]) > 1```

-Think about how can we use it in a Viz

### Prepare Your Dashboard
- you need to create **at least**
    - A map (cities, nationalities, or routes)
    - A table with important information
    - A line graph (distance, stages, % finished, etc.)
    - The Tour de France logo
    - At least one Dimension or Measure filter        


### Publish Your Dashboard
    - publish your dashboard on tableau public(Each group member should publish it with giving credit in the explanation to the other group members)

**Example**
This dashboard is created during the NF/Spiced 4,5 Months DA Bootcamp as a project by `Name1`, `Name2` & `Name3`


