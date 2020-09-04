---
title: "Binarisation"
author: "Vignesh J M"
date: 2020-09-04
description: "-"
type: technical_note
draft: false
---

```python
import numpy as np
from sklearn import preprocessing
```


```python
Input_data = np.array([
   [2.1, -1.9, 5.5],
   [-1.5, 2.4, 3.5],
   [0.5, -7.9, 5.6],
   [5.9, 2.3, -5.8]]
)
```


```python
data_binarized = preprocessing.Binarizer(threshold=0.5).transform(Input_data)
```


```python
print("\nBinarized data:\n", data_binarized)
```

    
    Binarized data:
     [[1. 0. 1.]
     [0. 1. 1.]
     [0. 0. 1.]
     [1. 1. 0.]]

