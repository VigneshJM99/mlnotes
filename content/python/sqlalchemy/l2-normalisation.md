---
title: "L2 Normalisation"
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
data_normalized_l2 = preprocessing.normalize(Input_data, norm='l2')
```


```python
print("\nL2 normalized data:\n", data_normalized_l2)
```

    
    L2 normalized data:
     [[ 0.33946114 -0.30713151  0.88906489]
     [-0.33325106  0.53320169  0.7775858 ]
     [ 0.05156558 -0.81473612  0.57753446]
     [ 0.68706914  0.26784051 -0.6754239 ]]

