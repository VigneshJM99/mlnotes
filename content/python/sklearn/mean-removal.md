---
title: "Mean Removal"
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
print("Mean =", Input_data.mean(axis=0))
print("Stddeviation = ", Input_data.std(axis=0))
```

    Mean = [ 1.75  -1.275  2.2  ]
    Stddeviation =  [2.71431391 4.20022321 4.69414529]



```python
data_scaled = preprocessing.scale(Input_data)
print("Mean_removed =", data_scaled.mean(axis=0))
print("Stddeviation_removed =", data_scaled.std(axis=0))
```

    Mean_removed = [1.11022302e-16 0.00000000e+00 0.00000000e+00]
    Stddeviation_removed = [1. 1. 1.]

