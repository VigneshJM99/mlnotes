---
title: "Solve"
author: "Vignesh J M"
date: 2020-09-04
description: "-"
type: technical_note
draft: false
---

```python
from numpy import *
from numpy.linalg import solve
```


```python
a = array([[3, 1, 5],[1, 0, 8],[2, 1, 4]])
b = array([6, 7, 8])
```


```python
x = solve(a, b)
```


```python
print(x)
```

    [-3.28571429  9.42857143  1.28571429]



```python
dot(a, x)
```




    array([6., 7., 8.])


