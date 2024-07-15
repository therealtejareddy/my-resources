# Scikit-learn
---
#### Installation
`pip install -U scikit-learn`

### Linear Regression
```python
import numpy as np
from sklearn.linear_model import LinearRegression

X_train = np.array([[1],[2],[3]])
y_train = np.array([1,2,3])

reg_l = LinearRegression()
reg_l.fit(X_train,Y)

score = reg_l.score(X,y_train)
print("Coefficient"+str(reg_l.coef_))
print("Intercept"+str(reg_l.intercept_))
print(score)
Y_predict = reg_l.predict([[4],[5]])
```

### Logistic Regression
```python
from sklearn.datasets import load_iris
from sklearn.linear_model import LogisticRegression

X, y = load_iris(return_X_y=True)
clf = LogisticRegression()
clf.fit(X,y)
score = clf.score(X,y)
print(score)
```

### Decision Tree
```python
from sklearn.tree import DecisionTreeClassifier

model = DecisionTreeClassifier()
model.fit(x_train,y_train)
```

### RandomForest - Classfier
```python
from sklearn.ensemble import RandomForestClassifier
from sklearn.datasets import load_digits
from sklearn.model_selection import train_test_split

digits = load_digits()
x_train,x_test,y_train,y_test=train_test_split(digits.data, digits.target, test_size=0.3)

rf = RandomForestClassifier(n_estimators=100)
rf.fit(x_train,y_train)
score = rf.score(x_test,y_test)
print(score)
```
### SVM - Classfier
```python
from sklearn.svm import SVC
from sklearn.datasets import load_digits
from sklearn.model_selection import train_test_split

digits = load_digits()
x_train,x_test,y_train,y_test=train_test_split(digits.data, digits.target, test_size=0.3)

svm = SVC()
svm.fit(x_train,y_train)
score = svm.score(x_test,y_test)
print(score)
```

### KNN - Classifier
```python
from sklearn.neighbours import KNeighborsClassifier

model = KNeighborsClassifier()
model.fit(x_train,y_train)
```

### Cross validation
```python
from sklearn.linear_model import LogisticRegression
from sklearn.svm import SVC
from sklearn.model_selection import cross_val_score
from sklearn.datasets import load_digits
from sklearn.model_selection import train_test_split

digits = load_digits()
x_train,x_test,y_train,y_test=train_test_split(digits.data, digits.target, test_size=0.3)

logistic_cv = cross_val_score(LogisticRegression(),digits.data,digits.target)
svm_cv = cross_val_score(SVC(),digits.data,digits.target, cv=2)
```
---
### K Means Clustering
```python
from sklearn.cluster import KMeans
model = KMeans(n_clusters=3)
model.fit(X)
```
---
## Model Saving
### Pickle
```python
import pickle

#saving
with open("pickle_model","wb") as f:
    pickle.dump(model,f)

#loading
with open("pickle_model","rb") as f:
    model = pickle.load(f)
```
### Joblib
```python
import joblib
#saving
joblib.dump(model,"joblib_model.joblib")

#loading
model = joblib.load("joblib_model.joblib")
```