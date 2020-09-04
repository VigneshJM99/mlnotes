---
title: "Grouping & multi-indexing"
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
Location_Collected = df.groupby(['Location', 'Name', 'Fuel_Type']).Kilometers_Driven.agg([len])
Location_Collected
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
      <th></th>
      <th></th>
      <th>len</th>
    </tr>
    <tr>
      <th>Location</th>
      <th>Name</th>
      <th>Fuel_Type</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th rowspan="5" valign="top">Ahmedabad</th>
      <th>Audi A3 35 TDI Attraction</th>
      <th>Diesel</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Audi Q3 35 TDI Quattro Premium Plus</th>
      <th>Diesel</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Audi Q5 2008-2012 2.0 TFSI Quattro</th>
      <th>Petrol</th>
      <td>1</td>
    </tr>
    <tr>
      <th>BMW 3 Series 320d Prestige</th>
      <th>Diesel</th>
      <td>1</td>
    </tr>
    <tr>
      <th>BMW 3 Series 320d Sport</th>
      <th>Diesel</th>
      <td>1</td>
    </tr>
    <tr>
      <th>...</th>
      <th>...</th>
      <th>...</th>
      <td>...</td>
    </tr>
    <tr>
      <th rowspan="5" valign="top">Pune</th>
      <th>Volkswagen Polo Diesel Highline 1.2L</th>
      <th>Diesel</th>
      <td>2</td>
    </tr>
    <tr>
      <th>Volkswagen Polo Diesel Trendline 1.2L</th>
      <th>Diesel</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Volkswagen Polo GT TDI</th>
      <th>Diesel</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Volkswagen Polo GT TSI</th>
      <th>Petrol</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Volkswagen Vento Petrol Highline</th>
      <th>Petrol</th>
      <td>2</td>
    </tr>
  </tbody>
</table>
<p>1133 rows × 1 columns</p>
</div>




```python
mi = Location_Collected.index
type(mi)
```




    pandas.core.indexes.multi.MultiIndex




```python
Location_Collected.reset_index()
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
      <th>Location</th>
      <th>Name</th>
      <th>Fuel_Type</th>
      <th>len</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Ahmedabad</td>
      <td>Audi A3 35 TDI Attraction</td>
      <td>Diesel</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Ahmedabad</td>
      <td>Audi Q3 35 TDI Quattro Premium Plus</td>
      <td>Diesel</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Ahmedabad</td>
      <td>Audi Q5 2008-2012 2.0 TFSI Quattro</td>
      <td>Petrol</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Ahmedabad</td>
      <td>BMW 3 Series 320d Prestige</td>
      <td>Diesel</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Ahmedabad</td>
      <td>BMW 3 Series 320d Sport</td>
      <td>Diesel</td>
      <td>1</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>1128</th>
      <td>Pune</td>
      <td>Volkswagen Polo Diesel Highline 1.2L</td>
      <td>Diesel</td>
      <td>2</td>
    </tr>
    <tr>
      <th>1129</th>
      <td>Pune</td>
      <td>Volkswagen Polo Diesel Trendline 1.2L</td>
      <td>Diesel</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1130</th>
      <td>Pune</td>
      <td>Volkswagen Polo GT TDI</td>
      <td>Diesel</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1131</th>
      <td>Pune</td>
      <td>Volkswagen Polo GT TSI</td>
      <td>Petrol</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1132</th>
      <td>Pune</td>
      <td>Volkswagen Vento Petrol Highline</td>
      <td>Petrol</td>
      <td>2</td>
    </tr>
  </tbody>
</table>
<p>1133 rows × 4 columns</p>
</div>


