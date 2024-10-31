# LITA_CAPSTONE-PROJECT-CUSTOMERDATA

## Project Overview

This project involves analyzing the customer data for a subscription service. This data analysis project aims to identify key customers segments and sales trend over the years. By analyzing the data sets given, we will be able to gather enough insights to be able to make an informed decision thereby knowing the best performance from our data.

## Data Analyzed

The datasets used for this project include the following:
- CustomerID: This reflects the unique identity related to each customer's orders.
- Customer name: This comprises of the name of individual customers.
- Region: This involves the geographical location where the company is located.
- Subscription Type: This entails the different subscription types being offered to customers.
- Subscription start & Subscription end: This shows the period for which the services were rendered.
- Canceled: This recorded the subscription that were canceled and those they were subscribed for.
- Revenue: This shows the revenue generated on all the subscription types for the periods covered.

## Project Objective

The project emphasizes on achieving the following goals:
- understanding the customer behaviours as regards to different subscription types.
- track the revenue generated on each subscription type.
- identify key trends in cancellation and renewal.
- knowing the revenue generated in each region.
- identify the subscription type with the highest revenue.


## Key Metrics

- Total sales per subscription type: Total revenue of different classes of subscription types in each periodi.e using "sumif" function argument box to apply the formula . This reflects the total sales of the subscription type in that region.
- Total number of customers in each region: This is achieved by using "Countif" function box. It shows the total number of customers in a particular region where the company is located.
- Most popular subscription type: This shows the subscription type with the highest number of customers and revenue.
- Active and Cancelled subscription: This was analyzed using the True and False response in the data sets.


## Tools and Method used

The tools and method used in this project analysis include:
1. Excel: Using Excel formulas to calculate the key metrics.
2. Pivot table: where the project is summarised in an understandable manner.
3. SQL: where queries are written and validated to extract key insights.
4. Github: For building of Portfolio
5. Power BI: This is used for data visualization of the insights found in Excel & SQL.

## Data Analysis and Inference

This is where we include some basic lines of codes or queries and some of the DAX functions to make the project presentable.

### 1. Total sales by Subscription type








## SQL
```SQL


SELECT * from [dbo].[LITA_CUSTOMERDATA DD]

--- Retrieve the total number of customers from each region---

SELECT Region, count (*) as Customers_Count
from [dbo].[LITA_CUSTOMERDATA DD]
group by Region

--- The most popular subscription type by the number of customers---

SELECT Top 1 SubscriptionType, count (CustomerId) as NumberOfCustomers
from [dbo].[LITA_CUSTOMERDATA DD]
group by SubscriptionType

--- customers who canceled their subscription within 6 months----

 


---calculate the average subscription duration for all customers----

SELECT CustomerId, AVG (Subscription_Duration) as Average_SubscriptionDuration
from [dbo].[LITA_CUSTOMERDATA DD]
group by CustomerID



----find customers with subscriptions longer than 12 months---



-----calculate total revenue by subscription type----

SELECT SubscriptionType, SUM (Revenue) as Total_Revenue
from [dbo].[LITA_CUSTOMERDATA DD]
group by SubscriptionType


----find the top 3 regions by subscription cancellations----

SELECT Top 3 Region , count (Canceled) as SubscriptionCancellation
from [dbo].[LITA_CUSTOMERDATA DD]
group by Region

----find the total number of active and canceled subscriptions----

SELECT count (*) As Canceled_Subscription
from [dbo].[LITA_CUSTOMERDATA DD]
where Canceled = 'TRUE'


SELECT count (*) As Active_Subscription
from [dbo].[LITA_CUSTOMERDATA DD]
where Canceled = 'FALSE'
```


## Power BI Visualization

![Screenshot (119)](https://github.com/user-attachments/assets/22bb083e-5e4f-4e39-823a-2f9384437415)


