# Supervised-Learning---Rossmann-Retail-Store-Prediction
Rossman sales Prediction data is a dataset that include ancient income facts for a retail save chain. The information consists of facts approximately the store, which includes Competitior’s element, type, vacation’s, as well as numbers of the customers and income transaction, which includes the date, time, and quantity of sale on each day.

![image](https://github.com/shivam887423/CAPSTONE-2/assets/119883273/82adba1b-5090-4f5a-ac13-016e052f7942)

# PROJECT OVERVIEW

# Research strategy

To come up with initial questions and to formulate our research strategy, we should first look at the given guidance from Rossmann itself:

Rossmann operates over 3,000 drug stores in 7 European countries. Currently, Rossmann store managers are tasked with predicting their daily sales for up to six weeks in advance. Store sales are influenced by many factors, including promotions, competition, school and state holidays, seasonality, and locality. With thousands of individual managers predicting sales based on their unique circumstances, the accuracy of results can be quite varied. In their first Kaggle competition, Rossmann is challenging you to predict 6 weeks of daily sales for 1,115 stores located across Germany. Reliable sales forecasts enable store managers to create effective staff schedules that increase productivity and motivation. By helping Rossmann create a robust prediction model, you will help store managers stay focused on what’s most important to them: their customers and their teams!


# Focus
We will focus our Data Science project on the delivery of a robust statistical model, which is able to accurately predict a 6-week sales performance of Rossmann’s drugstores based on historical data By running through the data science process we will be able to answer the following research questions:

To what extend is sales performance influenced by factors like: promotions, competition, school and state holidays, seasonality, and locality. What is an appropriate model to predict sales?

# Approach
Our approach follows the generic Data Science process. As we just did in the parts above, the process starts with asking an interesting question. With the case of Rossmann we have identified a case, which is interesting for us because the underlying issue of sales prediction is relevant for all kinds of businesses, too. The second step is to get the data. Then, we will explore our data, which is the usual step to take after obtaining data. We will show plots to illustrate properties, trends, anomalies and patterns of the data. After ploting the first results, we will apply different statistical models and compare them to choose the most performing one. Finally, we will answer our initial questions and discuss future research directions.

## Dataset used

**Two datasets are used:**

**(1) Rossmann Stores Data.csv**

The dataset contains historical data including Sales of each Rossmann store across Europe.

- Store : a unique Id for each store
- DayOfWeek : Day of week (1-7)
- Date :  Date    
- Sales : the turnover for any given day (DEPENDENT VARIABLE)         
- Customers : the number of customers on a given day  
- Open : an indicator for whether the store was open: 0 = closed, 1 = open         
- Promo : indicates whether a store is running a promo on that day       
- StateHoliday : indicates a state holiday.a = public holiday, b = Easter holiday, c = Christmas, 0 = None
- SchoolHoliday : indicates if the (Store, Date) was affected by the closure of public schools

**Total number of rows in data : 1017209**

**Total number of columns : 9**

**(2) Store.csv**

The dataset conatains general information of each store.

- Store :   a unique Id for each store                 
- StoreType :                  differentiates between 4 different store models: a, b, c, d 
- Assortment :    describes an assortment level: a = basic, b = extra, c = extended              
- CompetitionDistance :  distance in meters to the nearest competitor store    
- CompetitionOpenSinceMonth :  gives the approximate  month of the time the nearest competitor was opened
- CompetitionOpenSinceYear :  gives the approximate year of the time the nearest competitor was opened            
- Promo2 :   Promo2 is a continuing and consecutive promotion for some stores: 0 = store is not participating, 1 = store is participating                   
- Promo2SinceWeek :  describes the calendar week when the store started participating in Promo2         
- Promo2SinceYear :      describes the year when the store started participating in Promo2      
- PromoInterval :   describes the consecutive intervals Promo2 is started, naming the months the promotion is started anew. E.g. "Feb,May,Aug,Nov" means each round starts in February, May, August, November of any given year for that store.

- **Total number of rows in data : 1115**
  
- **Total number of columns : 10**

 # Data Cleaning and Feature Engineering
**(1) Removing Duplicate rows**

No duplicate rows were present in dataset.

**(2) Handling null values**
No null values were present in Rossmann dataset.

Null values were present in sales dataset.

To remove null values in sales dataset I have imputed them with mode of the respective column.

**(3) Converting columns to appropriate data types**

Changed datatype of Date to date type.

**(5) Creating new columns**

Created new columns Day,Week and Month from date column.

**(6) Feature encoding**

Used One hot encoding to transform categorical feature - StoreType, Assortment, PromoInterval.

Used Label encoding to transform categorical features - StateHoliday.

**(7) Handling skewness**

Used square root transformation and logarithmic transformation to reduce skewness of skewed features.

**(8) Removing outliers**

Checked for outliers in sales column using IQR method and dropped them.

**(8) Standardization of features**

Used Min-Max Scaler for normalization of features.This step scales data into a uniform format that would utilize the data in a better way while performing fitting and applying different algorithms to it.

# Exploratory Data Analysis
Mainly performed using Matplotlib and Seaborn library and the following graph and plots had been used:

Bar Plot.

Histogram.

Scatter Plot.

Pie Chart.

Line Plot.

Heatmap.

Box Plot.

# Graphs

## Univirate Analysis

**Sales vs Day of the week**

![image](https://github.com/shivam887423/CAPSTONE-2/assets/119883273/e4be0b80-c840-4c3d-ae32-94e9841d33ea)


**Histogram of Sales in Rossmann Retail Dataset**

![image](https://github.com/shivam887423/CAPSTONE-2/assets/119883273/915484fe-6446-4c09-8e03-7db66059c43e)

## Bivirate Analysis

 **Scatter plot of Sales vs. Customers**

 ![image](https://github.com/shivam887423/CAPSTONE-2/assets/119883273/47bec4ec-0170-4742-9120-d3b844378db3)

 **Barplot for Sales vs Promo2sinceYear**

 ![image](https://github.com/shivam887423/CAPSTONE-2/assets/119883273/e6d256c5-0385-4275-857c-b54b95b731e8)

 ## Multivirate Analysis

** Sales" and "CompetitionOpenSinceMonth**

 ![image](https://github.com/shivam887423/CAPSTONE-2/assets/119883273/22671833-9e6e-4a7a-b518-cd6036db7801)

 ** Top 5 columns that are correlated with Sales **

 ![image](https://github.com/shivam887423/CAPSTONE-2/assets/119883273/92059333-3289-4cd4-84e4-801e70fcc4ae)









