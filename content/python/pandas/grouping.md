---
title: "Grouping"
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
df.groupby('Location').Location.count()
```




    Location
    Ahmedabad      51
    Bangalore      82
    Chennai        97
    Coimbatore    136
    Delhi         106
    Hyderabad     134
    Jaipur         86
    Kochi         121
    Kolkata       119
    Mumbai        159
    Pune          143
    Name: Location, dtype: int64




```python
df.groupby('Fuel_Type').Fuel_Type.count()
```




    Fuel_Type
    CNG         6
    Diesel    647
    LPG         2
    Petrol    579
    Name: Fuel_Type, dtype: int64




```python
df.groupby('Transmission').Transmission.count()
```




    Transmission
    Automatic    329
    Manual       905
    Name: Transmission, dtype: int64




```python
df.groupby('Owner_Type').Owner_Type.count()
```




    Owner_Type
    First             1023
    Fourth & Above       3
    Second             184
    Third               24
    Name: Owner_Type, dtype: int64


