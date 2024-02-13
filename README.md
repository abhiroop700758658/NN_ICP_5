# NN_ICP_5
Code Explanation Link: 

**Navie Bayes Problem:**

It loads the 'glass.csv' dataset using the pandas library. This dataset presumably contains information about different types of glass, with various features such as refractive index, sodium content, etc.

It separates the features (X) from the target variable (y). The features are stored in the DataFrame X, while the target variable (the type of glass) is stored in the Series y.

It splits the dataset into training and testing sets using the train_test_split function from scikit-learn. The training set comprises 70% of the data, while the testing set comprises the remaining 30%. This ensures that the model's performance can be evaluated on unseen data.

It instantiates a Naïve Bayes model (specifically Gaussian Naïve Bayes) using the GaussianNB class from scikit-learn. Naïve Bayes is a probabilistic classifier that assumes independence between features given the class.

It trains the Naïve Bayes model on the training data using the fit method. During this process, the model learns the statistical distributions of the features conditioned on the target variable.

It uses the trained model to make predictions on the testing set using the predict method. The model assigns a predicted class label to each instance in the test set based on its learned probabilistic model.

It calculates the accuracy of the model on the test set using the score method, which computes the proportion of correctly classified instances. Additionally, it generates a detailed classification report using the classification_report function, which includes metrics such as precision, recall, and F1-score for each class.

It prints out the accuracy of the model and the classification report to the console for analysis and interpretation.

Overall, this code demonstrates the process of training a Naïve Bayes model on the Glass dataset, evaluating its performance, and obtaining detailed metrics to assess its effectiveness in classifying different types of glass.


**Linear SVM Problem**

It loads the 'glass.csv' dataset using the pandas library. This dataset presumably contains information about different types of glass, with various features such as refractive index, sodium content, etc.

It separates the features (X) from the target variable (y). The features are stored in the DataFrame X, while the target variable (the type of glass) is stored in the Series y.

It splits the dataset into training and testing sets using the train_test_split function from scikit-learn. The training set comprises 70% of the data, while the testing set comprises the remaining 30%. This ensures that the model's performance can be evaluated on unseen data.

It instantiates a Support Vector Machine (SVM) model with a linear kernel using the SVC class from scikit-learn. This model is suitable for binary classification tasks and aims to find the optimal hyperplane that separates the classes in the feature space.

It trains the SVM model on the training data using the fit method. During this process, the model learns the relationships between the features and the target variable, adjusting its parameters to minimize classification errors.

 It uses the trained model to make predictions on the testing set using the predict method. The model assigns a predicted class label to each instance in the test set based on its learned decision boundary.

It calculates the accuracy of the model on the test set using the score method, which computes the proportion of correctly classified instances. Additionally, it generates a detailed classification report using the classification_report function, which includes metrics such as precision, recall, and F1-score for each class.

It prints out the accuracy of the model and the classification report to the console for analysis and interpretation.

Overall, this code demonstrates the process of training a linear Support Vector Machine (SVM) model on the Glass dataset, evaluating its performance, and obtaining detailed metrics to assess its effectiveness in classifying different types of glass.

**ACCURACY**

The linear Support Vector Machine (SVM) achieved better accuracy with an accuracy score of 0.6769 compared to the Naïve Bayes classifier, which had an accuracy of 0.3077.

There are several reasons why the linear SVM might have outperformed Naïve Bayes in this scenario:

Data Separability: SVM is particularly effective when classes are well-separated, and there exists a clear margin of separation between them. In such cases, SVM can find the optimal hyperplane to separate the classes, leading to better accuracy. Naïve Bayes, on the other hand, might struggle if the classes overlap significantly or if the assumption of feature independence is violated.

Model Complexity: Linear SVM is a more complex model compared to Naïve Bayes. It can capture nonlinear relationships between features through the use of kernels, even in its linear form. This increased complexity allows SVM to learn more intricate decision boundaries, which can improve its accuracy, especially in datasets with complex structures.

Handling of Features: Naïve Bayes assumes feature independence, which might not hold true in all datasets. If features are correlated or have complex relationships, Naïve Bayes might not capture these dependencies accurately. SVM, on the other hand, does not make such assumptions and can handle feature interactions more effectively.

Robustness to Outliers: SVM is generally more robust to outliers compared to Naïve Bayes. Outliers can significantly affect the performance of Naïve Bayes, especially if they influence the calculation of probabilities. SVM, with its margin-based approach, is less affected by outliers as it focuses on correctly classifying instances near the decision boundary.

Given these reasons, it's reasonable to expect that in this particular scenario, where the dataset might have complex relationships and the classes may not be well-separated, the linear SVM performed better due to its ability to handle such complexities and its robustness to outliers.





