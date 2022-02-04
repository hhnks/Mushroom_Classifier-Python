# Mushroom_Classifier-Python

My postgraduate studies project:
A classifier to determine whether a mushroom is poisonous or edible

In this project, a classifier was built to determine if a mushroom is poisonous based on its external appearance characteristics. An attempt was also made to interpret the classifier using the `DALEX` package and to explain the prediction for a selected observation.

The data was donated in April 2021 on the UCI Machine Learning Repository (http://archive.ics.uci.edu/ml/datasets/Secondary+Mushroom+Dataset) and contains 61069 hypothetical fungal observations that were randomly simulated from the popular Mushroom Data Set (1987), which contains information on 173 fungal species. The dataset was created as part of the thesis work of D. Heider and G. Hattab at the University of Marburg.

The set consists of a `class` target variable determining whether the mushroom is *poisonous* or *edible* and 20 variables.


## What's interesting?

- **Label encoding**: Dataset includes mostly categorical variables. Due to the fact that machine learning algorithms perform better with numerical inputs, categorical encoding was needed. Because of the rather large number of classes in the qualitative variables, Label Encoding was used because One-Hot Encoding would generate a very large number of predictors. Encoding was performed with `Sci-Kit Learn`.

- **`DALEX`**: The project was an opportunity for me to try out the `DALEX` library which includes methods for the exploration, explanation and visualization of machine learning models. Recently, there is a growing interest in the topic of XAI (Explainable artificial intelligence) and the development of new XAI methods. This is due to the increasing demand for interpretation of "black box" models. In my work, I've visualized the differences between 3 models and i showed how each model deals with classification of selectd observation (example histogram for Logistic Regression model below). 

![obraz](https://user-images.githubusercontent.com/84125127/152532931-8d33db5b-561f-41e8-b636-382438c33b79.png)

## Workflow of a project

Project is divided into parts:

1. Introduction <br />
2. Data description <br />
3. Preparing data for modeling <br />
  3.1. Importing Libraries and Dataset <br />
  3.2. EDA <br />
 &nbsp;&nbsp;   3.2.1. Continuous Variables <br />
   &nbsp;&nbsp; 3.3.2. Qualitative variables <br />
  3.3. Data Cleaning (NAs) <br />
 &nbsp;&nbsp;   3.3.1. Label Encoding <br />
 &nbsp;&nbsp;   3.3.2. Checking correlation between variables <br />
  3.4. Split Dataset to Train and Test sets <br />
4. Modeling <br />
  4.1. <br />
 &nbsp;&nbsp;   4.1.1. Logistic regression <br />
 &nbsp;&nbsp;   4.1.2. Support vector machine (SVM) <br />
 &nbsp;&nbsp;   4.1.3. Random Forest <br />
  4.2. Cross-validation <br />
 &nbsp;&nbsp;   4.2.1. Logistic regression <br />
 &nbsp;&nbsp;   4.2.2. Support Vector Machine (SVM) <br />
 &nbsp;&nbsp;   4.2.3. Random Forest <br />
  4.3. Summary <br />
  4.4. Interpretation of models with `DALEX` <br />
Conclusions <br />

## Jupyter Notebook 6.3.0

Python libraries:
* `NumPy`
* `Pandas`
* `Matplotlib.pyplot`
* `Seaborn`
* `SciKit-Learn`
* `DALEX`
