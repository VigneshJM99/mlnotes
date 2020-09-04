---
title: "Getting Started"
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
df.Mileage.dtype
```




    dtype('O')




```python
df.dtypes
```




    Name                  object
    Location              object
    Year                   int64
    Kilometers_Driven      int64
    Fuel_Type             object
    Transmission          object
    Owner_Type            object
    Mileage               object
    Engine                object
    Power                 object
    Seats                float64
    dtype: object




```python
df.Kilometers_Driven.astype('float64')
```




    0        40929.0
    1        54493.0
    2        34000.0
    3       139000.0
    4        29000.0
              ...   
    1229     89411.0
    1230     59000.0
    1231     28000.0
    1232     52262.0
    1233     72443.0
    Name: Kilometers_Driven, Length: 1234, dtype: float64


