---
title: "Unsupervised Learning"
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
from sklearn.decomposition import PCA
```


![png](unsupervised-learnibg_5_0.png)



```python
model = PCA(n_components=2)
model
```




    PCA(n_components=2)




```python
model.fit(X_iris)
```




    PCA(n_components=2)




```python
X_2D = model.transform(X_iris)
iris['PCA1'] = X_2D[:, 0]
iris['PCA2'] = X_2D[:, 1]
sns.lmplot("PCA1", "PCA2", hue='species', data=iris, fit_reg=False);
```


![png](unsupervised-learnibg_8_0.png)

