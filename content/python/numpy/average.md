---
title: "Average"
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
a = array([1, 2, 3, 4, 5])
w = array([0.1, 0.2, 0.3, 0.4, 0.5])
```


```python
average(a)
```




    3.0




```python
average(a, weights = w)
```




    3.6666666666666665




```python
average(a, weights = w, returned = True)
```




    (3.6666666666666665, 1.5)


