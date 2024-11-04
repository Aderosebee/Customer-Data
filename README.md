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
The project aims to analyze customer subscription data to assess revenue, subscription patterns, and the overall performance of various subscription types. Key columns in the data include CustomerID, CustomerName, Region, SubscriptionType, SubscriptionStart, SubscriptionEnd, Canceled, Revenue, Subscription Duration, and Average Subscription Duration. This analysis will provide insights into customer behavior, identify regions or subscription types that contribute most to revenue, and determine how long customers typically stay subscribed. The data will also help in understanding churn rates by looking at canceled subscriptions.

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
### Data Source
The main data sources for this analysis is the  "Customer.csv" files, which is an open-source dataset available for free download from online repositories like Kaggle, FRED, or other similar platforms.

### Tools Used
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
Rows: 50000
Columns: 7 Columns




