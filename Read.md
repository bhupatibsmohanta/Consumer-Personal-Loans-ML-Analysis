Credit Cards 
***************

reading of Train data and Test using pandas library and user personal information which are 
not important for data analysis are dropped. e.g. name, address, sex, Marital_Status, email etc.

Data Preprocessing:
--------------------
i) Missing Values Treatment :
   can be done manually for each categorical data.
   use business logic or most probable values to fill the missing values.

ii) Categorical Data Encoding:
    can be done manually for each categorical data or 
    using LabelEncoder library which automatically assign numerical values to each category in the feature.

    It is important to convert categorical data into numerical values as we can not apply ML algorithms on categorical data.

iii) Feature scaling for continuos data:
     MinMaxScaler() is a better option than StandardScaler(), 
     as the range of scaling for MinMaxScaler() is between 0 to 1 
     where as the range of scaling for StandardScaler() is between -1 to 1 as

iv) Dimentionality Reduction:
    It can be done by Prinicipal component analysis techniques using PCA library.
    PCA returns n_components features which are highly correlated.

Applying ML Algorithms:
-----------------------
models:
    (1) Support Vector Classifier   (rbf gives best result as all the features have non linear data)
    (2) Logistic Regression
    (3) k-Nearest Neighbors         (performed best for 15 nearest neighbors)
    (4) Random Forest Classifier   (min_samples_split between 23-27 gives best result)
    (5) XGB
    (6) Decision tree Classifier
  
try each of these models with different n_components values.
find out for which value of n_components the model performs the best.

Compare best score of all the models.


Realtime testing:
-----------------
Use the best model from above mentioned models and predict the 'CPL_Status' for Test data.

