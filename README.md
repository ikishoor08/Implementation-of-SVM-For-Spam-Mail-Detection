# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. .Import required libraries (pandas, chardet, sklearn, etc.).

2.Detect the encoding of the CSV file using chardet.

3.Read the CSV file with the correct encoding.

4.Check the data for structure and missing values.

5.Split the data into input (x = messages) and output (y = labels).

6.Divide the data into training and testing sets.

7.Convert text data into numbers using CountVectorizer.

8.Train an SVM model, make predictions, and calculate accuracy.


## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: KISHOOR I
RegisterNumber: 212225040190

import chardet

file = 'spam (1).csv'

with open(file, 'rb') as rawdata:
    result = chardet.detect(rawdata.read(100000))

print(result)

import pandas as pd

data = pd.read_csv('spam (1).csv', encoding='Windows-1252')

print(data.info())

print(data.isnull().sum())

# Correct columns
x = data["v2"].values   # message text
y = data["v1"].values   # spam/ham labels

from sklearn.model_selection import train_test_split

x_train, x_test, y_train, y_test = train_test_split(
    x, y, test_size=0.2, random_state=0
)

from sklearn.feature_extraction.text import CountVectorizer

cv = CountVectorizer()

x_train = cv.fit_transform(x_train)
x_test = cv.transform(x_test)

from sklearn.svm import SVC

svc = SVC()

svc.fit(x_train, y_train)

y_pred = svc.predict(x_test)

print(y_pred)

from sklearn import metrics

accuracy = metrics.accuracy_score(y_test, y_pred)

print("Accuracy:", accuracy)
*/
```

## Output:

<img width="1243" height="227" alt="image" src="https://github.com/user-attachments/assets/2c6abbe7-be2c-49e9-b865-7009c1f5d34f" />

<img width="1231" height="257" alt="image" src="https://github.com/user-attachments/assets/55f11367-5657-46bc-a19b-e721cc1a4d15" />

<img width="1231" height="130" alt="image" src="https://github.com/user-attachments/assets/55f4e9d8-0c43-4cd6-aa8c-0f2161e68263" />

<img width="1243" height="37" alt="image" src="https://github.com/user-attachments/assets/f9428d88-a07f-4c88-889c-099907416721" />

<img width="1243" height="38" alt="image" src="https://github.com/user-attachments/assets/14401302-edea-4953-91e2-9e307f967aed" />


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
