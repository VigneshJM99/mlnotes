---
title: "Array_Split"
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
a = array([[1, 2, 3, 4],[5, 6, 7, 8]])
array_split(a, 2, axis = 0)
```




    [array([[1, 2, 3, 4]]), array([[5, 6, 7, 8]])]




```python
array_split(a, 4, axis = 1)
```




    [array([[1],
            [5]]),
     array([[2],
            [6]]),
     array([[3],
            [7]]),
     array([[4],
            [8]])]




```python
array_split(a, 3, axis = 1)
```




    [array([[1, 2],
            [5, 6]]),
     array([[3],
            [7]]),
     array([[4],
            [8]])]




```python
array_split(a, [2, 3], axis = 1)
```




    [array([[1, 2],
            [5, 6]]),
     array([[3],
            [7]]),
     array([[4],
            [8]])]


