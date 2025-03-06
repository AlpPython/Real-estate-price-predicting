# Real-estate-price-predicting
You can find original database via this link and then run all kernels in ipynb file 
to get the same results (all kernels had comments about their destination):
https://www.kaggle.com/datasets/ahmedshahriarsakib/usa-real-estate-dataset

This project provides categorical boosting model for US real estate price predictinng. 
This model has 0.76 R-squared coefficient and predicts prices with about 15% accuracy

I've downloaded original dataset from Kaggle and firt of all made some visualisations
After that I've dropped outliers which exceed 3 standard deviations (Z-criteria) and added some data visualisations
This set includes information about 2,2 millions real estate advertisements from Redfin site

It contains information about geographycal location and internal characteristics
All this represented by these columns: price (in US dollars), bed (number of bedrooms),
bath, house_size (in square feet), acre_lot (the territory of the plot next to the house if it is a house), 
state, city, street, zip_code and prev_sold_date (if exists)

I tried different models with the rising complexity
First of all it was linear regression model and it has very-low and unstable predictive power
It described about 3 percent of the observed variance (and uses only 3 independent variables: house_size, bed and bath)
These predictions were not better than predictions based on average price

So after that I could try to use linear regression model with dummy-varieties, but I choosed to move in the direction of much more powerful tools

I used CatBoost model for combining categorical and numerical independent varieties
I have played with different tree depth in ensamble method learning and with the different number of learning interactions
Optimum was found with maximum tree depth equal to 16 and 1000 interactions with 0.1 learning velosity
It had 0.75 R-squared coefficiet which means that this model explains 3/4 of amarican real estate prices variety
