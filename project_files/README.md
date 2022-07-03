Insurance Purchase Prediction - AllState Online Car Insurance Customers

As customers shop for a car insurance policy, they visit websites of multiple insurance companies to generate a number of quotes with different coverage options before purchasing a plan. Once the customer arrives at choosing their quote, they may choose many different options before arriving at their ultimate purchase option. Each revision that’s required, increases the probability of losing the customer. Allstate Insurance would like to develop a predictive model that can predict the coverage plan that the customer would eventually buy. If the eventual purchase can be predicted sooner in the shopping window, the quoting process is shortened and the company is less likely to lose the customer's business. 

MODEL BUILDING APPROACH
The key steps followed to build a model for each of the 7 product vector were:
1)	Training a basic model based on 3 different classifiers - Random Forest, Gradient Boost and XG Boost. For binary vectors (B and E), a Logistic Regression classifier was also evaluated.
2)	Applying 60 iterations of Randomized Search CV to determine performance of different hyperparameter combinations on the training dataset.  
3)	Applying each of the 60 sets of hyperparameters on the validation set and measuring micro accuracy.
4)	Choose the best set of hyperparameters as the one that performs most consistently across the training and validation set. 
5)	Based on these hyperparameters, compare the performance of different classifiers on the test set to then choose the best classifier for each vector.

NOTEBOOKS
04_Pre_processing_and_training_data_development-final.ipynb

This notebook performs the following tasks. There are detailed step by step instructions in the notebook on how to perform these tasks.
1) Converts the dataset into a wide form. 
2) Extract all customer and product information from quote 1 and 2.
3) Pre-process and Transform data. 

05_Modelling_final.ipynb

This notebook trains the model for each vector, makes predictions on the test set and scores the performance of each model. The step-by-step instructions are contained in the notebook.

OTHER FILES

1) Project Report: Capstone project_report_amit_kukreja.pdf
2) Model Metrics: Capstone project_model metrics files.pdf
3) Project Presentation: Capstone_project_presentation_amit_kukreja.pdf
