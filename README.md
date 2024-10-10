# ML_Model_Megaline
Develop a model that picks the correct plan for Megaline's legacy customers.

# Introduction
In this project, we will work with a dataset from a mobile network company named Megaline Mobile. Their main concern is about the number of customers still using their old plan. They are aiming to create a model that can analyze customer behavior and recommend to them either Smart or Ultra packages.

The dataset provided to use contains data on customer behavior, specifically the ones who have already made the switch to new packages from a previous statistical data analysis project. We will develop a model that can accurately choose the appropriate package for each customer. Our primary goal is to achieve a high accuracy level with the minimum set at 75%.

# Data Description

- `сalls` — number of calls,
- `minutes` — total call duration in minutes,
- `messages` — number of text messages,
- `mb_used` — Internet traffic used in MB,
- `is_ultra` — plan for the current month (Ultra - 1, Smart - 0).

# Conclusion

We found through our sanity check that 70% of Megaline Mobile customers are included in the Ultra package. 

When the models were not tuned, none reached the accuracy criteria of 75%. 

The Decision Tree model after tuning passed the criteria with 77.7%.

The Random Forest model after tuning passed the criteria with 78.7%.

The Logistic Regression model did not reach criteria with 73.5%.

From all the model experiments, we found that there are 2 that met the criteria:

Decision Tree: max_depth = 8
Random Forest: max_depth = 10 , n_estimator=450.

It can be concluded that the best model with the highest efficiency is the Random Forest model with a max_depth set to 10 and `n_estimator = 450`
