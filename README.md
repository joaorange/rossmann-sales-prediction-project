# Drugstore Chain Sales Prediction

![144940356-a00abf79-b51b-47ce-b458-c706e326fdb1](https://github.com/joaorange/rossmann-sales-prediction-project/assets/86979717/310c6e66-fe9d-4d92-b846-dc58ce65f711)

This project is fictitious, and seeks to extract insights and propose data-based business solutions for a chain of drugstores. The objectives of this project were to perform exploratory data analysis, develop an accurate sales forecast model for the stores in the next six weeks, and create a telegram bot that can be accessed by the CEO or any other interested party to see the predictions.

Data can be found at <a href="https://www.kaggle.com/c/rossmann-store-sales">Kaggle</a>.

[![forthebadge made-with-python](http://ForTheBadge.com/images/badges/made-with-python.svg)](https://www.python.org/)

# 1. Description

Rossmann is one of the largest drug store chains in Europe, with around 56,200 employees and more than 4000 stores. 
The stores will receive investment for renovation, and the CFO need to know how much each store will sell to see the amount of money that will be invested in each unity.
The data team was requested to develop a sales model prediction that forecast the sales for the next 6 weeks for every store. The telegram bot was made to inform these predictions.

# 2. Business Strategy Results

The model developed predicts a gross income of $221.70 MM in the next 6 weeks for the stores.
Based on the mean absolute percentage error that the model gave to the "train" dataset for the sales of the stores, the best scenario has a gross income of $243.30 MM and a worst scenario of $200.09 MM.

# 3. Business Assumptions
The following assumptions were considered:

* The data available is only from 2013-01-01 to 2015-07-31;

* The data set original variables, and their respective descriptions, are as follows:

| Variable | Definition |
| ------------- | :-------------: |
| store | unique id for every store |
| date | date when the sale was made |
| sales | volume of products sold in one day |
| customers | number of customers |
| open  | whether the store was open (1) or closed (0)  |
| promo | whether the store was participating on a promotion (1) or not (0) |
| sate_holiday | whether it was a state holiday (a=public holiday, b=easter holiday, c=christmas) or not (0) |
| store_type  | designates the store model as a, b, c or d  |
| assortment | indicates the store assorment as: a=basic, b=extra, c=extended  |
| competition_distance | distance in meters to the nearest competitor store |
| competition_open_since_month  | the approximate month competitor was opened |
| competition_open_since_year | the approximate year competitor was opened |
| promo2  | wheter the store was participating on a consecutive promotion (1) or not (0) |
| promo2_since_week | indicates the calendar week the store was participating in promo2 |
| promo2_since_year | indicates the year the store was participating in promo2  |
| promo2_interval  | indicates the intervals in which promo2 started |

* The data set created variables, and their respective descriptions, are as follows:

| Variable | Definition |
| ------------- | :-------------: |
| year | year when the sale was made |
| month | month when the sale was made |
| day |  day when the sale was made |
| week_of_year | week of the year that the sale occurred (int type) |
| year_week | week of the year that the sale occurred (object type, %Y-%W) |
| week_of_year | week of the year that the sale occurred (int type) |
| year_week | week of the year that the sale occurred (object type, %Y-%W) |
| competition_since | join of 'competition_open_since_year' and 'competition_open_since_month' |
| competition_time_month | calculates the time in months that competitor has been open based on the purchased date |
| promo_since | join of 'promo2_since_year' and 'promo2_since_week'|
| promo_time_week | calculates the time in weeks that promotion began based on the purchased date |
| is_promo | whether the purchase occurred during an active promo2 (1) or not (0) |

# 4. Solution Strategy

1. Data Description
2. Feature Engineering
3. Variable Filtering
4. Exploratory Data Analysis
5. Data Preparation
6. Feature Selection
7. Machine Learning Modeling
8. Hyperparameter Fine Tuning
9. Translation and interpretation of error, model-to-Business interpretation
10. Deploy model to production


# 5. Top 4 Data Insights

1. There are a negative correlation, on average, between stores sales and the length of time that there's competition.

![image](https://github.com/joaorange/rossmann-sales-prediction-project/assets/86979717/24af8131-256d-4a97-b7af-a8c98f2dfd47)

2. Stores with more consecutive promotions sell less than those with only the original promotion.
![image](https://github.com/joaorange/rossmann-sales-prediction-project/assets/86979717/f7b5ef6c-7c33-48c4-bd26-3ec1b0b1e62f)

3. Stores sell less in the second half of year.


![image](https://github.com/joaorange/rossmann-sales-prediction-project/assets/86979717/fb46746d-b054-41a5-b69b-ad373431b441)

4. There is no correlation between the number of sales and the distance from competitors.
![image](https://github.com/joaorange/rossmann-sales-prediction-project/assets/86979717/8050028b-81e0-416e-9d26-6cc81137de24)


# 6. Machile Learning Model

The following machine learning models were used:

* Random Forest Regressor;
* Linear Regression;
* Regularized Linear Regression;
* XGBoost Regressor.

The resuts after the cross validation were the following:

![image](https://github.com/joaorange/rossmann-sales-prediction-project/assets/86979717/ec228e7e-6cd8-4e4f-941e-ccde1a7cc910)

MAE = mean absolute error; MAPE = mean absolut percentage error; RSME = root mean squared error.

The XGBoost Regressor after fine tuning was the model used:

![image](https://github.com/joaorange/rossmann-sales-prediction-project/assets/86979717/bcd18cab-0e64-4625-b9cc-b91bcc5a2543)

Error rate: 

![image](https://github.com/joaorange/rossmann-sales-prediction-project/assets/86979717/12e6d7a3-a33a-432e-8540-6716b227db9a)

Actual sales and prediction sales: 

![image](https://github.com/joaorange/rossmann-sales-prediction-project/assets/86979717/e14fb4b8-70ad-40e4-8cb7-800dc9245774)


# 7. Telegram Bot

The bot can be accessed <a href="https://t.me/rossmann23_bot">here</a>.

![image](https://github.com/joaorange/rossmann-sales-prediction-project/assets/86979717/40625099-b104-40ef-841c-5edec1b0498c)


# 8. Conclusion

The objective of this project was to develop a prediction model for Rossmann's sales. Through model validation and the telegram bot, the model was developed and applied in a way that its results could be communicated effectively.

# 9. Next Steps

* Test other models to see if the error indicators can be reduced;
* Look for demographic or economic sources of data on where stores are located and see if this can improve the effectiveness of the models;
* Improve communications in telegram bot.
