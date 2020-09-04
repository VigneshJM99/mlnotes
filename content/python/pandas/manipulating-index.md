---
title: "Manipulating the index"
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
df.set_index("Mileage")
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
      <th>Engine</th>
      <th>Power</th>
      <th>Seats</th>
    </tr>
    <tr>
      <th>Mileage</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>32.26 km/kg</th>
      <td>Maruti Alto K10 LXI CNG</td>
      <td>Delhi</td>
      <td>2014</td>
      <td>40929</td>
      <td>CNG</td>
      <td>Manual</td>
      <td>First</td>
      <td>998 CC</td>
      <td>58.2 bhp</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>24.7 kmpl</th>
      <td>Maruti Alto 800 2016-2019 LXI</td>
      <td>Coimbatore</td>
      <td>2013</td>
      <td>54493</td>
      <td>Petrol</td>
      <td>Manual</td>
      <td>Second</td>
      <td>796 CC</td>
      <td>47.3 bhp</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>13.68 kmpl</th>
      <td>Toyota Innova Crysta Touring Sport 2.4 MT</td>
      <td>Mumbai</td>
      <td>2017</td>
      <td>34000</td>
      <td>Diesel</td>
      <td>Manual</td>
      <td>First</td>
      <td>2393 CC</td>
      <td>147.8 bhp</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>23.59 kmpl</th>
      <td>Toyota Etios Liva GD</td>
      <td>Hyderabad</td>
      <td>2012</td>
      <td>139000</td>
      <td>Diesel</td>
      <td>Manual</td>
      <td>First</td>
      <td>1364 CC</td>
      <td>null bhp</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>18.5 kmpl</th>
      <td>Hyundai i20 Magna</td>
      <td>Mumbai</td>
      <td>2014</td>
      <td>29000</td>
      <td>Petrol</td>
      <td>Manual</td>
      <td>First</td>
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
    </tr>
    <tr>
      <th>20.54 kmpl</th>
      <td>Volkswagen Vento Diesel Trendline</td>
      <td>Hyderabad</td>
      <td>2011</td>
      <td>89411</td>
      <td>Diesel</td>
      <td>Manual</td>
      <td>First</td>
      <td>1598 CC</td>
      <td>103.6 bhp</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>17.21 kmpl</th>
      <td>Volkswagen Polo GT TSI</td>
      <td>Mumbai</td>
      <td>2015</td>
      <td>59000</td>
      <td>Petrol</td>
      <td>Automatic</td>
      <td>First</td>
      <td>1197 CC</td>
      <td>103.6 bhp</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>23.08 kmpl</th>
      <td>Nissan Micra Diesel XV</td>
      <td>Kolkata</td>
      <td>2012</td>
      <td>28000</td>
      <td>Diesel</td>
      <td>Manual</td>
      <td>First</td>
      <td>1461 CC</td>
      <td>63.1 bhp</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>17.2 kmpl</th>
      <td>Volkswagen Polo GT TSI</td>
      <td>Pune</td>
      <td>2013</td>
      <td>52262</td>
      <td>Petrol</td>
      <td>Automatic</td>
      <td>Third</td>
      <td>1197 CC</td>
      <td>103.6 bhp</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>10.0 kmpl</th>
      <td>Mercedes-Benz E-Class 2009-2013 E 220 CDI Avan...</td>
      <td>Kochi</td>
      <td>2014</td>
      <td>72443</td>
      <td>Diesel</td>
      <td>Automatic</td>
      <td>First</td>
      <td>2148 CC</td>
      <td>170 bhp</td>
      <td>5.0</td>
    </tr>
  </tbody>
</table>
<p>1234 rows × 10 columns</p>
</div>




```python
#Conditional Selection

df.Location == "Dehli"
```




    0       False
    1       False
    2       False
    3       False
    4       False
            ...  
    1229    False
    1230    False
    1231    False
    1232    False
    1233    False
    Name: Location, Length: 1234, dtype: bool




