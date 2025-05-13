# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required libraries.

2.Upload and read the dataset.

3.Check for any null values using the isnull() function.

4.From sklearn.tree import DecisionTreeClassifier and use criterion as entropy.

5.Find the accuracy of the model and predict the required values by importing the required module from sklearn. 

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Aman Singh
RegisterNumber:  212224040020
*/
```

```python
import pandas as pd
df=pd.read_csv("Salary.csv")
df.head()
df.info()
df.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
df["Position"]=le.fit_transform(df["Position"])
df.head()


x=df[['Position','Level']]
x.head()
y=df['Salary']
y.head()



from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
from sklearn.tree import DecisionTreeRegressor
model=DecisionTreeRegressor()
mdeol.fit(x_train,y_train)
y_pred=model.predict(x_test)
y_pred


model.score(x_test,y_test)

model.predict([[5,6]])
```
## Output:

<img width="387" alt="Screenshot 2025-05-13 at 11 30 50 AM" src="https://github.com/user-attachments/assets/9d773f3f-0a1c-4ab0-8ec0-572e8f7c150f" />
<br>

<img width="468" alt="Screenshot 2025-05-13 at 11 31 03 AM" src="https://github.com/user-attachments/assets/086250a2-2c5b-441c-b006-c1ca3f3ee0c2" />
<br>
<img width="410" alt="Screenshot 2025-05-13 at 11 31 20 AM" src="https://github.com/user-attachments/assets/8c7cf7c1-f1f1-4b73-a149-a061e66a4f47" />
<br>
<img width="358" alt="Screenshot 2025-05-13 at 11 31 31 AM" src="https://github.com/user-attachments/assets/39acd3fe-03a4-4af6-a0e0-9fd963715d97" />
<br>

<img width="407" alt="Screenshot 2025-05-13 at 11 31 42 AM" src="https://github.com/user-attachments/assets/2259e501-bf68-42a7-a48f-394e7d4c9efc" />
<br>

<img width="384" alt="Screenshot 2025-05-13 at 11 31 52 AM" src="https://github.com/user-attachments/assets/4e0efa30-ce18-446d-83e5-35e3bab1c29c" />
<br>
<img width="482" alt="Screenshot 2025-05-13 at 11 32 11 AM" src="https://github.com/user-attachments/assets/803aeae3-98a2-4fa8-9ae3-0b55b1743541" />
<br>

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
