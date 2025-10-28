Model Evaluation Report
Objective
To train and evaluate Machine Learning models to classify URLs as safe (label 0) or phishing (label 1), based on the dataset_features_final.csv dataset (with 23 features).
1. Models Tested
Two machine learning models were trained and evaluated using data from the file dataset_features_final.csv. Below is a brief description of how each one operates:
•	Logistic Regression: This is a statistical, linear model primarily used for binary classification tasks (predicting one of two outcomes, like 0.0 or 1.0). It works by estimating the probability that a given input belongs to a specific class. It does this by fitting the data to a logistic (or sigmoid) function, which maps any real-valued number into a value between 0 and 1.
•	Random Forest: This is an "ensemble" learning method, meaning it combines multiple models to get a better prediction. It operates by constructing a multitude of "decision trees" during training. When making a prediction, each tree in the "forest" provides a "vote" for a class. The model outputs the class that receives the majority of the votes. It is a powerful, non-linear model known for its high accuracy.

2. Model Selection
Selected Model: Random Forest
Reason for Selection:
Based on the evaluation results, the Random Forest model was selected due to its superior and perfect performance on the test dataset.
•	Performance Comparison: The Random Forest model achieved an overall Accuracy of 1.00 (100%), whereas the Logistic Regression model only achieved 0.98 (98%).
•	Detailed Analysis (Class 1.0): The most significant issue with Logistic Regression was its ability to identify the minority class (class 1.0). It only achieved a Recall of 0.83, meaning it missed 17% of all actual 1.0 cases. In contrast, the Random Forest achieved a Recall of 1.00 for this class.
•	Conclusion: The Random Forest model achieved perfect scores (1.00) across all metrics (Precision, Recall, F1-score) for both classes, demonstrating flawless classification on this dataset.

3. Detailed Results (Random Forest Model and Logistic Regression model)
Below is the detailed classification report for the selected Random Forest model and Logistic Regression model:
 
###Random Forest###
```
              precision    recall  f1-score   support

         0.0       1.00      1.00      1.00     59695
         1.0       1.00      1.00      1.00      4898

    accuracy                           1.00     64593
   macro avg       1.00      1.00      1.00     64593
weighted avg       1.00      1.00      1.00     64593
```
###Logistic Regression###
```
              precision    recall  f1-score   support

         0.0       0.99      1.00      0.99     59695
         1.0       0.94      0.83      0.88      4898

    accuracy                           0.98     64593
   macro avg       0.96      0.91      0.94     64593
weighted avg       0.98      0.98      0.98     64593
```
