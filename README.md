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

## Data Analysis 

This is where we include some basic lines of codes or queries and some of the DAX functions to make the project presentable.

## Excel Analysis

![Screenshot (138)](https://github.com/user-attachments/assets/c3506b4a-6251-47c2-8022-97a93c103313)

## Pivot Table Summarization

### 1. Total sales by Subscription type

![Screenshot (112)](https://github.com/user-attachments/assets/e296abca-02cd-4bce-b6ff-fc2e53ccbdb4)

### 2. Average Sales by Subscription Type

![Screenshot (140)](https://github.com/user-attachments/assets/341245a0-994d-4415-ab0c-0cacec4520a7)

### 3. Total Sales by Region

![Screenshot (114)](https://github.com/user-attachments/assets/e418c69f-ad44-46c4-a492-8077b375e6e3)

### 4. Revenue by Active and Canceled Subscription

![Screenshot (139)](https://github.com/user-attachments/assets/d2618ef5-1c78-409e-b6f0-ae7feee0474a)

### 5. The overall popular subscription Type

![Screenshot (115)](https://github.com/user-attachments/assets/1dc765bb-399b-4f25-b446-c7d2684e5350)

### 6. Popular Subscription Type in each month

![Screenshot (117)](https://github.com/user-attachments/assets/982901b9-34bd-4fc4-97b6-3b2192ed1bd9)
![Screenshot (118)](https://github.com/user-attachments/assets/052554b0-43e1-4c08-bf1f-f1810e15004c)

### 7. Subscription Type by count of Duration

![Screenshot (116)](https://github.com/user-attachments/assets/789cbe7f-dd72-48a9-b3b7-40d2026d405d)


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

## Inference

