<h2 align="center">credit_default_prediction</h2>
<br>
<h3> 📄 Introduction</h3>
This project aims to develop a credit default prediction model, leveraging a dataset of historical customer records of both defaulters and non-defaulters. The primary objective is to accurately predict the probability of a user defaulting on credit, based on a range of relevant features extracted from the dataset.
    
The response variable used is "Default", where a value of 1 indicates that the customer defaulted and a value of 0 represents that the customer did not default.

A number of techniques such as regression, prinicpal component analysis are used to choose a model that gives the lowest mean absolute error. The final chosen model for this dataset is weighted logistic.
</br>
<h3>🔨 Tools and Techniques used</h3>

- R
- R Studio
- Regression (Logistic, Weighted logistic, Lasso, Partial Least Square)
- Principal Component Analysis

<h3> 🔭 Objective</h3>

- Predict the credit default probability of a user. 

<h3>🔗 Contact Me</h3>
 <a href='https://www.linkedin.com/in/aishwarya-ucd/'><img align='center' alt="linkedin" src="https://raw.githubusercontent.com/shahbajjamil/Social-Meadia-Icons/master/Icons-logos/linkedin-circle.png" height='26px'/></a>



<h3>🔄 Model Selection Steps</h3>

- The first step is pre-processing data. Some of the steps involved in pre-processing are: 
  1. Converting numerical variables to correct format 
  2. Stripping away characters from ‘term’ column to make it suitable for use in regression 
  3. Checking for NAs 
  4. Replacing NAs with mean value of columns based on the frequency of occurence 
  5. Converting categorical variables to dummy

- Then, the scatter plots of all the numerical variables are constructed to find if there is a need of variable transformation. All the plots showed random or linear pattern.

- The first model applied is logistic regression as this is a clear classification problem. The training data is further divided into train and test for this method. The MAE for logistic using the test data from training set as well as the actual test set is calculated. The MAE for actual test set is 1929.
- The next model is lasso regression. There were 14 significant variables as lasso output and the MAE value was 3579.
- The next model is logistic but using Principal component analysis. PCA is a good approach to apply for dimensionality reduction. And after fitting PCA and using actual test data, MAE was 1344.
- When fitted a PLS model, it performed bad because these are best for continuous variables. PLS assumes a linear relationship between the independent and dependent variables. While this assumption is reasonable for many regression problems, it may not hold for classification problems, where the relationship between the independent and dependent variables may be more complex and nonlinear.
- The next model was weighted logistic regression. The data is imbalanced with approx 50% more instances of 0 than 1 in the default column. Hence applied weighted logistic regression. I have give weight of 50 to “0” and 1 to “1” in the regression. The error is 0.07 and the MAE is 1226. This is the least MAE. And hence this is the final model. This model has the least mean absolute error and is a good fit for this imbalanced datset.
