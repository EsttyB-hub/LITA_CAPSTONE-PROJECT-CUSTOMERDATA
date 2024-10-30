# LITA_CAPSTONE-PROJECT-CUSTOMERDATA

## Project Overview

This project involves analyzing the customer data for a subscription service. 

## Data Analyzed

The datasets used for this project include the following:
- OrderID: 

## Project Objective

The project emphasizes on achieving the following goals:
- Total sales by Product: T- Total sales per month: This reflects the total sales generated on the products on a monthly basis.

## Key Metrics

- Average sales per product: Average total revenue of different classes of products in each periodi.e using Averageif function argument box to apply the formula . This reflects the average sales of the products in that region.
## Tools and Method used

The tools and method used in this project analysis include:
1. Excel: Using Excel formulas to calculate the key metrics.
2. Pivot table: where the project is summarised in an understandable manner.
3. SQL: where queries are written and validated to extract key insights.
4. Github: For building of Portfolio
5. Power BI: This is used for data visualization of the insights found in Excel & SQL.

## Visual Analysis and Inference

This is where we include some basic lines of codes or queries and some of the DAX functions to make the project presentable.

### 1. Total sales by product








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


