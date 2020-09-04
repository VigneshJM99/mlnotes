---
title: "L1 Normalisation"
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
Input_data = np.array(
   [
      [2.1, -1.9, 5.5],
      [-1.5, 2.4, 3.5],
      [0.5, -7.9, 5.6],
      [5.9, 2.3, -5.8]
   ]
)
```


```python
data_normalized_l1 = preprocessing.normalize(Input_data, norm='l1')
```


```python
print("\nL1 normalized data:\n", data_normalized_l1)
```

    
    L1 normalized data:
     [[ 0.22105263 -0.2         0.57894737]
     [-0.2027027   0.32432432  0.47297297]
     [ 0.03571429 -0.56428571  0.4       ]
     [ 0.42142857  0.16428571 -0.41428571]]

