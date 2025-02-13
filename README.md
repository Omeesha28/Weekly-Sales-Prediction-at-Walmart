<h1 align='center'>Weekly Sales Prediction at Walmart Dataset</h1>

<p align="center">
  <img src="dataset-cover.jpeg" width="600">
</p>

## Project Objective

### Introduction:

As one of the premier multinational retail giants, Walmart faces fierce competition in the dynamic retail landscape. To sustain its market leadership, Walmart relies on strategic decisions backed by insightful data analysis.

### Objective:

Through rigorous exploratory data analysis (EDA), we embarked on a journey to harness the power of past data from Walmart stores. Our aim was to construct a predictive model capable of forecasting Weekly Sales accurately. Such a model serves as a potent tool for business managers, enabling them to uncover critical insights and pinpoint areas for enhanced strategic planning.

### Key Contributions:

Strategic Decision Support: Our predictive model empowers Walmart's leadership with actionable insights, allowing them to make informed decisions crucial for maintaining market dominance.
Identifying Business Weaknesses: By scrutinizing past data, our model identifies potential shortcomings in business planning, enabling proactive measures to address them effectively.
Enhanced Planning Efficiency: With the ability to anticipate Weekly Sales, Walmart can optimize resource allocation, streamline operations, and bolster overall efficiency.

### Conclusion:

In the fiercely competitive retail sector, the ability to forecast Weekly Sales accurately is indispensable for Walmart's sustained success. Our predictive model, born out of comprehensive exploratory data analysis, stands as a testament to Walmart's commitment to innovation and strategic foresight.

## Table of Contents

<details open>
<summary>Show/Hide</summary>
<br>

### Data Source
Source : The dataset is taken from Kaggle
URL : https://www.kaggle.com/code/yasserh/walmart-sales-prediction-best-ml-algorithms/input

Data analysis
Data in the form of columns:
* Store - the store number (1-45)
* Date - the week of sales (2010,2011,2012)
* Weekly_Sales - sales for the given store
* Holiday_Flag - whether the week is a special holiday week (1 – Holiday week and 0 – Non-holiday week)
* Temperature - Temperature on the day of sale
* Fuel_Price - Cost of fuel in the region
* CPI – Prevailing consumer price index
* Unemployment - Prevailing unemployment rate


