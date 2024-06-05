We are tasked to identify phone calls with ML. 

To do this we shall use the Random Forest Classifier.



A Random Forest classifier is well-suited for classifying spam calls for several reasons:

Robustness to Overfitting: Random Forests are composed of multiple decision trees, and by averaging their predictions, they reduce the risk of overfitting that individual trees might face. This robustness is crucial when dealing with potentially noisy and diverse spam call data.

Handling High-Dimensional Data: Spam call datasets often contain a large number of features (e.g., call duration, frequency of calls, caller ID patterns). Random Forests can effectively handle high-dimensional data and identify the most relevant features for classification.

Non-Linearity: Random Forests can capture complex, non-linear relationships between features and the target variable (spam or not spam). This is important because the patterns that differentiate spam calls from legitimate calls might be intricate and not easily separable by linear methods.

Feature Importance: Random Forests provide a measure of feature importance, helping to identify which features are most indicative of spam calls. This can be valuable for refining the model and understanding the characteristics of spam calls.

Scalability: Random Forests are scalable and can handle large datasets efficiently. This is essential for practical applications, as the volume of call data can be substantial.

Robustness to Missing Data: Random Forests can handle missing values effectively, which is beneficial because real-world data often contains gaps or incomplete records.

Versatility and Ensemble Learning: As an ensemble learning method, Random Forests aggregate the predictions of multiple decision trees, increasing the overall accuracy and robustness of the model. Each tree in the forest votes on the classification, and the majority vote determines the final output, which typically results in a more reliable prediction.

Practical Example
Consider a spam call classification scenario with features such as:

Call duration
Number of calls per day
Caller ID prefix
Time of day the call is made
Whether the number is in the contact list
Frequency of similar calls received
A Random Forest classifier would build multiple decision trees using random subsets of these features and data samples. Each tree would make a prediction on whether a call is spam or not, and the final classification would be determined by aggregating these predictions.


As such, we will use keras' random forest classifier, specify that we want 100 estimators.
