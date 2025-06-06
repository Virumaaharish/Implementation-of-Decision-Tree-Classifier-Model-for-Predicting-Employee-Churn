# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook
## Algorithm
1. import pandas module and import the required data set.
2. Find the null values and count them.
3. Count number of left values.
4. From sklearn import LabelEncoder to convert string values to numerical values. 5.From sklearn.model_selection import train_test_split. 6.Assign the train dataset and test dataset. 7.From sklearn.tree import DecisionTreeClassifier. 8.Use criteria as entropy. 9.From sklearn import metrics. 10.Find the accuracy of our model and predict the require values.


## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: Virumaa harish M
RegisterNumber:  212223230246
*/
```
```
``
import pandas as pd
data=pd.read_csv("/content/Employee.csv")
data.head()
data.info()
data.isnull().sum()
data["left"].value_counts()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()
x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()
y=data["left"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
dt.predict([[0.5,0.8,9,260,6,0,1,2]])

```
## Output:
#### Data.head()
![image](https://github.com/POZHILANVD/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/144870498/c4c54e86-9348-41be-9e16-c13bf0ce29dc)

#### Data.info():
![image](https://github.com/POZHILANVD/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/144870498/7365cd52-2cf2-410c-8933-5bede46f8f6d)

#### isnull() and sum():
![image](https://github.com/POZHILANVD/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/144870498/aaf09055-e6ed-42dd-83b5-a158fcbf5534)

#### Data Value Counts():
![image](https://github.com/POZHILANVD/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/144870498/01c623db-6af1-4c8f-986a-380916c161fc)

#### Data.head() for salary:
![image](https://github.com/POZHILANVD/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/144870498/50b3e487-9e5a-4197-8dae-b219c75f867d)

#### x.head():
![image](https://github.com/POZHILANVD/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/144870498/0dd44e4f-3443-4107-8b4c-f18cc2f00ed3)

#### Accuracy Value:
![image](https://github.com/POZHILANVD/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/144870498/0a43bb55-252e-4bbf-be71-810c6cd9f59e)

#### Data Prediction:
![image](https://github.com/POZHILANVD/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/144870498/5cd36afc-05c0-4144-bbd6-5434676f8b1a)

## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
