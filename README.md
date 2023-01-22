# Mini-Project-BigMart-Sales-Predictive-Analysis
## Table of content

1. [Problem Statement](#Problem-Statement)
2. [Exploratory Data Analysis](#Exploratory-Data-Analysis)
3. [Missing Value Treatment](#Missing-Value-Treatment)
4. [Feature Engineering](#Feature-Engineering)
5. [Data Encoding](#Data-Encoding)
6. [Modeling](#Modeling)



## Problem Statement

The objective of this internship task is to utilize 2013 sales data collected by the data scientists at BigMart for 1559 products across 10 stores in various cities, along with the attributes of each product and store, to construct a predictive model with the aim of determining the sales of each product at a specific store. Furthermore, through the utilization of this model, BigMart intends to gain insight into the properties of products and stores that play a crucial role in increasing sales. The dataset provided contains detailed information about the products offered by various outlets, including product size, fat content, and MRP information. The aim of this project is to identify the features of a product that lead to increased overall sales in the outlets. To achieve this, predictive models will be implemented utilizing the sklearn machine learning library, and the model providing the most accurate prediction will be determined through a summary of model accuracy.

## Exploratory Data Analysis

The data utilized for this project consists of 12 columns and over 8,000 rows. The description of each column is as follows:

| Variable        | Description|
| :-------------: | :-------------: |
| Item_Identifier| Unique product ID|
| Item_Weight | Weight of product|
| Item_Fat_Content | Whether the product is low fat or not|
| Item_Visibility | The % of total display area of all products in a store allocated to the particular product|
| Item_Type | The category to which the product belongs|
| Item_MRP | Maximum Retail Price (list price) of the product|
| Outlet_Identifier | Unique store ID|
| Outlet_Establishment_Year | The year in which store was established|
| Outlet_Size | The size of the store in terms of ground area covered|
| Outlet_Location_Type | The type of city in which the store is located|
| Outlet_Type | Whether the outlet is just a grocery store or some sort of supermarket|
| Item_Outlet_Sales | Sales of the product in the particulat store. This is the outcome variable to be predicted.|

### Univariate data analysis 


### Bivariate data analysis 



## Data Preprocessing and handling missing value treatment


In the Data Preprocessing and handling missing value treatment section, we first determined the number of null values present in the dataset. Then, we calculated the percentage of null values in relation to the overall number of rows. Since the percentage of null values was less than 5%, we filled the missing values in the column "item weight" and "outlet size" with the mean value of the respective columns. This approach was chosen as it preserves the overall distribution of the data and does not introduce significant bias.

<img width="844" alt="image" src="https://user-images.githubusercontent.com/63984422/213921691-a47914ee-b896-4da0-b02a-ba92aa504b4d.png">


## Feature Engineering



## Data Encoding



## Modeling



The process we will take to build this machine learning model is as follows:

First clean the data
