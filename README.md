# Predicting-Loan-Defaulters-and-Interest-Rate

We did a project on Interest Rate and Loan Default Prediction using Python and Spark for our IST 718: Big Data Analytics coursework. For this project, we analyzed Lending Club’s dataset consisting of 151 features and 2.2 million rows. The dataset ranged from 2007 - 2018. 

Lending Club is a marketplace for loans that match the loan borrowers with the investors. We have obtained the data from Lending Club’s website for our analysis. 

**Python Libraries:** Pandas, Numpy, Pyspark, Matplotlib, Seaborn


**Problem & Objectives:**
1. We aim to predict the Interest rate based on the financial history of loan borrowers. 
2. Many loans aren’t completely paid off on time resulting in borrowers defaulting on their loan. So, we developed an algorithm that predicts if the loan will be paid off on time or not. 


**Data Cleaning and Transforming:**
Using our domain knowledge, we first extracted 37 features out of 151 features for our analysis. Then, we checked for missing and null values in our dataset. We converted data types of our features and changed formats of our date and time columns. We also renamed all our columns so that the dataset is more interpretable.


**Exploratory Data Analysis:**
We started analyzing the data by using visualization graphs and plots. We used Matplotlib and Seaborn libraries for visualizing our data. We build various bar graphs, box plots, line graphs, and pie charts to answer important business questions. Later, we developed a correlation matrix to know the relationship between each variable.


**Machine Learning Models:**
For each of our models, we divided the data into three datasets i.e. Training data, Validation data, and Testing data. We created data pipelines using Pyspark for our ML models. Then, we fit the model on our training data, transform it on validation data, and finally, we tested it on our testing data. We also perform hyperparameter tuning using different parameters based on our model and we evaluated our model based on different evaluation metrics.


**ML Models used for Predicting Interest Rate:**

**1. Linear Regression:** For our regression model, we first created various Dummy variables to transform our categorical variables. We used various methods for selecting features for our model like correlation values. We performed hyperparameter tuning and tried many different Linear Models to get the best model based on RMSE and R2 value.
> Hyperparameter Used: Maximum Iterations
> Evaluation Metrics: RMSE = 1.239 and R2 = 0.942

**2. Decision Tree Regressor:** For our decision tree regressor model, we used a couple of hyperparameters. We again tried 4 models using different features and parameters and obtained our best model based on RMSE value.
> Hyperparameter Used: Maximum Depth and Maximum Bins
> Evaluation Metrics: RMSE = 1.0003


**ML Models used for Classifying Loan Defaulters:**

**1. Logistic Regression:** Our main issue while classifying data was Class Imbalance. Our data had 22% loan defaulters whereas 78% were non-defaulters. For this, we made use of Class Weight parameters in our logistic regression model. We created dummy variables for our model and also run cross-validations. We performed hyperparameter tuning and tried multiple models for obtaining the best model based on AUC values.
> Hyperparameter Used: Regularization Parameter and Elastic Net Parameter
> Evaluation Metrics: AUC Value

**2. Random Forest:** Here, we made use of Stratified Sample by Majority downsampling to overcome our Class Imbalance problem. Again, we performed hyperparameter tuning and tried multiple models for obtaining the best model based on AUC values.
> Hyperparameter Used: Maximum Depth, Number of Trees
> Evaluation Metrics: AUC Value


**Model Development:** We also developed a system where we can enter any person’s financial history and we can obtain the Interest Rate and the probability of that individual being a non-defaulter.


**Conclusion:**
1. Our analysis can be used by Lending Club to set different Interest rates for different individuals based on their financial history.
2. We can also predict if the loan will be paid off on time or not. Therefore, Investors can also leverage the model to know the chances of getting a return on their Investments. 
