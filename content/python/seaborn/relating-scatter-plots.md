---
title: "Relating Variables With Scatter Plots"
author: "Vignesh J M"
date: 2020-09-04
description: "-"
type: technical_note
draft: false
---

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
sns.set(style="darkgrid")
```


```python
tips = sns.load_dataset("tips")
sns.relplot(x="total_bill", y="tip", data=tips);
```


![png](relating-scatter-plots_2_0.png)



```python
sns.relplot(x="total_bill", y="tip", hue="smoker", data=tips);
```


![png](relating-scatter-plots_3_0.png)



```python
sns.relplot(x="total_bill", y="tip", hue="smoker", style="smoker",
            data=tips);
```


![png](relating-scatter-plots_4_0.png)



```python
sns.relplot(x="total_bill", y="tip", hue="smoker", style="time", data=tips);
```


![png](relating-scatter-plots_5_0.png)



```python
sns.relplot(x="total_bill", y="tip", hue="size", data=tips);
```


![png](relating-scatter-plots_6_0.png)



```python
sns.relplot(x="total_bill", y="tip", hue="size", palette="ch:r=-.5,l=.75", data=tips);
```


![png](relating-scatter-plots_7_0.png)



```python
sns.relplot(x="total_bill", y="tip", size="size", data=tips);
```


![png](relating-scatter-plots_8_0.png)



```python
sns.relplot(x="total_bill", y="tip", size="size", sizes=(15, 200), data=tips);
```


![png](relating-scatter-plots_9_0.png)

