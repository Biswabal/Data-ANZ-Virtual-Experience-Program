# Data@ANZ Virtual Experience Program with Forage

This repository contains solution which I have completed as a part of [Data@ANZ Virtual Experience Program](https://www.theforage.com/virtual-internships/prototype/ZLJCsrpkHo9pZBJNY/Data%40ANZ%20Program?ref=DsEXFixxovqkRxR2u).


# About the Program

There were two tasks completed as a part of this program. The tasks were based on a synthesised transaction dataset containing 3 months’ worth of transactions for 100 hypothetical customers. It contains purchases, recurring transactions, and salary transactions. The dataset were designed to simulate realistic transaction behaviours that are observed in ANZ’s real transaction data

## Task 1 Exploratory Data Analysis

The purpose of this task is to gather overall interesting insights from the data.

Please find Exploartory Data Analysis using Tableau [*here*](https://public.tableau.com/app/profile/biswabal.gurung/viz/ANZ-VirtualExperiencePrograms-Forage-Task1/ANZTransactionDataAnalysis).

Summary of my findings: 

* Most transaction happens to be on Friday and purchase is the most common type of transaction.
* Customer prefers to purchase more on Saturdays and Fridays, especially female customers.
* Transaction volumes are high between 9 am till noon.
* Salaries are credited only during Weekdays and compared to other types of transaction the average transaction amount for salaries is highest.
* Customer between 31-40 years of age tends to have higher income but they also spends more, whereas customer over 60 years has less income and spends less.
* The average spending of customers is likely to fall as they grow over 40 years of age.
* NSW, Queensland and Victoria hosts some of the top merchants with highest amount of sale.

## Task 2 Predictive Analytics

The purpose of this task is to identify the annual salary for each customer, to explore correlations between annual salary and various customer attributes, and to build simple regression model and Decision tree based model to predict salary.

Not so strong correlations were found between annual salary and various customer attributes but few interesting points to note are:

* Male customer's salary tends to increase with age unlike female customers.
* Female tends spend less and save more as their salary increases unlike male customers.

| **Model** | **MAE** | **RMSE**
|:----:|:----:|:----:|
| **model1 (Linear Regression Model)** | 20991.79 | 25360.34
| **model2 (Decision Tree Regressor)** | 18582.26 | 24173.84

Although Decision Tree performed better than Linear Regression, the MAE and RMSE for both the models are very high. It suggests that both the models are highly inaccurate and cannot be used by ANZ to segment customers into income brackets for reporting purpose. On hypertuning parameters the models could have performed slightly better but we cannot rely on it because the data we have is only for 100 customers. So, inorder to build more reliable models we need to come up with advance feature engineering and feature selection methods and more data to train and test the model.

If the goal is to segment customers, why not we create discrete class labels for annual salary and perform classification as it is more likely to give better results. However, more research is to be done on this part.
