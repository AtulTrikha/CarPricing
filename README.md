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

* Most used cars are less than 10 years old (>2015)
* The largest number of vehicles are white automatic sedans
* There are very few diesel and electric cars in the used car dealerships
* California and Florida sell the most used cars
* Ford, Cheverlot and Toyota are the most popular manufacturers

![Interesting facts Image](https://github.com/AtulTrikha/CarPricing/blob/main/images/vehicle_data_plot.png "Interesting facts")