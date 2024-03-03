# Python_Cohort_Analysis
Use KPMG transaction data to make a cohort to evaluate user engagement from their first transaction.

## I. Introduction
### 1. Business Question
- Using Python to analyze transaction data from KPMG to evaluate user engagement from their first transaction
### 2. Dataset
- KPMG dataset includes transaction data which customers of KPMG made in 2017, in which the columns customer_id and transaction_date are important data columns.
![image](https://i.imgur.com/Wiw7stS.png)
- There are many missing values (in online_order, brand,.. columns), apply filling missing value method: filling with mean and filling with mode.
- Values in 'transaction_id' column are unique => there are no duplicate records in the dataset
- We need to filter order_status = ‘Approved’ before cohort analysis


## II. Cohort Analysis Method
### 1.Definition
- A cohort is a collection of users who have something in common.
- Cohort analysis is a tool to measure user engagement over time. It helps to know whether user engagement is actually getting better over time or is only appearing to improve because of growth. Customers are divided into mutually exclusive cohorts, which are then tracked over time. Vanity indicators don’t offer the same level of perspective as cohort research.
### 2.Types of cohorts
Generally, there are three major types of Cohort:
- Time cohorts: customers who signed up for a product or service during a particular time
frame.
- Behavior cohorts: customers who purchased a product or subscribed to service in the past.
- Size cohorts: refer to the various sizes of customers who purchase the company’s products or
services.
### 3. Our method
- We will focus on performing Cohort Analysis based on Time. Customers will be divided into acquisition cohorts depending on the month of their first purchase. The cohort index would then be assigned to each of the customer’s purchases, which will represent the number of months since the first transaction.

## III. Data Visualization with Python
![alt](https://i.imgur.com/G8sFQ2A.png)

![alt](https://i.imgur.com/I6yp39G.png)

## IV. Insights
- The retention rate of KPMG transaction data falls within the range of 14.3% to 52.5%. This is a relatively low average retention rate. The number of customers who made the first purchase decreased sharply over the months, from 1343 customers (Jan 2017) to 4 customers (Dec 2017)
- Retention rates of customers purchasing their first products in January, February, and March 2017 were relatively stable (about 35.6% to 43.2%). Meanwhile, these rates from July to December 2017 are more fluctuating, especially in October: 14.3% in the 2nd month but 47.3% in the 3rd month.
- In the last months of quarters, typically, the months tend to have the lowest retention rates from previous months. For instance, in June (with retention rates from January at 35.7% and from April also at 35.7%), September (with retention rates from July at 26.2%, from April at 31.5%, and from January at 35.6%), and December (with retention rates from August at 25.9%, from July at 32.5%, and from February at 34.9%).
- During the beginning and middle months of the quarters, the retention rates of customers tend to be higher. In July, the retention rates from previous months range from 31.4% to 39.2%. In August, the range is from 37.8% to 52.5%. For October, it ranges from 33.9% to 42.5%, and for November, it ranges from 14.3% to 43.8%.

## V. Recommendations

