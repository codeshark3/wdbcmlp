### 

Cancer is a leading cause of death worldwide, responsible for one out of every six fatalities.
 Breast cancer is the most common type, with around 2.90 million women diagnosed annually and claiming the lives of around 40,920 women in 2018.
Machine Learning (ML) can identify patterns in data and predict whether cancer is malignant or benign. 
ML uses features such as clump thickness, and uniformity of cell shape, age and family history, to improve the accuracy of breast cancer prediction.
This project is my implementation of the Breast Cancer Diagnosis framework proposed by Aamir et al. in 2022.
https://doi.org/10.1155/2022/5869529



### 

The project is divided into two parts:
1. Data collection and preprocessing
2. Model training and evaluation
 
### 

Data collection and preprocessing
 
The data is collected from UCI Machine Learning Repository. The dataset is split into training and testing sets.
This data is from a well curated dataset and has already been preprossed. Nans,missing values and outliers are removed.

###

Feature Extraction

Some features do not have as much importance as others. For example, the number of cells in the breast tissue might  not be as important as the clump thickness. These features must be removed from the dataset before training the model to reduce the dimensionality  and complexity of the data. This is done through recursive feature elimination, which removes features that are not significantly  correlated with the target variable. The features are then removed one by one, starting with the least important feature. Also correclation between features is checked to see if it is significant.
After extraction the data is scaled using z-score normalization. This is done to ensure that all features have a similar range of values. After normalization, the data is split into training and testing sets. The training set is used to train the model, while the testing set is used to evaluate the model's performance.

 
### 

Model training and evaluation
 
The model is trained using the training set. The model is then evaluated on the testing set using various metrics such as accuracy, precision, recall, and F1 score. In this project two models are used, a multilayer perceptron model and a random forest model with cross-validation. The results of the evaluation are presented in the following table:

[Table 1: Model performance metrics]
| Model | Accuracy | Precision | Recall | F1 Score |
|-------|----------|-----------|--------|----------|
| MLP | 92.1 | 0.92 | 0.92 | 0.92 |
| Random Forest | 92.9 | 0.93 | 0.93 | 0.93 |


### 

Conclusion
 
This project demonstrates the effectiveness of ML in breast cancer diagnosis. The model achieves high accuracy and precision, making it a valuable tool for early detection and treatment of breast cancer.The use of different hyperparameters may be required to optimize the model's performance. Further research and development in this area can lead to more accurate and effective diagnosis, ultimately improving patient outcomes.