```python
df.loc[df.Location == 'Dehli']
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
df.loc[(df.Location == 'Dehli') & (df.Seats >4)]
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
df.loc[(df.Location == 'Dehli') | (df.Seats >4)]
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
      <th>1</th>
      <td>Maruti Alto 800 2016-2019 LXI</td>
      <td>Coimbatore</td>
      <td>2013</td>
      <td>54493</td>
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
      <td>34000</td>
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
      <td>139000</td>
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
      <td>29000</td>
      <td>Petrol</td>
      <td>Manual</td>
      <td>First</td>
      <td>18.5 kmpl</td>
      <td>1197 CC</td>
      <td>82.85 bhp</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Mahindra XUV500 W8 2WD</td>
      <td>Coimbatore</td>
      <td>2016</td>
      <td>85609</td>
      <td>Diesel</td>
      <td>Manual</td>
      <td>Second</td>
      <td>16.0 kmpl</td>
      <td>2179 CC</td>
      <td>140 bhp</td>
      <td>7.0</td>
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
<p>1201 rows × 11 columns</p>
</div>




```python
df.loc[df.Location.isin(['Dehli', 'Chennai'])]
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
      <th>12</th>
      <td>Toyota Corolla H5</td>
      <td>Chennai</td>
      <td>2007</td>
      <td>90000</td>
      <td>Petrol</td>
      <td>Manual</td>
      <td>Third</td>
      <td>13.4 kmpl</td>
      <td>1794 CC</td>
      <td>125 bhp</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Ford Ikon 1.4 TDCi DuraTorq</td>
      <td>Chennai</td>
      <td>2009</td>
      <td>140000</td>
      <td>Diesel</td>
      <td>Manual</td>
      <td>First</td>
      <td>13.8 kmpl</td>
      <td>1399 CC</td>
      <td>68 bhp</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>30</th>
      <td>Toyota Etios Cross 1.4L VD</td>
      <td>Chennai</td>
      <td>2014</td>
      <td>70000</td>
      <td>Diesel</td>
      <td>Manual</td>
      <td>Second</td>
      <td>23.59 kmpl</td>
      <td>1364 CC</td>
      <td>67.06 bhp</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>33</th>
      <td>Mitsubishi Pajero 2.8 SFX</td>
      <td>Chennai</td>
      <td>2012</td>
      <td>121000</td>
      <td>Diesel</td>
      <td>Manual</td>
      <td>First</td>
      <td>10.5 kmpl</td>
      <td>2835 CC</td>
      <td>107.2 bhp</td>
      <td>6.0</td>
    </tr>
    <tr>
      <th>35</th>
      <td>Maruti Swift Dzire VXI</td>
      <td>Chennai</td>
      <td>2015</td>
      <td>51000</td>
      <td>Petrol</td>
      <td>Manual</td>
      <td>First</td>
      <td>19.1 kmpl</td>
      <td>1197 CC</td>
      <td>85.8 bhp</td>
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
      <th>1176</th>
      <td>Hyundai i10 Era 1.1</td>
      <td>Chennai</td>
      <td>2008</td>
      <td>71467</td>
      <td>Petrol</td>
      <td>Manual</td>
      <td>First</td>
      <td>19.81 kmpl</td>
      <td>1086 CC</td>
      <td>68.05 bhp</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>1203</th>
      <td>Maruti Celerio VXI AT</td>
      <td>Chennai</td>
      <td>2015</td>
      <td>31717</td>
      <td>Petrol</td>
      <td>Automatic</td>
      <td>First</td>
      <td>23.1 kmpl</td>
      <td>998 CC</td>
      <td>67.04 bhp</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>1205</th>
      <td>Datsun GO T Petrol</td>
      <td>Chennai</td>
      <td>2016</td>
      <td>36000</td>
      <td>Petrol</td>
      <td>Manual</td>
      <td>First</td>
      <td>19.83 kmpl</td>
      <td>1198 CC</td>
      <td>67 bhp</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>1208</th>
      <td>Mahindra Renault Logan 1.5 DLE Diesel</td>
      <td>Chennai</td>
      <td>2007</td>
      <td>160000</td>
      <td>Diesel</td>
      <td>Manual</td>
      <td>Second</td>
      <td>19.2 kmpl</td>
      <td>1461 CC</td>
      <td>65 bhp</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>1224</th>
      <td>Renault Duster 85PS Diesel RxL</td>
      <td>Chennai</td>
      <td>2015</td>
      <td>70000</td>
      <td>Diesel</td>
      <td>Manual</td>
      <td>First</td>
      <td>19.87 kmpl</td>
      <td>1461 CC</td>
      <td>83.8 bhp</td>
      <td>5.0</td>
    </tr>
  </tbody>
</table>
<p>97 rows × 11 columns</p>
</div>




```python
df.loc[df.Seats.notnull()]
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
      <td>40929</td>
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
      <td>54493</td>
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
      <td>34000</td>
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
      <td>139000</td>
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
      <td>29000</td>
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
<p>1223 rows × 11 columns</p>
</div>


