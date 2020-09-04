---
title: "Insert"
author: "Vignesh J M"
date: 2020-09-04
description: "-"
type: technical_note
draft: false
---

```python
from numpy import *
```


```python
a = array([10, 20, 30, 40])
insert(a, [1,3], 50)
```




    array([10, 50, 20, 30, 50, 40])




```python
insert(a, [1, 3],[50,60])
```




    array([10, 50, 20, 30, 60, 40])




```python
a = array([[10, 20, 30],[40, 50, 60],[70, 80, 90]])
insert(a, [1, 2], 100, axis = 0)
```




    array([[ 10,  20,  30],
           [100, 100, 100],
           [ 40,  50,  60],
           [100, 100, 100],
           [ 70,  80,  90]])




```python
insert(a, [0,1], [[100], [200]], axis = 0)
```




    array([[100, 100, 100],
           [ 10,  20,  30],
           [200, 200, 200],
           [ 40,  50,  60],
           [ 70,  80,  90]])




```python
insert(a, [0, 1], [100, 200], axis = 1)
```




    array([[100,  10, 200,  20,  30],
           [100,  40, 200,  50,  60],
           [100,  70, 200,  80,  90]])


