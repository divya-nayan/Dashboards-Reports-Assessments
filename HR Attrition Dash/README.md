# IPL 2008-2022 Analysis Dashboard

### Dashboard Link :  https://www.novypro.com/project/hr-attrition-dashboard-using-powerbi-excel--sql

## Problem Statement

Company XYZ has provided with their employees datasets in excel format, containing descriptive columns like Departments, Salary, Years of experiences, Attrition count, State, Job Role, Job Satisfaction Rating, Date and other relevant factors. We're supposed to create a dashboard that can briefly summarized the employee status and domain where we need to focus on in order to deal with attrition issues. HR needs to have a updated dashboard which can guide them and make their task easier than before.


### Steps followed 

- Step 1 : Understanding and defining problem statements.
- Step 2 : Loading Datasets to PowerBI and reviewing the columns.
- Step 3 : Transformed the columns and adjusted their data types and replaced mistyped values.
- Step 4 : Deleted Blank spaces & got rid of irrelevant columns.
- Step 5 :I selected 5 cards to showcase important metrics like "Total Employees", "Attrition count", "Attrition Rate", "Active Employees", and "Average Age". 
- Step 6 : Then, 1 Donut chart was introduced to highlight number of employees based on Department.
- Step 7 : 1 Bar chart was utilized to display employee count based on their Education and simultaneously their marital status was highlighted.
- Step 8 : 1 Area chart displays attrition count based on the Age-group.
- Step 9 : 1 Metric chart was introduced to display the Job satisfaction rate based on their job role. 

        
- Step 10 : 1 Pie chart was put on display to highlight Average Monthly Salary of employees as per their Job role.We've provided 2 slicers, each for Job Role and gender, for option selections.

Following DAX expression was written for the same,
        
        Attrition Rate = Attrition Rate = DIVIDE(SUM('HR data'[Attrition Count]), SUM('HR data'[Employee Count]), "")
             
 - Step 11 : New measure was created to find  "Active Employee",
 
 Following DAX expression was written to find Active Employee,
 
         Active Employee = Active Employee = SUM('HR data'[Employee Count]) - SUM('HR data'[Attrition Count])
 
   

 
 # Report Snapshot (Power BI DESKTOP)

 
![Dashboard snap](https://github.com/divya-nayan/Dashboards-Reports-Assessments/assets/53559386/8b7c9ecc-5ae9-4c44-bfbd-2371a259568e)

# Insights

A single page report was created on Power BI Desktop & it was then published to novyPro.com.

Following inferences can be drawn from the dashboard;

### [1] Average Attrition Rate is around 15%

   Age-Group of 25-34 is contributing maximun for this Attrition Circumstances.

   Also Maximum number of Active employees belongs to the category of age group 25-34.
   
           
           
### [2] Other Insights

R & D department has maximum number of employees, around 65% of total employees.


In Job Satisfaction Rating, Around 60% of employees have given 75% & 100% satisfaction ratings.

 
