Data Overview
**EDA**
We analyze some statistic readings of data based on each feature.
It includes mean, max, min, count, std, 25% 50% 70%.
![image](https://user-images.githubusercontent.com/32372822/144900775-89f681d0-9d8c-4251-ae4a-2a6a255a2a06.png)
This is helpful when we preform data cleaning, feature engineering and feature selection.


K-Fold - Create subset of data to training, validation and testing before any data processing.
Data Leakage - Think about how model will see the real data. Some preprocessing can be done on testing data if those preprocessing can be done in reality.

**Check Data:**

**Imbalance** - What is the precentage of Positive/Negative of target feature - we need to handle imbalance.
Data is highle imbalanced that only 4% positive target feature
Solution - Adjust the weight of positive target feature

**Missing Data** - 0% missing data. 
If there is missing data, can dropna() or fillna() with avg values.

**Outliers** (not for testing data)- z-score can be used to label outliers mathmematically.
Apply CLT to the raw data and compute Normal distribution
The futher a data from the mean of the distribution, the more likely it is a outlier.
We can set threshold to define an outlier and get rid of them

**Correlations** - because correlation has impact on weighting of different features, we prefer to handle correlations by removal or PCA.
![image](https://user-images.githubusercontent.com/32372822/144901146-622786e3-f9ac-4620-a155-d9fe4e436913.png)


**Feature Engineering**
**I. MAke features clean and consist**
**I.1 Scaling **- std values of data in to a specific range. E.g. Revenue, spend, discount, etc.
**I.2 Encoding** - transform categorial data to numerial data - Gene of the movie, datetime of the movie.
**I.3 Discretization **- For interpretation
**I.4 Dimension Reduction** - For those with high correlations, e.g. Spend and Revenue, perform PCA to reduce the dimension while keeping the information.
**I.5 Handle text** - In this case, encoding with gene of the movie to values.
**
II. Create new features**
**II.1  Create aggregated values.** E.g. Kiddie Tray purchase in the past 10 visits, Count of fountain drink, Movie Gene of the past 10 visits,
II.2 

**Feature Selection**
**I. Filter**
Didn't do too well.
**II. Wrapper**
Backwards selection by removing the least important features and keep those important ones. 

----------------------
**Modeling**
We compare RandomForest and AdaBoost. End with Random Forest for better interpretation.
**Training**
Using ScikitLearn packages, we split dataset to 10 10 80 for testing, validation and training
We limit the depth of the RandomForest.

**Validation**
We focus on the following metrics of classfication.
Precision
Senstivity
F1-Score
ROC
![image](https://user-images.githubusercontent.com/32372822/144923954-d23254a7-5798-4edc-ad39-993c29e254f3.png)

**Model Tuning** 
With Grid Search, we tuned with maximum Tree depth and branching options.

**Improvement**
![image](https://user-images.githubusercontent.com/32372822/144924154-cebc6122-6afe-4867-a532-f99cc60e3f4f.png)









