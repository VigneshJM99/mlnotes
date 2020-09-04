---
title: "Splitting the dataset"
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
   X, y, test_size = 0.3, random_state = 1
)
```


```python
print(X_train.shape)
print(X_test.shape)
```

    (105, 4)
    (45, 4)



```python
print(y_train.shape)
print(y_test.shape)
```

    (105,)
    (45,)

