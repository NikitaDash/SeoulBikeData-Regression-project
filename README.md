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

# Feature Description:

Date : Date feature which is str type is needed to convert it into Datetime format DD/MM/YYYY.The new feature extracted from Date are Day, Month and year

Rented Bike Count : Number of bike rented which is our Dependent variable according to our problem statement which is int type.

Hour: Hour feature which is in 24 hour format which tells us number bike rented per hour is int type.

Temperature(°C): Temperature feature which is in celsius scale(°C) is Float type.

Humidity(%): Feature humidity in air (%) which is int type.

Wind speed (m/s) : Wind Speed feature which is in (m/s) is float type.

Visibility (10m): Visibility feature which is in 10m, is int type.

Dew point temperature(°C): Dew point Temperature in (°C) which tells us temperature at the start of the day is Float type.

Solar Radiation (MJ/m2): Solar radiation or UV radiation is Float type.

Rainfall(mm): Rainfall feature in mm which indicates 1 mm of rainfall which is equal to 1 litre of water per metre square is Float type.

Snowfall (cm): Snowfall in cm is Float type. Seasons: Season, in this feature four seasons are present in data is str type.

Holiday: whether no holiday or holiday can be retrieved from this feature is str type.

Functioning Day: Whether the day is Functioning Day or not can be retrieved from this feature is str type.

Weekend : Weekend extracted from Day 1 when the day is Saturday or Sunday while 0 when weekdays

# Work Flow :
1. Data Collecting
2. Data Filtering
3. EDA
4. Data Preparation
5. Data Modeling

# Conclusion and Insight:
1. In summer season highest number of bike was rented as compared to other seasons with count touching at 3500 while in winter season lowest number of bike was rented touching the count of close to just 1000. From this we can assume that people tends to rent more bikes in summer as compare to other seasons also people tends to rent less bike in winter season.
2. During working day people tend to rent more bikes as around 3500 from this we can assume that on holidays people tends to rent less bike.
Also we can see people tends to rent less or no bike during no functioning day.
3. In weekend vs Rented Bike count we can see that people tends to rent more bike during weekdays as compared to weekends.
4. After applying linear regression model, we got R2 score of 0.6478 for training data and R2 score of 0.6583 for test data, which signifies that model is optimally fit on both training and test data i.e. no overfitting is seen.
5. We also tried Tree based classifiers for our data, we applied Decision Tree Regressor, with that we we got R2 score of 1.00 for training data and 0.7962 for test data which shows overfitting.
6. To get better accuracy on tree based model, we applied Random forest, with that we got R2 score of 0.9856 for training data and 0.888 for test data.
7. Finally, we applied Gradient boost with parameters selected after grid search which resulted in highest R2 score of 0.958 for training data and 0.933 for test data with very less mean squared error of 6 and 10 in training as well as in test data.


|Name|Train_Time|Train_R2_Score|Test_R2_Score|Test_RMSE_Score|
|---|---|---|---|---|
|LinearRegression:	|0.008595	|0.647891	|0.658364	|6.435239|
1	Lasso:	0.008617	0.636225	0.643483	6.573891
2	Ridge:	0.006999	0.647891	0.658356	6.435309
3	KNeighborsRegressor:	0.026799	0.759540	0.634925	6.652328
4	SVR:	1.694278	0.457188	0.465150	8.051900
5	DecisionTree	0.043268	1.000000	0.796217	4.970115
6	RandomForest	2.709142	0.985689	0.888823	3.671046
7	ExtraTreeRegressor :	1.870717	1.000000	0.895523	3.558714
8	GradientBoostingRegressor:	0.893459	0.888886	0.872145	3.936779
9	XGBRegressor:	0.538134	0.977729	0.898301	3.511089
10	Light-GBM:	0.191949	0.970815	0.907160	3.354671
11	MLPRegressor:	2.435042	0.046814	0.043449	10.768041





