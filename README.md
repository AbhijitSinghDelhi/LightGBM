# LightGBM
LightGBM Boosting

Explanation of the Code
Load Data:

load_breast_cancer() loads the breast cancer dataset, which contains features like mean radius, mean texture, mean perimeter, etc., and the target variable indicating whether the tumor is malignant (1) or benign (0).
Split Data:

train_test_split splits the dataset into training and testing sets.
Create Dataset for LightGBM:

lgb.Dataset creates a LightGBM dataset from the training and testing data.
Set Parameters:

The parameters for the LightGBM model are set. boosting_type specifies the boosting algorithm, objective defines the loss function for binary classification, metric defines the evaluation metric (binary log loss in this case), num_leaves controls the complexity of the tree, learning_rate controls the step size, and feature_fraction specifies the fraction of features to be used.
Train Model:

lgb.train trains the model using the specified parameters, training data, and validation data.
Make Predictions:

The model makes predictions on the test set using the best iteration found during training.
Predictions are converted to binary (0 or 1) based on a threshold of 0.5.
Evaluate:

The accuracy and ROC AUC score of the model are calculated using accuracy_score and roc_auc_score.
