KPI Exercise

## Part I

A tech company has developed an app that enables people to book a taxi with the click of a button. In order to increase the company’s growth they are constantly trying to find new ways to expand their business. To do this, they want to build a new feature for their app called 'match' that allows passengers to share their taxi with passengers who travel similar routes. The cost is split across the passengers, resulting in a less expensive but possibly longer journey.

By implementing this feature they want to increase their passenger base to more price sensitive passengers and increase capacity in times of high demand. The timeline to build this feature is 3 months and the company aims to add 25.000 new active customers (=have done at least 1 tour) within the first 3 months and reach 2.500 shared rides per month.

### Exercise 1:
What metrics would you track and report to evaluate the success of the company’s general business model.
Which of these would you classify as KPIs?

### Exercise 2:
What metrics would you track and report to gauge if this feature is a success?
Use SMART to define the goal and KPIs of the project.

**SMART**:

- Specific: Plan effectively with specific targets in mind
- Measurable: Track your progress and reevaluate along the way
- Achievable: Set realistic goals that are challenging but achievable
- Relevant: Ensure the goal serves a relevant purpose
- Time-bound: Specify a deadline, monitor progress and reevaluate

---
**OPTIONAL**

## Part II
The objective of the project is clear and you’ve defined relevant KPIs and metrics that you will be monitoring in order to make this project a success. The next step is planning the execution.


You create a plan with the
- Developers who will build the feature and make sure your metrics are tracked
- Designers und UX/UI researchers who will design and build the interface
- Data Engineers who will create the data pipeline in order to get your KPIs and metrics in form of clean and structured data into a database

Now it’s time to execute. Every department delivers their parts and according to the project plan you launch a test run of the new match feature in 2 small markets.

In order to assess whether the feature works as intended and produces the results you are aiming for, you want to take a look at the data and assess the relevant metrics and KPIs. The Data Engineering team has stored the data in a table in a SQL database and provided you with user credentials. You have never accessed a database and used SQL in order to retrieve data before, but you think to yourself: “How hard can it be?”.

It turns out, very hard. First, it takes several hours for you to find a tool that lets you access the database, then your user credentials don’t work. After back and forth emails with the data engineering team, it turns out there was a typo in your credentials.
Now that you have resolved that issue, your problems have only just begun. Where is that freaking table with the metrics about the feature? After hours of going through several database schemas you finally find the table. Great, you also find a crash course on SQL basics online and since you are a fast learner, manage to acquire basic SQL skills within an hour. “Great, let’s look at the KPIs.” is what you think, only to find yourself confronted with the next problem: What do all these columns and values mean? After several hours over multiple days talking to the developers and data engineers you are able to create documentation about all the available data points and their meaning. Finally, you can take a look at the metrics and KPIs. You run some basic SQL queries only to find out that, for the first few days, the feature was actually not live and there is no data. You also find that certain values are in the wrong format, some data points are recorded multiple times resulting in 30% of your data being duplicates. On top of that now that you see the feature in action you can identify different use patterns across different customer groups. You suspect this was caused because the feature wasn't actually live for the first few days, but you can’t be sure. Finally, you realize you are missing some key metrics that would help you understand how the feature is performing from different stakeholder perspectives.
Completely exhausted, you sit in your office chair asking yourself: “What did I do wrong?”

### Exercise 3:
What do you think went wrong?
