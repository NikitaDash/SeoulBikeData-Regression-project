# SeoulBikeData-Regression-project

# Project Summery

This project revolves around predictive modeling for Seoul's bike rental demand, leveraging a dataset comprising 8,760 rows and 14 columns. The workflow adheres to a systematic and formal structure, commencing with data collection and preliminary analysis to ascertain the dataset's fundamental characteristics, including its dimensions and data types. Subsequently, data filtering and cleaning are executed to enhance data quality by eliminating superfluous columns and addressing missing values.

The project progresses to Exploratory Data Analysis (EDA), where insightful visualizations are generated to illuminate relationships between dependent and independent variables. This phase also encompasses an analysis of mean distributions and correlations between columns. With a well-informed understanding of the data, attention shifts towards data preparation, encompassing feature engineering, encoding, and the division of data into training and testing sets.

Data scaling ensures optimal model performance. Model selection is a deliberate process aimed at choosing the most suitable algorithm. Model evaluation employs various metrics to gauge model performance, with hyperparameter tuning employed to enhance accuracy and mitigate overfitting. Ultimately, a comprehensive comparison between test and train data illuminates the model's performance and errors, ensuring a robust predictive model for Seoul's bike rental demand.




#  Problem description

The Seoul bike sharing demand data set is hosted in the UCI Machine Learning Repository. The data set contains the count of the number of bikes rented at each hour in the Seoul bike-sharing system and information regarding weather conditions.

The final product will consist of a model that predicts the number of bicycles rented in any given day based on the hour and other weather-related variables such as rainfall and humidity. The system’s predictions are used to guarantee that available bikes will meet the demand for the service.

# Data Description
The dataset contains weather information (Temperature, Humidity, Windspeed, Visibility, Dewpoint, Solar radiation, Snowfall, Rainfall), the number of bikes rented per hour and date information.

## **Attribute Information:**
Date : year-month-day

Rented Bike count - Count of bikes rented at each hour

Hour - Hour of he day

Temperature-Temperature in Celsius

Humidity - %

Windspeed - m/s

Visibility - 10m

Dew point temperature - Celsius

Solar radiation - MJ/m2

Rainfall - mm

Snowfall - cm

Seasons - Winter, Spring, Summer, Autumn

Holiday - Holiday/No holiday

Functional Day - NoFunc(Non Functional Hours), Fun(Functional hours)

# Work Flow :
1. Data Collecting
2. Data Filtering
3. EDA
4. Data Preparation
5. Data Modeling




