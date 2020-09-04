---
title: "Missing Data"
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
df[pd.isnull(df.Year)]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Location</th>
      <th>Year</th>
      <th>Kilometers_Driven</th>
      <th>Fuel_Type</th>
      <th>Transmission</th>
      <th>Owner_Type</th>
      <th>Mileage</th>
      <th>Engine</th>
      <th>Power</th>
      <th>Seats</th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>
</div>




```python
df.Seats.fillna("Unknown")
```




    0       4
    1       5
    2       7
    3       5
    4       5
           ..
    1229    5
    1230    5
    1231    5
    1232    5
    1233    5
    Name: Seats, Length: 1234, dtype: object




```python
df.Location.replace("Dehli", "Dehli-Capital")
```




    0            Delhi
    1       Coimbatore
    2           Mumbai
    3        Hyderabad
    4           Mumbai
               ...    
    1229     Hyderabad
    1230        Mumbai
    1231       Kolkata
    1232          Pune
    1233         Kochi
    Name: Location, Length: 1234, dtype: object


