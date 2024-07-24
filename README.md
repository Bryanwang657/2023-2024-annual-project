# Machine-Learning-Projects
This is a repository contains my final project for ML656

## Business Data and Understanding

The National Center for Immunization and Respiratory Diseases (NCIRD), in collaboration with the National Center for Health Statistics (NCHS) and the Centers for Disease Control and Prevention (CDC), aims to evaluate past immunization survey data from 2009. The objective is to predict which individuals, based on specific demographic profiles, are likely to receive vaccines in the upcoming year. By developing a predictive model with a high level of confidence, these organizations can better manage vaccine production, reducing the costs associated with overproduction or underproduction. Additionally, understanding the likelihood of vaccine refusal will help in creating targeted literature to address misinformation about the risks associated with the H1N1 and seasonal flu vaccines.

## Target Variables and Data Collection

The target variables in this study are binary indicators of whether an individual will voluntarily receive an H1N1 or a seasonal flu vaccine. Data was collected via random-digit-dialing surveys conducted in U.S. households. This results in two distinct target variables: one for the H1N1 vaccine and one for the seasonal flu vaccine.

## Data Preparation

The dataset is comprehensive and aligns well with the business problem. Both training and testing data are available in a feature vector format, facilitating straightforward preprocessing. The data includes responses to various survey questions about H1N1 concerns, knowledge, behavioral patterns, medical conditions, healthcare recommendations, and demographic information such as age, education, race, income, and employment status.

## Preprocessing Steps

To prepare the data, I handled null values by replacing them with mode values and removed outliers to prevent skewed results. Given the randomized nature of the survey across the U.S., the data should be representative of the broader population.

## Modeling Approach

The goal is to create a model predicting the likelihood of vaccine uptake based on demographic criteria. This involves supervised learning since the dataset is complete. The survey responses include binary, numeric qualitative, and categorical variables. Various modeling techniques were applied, including logistic regression, gradient boosting classifier, decision tree, optimized decision tree, random forest, optimized random forest, k-nearest neighbors, and ensemble modeling, all conducted using Python in Google Colaboratory.

Ensemble modeling was assumed to yield the best results by combining multiple models for greater accuracy. The performance of individual models was evaluated based on their Area Under the Curve (AUC).

## Evaluation and Deployment

The models were evaluated by comparing the AUC of each. AUC provides a robust measure of model performance by plotting the true positive rate against the false positive rate, offering a more reliable metric than accuracy alone. The dataset was split into 80% training and 20% testing data. Feature scaling was applied to normalize the data, and Lasso (L1-Regularization) was used for feature selection to avoid overfitting and enhance model robustness.

The Random Forest with Cross Validation emerged as the top-performing model, although it requires significant resources. Hence, the Gradient Boosting Classifier is recommended as a viable alternative due to its similar performance but lower resource demands.

## Implications and Future Considerations

The model aims to optimize vaccine production costs and assist in targeting educational efforts towards those hesitant about vaccines. However, while the model provides valuable insights, it is not a definitive solution for vaccine production issues. External factors, such as the impact of the COVID-19 pandemic, which began in 2020, could significantly influence vaccination behavior and were not accounted for in the 2009 data.

