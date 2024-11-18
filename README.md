# Power-BI-Finance-Dashboard

### Load the data in Power BI
1. Click on ```Excel workbook``` option under the ```Home``` Menu and import the excel file and choose the FinData worksheet
2. Apply the ```Unpivot Other Columns``` option to conver the table from wide format to long format.
3. Change the required data type like Date.

![image](https://github.com/user-attachments/assets/9bbb9973-a39e-4bfa-83ce-74a891ccdda5)

### Create different Measure
1. Total Value = SUM(FinData[Amount])
2. Savings = CALCULATE([Total Value], FinData[Type]="Savings")
3. Income = CALCULATE([Total Value], FinData[Type] = "Income")
4. Expenses = CALCULATE([Total Value], FinData[Type] = "Expense")

![image](https://github.com/user-attachments/assets/80fb4c45-83fb-4cbb-896a-48d360a7487b)

### Create new Date columns
1.  Click on Table View
2.  Click on New Column
3.  Write the DAX
    a. Month-Year = FORMAT(FinData[Date], "mmm-yy")
    b. Year = FORMAT(FinData[Date], "yyyy")
    
![image](https://github.com/user-attachments/assets/ea12e84b-ad59-46d3-bf45-863c5d6a5933)




