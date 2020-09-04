---
title: "Indexing In Pandas"
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
df.iloc[0]
```




    Name                 Maruti Alto K10 LXI CNG
    Location                               Delhi
    Year                                    2014
    Kilometers_Driven                      40929
    Fuel_Type                                CNG
    Transmission                          Manual
    Owner_Type                             First
    Mileage                          32.26 km/kg
    Engine                                998 CC
    Power                               58.2 bhp
    Seats                                      4
    Name: 0, dtype: object




```python
df.iloc[:,0]
```




    0                                 Maruti Alto K10 LXI CNG
    1                           Maruti Alto 800 2016-2019 LXI
    2               Toyota Innova Crysta Touring Sport 2.4 MT
    3                                    Toyota Etios Liva GD
    4                                       Hyundai i20 Magna
                                  ...                        
    1229                    Volkswagen Vento Diesel Trendline
    1230                               Volkswagen Polo GT TSI
    1231                               Nissan Micra Diesel XV
    1232                               Volkswagen Polo GT TSI
    1233    Mercedes-Benz E-Class 2009-2013 E 220 CDI Avan...
    Name: Name, Length: 1234, dtype: object




```python
df.iloc[:3,0]
```




    0                      Maruti Alto K10 LXI CNG
    1                Maruti Alto 800 2016-2019 LXI
    2    Toyota Innova Crysta Touring Sport 2.4 MT
    Name: Name, dtype: object




```python
df.iloc[1:3,0]
```




    1                Maruti Alto 800 2016-2019 LXI
    2    Toyota Innova Crysta Touring Sport 2.4 MT
    Name: Name, dtype: object




```python
df.iloc[[0,1,2],0]
```




    0                      Maruti Alto K10 LXI CNG
    1                Maruti Alto 800 2016-2019 LXI
    2    Toyota Innova Crysta Touring Sport 2.4 MT
    Name: Name, dtype: object




```python
df.iloc[-5:]
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
      <th>1229</th>
      <td>Volkswagen Vento Diesel Trendline</td>
      <td>Hyderabad</td>
      <td>2011</td>
      <td>89411</td>
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
      <td>59000</td>
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
      <td>28000</td>
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
      <td>52262</td>
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
      <td>72443</td>
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
</div>




```python
df.loc[0, 'Name']
```




    'Maruti Alto K10 LXI CNG'


