# Overview
There are 3 parts of jupyter notebook file in this project: 
1. [Part 1 - EDA.ipynb](https://github.com/titods/Identifying-Customer-Segments-and-Purchasing-Patterns-in-Retail-Industry-Superstore-/blob/main/Part%201%20-%20EDA.ipynb) consist of `Introduction`, `Load the dataset`, `Data cleaning`, and `Exploratory Data Analysis (EDA)` sections.
2. [Part 2 - Customer Segmentation.ipynb](https://github.com/titods/Identifying-Customer-Segments-and-Purchasing-Patterns-in-Retail-Industry-Superstore-/blob/main/Part%202%20-%20Customer%20Segmentation.ipynb) consist of `Customer Segmentation` section.
3. [Part 3 - Market Basket Analysis.ipynb](https://github.com/titods/Identifying-Customer-Segments-and-Purchasing-Patterns-in-Retail-Industry-Superstore-/blob/main/Part%203%20-%20Market%20Basket%20Analysis.ipynb) consist of `Market Basket Analysis`, `Conclusions`, and `Recommendations` sections.

# Introduction

Superstore is a fictional retail business located in the United States which sells Office Supplies, Furniture, and Technology Products. Their customers are the mass Consumer, Corporate and Home Offices. This business has been running from 03 January 2018. They want to analyze and assess their business performance from early 2018 to the end of 2021 such as identifying the customer segments and the purchasing patterns of customers.

*Note: the picture is for reference only*
<img src="image/superstore.jpg" width="600">

## Objective

- To get some insights about Superstore's market performance and main driver of loss in Superstore.
- To identify and understand customer segments in Superstore.
- To identify and understand purchasing patterns of customers in Superstore.

## Business  value

- We could identify opportunities for Superstore to boost business growth.
- We could treat each customer differently according to their segments. (reducing the risk and increasing the efficiency in deciding marketing strategy deployment in Superstore).
- We could help product development team to develop a product and to create product differentiation based on history of product purchases.

## Methodology

- Exploratory Data Analysis.
- Customer segmentation using clustering algorithm i.e. K-Means, Gaussian Mixture Model, and Hierarchical Clustering.
- Market basket analysis using apriori algorithm.

## The dataset

The dataset is obtained from [Kaggle](https://www.kaggle.com/datasets/sirajahmad/superstore) and also provided in [Tableau community](https://community.tableau.com/s/question/0D54T00000CWeX8SAL/sample-superstore-sales-excelxls). The timestamps are from **03 January 2018** to **30 December 2021**. This dataset only contains sales information in United States but if you want more granular sales across different country, There are also Global Superstore dataset (click [here](https://www.kaggle.com/datasets/gauravtopre/global-superstore-dataset)) which provides more granular Superstore's sales across different country (but the timestamps are different).

There will be one file after downloading the dataset, that is `Sample - Superstore.xls` which contains sheet about the orders (`Orders` sheet name), the regional manager each region (`People` sheet name), and the returned product (`Returns` sheet name).

Data description for `Orders`:
- `Row ID` &rarr; Unique ID for each row.
- `Order ID` &rarr; Unique Order ID for each Customer.
- `Order Date` &rarr; Order Date of the product.
- `Ship Date` &rarr; Shipping Date of the Product.
- `Ship Mode` &rarr; Shipping Mode specified by the Customer.
- `Customer ID` &rarr; Unique ID to identify each Customer.
- `Customer Name` &rarr; Name of the Customer.
- `Segment` &rarr; The segment where the Customer belongs.
- `Country/Region` &rarr; Country of residence of the Customer.
- `City` &rarr; City of residence of the Customer.
- `State` &rarr; State of residence of the Customer.
- `Postal Code` &rarr; Postal Code of every Customer.
- `Region` &rarr; Region where the Customer belongs.
- `Product ID` &rarr; Unique ID of the Product.
- `Category` &rarr; Category of the Product.
- `Sub-Category` &rarr; Sub-Category of the Product.
- `Product Name` &rarr; Name of the Product.
- `Sales` &rarr; Total Sales of the Product.
- `Quantity` &rarr; Quantity of the Product.
- `Discount` &rarr; Discount provided.
- `Profit` &rarr; Profit/Loss incurred (profit = positive value & loss = negative value).

Data description for `Returns`:
- `Returned` &rarr; If the Order has been returned.
- `Order ID` &rarr; Unique Order ID for each Customer.

Data description for `People`:
- `Regional Manager` &rarr; Name of the Regional Manager.
- `Region` &rarr; Region where the Customer belongs.
