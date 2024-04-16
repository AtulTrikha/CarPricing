# What Drives the Price of a Car?

## Executive Summary
**Objective**: The project aims to analyze a dataset from Kaggle containing car information to determine factors influencing a car's price. The goal is to offer clear recommendations to a used car dealership on what consumers value in a used car.

**Key Findings**: The price of used cars is influenced by various factors: a clean title is essential, with each year of age reducing the price. Manufacturer and condition also play significant roles, with each unit increase in manufacturer index and condition index decreasing the price. Additionally, the number of cylinders increases the price, while odometer reading, transmission type (mostly automatic), and rear-wheel drive (rwd) configuration also impact pricing.

**Recommendation**: Focus on acquiring high-value brands and adjust pricing strategies based on age, mileage, and fuel type.

**Framework/Methodology**: For this task, I am employing the CRISP-DM framework, which is structured into six key phases. 

![CRISP-DM six key phases Image](https://github.com/AtulTrikha/CarPricing/blob/main/images/Six_Phases_of_CRISP.png "CRISP-DM six key phases ")

## Repository contents

* ``data`` - vehicles.csv data file from Kaggle Machine Learning dataset repository used in the notebooks
* ``images`` - Image files used in Notebook and Project Description
* ``notebook`` - What Drives the Price of a Car Notebook

## Business Understanding

The primary business goal is to pinpoint essential features influencing used car prices. This insight equips Car Dealers and their Sales Teams to optimize their inventory, thereby boosting sales. 

The task involves meticulous data preprocessing, strategic feature engineering, and the development of a robust predictive model. Ultimately, crafting an effective model capable of reliably estimating used car prices.

## Data Understanding

**Dataset Size**: 426,880

**Feature Definitions**:

01. Price: Price in USD, not adjusted for inflation.
02. Year: The year in which the car was manufactured
03. Manufacturer: 43 unique auto brands that manufacture the automobiles that are a part of this dataset.
04. Model: The model of the car.
05. Condition: The condition of the car; excellent, good, fair, like new, salvage, new.
06. Cylinders: The number of cylinders in the car engine ranging from 3 to 12. Also has the ‘other’ category too.
07. Fuel: There were five types of fuel, ‘diesel’, ‘gas’, ‘electric’, ‘hybrid’ and ‘other’.
08. Odometer: The distance travelled by the car after it was first bought.
09. Title Status: The cars have 6 types of statues; ‘clean’, ‘lien’, ‘rebuilt’, ‘salvage’ , ‘parts only’ and ‘missing’.
10. Transmission: There are 3 types of transmission; ‘automatic’, manual and other.
11. Drive: There are 3 types of drive transmissions; ‘4WD, ‘FWD’ and ‘RWD’. (Four-wheel drive, forward-wheel drive and rear-wheel drive.)
12. Size: Size of the vehicle
13. Type: This feature identifies if a vehicle is a SUV or a mini-van. There 13 unique values in this feature.
14. Paint_Color: This feature identifies the color of the car. There 12 unique values in this feature.
15. State: The state is political territory and is represented in short form in the data set. Like “fl” is used for the state of Florida.

**Missing Values**:
![Missing Values Image](https://github.com/AtulTrikha/CarPricing/blob/main/images/missing_values.png "Missing Values")

**Unrealistic Values**: (for example, price with zero and single digits values
![Unrealistic Values Image](https://github.com/AtulTrikha/CarPricing/blob/main/images/unrealistic_values.png "Unrealistic Values")

**Interesting facts**

* The majority of used cars are younger than 10 years old, predominantly from years after 2015.
* The most common type of vehicle found is white automatic sedans.
* Diesel and electric cars are notably scarce in used car dealerships.
* California and Florida emerge as the leading states in terms of used car sales.
* Ford, Chevrolet, and Toyota stand out as the most favored manufacturers among buyers.

![Interesting facts Image](https://github.com/AtulTrikha/CarPricing/blob/main/images/vehicle_data_plot.png "Interesting facts")

## Data Preparation

Summary of the Data Preparation is as follows:

- Remove records with Zero Prices and Odometer values
- Removed unnecessary features
- Drop a number of factors (i.e., VIN, id, region etc.) that are not significant in user car price determination
- Review and remove the other factors (i.e., state, paint color, manufacturer, transmission etc.) and check if they have an impact on car price based on the provided data
- Filtering the data based on year on manufacture = 1990 as the number of vehicles before 1990 were very low

## Modeling

- Split the data to training and test sets, 70/30 split ratio so that we can assess how well the model can predict
- Fit below five regression models on the training set and evaluate them on the test set using the R^2 score. The models we use are:

	- Linear Regression
	- Ridge Regression
	- Lasso Regression
	- Decision Tree Regression
	- Random Forest Regression

For each model, we print the R^2 score and the feature importance. For linear models, we use the coef_ attribute to get the coefficients of the features.

## Evaluation

Based on the analysis of the various regression models, we can conclude that the Random Forest Regression model performs better than the other regression models with an R-squared score of 0.724. The feature importance scores of the decision tree regression model also show that the year, fuel type, and odometer are the most important factors affecting used car prices.

However, it is important to note that the other regression models still provide some valuable insights into the factors that affect used car prices. For instance, the linear regression model highlights the importance of the year and age of the car, while the ridge and lasso regression models emphasize the importance of the average brand price, transmission, and cylinder type.

Overall, our findings suggest that the business objective of identifying the drivers of used car prices can be achieved by considering a range of factors including the year, age, fuel type, transmission, and cylinder type. It is also worth noting that the earlier phases of data exploration and preprocessing were crucial in ensuring the quality of the data and the accuracy of the models.

Moving forward, we can recommend further analysis to explore the interactions between these factors and their impact on used car prices. We can also suggest revisiting the business objective to ensure that it is aligned with the insights gained from the regression models. Additionally, we can advise our client to consider incorporating more detailed data on car features and specifications to improve the accuracy of the models.

## Deployment

### Introduction:
We were tasked with building a model to predict used car prices for a group of used car dealers. Our goal was to identify the key drivers of used car prices and provide meaningful insights to the dealers.

### Methodology:
We began by exploring and cleaning the dataset. We removed null values and columns that were irrelevant to our analysis. We then conducted exploratory data analysis to identify any patterns or relationships in the data.

Next, we built several regression models using different algorithms, including linear regression, ridge regression, lasso regression, and decision tree regression. We evaluated the performance of each model using R^2 scores and feature importance scores.

### Findings:
Our analysis revealed that the year of the car, mileage (odometer), average brand price, number of cylinders, and fuel type were the most significant drivers of used car prices. Random Forest Regression model performs better than the other regression models with an R-squared score of 0.724, indicating that it was able to explain 72% of the variability in the data.

### Recommendations:
Based on our findings, we recommend that used car dealers pay close attention to the age of the cars they are buying and selling, as well as the mileage on the car. They should also consider the average price of the brand they are dealing with, the number of cylinders in the car, and the fuel type. These factors can greatly impact the price of a used car.

### Conclusion:
Overall, our analysis provides valuable insights into the drivers of used car prices. We believe that used car dealers can use this information to fine-tune their inventory and improve their sales.