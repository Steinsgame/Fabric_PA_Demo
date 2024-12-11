# Connecting Microsoft Fabric Database with Powerautomate
## Creating a Support system that loads data from microsoft forms into fabric database
Microsoft announced a major addition to the fabric space by introducing fabric database, I would take you through an interesting step by step approach to connect your forms data to the database directly using powerautomate
## Requirement
1. Fabric Trail or Fabric Capacity
2. Powerautomate Premium
   
## Steps
1. Create Fabric Database:
In a fabric enabled workspace
![Alt Text](Assets/Fabric_Enabled_Workspace.png)

click on New Items, then select SQL database
![Alt Text](Assets/sql_db.png)

Give your database a name, and load data into your database
![Alt Text](Assets/db_interface.png)

2. Create Microsoft Forms:
Create a microsoft forms with your desired field, for this demo kindly see the fields below
![Alt Text](Assets/PA_Forms.png)


3. Create Powerautomate flow:
Go to make.powerautomate.com, click on create automated cloud flow, give your flow a name,
Select when a new response is submitted from forms as the trigger, then get response details, and add the response id from the flow
![Alt Text](Assets/response_details.png)

Add an action to insert row from sql server, Click on new connection, select Microsoft entra ID
![Alt Text](Assets/New_connection.png)
![Alt Text](Assets/Insert_Row_Flow.png)

Under the server name Copy the Sever name immediately after the datasource for the connection string, then the database after the column of that, add dynamic contents of the response details
![Alt Text](Assets/Connection_String.png)

4. Test your flow
![Alt Text](Assets/flow_snapshot.png)









