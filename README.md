# Bike Sharing Demand Prediction for BoomBikes
> This project involves building a multiple linear regression model to predict the demand for shared bikes in the post-pandemic period. The model will help the management of BoomBikes understand key factors driving bike demand and make informed business decisions to recover from the revenue decline caused by the COVID-19 pandemic.

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)
* [Contact](#contact)

## General Information
- **Problem Statement**: BoomBikes, a US-based bike-sharing provider, has faced significant revenue losses due to the COVID-19 pandemic. As they prepare to resume operations post-lockdown, they aim to understand the factors that influence bike demand to design a strategic recovery plan. This project focuses on building a regression model to predict bike demand using historical data on bike rentals, weather conditions, and calendar information.
  
- **Business Goal**: The goal is to model the demand for shared bikes based on available features like weather, season, temperature, and other variables. The insights derived from the model will help the company:
  1. Identify key predictors of bike demand.
  2. Understand how these predictors affect demand.
  3. Make data-driven business decisions to meet customer demand effectively and regain market share.

- **Dataset**: The dataset (`/data/day.csv`) contains daily records of bike-sharing data from 2018 and 2019, including variables like weather, season, holiday information, temperature, humidity, wind speed, and total bike rental counts (casual and registered).

### Important Notes on Data:
- Variables like `season` and `weathersit` have numeric values representing categories that should be treated as categorical rather than ordered numeric data.
- The `yr` variable represents the years 2018 and 2019. Although it only has two values, it is significant as it reflects the growing popularity of bike-sharing systems over time.
- The target variable for this regression task is `cnt` (total rentals), which combines both casual and registered users.

## Conclusions
* The equation of the best fit line is given by:
> cnt = 0.21 + 0.23 × yr - 0.10 × holiday + 0.55 × atemp - 0.15 × hum - 0.16 × windspeed 
    + 0.11 × season_summer + 0.16 × season_winter - 0.05 × weather_mist_cloud 
    - 0.23 × weather_light_snow_rain + 0.08 × Quarter_JulAugSep
    
* The close alignment of R2 and adjusted R2 values between the training and test sets in a linear regression model indicates effective generalization. This similarity suggests the model avoids overfitting to the training data and is likely to perform consistently on new, unseen data.

* Three key feature variables, atemp, yr, and season_winter, exhibit the highest coefficient values, indicating their significant impact.

* Leverage High-Impact Features: Focus on features such as temp, yr, and season_winter as they exhibit the highest coefficient values, indicating significant impact on bike demand.

* Seasonal Strategies: Develop targeted marketing and pricing strategies for different seasons, particularly emphasizing promotions during Summer and Winter. Also the company can reduce the expences during heavey rain and snow people will mostly use cars instead of rental bikes.

* Optimize Operational Planning: Adjust bike availability and distribution based on the significant features identified, optimizing resources for peak demand periods.

## Technologies Used
- Python==3.10.12
- pandas==2.2.2
- numpy=1.26.4
- scikit-learn==1.5.2
- matplotlib==3.9.1
- seaborn==0.13.2

## Acknowledgements
- This project was inspired by a real-world business problem from the bike-sharing industry, particularly the challenges faced by BoomBikes due to the pandemic.
- The dataset is cited from Fanaee-T, Hadi, and Gama, Joao, "Event labeling combining ensemble detectors and background knowledge", Progress in Artificial Intelligence (2013).
- Reference publication: [Event Labeling and Ensemble Learning](http://dx.doi.org/10.1007/s13748-013-0040-3).

## Contact
Created by [Shubham Sharma](https://www.linkedin.com/in/shubham-sharma-andy/) - feel free to contact me!