1. [ File Descriptions ](#File_Description)
2. [ Technologies Used ](#Technologies_Used)    
3. [ Structure ](#Structure)
4. [ Summary ](#Summary)
   * [ 1. Data Cleaning](#Data_Cleaning)
   * [ 2. Data Analysis ](#Data_Analysis) 
   * [ 3. Modelling, Hyperparameter Tuning & Evaluation](#Modelling)
       * [ Conclusion ](#Conclusion)
       * [ Future Improvements ](#Future_Improvements)
</details>

## File Descriptions
<details>
<a name="File_Description"></a>
<summary>Show/Hide</summary>
<br>

* <strong>[Final_project ](https://github.com/Omeesha28/Final_project.git)</strong>: folder containing all data files
    * <strong>1.Walmart.csv</strong>: data before any changes
    * <strong>2.df_date_convert.csv</strong>: data after checking for null and duplicate values and convert 'Date' column to datetime, extract year, month, day and week from Date
    * <strong>3.df2_data.csv</strong>: Save DataFrame to a CSV file for Neural Netwroking Model
    * <strong>4.X_linear_data.csv</strong>: Spliting data and saving the X  data in csv file
    * <strong>5.y_linear_data.csv</strong>: Spliting data and saving the y  data in csv file
    * <strong>6.df_split_date_data.csv</strong>: Fluction to split year into four seasons then correct data format of the 'date' column
    * <strong>7.df_data_after_drop.csv</strong>: Save DataFrame to a CSV file after dropping unwanted columns
    * <strong>8.df_drop_outlier.csv</strong>: Save DataFrame to a CSV after dropping outliers
</details>

## Tecnologies Used
<details>
<a name="Technologies_Used"></a>
<summary>Show/Hide</summary>
<br>
    
* <strong>Python</strong>
* <strong>Pandas</strong>
* <strong>Numpy</strong>
* <strong>Matplotlib</strong>
* <strong>Seaborn</strong>
* <strong>Scikit-Learn</strong>
* <strong>Sklearn</strong>
* <strong>Plotly</strong>
* <strong>Tensorflow</strong>
* <strong>Category_encoders</strong>
</details>

## Structure
<details>
<a name="Structure"></a>
<summary>Show/Hide</summary>
<br>

  * 1.1 Import 
  * 1.2 Data Understanding
  * 1.3 Checking for Nulls
  * 1.4 Check Duplicated Data
  * 1.5 Feature Engineering: Date Variable
  * 1.6 Data Distribution
    * 1.6.1 Data Distribution: Target
    * 1.6.2 Data Distribution: Numerical Features
    * 1.6.3 Data Distribution: Categorical Features
  * 1.7 Feature Analysis
    * 1.7.1 Feature Analysis: Holiday_Flag vs Weekly_Sales
    * 1.7.2 Feature Analysis: Month, Year vs Weekly_Sales
    * 1.7.3 Feature Analysis: Histogram to show the distribution of the data for Uempoloyment, Fuel Price, Temperature and Weekly_Sales
  * 1.8 Finding and Handling Outliers
  
</details>


   
<a name="Summary"></a>
## Summary

<a name="Data_Cleaning"></a>
### Data Cleaning
<details open>
<summary>Show/Hide</summary>
<br>

#### Data Cleaning
Walmart dataset consisting of 6435 rows and 8 columns, which has the target column Weekly_Sales. we could say the dataset is quite clean, where there are no missing values and duplicate values.
There are 497 rows outlier data which is dropped in total 
</details>

<a name="Data_Analysis"></a>
### Data Analysis
<details open>
<summary>Show/Hide</summary>
<br>

#### Data Analysis
From the Annual Sales graph, it can be seen that the largest sales occurred in 2011, followed by 2010 and 2012. It should be noted that the data ranges are not balanced every year.

</details>


<a name="Modelling, Hyperparameter Tuning & Evaluation"></a>
## Modelling
<details open>
<summary>Show/Hide</summary>
<br>

### Neural Networking/ Deep Learning Model
Split training/test datasets, Preprocess numerical data for neural network, Create a StandardScaler instances,
Fit the StandardScaler and finally Scale the data

### Logistic Regression Model
Import from SKLearn, Assign random_state parameter,Random_state parameter = 1, Fit the model using training data
Make a prediction using the testing data, Generate Confusion Matrix, Print Classification Report


### Linear Regression
Split data for train and test, Split data into Numerical and Categorical features, Create data transformation,pipeline, Fit the training data,Transform the training and testing data,Fit the data to the Linear Regression Model, Create a function to distribute our plot, Plot the predicted values using training data compared to the actual values of the training data

### Define Polynomial Regression Model 
Model Evaluation: Define a function to evaluate the model performance, typically using metrics like Mean Squared Error (MSE), R-squared.
Predict Data: Use the model to predict outputs using both the training and testing data.
Parameter Tuning: Tune the hyperparameters of the polynomial regression model. This can involve techniques like grid search or randomized search to find the best combination of hyperparameters.
Function for Hyperparameter Optimization: Define a function that takes in the model, data, and hyperparameter grid and returns the best set of hyperparameters.
Fit the Data to Polynomial Regression Model: Fit the training data to the polynomial regression model using the best set of hyperparameters.
Test for Training Accuracy: Evaluate the model's performance on the training data, typically by calculating metrics like MSE or R-squared.
Plot Predicted Values vs. Actual: Visualize the predicted values against the actual values to assess the model's performance graphically.

</details>

<a name="Conclusion"></a>
## Conclusion
The best model for predicting weekly sales is Polynomial Regression. This model can provide information that helps business managers identify and understand weaknesses in business planning.
The Marketing Division should increase advertising during the weeks after Christmas and before Thanksgiving.
Need additional people from the Logistics division in November-December because sales increased significantly compared to other months. Re-stock goods sufficiently on weekdays to minimize production costs.

</details>

<a name="Future_Improvements"></a>
## Future_Improvements
Try a different pre-processing approach and see if model performances change.

Bring in new sources of data to see if there are significant differences on time factor used

</details>
