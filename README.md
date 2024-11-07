# COURSE PROJECT

[Sales Data](sales-data)

[Project Overview](project-overview)

[Tools](tools)

[Customer Data](customer-data)

This is where I document the project we were given at the end of the Data Analysis training organized by LITA

We were given two data to work on, **Sales Data** and **Customer Data**

## Sales Data

### Project Overview

This data analysis project aim to analyze the sales performance of a retail store. By analyzing sales performance of the store, we want to identify sales performance of the products and region and to have more understanding on the store's performance and make data driven recommendations.

### Data Source
 Sales Data: This data contains sales performance of a retail store. It contains the products sold by the company in different region of the country from January 2023 to August 2024.

### Tools

- Microsoft Excel [Download Here](https://microsoft.com);
  1. Data Cleaning
  2. Analysis
  3. Visualization
- SQL: Sequeled Query Language for querying of data [Download here](https://learn.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms)
- GitHub: For portfolio building [Download Here](https://github.com/)
- Power BI (Business Intelligence) [Download Here](https://app.powerbi.com/)for;
  1. Data entry
  2. Data Cleaning
  3. Visualization and Reporting

### Data Cleaning and Preparation

In the initial data preparation phase, I performed the following tasks:
1. Data loading and inspection
2. Handling missing values
3. Data Cleaning and Formatting

#### Excel

Here, the following task were performed;

i. Data Entry

ii. Removal of duplicates

iii. Calculations

iv. Pivot Table for visualization

![Sales data excel](https://github.com/user-attachments/assets/ec04a135-f2a9-4234-bd85-88b82283f4fd)

![Sales Data Pivot Table](https://github.com/user-attachments/assets/520d7d24-3f93-416e-afcb-466fc42d4147)

#### SQL

Here,I use queries to analyse the data and answer some questions.

Here is an example

```Select * from [dbo].[LITA Capstone Dataset csv]```

```select sum (TotalSales) as ShirtTotalSales from [dbo].[LITA Capstone Dataset csv]where Product ='Shirt' ```

```select count (Quantity) as NoofNorthSales from [dbo].[LITA Capstone Dataset csv]where Region = 'North' ```

```select * from [dbo].[LITA Capstone Dataset csv]select Product, sum(TotalSales) as TotalSales from [dbo].[LITA Capstone Dataset csv] Group by Product order by 2 desc```

```SELECT Product from [dbo].[LITA Capstone Dataset csv] group by Product Having sum (case when OrderDate Between '2024-06-01' and '2024-08-31' then 1 else 0 end)=0```

```select Product, sum (TotalSales) as TotalRevenue from [dbo].[LITA Capstone Dataset csv] Group by Product```

#### PowerBI

I use PowerBI for visualization and reporting of the data to cover trends and sales performance in the regions

![Sales Powerbi 1](https://github.com/user-attachments/assets/449d0fdf-7df1-430c-8fd6-8378810f8356)




##  Customer Data
__________________________________________________________
### Project Overview

This data analysis project aim to understand customer behavior, track subscription types, 
and identify key trends in cancellations and renewals of subscription for a company that offers subscription service     

### Data Source
 Customer Data: This data contains customer data for a subscription service 

### Tools

- Microsoft Excel [Download Here](https://microsoft.com);
  1. Data Cleaning
  2. Analysis
  3. Visualization
- SQL: Sequeled Query Language for querying of data
- GitHub: For portfolio building
- Power BI (Business Intelligence) for;
  1. Data entry
  2. Data Cleaning
  3. Visualization

#### Excel

Here, the following task were performed;

i. Data Entry

ii. Removal of duplicates

iii. Calculations

iv. Pivot Table for visualization

![Customer Data Excel](https://github.com/user-attachments/assets/a473572d-5a51-41ca-a55e-22b661fd3c39)

![Customer Data Pivot](https://github.com/user-attachments/assets/3c6e3729-ab22-458c-a60f-6056b33ad1d8)

#### SQL

Here,I use queries to analyse the data and answer some questions

Here is an example

```select * from [dbo].[CustomerData2] select Region, count(CustomerID) as TotalCustomers from [dbo].[CustomerData2] Group by Region```

```select * from [dbo].[CustomerData2] select Region, count(CustomerID) as TotalCustomers from [dbo].[CustomerData2] Group by Region```

```select CustomerName from [dbo].[CustomerData2] where Canceled = 'TRUE' AND Datediff (Month, SubscriptionEnd, SubscriptionStart)<=6```

```Select SubscriptionType, Sum (Revenue) AS TotalRevenue from [dbo].[CustomerData2] group by SubscriptionType```

