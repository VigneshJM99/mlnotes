---
title: "Renaming"
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
df.rename(columns = {'Seats':'Capacity'})
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
      <th>Capacity</th>
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
<p>1234 rows × 11 columns</p>
</div>




```python
df.rename(index = {0:'First_entry', 1:'Second_entry'})
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
      <th>First_entry</th>
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
      <th>Second_entry</th>
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
<p>1234 rows × 11 columns</p>
</div>




```python
df.rename_axis("Cars_Price", axis = 'rows').rename_axis("Factors", axis = 'columns')
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
      <th>Factors</th>
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
    <tr>
      <th>Cars_Price</th>
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
      <th></th>
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
<p>1234 rows × 11 columns</p>
</div>


