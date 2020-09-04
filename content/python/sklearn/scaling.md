---
title: "Scaling"
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
data_scaler_minmax = preprocessing.MinMaxScaler(feature_range=(0,1))
data_scaled_minmax = data_scaler_minmax.fit_transform(Input_data)
```


```python
print ("\nMin max scaled data:\n", data_scaled_minmax)
```

    
    Min max scaled data:
     [[0.48648649 0.58252427 0.99122807]
     [0.         1.         0.81578947]
     [0.27027027 0.         1.        ]
     [1.         0.99029126 0.        ]]

