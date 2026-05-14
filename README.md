# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
```
1.Import libraries and load the Salary dataset using Pandas.
2.Separate input features and target salary values, then convert categorical data into numerical form.
3.Create and train the Decision Tree Regressor model using the dataset.
4.Predict salary values, evaluate the model, and visualize the decision tree.
```

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: 212225230261
RegisterNumber: sharmila
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeRegressor, plot_tree
from sklearn.metrics import accuracy_score, classification_report
data = pd.read_csv("Salary (1).csv")
X = data.drop("Salary", axis=1)
y = data["Salary"]
X = pd.get_dummies(X, drop_first=True)
#X_train, X_test, y_train, y_test = train_test_split(    X, y, test_size=0.2, random_state=42)
model = DecisionTreeRegressor(random_state=42)
model.fit(X, y)
y_pred = model.predict(X)
# Accuracy
print("\nAccuracy:", accuracy_score(y, y_pred)*100)

# Classification Report
print("\nClassification Report:")
print(classification_report(y, y_pred))

plt.figure(figsize=(25,12))
plot_tree(
    model,
    feature_names=X.columns,
    filled=True
)

plt.title("Decision Tree Regressor")
plt.show()
*/
```

## Output:
<img width="925" height="796" alt="image" src="https://github.com/user-attachments/assets/973aa5e7-8612-4bf2-adf8-e52cc248be1f" />


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
