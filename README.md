# Credit-Card-Application--Classification-ML-Project

Dataset
For our Project we took two datasets and for Classification, we took the dataset of Credit Card Application from Kaggle. There were two CSV files: Credit_card_application.csv and credit_record.csv which we combined to create one dataset.

These are the insights of the combined dataset before pre processing

There were total 21 columns
There were 438558 instances (rows)
There were 6 Categorical columns.
There were 3 Oridanl Columns.
5%-10% of the dataset was missing.
The dataset was huge. We imputed the dataset with median and mean after checking the skewness of the dataset. We visualized the dataset using bar charts, histogram and pie charts.

Cleaning Process:
The dataset was huge therefore, it took a lot of preprocessing. The values were imputed on the basis of mean and median after visualizing and checking the skewness. We imputed categorical/ordinal values on the basis of count. In the end, we took a sample of 3000 rows out of 38558 dataset because it was huge.

Classification models:
We ran different types of classification models such as:

Knn Classifier:
We ran Knn Classifier on Grid Search and the best parameters that we received KNeighborsClassifier(metric='manhattan', - n_neighbors=10)
we received the train and test scores as follows:
Train score: 0.7817
Test score: 0.7933
Logistic Regressor:
We ran Logistic Regressor on Grid Search and the best parameters that we received is - GridSearchCV(cv=5,estimator=LogisticRegression(max_iter=1000, random_state=0), param_grid={'C': [0.01, 0.1, 1, 10, 100]}, scoring='roc_auc')

we received scores as follows:

accuracy_score: 0.815

roc_auc_score: 0.46424031393356546

Linear SVC:
We ran Linear SVC on Grid Search and the best parameters that we received is Best parameters: {'C': 0.001, 'gamma': 0.001}
Best cross-validation score: 0.78.
we received the train and test scores as follows:
Train score: 0.7779
Test score: 0.8150
SVC Kernel Poly:
We ran GridSearchCV on SVC kernel Poly in order to find the best parameters. We received these as follows:
Best parameters: {'C': 0.001, 'gamma': 0.001}
Best cross-validation score: 0.78
SVC rbf:
We ran GridSearchCV on SVC rbf in order to find the best parameters. We received these as follows:
SVC(C=0.001, gamma=0.001, max_iter=450)
best score: 0.7779166666666667
SVC Kernel - linear:
We hyper tuned this model in order to find the best parameters

best score: 0.7779166666666667
Best parameters: {'C': 0.001, 'gamma': 0.001}
Decision Tree :
We ran Grid Search on Decision Tree in order to find the maximum depth and best parameters

Best Parameters: {'criterion': 'gini', 'max_depth': 3}
Accuracy on training set: 0.776
Accuracy on test set: 0.812
We have KNN classification, Logistic Regression, Linear Support Vector Machine, Kerenilzed Support Vector Machine (rbf, poly, and linear), Decision Tree Classifier. The best accuracy score as per recall is for SVC POLY with hyperparamter tuning.\

Confusion Matrix [[ 57 10] [427 106]]

106 good clients were predicted correctly

We have avoided visualization for the models as it's breaking the code¶
