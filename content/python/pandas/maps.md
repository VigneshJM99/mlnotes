---
title: "Maps"
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
df_Km_mean = df.Kilometers_Driven.mean()
df.Kilometers_Driven.map(lambda p: p - df_Km_mean)
```




    0      -17578.288493
    1       -4014.288493
    2      -24507.288493
    3       80492.711507
    4      -29507.288493
                ...     
    1229    30903.711507
    1230      492.711507
    1231   -30507.288493
    1232    -6245.288493
    1233    13935.711507
    Name: Kilometers_Driven, Length: 1234, dtype: float64




```python
def dfmean_km(row):
    row.Kilometers_Driven = row.Kilometers_Driven - df_Km_mean
    return row

df.apply(dfmean_km, axis = 'columns')
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
    <tr>
      <th>0</th>
      <td>Maruti Alto K10 LXI CNG</td>
      <td>Delhi</td>
      <td>2014</td>
      <td>-17578.288493</td>
      <td>CNG</td>
      <td>Manual</td>
      <td>First</td>
      <td>32.26 km/kg</td>
      <td>998 CC</td>
      <td>58.2 bhp</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Maruti Alto 800 2016-2019 LXI</td>
      <td>Coimbatore</td>
      <td>2013</td>
      <td>-4014.288493</td>
      <td>Petrol</td>
      <td>Manual</td>
      <td>Second</td>
      <td>24.7 kmpl</td>
      <td>796 CC</td>
      <td>47.3 bhp</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Toyota Innova Crysta Touring Sport 2.4 MT</td>
      <td>Mumbai</td>
      <td>2017</td>
      <td>-24507.288493</td>
      <td>Diesel</td>
      <td>Manual</td>
      <td>First</td>
      <td>13.68 kmpl</td>
      <td>2393 CC</td>
      <td>147.8 bhp</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Toyota Etios Liva GD</td>
      <td>Hyderabad</td>
      <td>2012</td>
      <td>80492.711507</td>
      <td>Diesel</td>
      <td>Manual</td>
      <td>First</td>
      <td>23.59 kmpl</td>
      <td>1364 CC</td>
      <td>null bhp</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Hyundai i20 Magna</td>
      <td>Mumbai</td>
      <td>2014</td>
      <td>-29507.288493</td>
      <td>Petrol</td>
      <td>Manual</td>
      <td>First</td>
      <td>18.5 kmpl</td>
      <td>1197 CC</td>
      <td>82.85 bhp</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>1229</th>
      <td>Volkswagen Vento Diesel Trendline</td>
      <td>Hyderabad</td>
      <td>2011</td>
      <td>30903.711507</td>
      <td>Diesel</td>
      <td>Manual</td>
      <td>First</td>
      <td>20.54 kmpl</td>
      <td>1598 CC</td>
      <td>103.6 bhp</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>1230</th>
      <td>Volkswagen Polo GT TSI</td>
      <td>Mumbai</td>
      <td>2015</td>
      <td>492.711507</td>
      <td>Petrol</td>
      <td>Automatic</td>
      <td>First</td>
      <td>17.21 kmpl</td>
      <td>1197 CC</td>
      <td>103.6 bhp</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>1231</th>
      <td>Nissan Micra Diesel XV</td>
      <td>Kolkata</td>
      <td>2012</td>
      <td>-30507.288493</td>
      <td>Diesel</td>
      <td>Manual</td>
      <td>First</td>
      <td>23.08 kmpl</td>
      <td>1461 CC</td>
      <td>63.1 bhp</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>1232</th>
      <td>Volkswagen Polo GT TSI</td>
      <td>Pune</td>
      <td>2013</td>
      <td>-6245.288493</td>
      <td>Petrol</td>
      <td>Automatic</td>
      <td>Third</td>
      <td>17.2 kmpl</td>
      <td>1197 CC</td>
      <td>103.6 bhp</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>1233</th>
      <td>Mercedes-Benz E-Class 2009-2013 E 220 CDI Avan...</td>
      <td>Kochi</td>
      <td>2014</td>
      <td>13935.711507</td>
      <td>Diesel</td>
      <td>Automatic</td>
      <td>First</td>
      <td>10.0 kmpl</td>
      <td>2148 CC</td>
      <td>170 bhp</td>
      <td>5.0</td>
    </tr>
  </tbody>
</table>
<p>1234 rows × 11 columns</p>
</div>




```python
df_km_mean = df.Kilometers_Driven.mean()
df.Kilometers_Driven - df_km_mean
```




    0      -17578.288493
    1       -4014.288493
    2      -24507.288493
    3       80492.711507
    4      -29507.288493
                ...     
    1229    30903.711507
    1230      492.711507
    1231   -30507.288493
    1232    -6245.288493
    1233    13935.711507
    Name: Kilometers_Driven, Length: 1234, dtype: float64




```python
df.Location + "-" + df.Name
```




    0                           Delhi-Maruti Alto K10 LXI CNG
    1                Coimbatore-Maruti Alto 800 2016-2019 LXI
    2        Mumbai-Toyota Innova Crysta Touring Sport 2.4 MT
    3                          Hyderabad-Toyota Etios Liva GD
    4                                Mumbai-Hyundai i20 Magna
                                  ...                        
    1229          Hyderabad-Volkswagen Vento Diesel Trendline
    1230                        Mumbai-Volkswagen Polo GT TSI
    1231                       Kolkata-Nissan Micra Diesel XV
    1232                          Pune-Volkswagen Polo GT TSI
    1233    Kochi-Mercedes-Benz E-Class 2009-2013 E 220 CD...
    Length: 1234, dtype: object


