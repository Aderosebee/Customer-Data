# Capstone Project 2
---
## Project Title: Customer Data
---
[Project Overview For Customer Data](#project-overview-for-customer-data)

[Measures](#measures)

[Data Source](#data-source)

[Tools Used](#tools-used)

[Data Cleaning and Preparation](#data-cleaning-and-preparation)

[Objectives](#objectives)

[Exploratory Data Analysis](#exploratory-data-analysis)

[On Excel](#on-excel) 

[SQL Data Analysis](#sql-data-analysis)

[Data Visualization](#data-visualization)

[Conclusion](#conclusion)

[Recommendation](#recommendation)

### Project Overview For Customer Data
---
The project aims to analyze customer subscription data to assess revenue, subscription patterns, and the overall performance of various subscription types. Key columns in the data include CustomerID, CustomerName, Region, SubscriptionType, SubscriptionStart, SubscriptionEnd, Canceled, Revenue, Subscription Duration, and Average Subscription Duration. This analysis will provide insights into customer behavior, identify regions or subscription types that contribute most to revenue, and determine how long customers typically stay subscribed. The data will also help in understanding churn rates by looking at canceled subscriptions.

---
### Measures
- CustomerID: Unique identifier for each customer.
- CustomerName: Name of the customer (anonymized if necessary).
- Region: Geographical area where the customer is located (e.g., North, South, East, West).
- SubscriptionType: Type of subscription plan the customer is enrolled in (e.g., Basic, Premium).
- SubscriptionStart: Start date of the customer's subscription.
- SubscriptionEnd: End date of the customer's subscription.
- Canceled: Indicates if the subscription was canceled (TRUE or FALSE).
- Revenue: Revenue generated from the customer's subscription.
- Subscription Duration: Duration (in days) of the subscription period

---
### Data Source
The main data sources for this analysis is the  "Customer.csv" files, which is an open-source dataset available for free download from online repositories like Kaggle, FRED, or other similar platforms.

### Tools Used
---
- Excel: Employed for data cleaning and visualization.
- SQL: Utilized for data cleaning through queries.
- Power BI: Used for both data cleaning and visualization.

### Data Cleaning and Preparation
---
In the intial phase of Data Cleaning and Preparations, we perform the following action;

- Data loading and Inspection
- Handling missing variables
- Data Cleaning and Formatting

### Objectives
---
1. Retrieve the total number of customers from each region.
2. Find the most popular subscription type by the number of customers.
3. Find customers who canceled their subscription within 6 months.
4. Calculate the average subscription duration for all customers.
5. Find customers with subscriptions longer than 12 months.
6. Calculate total revenue by subscription type.
7. Find the top 3 regions by subscription cancellations.
8. Find the total number of active and canceled subscriptions.

###  Exploratory Data Analysis
---
EDA are set of steps used to explore and understand the dataset better, before cleaning and transformation.
Rows: 33787
Columns: 8 Columns

#### On Excel 
- Calculate using pivot table:
-  The total sales by region
-  Total sales
-  Average of  sales
-  Total sales per product
  
![Excel Pivot](https://github.com/user-attachments/assets/8b1e896d-551d-4747-8a6d-5255625e43cb)

#### SQL Data Analysis
This is where we include some basic lines of code or queries or even some of the DAX expressions used during your analysis;
---
- Show the table
```
select * from [dbo].[CUSTOMER DATA1]
```
![Show table](https://github.com/user-attachments/assets/43ee9086-d074-4c34-9db5-fa996c8ddab8)

- Total number of customers by region
```Select  region, count(distinct Customerid) as total_customers 
from [dbo].[CUSTOMER DATA1]
Group by region;
  ```
![Total customers by region](https://github.com/user-attachments/assets/a7164551-88a1-4020-9cfa-ac5b3047c8eb)

- Most poular subscription by number of customers
```Select top 1 subscriptiontype, count(distinct customerid) as total_customers
From [dbo].[CUSTOMER DATA1]
Group by subscriptiontype 
Order by total_customers desc;
```
![Popular subscription by customers](https://github.com/user-attachments/assets/6e053364-c7e5-48b0-8057-28c48a6ecc19)

- Subscription type by Total revenue
```SELECT subscriptiontype,
       SUM(revenue) AS total_revenue
FROM [dbo].[CUSTOMER DATA1]
GROUP BY subscriptiontype;
```
![Sub type bytotal revenue](https://github.com/user-attachments/assets/d63be903-e570-4120-953a-b68540942d9f)




