---
title: "Slice"
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
s = slice(3, 9, 2)
```


```python
a = arange(20)
a[s]
```




    array([3, 5, 7])




```python
a[3:9:2]
```




    array([3, 5, 7])


