# Assignment - Data Scientist
## Task
Binary Classification - Do an exploratory analysis of the dataset provided, decide on feature selection, preprocessing before training a model to classify as class ‘0’ or class ‘1’.

## Instructions:
1. Upload the assignment to github/gitlab (Share the repository link if it’s public or send invite if private)
or mail the assignment 
2. Split the training data in training and validation set with ratio of 4:1 to evaluate performance of the model on validation set.

## General Approach
The dataset doesn't have the named features. Hence, we can't analyse as per the business / domain.
### Exploratory Data Analysis
A high level descriptive analysis of the training dataset was carried out to understand the data.
Then, the training dataset was split in two parts - training and validation (4:1 ratio) so that there was no training-validation data leakage in the process and finally, an estimate for the model performance can be calculated.
Then, a detailed exploratory data analysis (EDA) of the training dataset was carried out as given below:
- Analysis of missing value - none found
- Analsis of columns with little information 
- Analysis of multi-collinearity
- Outlier detection
- Univariate analysis
- Segmented univariate analysis
The EDA could provide some idea about the relevant features. However, the features were not finalized yet as there could be non-linear dependencies. <br><br>
**Outcome of EDA**: Absolutely redundant features and list of outliers (to be removed from the training dataset before model training)

### Model Training
First of all, the redundant features and the outliers were removed from the training dataset.
Next, a binary classification experiment environment was set to test multiple classification models on this dataset. 
Next, the best out-of-box classification model was selected as per performance on the training dataset. 
Then, the model was finetuned and the feature importance was extracted.
Then, the top final features set was selected on the basis of feature importance and shapley value. 
The selected model was further finetuned after considering the selected features.
Finally, I got the fine-tuned classification model, which would be used for model inference. 

### Model Performance Analysis
The validation dataset was used to estimate the model performance. 
The evaluation metrics - precision, recall, f1-score and AUC - were used to compare and select the model.

### Model Inference
The fine-tuned model is used to predict the 'Y' value of the given dataset.

### Notes:
1. As the dataset is slightly imbalanced, Hence SMOTE technique was used to balance the dataset. 
2. StratifiedKFold strategy was used for cross validation.

