# **TimeSheet App**
<img src="https://github.com/sumedhsharangdhar/PowerPlatform/blob/main/TimesheetApp/TimesheetHome.png" width="250" height="400"> </img>

# Description 
The timesheet is app is used to simply submit the monthly timesheets using PowerApps. The datasource used is SharePoint. 
<br>
There are mainly 3 components : 
1) PowerApps for submitting the timesheet entry having customly designed Calendar 
2) Powerautomate flow for automatically creating month-wide entries for all the users with no of hours = 0.
3) SharePoint lists to store the data. 

# Template

### Step 1
1) Create a SP list with the following name: **UserProfileList**
<br/> This list cointains the list of users who are supposed to be using the app.

<table>
  <th>Column Name</th>  <th>Column Type</th>  <th>Comments</th> 
  <tr> <td>Title</td>  <td>Single line of Text</td> <td>This will be the default column that gets created in a SharePoint list</td> </tr>
  <tr> <td>UserName</td>  <td>Single line of Text</td> <td></td> </tr>
  <tr> <td>Project</td>  <td>Choice</td> <td>Choice values:<br>Finance<br>HR<br> etc..</td> </tr>
</table>

2) Create a SP list with the following name: **TimesheetData**
<br> This list is to store the data about hours filled by users using PowerApps
<table>
  <th>Column Name</th>  <th>Column Type</th>  <th>Comments</th> 
  <tr> <td>Title</td>  <td>Single line of Text</td> <td>This will be the default column that gets created in a SharePoint list</td> </tr>
  <tr> <td>Date</td>  <td>Date and Time</td> <td></td> </tr>
  <tr> <td>No of Hours</td>  <td>Number</td> <td></td> </tr>
  <tr> <td>UserName</td>  <td>Single line of Text</td> <td></td> </tr>
  <tr> <td>Project</td>  <td>Choice</td> <td>Choice values:<br>Finance<br>HR<br> etc..</td> </tr>
</table>

### Step 2
[Import App zip file](https://github.com/sumedhsharangdhar/PowerPlatform/blob/main/TimesheetApp/TimesheetApp_PowerApp.zip) in Power Apps. <br>Imported zip file will contain App. 

### Step 3
Edit the App.  <br>Remove the SharePoint data source from the App & add a new SharePoint data source connection with your newly created “UserPfileList” and "TimesheetData" list. 

### Step 4
[Import PowerAutomate zip file](https://github.com/sumedhsharangdhar/PowerPlatform/blob/main/TimesheetApp/MonthWiseDataAddition_Flow.zip) in PowerAutomate.

### Step 5
Go to flow.microsoft.com <br>Turn on the flow “MonthWiseDataAddition” <br>Edit the flow and update the SiteURL action to point to your SharePoint site where the new “UserProfileList” and "TimesheetData" lists have been created.

## < / >
