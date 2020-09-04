---
title: "Assigning data"
author: "Vignesh J M"
date: 2020-09-04
description: "-"
type: technical_note
draft: false
---

```python
import pandas as pd
```


```python
df = pd.read_excel('Car_Pricing.xlsx')
```


```python
df['Review'] = 'Ok'
```


```python
df['Review']
```




    0       Ok
    1       Ok
    2       Ok
    3       Ok
    4       Ok
            ..
    1229    Ok
    1230    Ok
    1231    Ok
    1232    Ok
    1233    Ok
    Name: Review, Length: 1234, dtype: object




```python
df['index_backwards'] = range(len(df), 0, -1)
df['index_backwards']
```




    0       1234
    1       1233
    2       1232
    3       1231
    4       1230
            ... 
    1229       5
    1230       4
    1231       3
    1232       2
    1233       1
    Name: index_backwards, Length: 1234, dtype: int64


