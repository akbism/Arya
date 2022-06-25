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
I started with very high level descriptive analysis of the training dataset and understand the data.
Then, I split the training dataset in two parts - training and validation (4:1 ratio) so that there was no training-validation data leakage in the process.
Then, I carried out detailed exploratory data analysis (EDA) of the training dataset as given below:
- Analysis of missing value - none found
- Analsis of columns with little information 
- Analysis of multi-collinearity
- Outlier detection
- Univariate analysis
- Segmented univariate analysis
The EDA could provide me some idea about the relevant features. However, I didn't finalized the features yet as there can be non-linear dependencies. <br><br>
**Outcome of EDA**: Absolutely redundant features and list of outliers (to be removed from the training dataset before model training)

### Model Training
First of all, I removed the redundant features and removed the outliers from the training dataset.
Next, I set a binary classification experiment environment to test multiple classification models on this dataset. 
Next, I selected the best out-of-box classification model performing on the given dataset. 
Then, I finetuned the model and extracted the feature importance.
Then, I selected the top final features on the basis of feature importance and shapley value. 
The selected model is further finetuned after considering the selected features.
Finally, I got the fine-tuned classification model, which would be used for model inference. 

### Model Inference
The fine-tuned model is used to predict the 'Y' value of the given dataset.



