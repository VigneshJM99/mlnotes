---
title: "Train the model"
author: "Vignesh J M"
date: 2020-09-04
description: "-"
type: technical_note
draft: false
---

```python
from sklearn.datasets import load_iris
iris = load_iris()
```


```python
X = iris.data
y = iris.target
```


```python
from sklearn.model_selection import train_test_split
```


```python
X_train, X_test, y_train, y_test = train_test_split(
   X, y, test_size = 0.4, random_state=1
)
```


```python
from sklearn.neighbors import KNeighborsClassifier
from sklearn import metrics
```


```python
classifier_knn = KNeighborsClassifier(n_neighbors = 3)
classifier_knn.fit(X_train, y_train)
```




    KNeighborsClassifier(n_neighbors=3)




```python
y_pred = classifier_knn.predict(X_test)
```


```python
print("Accuracy:", metrics.accuracy_score(y_test, y_pred))
```

    Accuracy: 0.9833333333333333



```python
sample = [[5, 5, 3, 2], [2, 4, 3, 5]]
```


```python
preds = classifier_knn.predict(sample)
pred_species = [iris.target_names[p] for p in preds] 
print("Predictions:", pred_species)
```

    Predictions: ['versicolor', 'virginica']



```python

```
