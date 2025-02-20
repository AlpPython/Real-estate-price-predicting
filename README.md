# Real-estate-price-predicting
This project provides categorical boosting model for US real estate price predictinng. 
This model has 0.76 R-squared coefficient and predicts prices with about 10% accuracy

I've downloaded original dataset from Kaggle and firt of all made some visualisations
After that I've dropped outliers which exceed 3 standard deviations (Z-criteria)
This set includes information about 2,2 millions real estate advertisements from Redfin site

It contains information about geographycal location and internal characteristics
All this represented by these columns: price (in US dollars), bed (number of bedrooms),
bath, house_size (in square feet), acre_lot (the territory of the plot next to the house if it is a house), 
state, city, street, zip_code and prev_sold_date (if exists)

I tried different models with the rising complexity
First of all it was linear regression model and it has very-low and unstable predictive power


