# AmazonProductsPricePrediction

Conclusion

**Prediction of discounted price of products:
 
•	Ridge Regression
a.	TFIDF Features:

Best Parameters: Alpha = 100
Best Score: 0.5311
Train MSE: 1021.21, Train R²: 0.7100
Test MSE: 1486.46, Test R²: 0.5741

b.	Count Vector Features:

Train MSE: 754.00, Train R²: 0.7858
Test MSE: 1854.59, Test R²: 0.4686

•	Random Forest Regressor

a.	Count Vector Features:

Train MSE: 8.13, Train R²: 0.9977
Test MSE: 67.88, Test R²: 0.9805

b.	TFIDF Features:

Train MSE: 8.10, Train R²: 0.9977
Test MSE: 73.35, Test R²: 0.9790




Observations:
•	The Random Forest Regressor significantly outperforms the Ridge Regression model in terms of Mean Squared Error (MSE) and R² (Coefficient of Determination) for both training and testing sets, regardless of the feature extraction method used.
•	Ridge Regression shows higher MSEs, indicating less accurate predictions compared to Random Forest.
•	For both models, the choice between TFIDF and Count Vector features seems to affect the performance, but the impact is more pronounced in the Ridge Regression model. The Ridge Regression model performs better with Count Vector on the training set but worse on the test set, suggesting that TFIDF might be a better choice for generalization.
•	For critical applications on this dataset, Random Forest should be considered due to its superior performance metrics. However, for applications where computational efficiency is key, Ridge Regression might be more suitable despite its lower accuracy.

**Predicting Sentiment of products:
 
•	Multinomial Naive Bayes
a.	Using Count Vector:

Training Data Performance: Accuracy of 71%, with precision, recall, and F1-score varying significantly across classes.
Test Data Performance: Accuracy of 69%, with generally lower precision, recall, and F1-scores compared to training data.
Average ROC Values: 0.8023 (Train), 0.7049 (Test).

b.	Using TFIDF:

Training Data Performance: Accuracy of 78%, higher than with Count Vector.
Test Data Performance: Accuracy of 78%, consistent with training data.
Average ROC Values: 0.7919 (Train), 0.7543 (Test).

•	Logistic Regression
a.	Using TFIDF:

Training Data Performance: Accuracy of 85%, higher than MNB.
Test Data Performance: Accuracy of 84%, indicating good generalization.
Average ROC Values: 0.9178 (Train), 0.8551 (Test).

b.	Using Count Vector:

Training Data Performance: Accuracy of 89%, higher than MNB and Logistic Regression with TFIDF.
Test Data Performance: Accuracy of 82%, slightly lower than training but still high.
Average ROC Values: 0.9642 (Train), 0.8159 (Test).

Observations:
•	Logistic Regression shows a more consistent performance between training and test data compared to MNB, suggesting better generalization capability.
•	Logistic Regression tends to have higher precision, recall, and F1-scores, especially with Count Vector. This indicates a stronger capability in correctly classifying different classes, particularly in multiclass settings.
•	The choice of feature extraction method (Count Vector vs. TFIDF) affects the performance of both models. Logistic Regression benefits more from the Count Vector method, while MNB shows relatively less variation in performance between the two methods.
•	Given its overall superior performance, Logistic Regression appears to be a more robust and accurate model for this particular text classification task.
