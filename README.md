# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Load and split the dataset into features and target variable, then divide it into training and testing sets.
2. Initialize and train the Logistic Regression model on the training data.
3. Use the model to predict placement status on the test data.
4. Evaluate the model using accuracy, confusion matrix, and classification report.

## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: MOPURI ANKITHA
RegisterNumber: 212223040117
*/
```
```
# Import necessary libraries
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import accuracy_score, confusion_matrix, classification_report

# Load dataset
# Assume the dataset has features like 'GPA', 'Exam_Score', 'Internships', and 'Placed' as target (1 for placed, 0 for not placed)
df = pd.read_csv('Placement_Data.csv')

# Define features (X) and target (y)
X = df[['ssc_p', 'hsc_p', 'degree_p']]  # Use actual column names from your dataset
y = df['status']  # Target column -  assuming 'status' is the target variable. Please verify with your dataset

# Split the data into training and testing sets
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Initialize and train the logistic regression model
model = LogisticRegression()
model.fit(X_train, y_train)

# Predict on the test set
y_pred = model.predict(X_test)

# Evaluate the model
accuracy = accuracy_score(y_test, y_pred)
conf_matrix = confusion_matrix(y_test, y_pred)
class_report = classification_report(y_test, y_pred)

print(f"Accuracy: {accuracy:.2f}")
print("Confusion Matrix:\n", conf_matrix)
print("Classification Report:\n", class_report)
```

## Output:
![image](https://github.com/user-attachments/assets/53b08c33-55a2-4612-86d6-7528babfb281)



## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
