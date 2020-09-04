---
title: "Grouping by apply()"
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
data = pd.read_excel('Car_Pricing.xlsx')
```


```python
data.groupby('Name').apply(lambda df: df.Kilometers_Driven.iloc[0])
```




    Name
    Audi A3 35 TDI Attraction                     84004
    Audi A3 35 TDI Premium Plus                   52300
    Audi A4 2.0 TDI                               46000
    Audi A4 2.0 TDI 177 Bhp Technology Edition    87001
    Audi A4 2.0 TDI Multitronic                   55000
                                                  ...  
    Volvo S60 D5 Kinetic                          70000
    Volvo S80 D5                                  87000
    Volvo V40 Cross Country D3                    60000
    Volvo XC60 D4 SUMMUM                          64000
    Volvo XC90 2007-2015 D5 AWD                   70000
    Length: 768, dtype: int64




```python
data.groupby(['Name']).Kilometers_Driven.agg([len, min, max])
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
      <th>len</th>
      <th>min</th>
      <th>max</th>
    </tr>
    <tr>
      <th>Name</th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Audi A3 35 TDI Attraction</th>
      <td>1</td>
      <td>84004</td>
      <td>84004</td>
    </tr>
    <tr>
      <th>Audi A3 35 TDI Premium Plus</th>
      <td>1</td>
      <td>52300</td>
      <td>52300</td>
    </tr>
    <tr>
      <th>Audi A4 2.0 TDI</th>
      <td>5</td>
      <td>21143</td>
      <td>70000</td>
    </tr>
    <tr>
      <th>Audi A4 2.0 TDI 177 Bhp Technology Edition</th>
      <td>1</td>
      <td>87001</td>
      <td>87001</td>
    </tr>
    <tr>
      <th>Audi A4 2.0 TDI Multitronic</th>
      <td>1</td>
      <td>55000</td>
      <td>55000</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>Volvo S60 D5 Kinetic</th>
      <td>1</td>
      <td>70000</td>
      <td>70000</td>
    </tr>
    <tr>
      <th>Volvo S80 D5</th>
      <td>1</td>
      <td>87000</td>
      <td>87000</td>
    </tr>
    <tr>
      <th>Volvo V40 Cross Country D3</th>
      <td>1</td>
      <td>60000</td>
      <td>60000</td>
    </tr>
    <tr>
      <th>Volvo XC60 D4 SUMMUM</th>
      <td>1</td>
      <td>64000</td>
      <td>64000</td>
    </tr>
    <tr>
      <th>Volvo XC90 2007-2015 D5 AWD</th>
      <td>2</td>
      <td>22230</td>
      <td>70000</td>
    </tr>
  </tbody>
</table>
<p>768 rows × 3 columns</p>
</div>


