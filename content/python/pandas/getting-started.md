---
title: "Getting Started"
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
pd.DataFrame({'Yes': [50, 21], 'No': [131, 2]})
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
      <th>Yes</th>
      <th>No</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>50</td>
      <td>131</td>
    </tr>
    <tr>
      <th>1</th>
      <td>21</td>
      <td>2</td>
    </tr>
  </tbody>
</table>
</div>




```python
pd.DataFrame({'Bob': ['I liked it.', 'It was awful.'], 'Sue': ['Pretty good.', 'Bland.']})
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
      <th>Bob</th>
      <th>Sue</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>I liked it.</td>
      <td>Pretty good.</td>
    </tr>
    <tr>
      <th>1</th>
      <td>It was awful.</td>
      <td>Bland.</td>
    </tr>
  </tbody>
</table>
</div>




```python
pd.DataFrame({'Bob': ['I liked it.', 'It was awful.'], 
              'Sue': ['Pretty good.', 'Bland.']},
             index=['Product A', 'Product B'])
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
      <th>Bob</th>
      <th>Sue</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Product A</th>
      <td>I liked it.</td>
      <td>Pretty good.</td>
    </tr>
    <tr>
      <th>Product B</th>
      <td>It was awful.</td>
      <td>Bland.</td>
    </tr>
  </tbody>
</table>
</div>




```python
pd.Series([1, 2, 3, 4, 5])
```




    0    1
    1    2
    2    3
    3    4
    4    5
    dtype: int64


