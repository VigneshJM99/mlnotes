---
title: "Data As Target"
author: "Vignesh J M"
date: 2020-09-04
description: "-"
type: technical_note
draft: false
---

```python
import seaborn as sns
import seaborn as sns; sns.set()
```


```python
iris = sns.load_dataset('iris')
%matplotlib inline
sns.pairplot(iris, hue='species', height=3);
```


![png](data-as-target_2_0.png)



```python
X_iris = iris.drop('species', axis=1)
X_iris.shape
```




    (150, 4)




```python
y_iris = iris['species']
y_iris.shape
```




    (150,)


