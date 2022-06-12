# BIKE SHARING ASSIGNMENT

 ## INTRODUCTION

- A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short term basis for a price or free. Many bike share systems allow people to borrow a bike from a "dock" which is usually computer-controlled wherein the user enters the payment information, and the system unlocks it. This bike can then be returned to another dock belonging to the same system.

## PROBLEM STATEMENT

- A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. The company is finding it very difficult to sustain in the current market scenario. So, it has decided to come up with a mindful business plan to be able to accelerate its revenue as soon as the ongoing lockdown comes to an end, and the economy restores to a healthy state. 


- In such an attempt, BoomBikes aspires to understand the demand for shared bikes among the people after this ongoing quarantine situation ends across the nation due to Covid-19. They have planned this to prepare themselves to cater to the people's needs once the situation gets better all around and stand out from other service providers and make huge profits.


- They have contracted a consulting company to understand the factors on which the demand for these shared bikes depends. Specifically, they want to understand the factors affecting the demand for these shared bikes in the American market. The company wants to know:

     - Which variables are significant in predicting the demand for shared bikes.
     - How well those variables describe the bike demands
     
## BUSINESS GOAL
 
 
-  Required to model the demand for shared bikes with the available independent variables. It will be used by the management to understand how exactly the demands vary with different features. They can accordingly manipulate the business strategy to meet the demand levels and meet the customer's expectations. Further, the model will be a good way for management to understand the demand dynamics of a new market. 


## ANALYSIS APPROACH

- Develop a model to find the variables which are significant the demand for shared bikes with the available independent variables.
- It will be used by the management to understand and manipulate the business strategy to meet the demand levels and meet the customer's expectations.


## Table of Contents
- Introduction
- Problem Statement
- Business Goal
- Analysis Approach
- Importing Packages
- Loading the dataset
- Description of the dataset
- Data Cleaning
- Exploratory Data Analysis
- Preparation of data for Linear Regression
- Split the dataset into train data & test data
- Feature Scaling
- Using RFE Approach 
- Model Building
- Validation of the Assumption of Linear Regression
- Making Predictions
- Evaluation of the Model
- Inference
- Conclusion

<!-- You can include any other section that is pertinent to your problem -->

## INFERENCE

#### Hypothesis Testing
  
- Hypothesis testing states that:

    - H0: B1=B2=...=Bn=0

    - H1: at least one Bi!=0
    
- From the final model summary, we can observe & it is evident that all our coefficients are not equal to zero which ensures that we reject the null hypothesis.

#### F Statistics
  
- F-Statistics is used for testing the overall significance of the Model: Higher the F-Statistics, more significant the Model is.

     - F-statistic: 196.5

     - Prob (F-statistic):  4.51e-186

- The F-Statistics value of 196.5 (which is greater than 1) and the p-value of '~0.0000' states that the overall model is significant.

#### Interpretation of Coefficients:

- atemp: A coefficient value of ‘0.4120’ indicated that a unit increase in atemp variable, increases the bike hire numbers by 0.4120 units.
- windspeed: A coefficient value of ‘-0.1293’ indicated that, a unit increase in windspeed variable decreases the bike hire numbers by 0.1293 units.
- yr: A coefficient value of ‘0.2372’ indicated that a unit increase in yr variable, increases the bike hire numbers by 0.2372 units.
- winter: A coefficient value of ‘0.0341’ indicated that, a unit increase in winter variable increases the bike hire numbers by 0.0341 units.
- spring: A coefficient value of ‘-0.1237’ indicated that, a unit increase in spring variable decreases the bike hire numbers by 0.1237 units.
- month 10: A coefficient value of ‘0.0472’ indicated that with respect to month 1, a unit increase in 10 variable increases the bike hire numbers by 0.0472 units.
- Mist_cloudy: A coefficient value of ‘-0.0844’ indicated that, a unit increase in Mist_cloudy variable, decreases the bike hire numbers by 0.0844 units.
- month 3: A coefficient value of ‘0.0388’ indicated that with respect to month 1, a unit increase in month 3 variable increases the bike hire numbers by  0.0388  units.
- month 5: A coefficient value of ‘0.0398’ indicated that with respect to month 1, a unit increase in month 5 variable increases the bike hire numbers by 0.0398  units.
- month 9: A coefficient value of ‘0.0823’ indicated that with respect to month 1, a unit increase in month 9 variable increases the bike hire numbers by 0.0823 units.
- Sunday: A coefficient value of ‘-0.0499’ indicated that, a unit increase in Sunday variable, decreases the bike hire numbers by 0.0499 units.
- Light rain_Light snow_Thunderstorm: A coefficient value of ‘-0.2988’ indicated that, a unit increase in Light rain_Light snow_Thunderstorm variable, decreases the bike hire numbers by 0.2988 units.
- holiday: A coefficient value of ‘-0.0950’ indicated that, a unit increase in holiday variable decreases the bike hire numbers by 0.0950 units.
- const: The Constant value of ‘0.2743’ indicated that, in the absence of all other predictor variables (i.e. when x1,x2...xn =0), The bike rental can still increase by 0.2743 units.

## CONCLUSION

#### The equation of best fitted surface based on the model 

cnt = 0.2743  + (yr × 0.2372)  - (0.0950 X holiday) + (0.4120 X atemp) - (0.1293 X Windspeed) - (0.1237 X Spring) + (0.0341 X winter) - (0.2988 X Light rain_Light snow_Thunderstorm) - (0.0844 X Mist_Cloudy) + (0.0388 X 3) + (0.0398 X 5) + (0.0823 X 9) - (0.0499 X Sunday) + (0.0472 X 10)


- Significant variables to predict the demand for shared bikes
   
   - atemp
   - Season(Spring, Winter)
   - months(3, 5, 9, 10)
   - holiday
   - windspeed 
   - Year (2019)
   - Sunday
   - weathersit(Light rain_Light snow_Thunderstorm, Mist_cloudy)
  

- The model has a good R^2 score of 0.821 on the test data, which means that 82.1% of the variation in total number of bike rentals can be explained by the variables in the linear regression model built. Hence, the model well justifies the data, and can be used for decision making.   

#### From the analysis of the above model, we can ensure that the comapany should focus on the following features:

- Company should focus on expanding business during Spring.
- Company should focus on expanding business during the month of 9.
- Based on previous data it is expected to have a boom in number of users once situation comes back to normal, compared to 2019.
- There would be less bookings during Light Snow or Rain, they could probably use this time to serive the bikes without having business impact.
- Demands increases in the month of 3, 5, 9, 10 and yr
- Demand decreases if it is holiday , Spring, Light rain_Light snow_Thunderstorm, Mist_cloudy, Sunday

Therefore, when the situation comes back to normal, the company should come up with new offers during spring when the weather is pleasant and also advertise a little for the month of 9 as this is when business would be at its best.

## Technologies Used
- IDE - Jupyter
- Base Language - Python - version 3.0
- Libraries used in python
   - Pandas - version 1.4.2
   - Matplotlib - version 3.5.1
   - Seaborn - version 0.11.2
   - Statsmodels - version 0.13.2
   - Scikitlearn - version 1.0.1

## Acknowledgements

- Created by PADMAVATHI D[https://github.com/Padma-aishu] as a part of MS in ML & AI program from IIITB & LJMU by UpGrad.
