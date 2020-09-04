---
title: "Grouping and Sorting"
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
Location_Collected = df.groupby(['Name', 'Fuel_Type']).Kilometers_Driven.agg([len])
```


```python
Location_Collected = Location_Collected.reset_index()
Location_Collected = Location_Collected.sort_values(by = 'len')
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
      <th>Name</th>
      <th>Fuel_Type</th>
      <th>len</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Audi A3 35 TDI Attraction</td>
      <td>Diesel</td>
      <td>1</td>
    </tr>
    <tr>
      <th>450</th>
      <td>Maruti Dzire ZDI</td>
      <td>Diesel</td>
      <td>1</td>
    </tr>
    <tr>
      <th>451</th>
      <td>Maruti Eeco 5 STR With AC Plus HTR CNG</td>
      <td>CNG</td>
      <td>1</td>
    </tr>
    <tr>
      <th>453</th>
      <td>Maruti Ertiga SHVS VDI</td>
      <td>Diesel</td>
      <td>1</td>
    </tr>
    <tr>
      <th>456</th>
      <td>Maruti Ertiga VXI Petrol</td>
      <td>Petrol</td>
      <td>1</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>157</th>
      <td>Honda Brio S MT</td>
      <td>Petrol</td>
      <td>7</td>
    </tr>
    <tr>
      <th>169</th>
      <td>Honda City 1.5 V MT</td>
      <td>Petrol</td>
      <td>8</td>
    </tr>
    <tr>
      <th>737</th>
      <td>Volkswagen Polo 1.2 MPI Highline</td>
      <td>Petrol</td>
      <td>8</td>
    </tr>
    <tr>
      <th>484</th>
      <td>Maruti Swift Dzire VDI</td>
      <td>Diesel</td>
      <td>8</td>
    </tr>
    <tr>
      <th>419</th>
      <td>Maruti Alto LXi</td>
      <td>Petrol</td>
      <td>9</td>
    </tr>
  </tbody>
</table>
<p>768 rows × 3 columns</p>
</div>




```python
Location_Collected.sort_values(by = 'len', ascending=False)
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
      <th>Fuel_Type</th>
      <th>len</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>419</th>
      <td>Maruti Alto LXi</td>
      <td>Petrol</td>
      <td>9</td>
    </tr>
    <tr>
      <th>484</th>
      <td>Maruti Swift Dzire VDI</td>
      <td>Diesel</td>
      <td>8</td>
    </tr>
    <tr>
      <th>737</th>
      <td>Volkswagen Polo 1.2 MPI Highline</td>
      <td>Petrol</td>
      <td>8</td>
    </tr>
    <tr>
      <th>169</th>
      <td>Honda City 1.5 V MT</td>
      <td>Petrol</td>
      <td>8</td>
    </tr>
    <tr>
      <th>157</th>
      <td>Honda Brio S MT</td>
      <td>Petrol</td>
      <td>7</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>543</th>
      <td>Mercedes-Benz E-Class 250 D W 124</td>
      <td>Diesel</td>
      <td>1</td>
    </tr>
    <tr>
      <th>544</th>
      <td>Mercedes-Benz E-Class E 220 d</td>
      <td>Petrol</td>
      <td>1</td>
    </tr>
    <tr>
      <th>545</th>
      <td>Mercedes-Benz E-Class E240 V6 AT</td>
      <td>Petrol</td>
      <td>1</td>
    </tr>
    <tr>
      <th>547</th>
      <td>Mercedes-Benz E-Class E250 CDI Launch Edition</td>
      <td>Diesel</td>
      <td>1</td>
    </tr>
    <tr>
      <th>151</th>
      <td>Honda BR-V i-VTEC VX MT</td>
      <td>Petrol</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
<p>768 rows × 3 columns</p>
</div>




```python
Location_Collected.sort_index()
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
      <th>Fuel_Type</th>
      <th>len</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Audi A3 35 TDI Attraction</td>
      <td>Diesel</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Audi A3 35 TDI Premium Plus</td>
      <td>Diesel</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Audi A4 2.0 TDI</td>
      <td>Diesel</td>
      <td>5</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Audi A4 2.0 TDI 177 Bhp Technology Edition</td>
      <td>Diesel</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Audi A4 2.0 TDI Multitronic</td>
      <td>Diesel</td>
      <td>1</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>763</th>
      <td>Volvo S60 D5 Kinetic</td>
      <td>Diesel</td>
      <td>1</td>
    </tr>
    <tr>
      <th>764</th>
      <td>Volvo S80 D5</td>
      <td>Diesel</td>
      <td>1</td>
    </tr>
    <tr>
      <th>765</th>
      <td>Volvo V40 Cross Country D3</td>
      <td>Diesel</td>
      <td>1</td>
    </tr>
    <tr>
      <th>766</th>
      <td>Volvo XC60 D4 SUMMUM</td>
      <td>Diesel</td>
      <td>1</td>
    </tr>
    <tr>
      <th>767</th>
      <td>Volvo XC90 2007-2015 D5 AWD</td>
      <td>Diesel</td>
      <td>2</td>
    </tr>
  </tbody>
</table>
<p>768 rows × 3 columns</p>
</div>




```python
Location_Collected.sort_values(by = ['Name', 'len'])
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
      <th>Fuel_Type</th>
      <th>len</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Audi A3 35 TDI Attraction</td>
      <td>Diesel</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Audi A3 35 TDI Premium Plus</td>
      <td>Diesel</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Audi A4 2.0 TDI</td>
      <td>Diesel</td>
      <td>5</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Audi A4 2.0 TDI 177 Bhp Technology Edition</td>
      <td>Diesel</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Audi A4 2.0 TDI Multitronic</td>
      <td>Diesel</td>
      <td>1</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>763</th>
      <td>Volvo S60 D5 Kinetic</td>
      <td>Diesel</td>
      <td>1</td>
    </tr>
    <tr>
      <th>764</th>
      <td>Volvo S80 D5</td>
      <td>Diesel</td>
      <td>1</td>
    </tr>
    <tr>
      <th>765</th>
      <td>Volvo V40 Cross Country D3</td>
      <td>Diesel</td>
      <td>1</td>
    </tr>
    <tr>
      <th>766</th>
      <td>Volvo XC60 D4 SUMMUM</td>
      <td>Diesel</td>
      <td>1</td>
    </tr>
    <tr>
      <th>767</th>
      <td>Volvo XC90 2007-2015 D5 AWD</td>
      <td>Diesel</td>
      <td>2</td>
    </tr>
  </tbody>
</table>
<p>768 rows × 3 columns</p>
</div>


