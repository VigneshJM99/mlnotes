---
title: "Example"
author: "Vignesh J M"
date: 2020-09-04
description: "-"
type: technical_note
draft: false
---

```python
import seaborn as sns
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
%matplotlib inline
import matplotlib.pyplot as plt
import numpy as np
rng = np.random.RandomState(35)
x = 10*rng.rand(40)
y = 2*x-1+rng.randn(40)
plt.scatter(x,y);
```


![png](example_4_0.png)

