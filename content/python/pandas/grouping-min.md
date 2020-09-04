---
title: "Grouping-min"
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
df.groupby('Kilometers_Driven').Kilometers_Driven.min()
```




    Kilometers_Driven
    1000        1000
    1001        1001
    1015        1015
    1520        1520
    2890        2890
               ...  
    196000    196000
    200000    200000
    205000    205000
    290000    290000
    350000    350000
    Name: Kilometers_Driven, Length: 755, dtype: int64


