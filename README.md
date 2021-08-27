# Wine-Quality-Prediction-Using-Regression

The data set was Categorical, but for applying regression we need numerical data, so I applied ** preprocessing techniques** which are following:
1) OneHot Encoding
2) TfidVectorizer
After this HotEncoding and TfidVectorize data is ready to merge, for merging we used hstack( ) our both vector data are merged row wise because we have the same number of row in both vectors but different number of columns.

**Model selection**
After deep Analysis, I have selected the Ridge Regression Model over Linear Regression model for predicting the quality of wine on given datasets. Because the number of independent variables are many in given data set, as well as we are not sure which of the independent variables influences dependent 
variable. In this kind of scenario, ridge regression plays a vital role than linear regression. Ridge Regression is a technique for analyzing multiple regression data that suffer from multicollinearity. When multicollinearity occurs, least squares estimates are unbiased, but their variances are large so they may be far from the true value. By adding a degree of bias to the regression estimates, ridge regression reduces the standard errors. It is hoped that the net effect will be to give estimates that are more reliable.

**Hyperparameters tuning**
We have used Ridge Regression, so for getting better result we change the values of some parameters to obtain the better result. 
We tune “Alpha” value in Ridge( ) function. We started putting values such as 0.06, 0.1 but when we are putting less values the result of Ridge Training and Testing score were less, so I decided to put higher values such as 0.8, 0.9 and I got very less score for Ridge Training and Testing because increasing “alpha” means pushing the Ridge Regression to be more robust against overfitting, but might be getting larger training error. After changing the alpha values again and again Model got the right value which was alpha=0.201 in which score of RidgeTraining and Testing was good. Furthermore, I have applied the different values of “max_feature” in TfidfVectorizer( ) function such as top 100 or top 200. After doing tuning on max_feature parameter by applying different values, Model found the right value of max_feature which was 300 by changing the value into 300, our Ridge Training and Testing score got improved.

**Results**

After applying Ridge Regression model on our given data sets, the model predicted the values having good Ridge Training and Testing Score. For achieving this score, I applied some configuration such as pre-processing on data and then found out better score of Ridge regression.

RIDGE_TRAIN_SCORE:
0.949

RIDGE_TEST_SCORE:
0.813
