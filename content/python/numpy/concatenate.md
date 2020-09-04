```python
---
title: "Concatenate"
author: "Vignesh J M"
date: 2020-09-04
description: "-"
type: technical_note
draft: false
---
```


```python
from numpy import *
```


```python
x = array([[1, 2],[3, 4]])
y = array([[5, 6],[7, 8]])
```


```python
concatenate((x, y))
```




    array([[1, 2],
           [3, 4],
           [5, 6],
           [7, 8]])




```python
concatenate((x, y), axis = 1)
```




    array([[1, 2, 5, 6],
           [3, 4, 7, 8]])


