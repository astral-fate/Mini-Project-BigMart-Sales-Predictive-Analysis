# Mini-Project-BigMart-Sales-Predictive-Analysis
## Table of content

1. [Problem Statement](#Problem-Statement)
2. [Exploratory Data Analysis](#Exploratory-Data-Analysis)
3. [Missing Value Treatment](#Missing-Value-Treatment)
4. [Feature Engineering](#Feature-Engineering)
5. [Data Encoding](#Data-Encoding)
6. [Modeling](#Modeling)
7. [Summary](#Summary)



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

Univariate data analysis means exploring just one column, finding the frequancy, its mean, median and std

<img width="485" alt="image" src="https://user-images.githubusercontent.com/63984422/213921972-cc991cc6-89e8-4dd4-8de6-0a4a17d715d4.png">

<img width="467" alt="image" src="https://user-images.githubusercontent.com/63984422/213921925-6ce99102-7d3e-45f1-a090-5ce337731f4c.png">


### Bivariate data analysis 

Bivariate data analysis refers to the examination of the correlation between two columns and the discovery of the relationship between them.

<img width="840" alt="image" src="https://user-images.githubusercontent.com/63984422/213922158-b0fa766a-369a-4604-95e2-11eac0a8e058.png">

## Data Preprocessing and handling missing value treatment


In the Data Preprocessing and handling missing value treatment section, we first determined the number of null values present in the dataset. Then, we calculated the percentage of null values in relation to the overall number of rows. Since the percentage of null values was less than 5%, we filled the missing values in the column "item weight" and "outlet size" with the mean value of the respective columns. This approach was chosen as it preserves the overall distribution of the data and does not introduce significant bias.

<img width="844" alt="image" src="https://user-images.githubusercontent.com/63984422/213921691-a47914ee-b896-4da0-b02a-ba92aa504b4d.png">



## Feature Engineering

In the Feature Engineering section, also known as Feature Transformation, modifications were made to the structure of the features or columns in the dataset. The data was cleaned of inconsistencies through the merger of "Low Fat" with "low fat" and "LF" and "Regular" with "reg". Additionally, a new category named "Non-Edible" was created for items that are not intended for consumption and therefore do not have a fat content. This process aimed to provide a more structured and accurate representation of the data and is crucial for the success of the predictive model.

<img width="651" alt="image" src="https://user-images.githubusercontent.com/63984422/213922378-b8ad0418-b049-4224-a443-5ea87aced919.png">


Since we have over 15 types of items, we subgrouped them into 3 main categories; food, drink, and non-consumable:

<img width="825" alt="image" src="https://user-images.githubusercontent.com/63984422/213922426-898e86eb-5583-408c-aeb7-b816082e2401.png">
<img width="631" alt="image" src="https://user-images.githubusercontent.com/63984422/213922440-bf8d56bd-ba30-4662-9749-3811947e26be.png">


## Data Encoding

I have labled encode the categories data such as outlet size, fat content, and item weight. I have fisr sorted the values, plot them, then encoded them.

<img width="448" alt="image" src="https://user-images.githubusercontent.com/63984422/213922622-e08fd416-a273-41fd-b21f-a6c588de9c26.png">

<img width="507" alt="image" src="https://user-images.githubusercontent.com/63984422/213922643-9d524930-09f7-4877-b852-364b0c3ce904.png">



## Modeling

After cleaning, and normlizing the target variable which is the 'Outlet_Sales', I have implented different regression models; linear, regular regression, random forest, and xgb model, and I have compared between their performance.


### Linear Regression 

<img width="726" alt="image" src="https://user-images.githubusercontent.com/63984422/213922864-2c9f6c45-96c4-4f41-ba36-acca320f63fd.png">



## Regular Regression 


<img width="651" alt="image" src="https://user-images.githubusercontent.com/63984422/213922874-4c56819b-eb28-49a9-8085-81e3554b91ba.png">


## Random Forest 

<img width="653" alt="image" src="https://user-images.githubusercontent.com/63984422/213922882-d48410de-9b8e-473a-ac55-ea6b9db1dbb3.png">


## Xgb model

<img width="602" alt="image" src="https://user-images.githubusercontent.com/63984422/213922907-82ad40d8-c445-44fd-9c8f-325c604c5a96.png">




