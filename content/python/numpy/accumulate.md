---
title: "Accumulate"
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
add.accumulate(array([1.,2.,3.,4.]))
```




    array([ 1.,  3.,  6., 10.])




```python
array([1., 1.+2., (1.+2.)+3., ((1.+2.)+3.)+4.])
```




    array([ 1.,  3.,  6., 10.])




```python
multiply.accumulate(array([1.,2.,3.,4.]))
```




    array([ 1.,  2.,  6., 24.])




```python
array([1., 1.*2., (1.*2.)*3., ((1.*2.)*3.)*4.])
```




    array([ 1.,  2.,  6., 24.])




```python
add.accumulate(array([[1,2,3],[4,5,6]]), axis = 0)
```




    array([[1, 2, 3],
           [5, 7, 9]])




```python
add.accumulate(array([[1,2,3],[4,5,6]]), axis = 1)
```




    array([[ 1,  3,  6],
           [ 4,  9, 15]])


