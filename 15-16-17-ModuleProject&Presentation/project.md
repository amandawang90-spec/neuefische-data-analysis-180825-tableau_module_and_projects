# Recreate the SQL API Project Using Tableau

## Duration:
~ 2.5 days
You will be presenting on day 17 in the afternoon.
---

## Main Objective of the Project:

- **5–10 minute presentation**
- **1–2 dashboards** (optionally embedded in a Tableau Story)
- **Publish to Tableau Public**

---

## Project Description:

In this project, you'll **rebuild your SQL API project using Tableau**, transforming your analytical insights into compelling dashboards. This serves two purposes: reinforcing your technical skills **ahead of the certification exam** and preparing you to present data effectively.

Use this opportunity to **review and apply** all major Tableau concepts covered throughout the module:

- Connecting to data (live vs. extract)
- Data Interpreter, folders, and joins
- Calculated fields, filters, and parameters
- Groups, sets, LOD expressions
- Mapping, chart types, dashboard design
- Publishing and sharing (Tableau Public)

This is a **final recap and practical application** before your mock and real certification exam.

You should:

- Connect to the **AWS PostgreSQL server** and build your dashboards based on previous analysis from the Airports/Flights/Weather module.
- If server access is a challenge, you're allowed to export and work from CSVs locally.
- If you prefer using a different dataset (e.g., from another module), please consult your instructor for approval.

The outcome should demonstrate **your ability to tell a data story**, apply analytical logic, and use Tableau effectively — all key exam and workplace-ready skills.



## How to connect to your AWS postgres database?
### To connect the AWS:
- open a new workbook
- under to a server click on more and find postgresql
- it will tell you to download the drivers click on that link
- open the page and scroll down and login(sign in on the right side does not work we do not know why :) )
- from the dropdown menu find postgres and it will automatically recognize your computer system properties
- download the file

#### Mac
After that you need to copy that `.jar` file into your `Library/Tableau/Drivers`  If there is no Tableau folder inside of the `Library` you need to create it manually (we will do this via terminal!!)
  
- In your terminal you need to pass the following code<br />
  **to create the folder:** <br />
  `mkdir -p ~/Library/Tableau/Drivers`<br />
  
  **go to the Downloads folder:** <br />
  `cd ~/Downloads`</b>
  
  **move the .jar file from Downloads to the Drivers** <br />
  `mv postgresql-42.7.5.jar ~/Library/Tableau/Drivers/`<br />
  
- if the system does not allow you and says permission denied you need to first give the permission with the following code and repeat the steps above): `sudo chmod -R 755 ~/Library`
  
- restart tableau and connect with the credentials


#### Windows
- C:\Program Files\Tableau\Tableau <version>\drivers
- Replace <version> with the version number of Tableau you're using (e.g., Tableau 2023.1).
- Copy and paste `.jar`  into the drivers folder