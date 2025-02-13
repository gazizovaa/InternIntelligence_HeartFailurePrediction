# InternIntelligence_HeartFailurePrediction
Source: https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction/data
</hr>
<h3>About Dataset</h3>

This project explores the use of machine learning to predict the likelihood of heart disease based on medical records. By leveraging various features such as age, cholesterol levels, blood pressure, and heart-related tests, the goal is to build a model that can accurately predict whether an individual has heart disease or not.
</hr>
 Table of Contents

1. [Introduction](#introduction)
2. [Dataset](#dataset)
3. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
4. [Machine Learning Model](#machine-learning-model)
5. [Model Evaluation](#model-evaluation)
6. [Conclusion](#conclusion)
</hr>
<h3>Introduction</h3>

Heart disease is one of the leading causes of death worldwide. However, early diagnosis can significantly improve treatment outcomes. This project uses a dataset containing medical information of individuals to predict the likelihood of heart disease. The objective is to identify which factors most influence the occurrence of heart disease and to build a machine learning model capable of predicting it. The dataset consists of multiple attributes relevant to heart disease diagnosis. Key features include the patient's age, sex, cholesterol levels, blood pressure, and exercise habits, among others. The target variable, **HeartDisease**, indicates whether an individual has heart disease (1) or not (0).

The features in the dataset are:

- **Age**: The patient's age

- **Sex**: Gender of the patient

- **ChestPainType**: Type of chest pain experienced (typical angina, atypical angina, non-anginal pain, or asymptomatic)

- **RestingBP**: Resting blood pressure (in mm Hg)
  
- **Cholesterol**: Serum cholesterol (in mg/dl)
  
- **FastingBS**: Fasting blood sugar level
  
- **RestingECG**: Electrocardiogram results

- **MaxHR**: Maximum heart rate achieved
  
- **ExerciseAngina**: Whether the patient experiences angina during exercise (Yes/No)
  
- **Oldpeak**: Depression induced by exercise relative to rest
  
- **ST_Slope**: Slope of the peak exercise ST segment
  
- **HeartDisease**: The target variable (0 for no heart disease, 1 for heart disease)
</hr>
<h3>Exploratory Data Analysis (EDA)</h3>

The initial step in the analysis was to examine the dataset, check for missing values, and explore the statistical summary of the data. This helped me understand the distribution and relationships of various features before applying machine learning techniques. I cleaned the dataset by renaming columns for consistency. For example, I renamed columns like "ChestPainType" to "Chest_Pain_Type" to ensure uniformity. After renaming, I explored the dataset to see how many unique values each feature contained and to understand the distribution of heart disease cases. One of the key aspects of EDA was visualizing relationships between different variables. For instance, I created a pairplot to show the relationship between various features of the dataset, with the Heart_Disease column used to distinguish between healthy and diseased individuals. I plotted histograms to see how the distribution of heart disease varied by gender, and I created a pie chart to show the different types of chest pain associated with heart disease.

Outlier detection was also an important part of my analysis. I used box plots to identify outliers in key features such as age, cholesterol, resting blood pressure, and heart rate. These visualizations helped me understand the distribution of data and informed the preprocessing steps for the machine learning model.
</hr>
<h3>Machine Learning Model</h3>

After performing EDA, I split the dataset into features (X) and the target variable (y). I separated the target variable, Heart_Disease, from the other features to create the prediction target. Then, I divided the data into training and testing sets, with 80% used for training and 20% for testing. This ensured that the model was trained on a large portion of the data and could be evaluated on unseen data. For preprocessing, I handled missing values by imputing the missing data using the median for numerical features and the most frequent value for categorical features. I also scaled the numerical features using standard scaling to normalize the data and applied one-hot encoding to the categorical features. With the preprocessed data ready, I built a logistic regression model. Logistic regression is a suitable classification algorithm for this problem, as it outputs probabilities that indicate the likelihood of an instance belonging to a particular class (heart disease or not). I trained the model on the training dataset and evaluated its performance using the test dataset.
</hr>
<h3>Model Evaluation</h3>

After training the model, I evaluated its performance using several metrics. These metrics included accuracy (the proportion of correct predictions), precision (the proportion of positive predictions that are correct), recall (the proportion of actual positives that are correctly identified), and the F1-score (a harmonic mean of precision and recall). Additionally, I examined the confusion matrix, which provided a detailed breakdown of the model's predictions, including true positives, true negatives, false positives, and false negatives. This matrix helped me understand where the model was making errors. I visualized the confusion matrix using a heatmap to provide an intuitive understanding of the model's performance, with labels indicating whether the predictions were correct or incorrect.
</hr>
<h3>Conclusion</h3>

This project demonstrated the power of machine learning in predicting heart disease based on medical attributes. The exploratory data analysis revealed important insights into the dataset, including key relationships between different features and heart disease. The logistic regression model performed reasonably well in predicting heart disease, but future work could focus on exploring other classification algorithms or improving the feature engineering process to enhance model accuracy.
