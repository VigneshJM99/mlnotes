---
title: "Summary Functions"
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
df.Mileage.describe()
```




    count          1234
    unique          301
    top       17.0 kmpl
    freq             35
    Name: Mileage, dtype: object




```python
df.Location.describe()
```




    count       1234
    unique        11
    top       Mumbai
    freq         159
    Name: Location, dtype: object




```python
df.Seats.mean()
```




    5.28454619787408




```python
df.Location.unique()
```




    array(['Delhi', 'Coimbatore', 'Mumbai', 'Hyderabad', 'Pune', 'Jaipur',
           'Chennai', 'Kochi', 'Bangalore', 'Kolkata', 'Ahmedabad'],
          dtype=object)




```python
df.Name.value_counts()
```




    Maruti Alto LXi                              9
    Maruti Swift Dzire VDI                       8
    Honda City 1.5 V MT                          8
    Volkswagen Polo 1.2 MPI Highline             8
    Honda Brio S MT                              7
                                                ..
    Hyundai i20 2015-2017 1.2 Magna              1
    Volkswagen Vento 1.5 TDI Highline Plus AT    1
    Honda CR-V 2.4 4WD AT                        1
    Ford Endeavour 2.2 Titanium AT 4X2           1
    Mercedes-Benz E-Class E 220 d                1
    Name: Name, Length: 768, dtype: int64


