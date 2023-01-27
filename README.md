# Bank customer churn analysis




Encoding Categorical data
1.	Replacing values: Replacing categories with desired numbers.
2.	Encoding labels: It will convert each value in a column to a number between 0 to n_categories .The disadvantage of the label encoding is that it may give more weight to the high number . 
(US as 8 and AS as 1 it may give more weight to US).
3.	One- hot Encoding: The strategy is to convert each value into a new column and assign a 1 or 0 value to the column. Advantage is it does not give weight.
The disadvantage is curse of dimensionality.
4.	  Binary Encoding:  First the categories are encoded as ordinal, then those integers are converted into binary code, then the digits from the binary string are split into separate columns. This encodes the data in fewer dimensions than one-hot.

Standardization
Standard Scaler : It follows standard normal distribution. It makes mean 0 and scales the data to unit variance. 
If there are outliers Standard scaler may not give balanced feature scales, due to influence of outliers when computing mean and standard deviation. It may result in shrinkage the range of the feature values.
Min max scaler: It scales all the data features in the range 0,1 or in -1,1 if there are negative value in the dataset.

Robust Scaler: It scales features using statistics that are robust to outliers. This method removes the median and scales the data in the range between 1st quartile and 3rd quartile. i.e., in between 25th quantile and 75th quantile range. This range is also called an Interquartile range. 
The median and the interquartile range are then stored so that it could be used upon future data using the transform method. If outliers are present in the dataset, then the median and the interquartile range provide better results and outperform the sample mean and variance. 
RobustScaler uses the interquartile range so that it is robust to outliers.



SVM: 
Larger margin
Lower misclassification and error rate.
Hyperparameters
1.	Gamma (Not in linear) : Low value indicates large similarity radius which results into more points grouped together. High values, the points should be very close to each other to be in same group.
2.	C is hyper or regularization parameter of svm which controls the error the strength of regularization is inversely proportion If c is small the penalty for misclassified point is low and decision boundary with large margin is chosen. If c is large then margin will be small as svm tries to minimize the number of  misclassified data points.
