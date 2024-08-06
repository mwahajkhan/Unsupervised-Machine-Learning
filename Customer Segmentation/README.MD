# Customer Segmentation for International Retail Customers

## 1.1 Problem Context

Many large stores with international customers face the common problem of managing customer preferences and segments at the individual customer level for more tailored service. These stores, like our client, often sell a wide range of products and have customers from various regions around the world.

- Our client is an online retailer selling all-occasion gifts.
- While most customers are domestic, a significant number of customers are from various international regions.
- The goal is to **create groups of these international customers based on their previous purchase patterns.**
- By doing so, the store aims to provide more personalized services and improve targeted marketing efforts for international customers.

## 1.2 Problems with the Current Approach

Currently, the retailer groups their international customers solely by country, which proves to be inefficient due to several reasons:

- The large number of countries dilutes the effectiveness of segmentation.
- Some countries have very few customers, making country-based segmentation impractical.
- The current approach fails to differentiate between large and small customers or to consider their diverse purchase patterns.

## 1.3 Problem Statement

To address these issues, the retailer has enlisted our help to create customer clusters, also known as **"customer segments"**, through a data-driven approach.

- We have been provided with a dataset **containing past purchase data at the transaction level**.
- Our task is to build a clustering model using this dataset.
- The clustering model should consider both aggregate sales patterns and specific items purchased to create meaningful customer segments.



Dataset used fot this project is the ***Online Retail Data-Set***

https://www.kaggle.com/datasets/tunguz/online-retail

# 2. Machine Learning Problem
## 2.1 Data Overview
For this project:
* The dataset has 35116 observations for previous international transactions.
* The observations span 37 different countries.
* **Note:** There is no target variable.

We have the following features:

Invoice information
* 'InvoiceNo' – Unique ID for invoice
* 'InvoiceDate' – Invoice date

Item information
* 'StockCode' – Unique ID for item
* 'Description' – Text description for item
* 'Quantity' – Units per pack for item
* 'UnitPrice' – Price per unit in GBP

Customer information
* 'CustomerID' – Unique ID for customer
* 'Country' – Country of customer

## 2.2 Mapping Buisness problem to ML problem
### 2.2.1 Type of ML Problem
It is an unsupervised learning task, where given the features about each transaction, we need to segment the customers based on their buying patterns.
* It is importnat to note that the given data is transaction-level while the clusters (or segmenst) we need to create are customer-level.





> Important libraries:

```
!pip install numpy pandas matplotlib seaborn sklearn xgboost
