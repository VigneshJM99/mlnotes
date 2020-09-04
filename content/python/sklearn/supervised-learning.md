---
title: "Supervised Learning"
author: "Vignesh J M"
date: 2020-09-04
description: "-"
type: technical_note
draft: false
---

```python
%matplotlib inline
import matplotlib.pyplot as plt
import numpy as np
import seaborn as sns
```


```python
iris = sns.load_dataset('iris')
```


```python
X_iris = iris.drop('species', axis = 1)
X_iris.shape
```




    (150, 4)




```python
y_iris = iris['species']
y_iris.shape
```




    (150,)




```python
rng = np.random.RandomState(35)
x = 10*rng.rand(40)
y = 2*x-1+rng.randn(40)
plt.scatter(x,y);
```


![png](supervised-learning_5_0.png)



```python
from sklearn.linear_model import LinearRegression
model = LinearRegression(fit_intercept=True)
model
```




    LinearRegression()




```python
X = x[:, np.newaxis]
X.shape
```




    (40, 1)




```python
model.fit(X, y)
```




    LinearRegression()




```python
model.coef_
```




    array([1.99839352])




```python
model.intercept_
```




    -0.9895459457775022




```python
xfit = np.linspace(-1, 11)
Xfit = xfit[:, np.newaxis]
yfit = model.predict(Xfit)
plt.scatter(x, y)
plt.plot(xfit, yfit);
```


![png](supervised-learning_11_0.png)

