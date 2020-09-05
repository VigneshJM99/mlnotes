---
title: "violinplots"
author: "Vignesh J M"
date: 2020-09-04
description: "-"
type: technical_note
draft: false
---

```python
import seaborn as sns
import matplotlib.pyplot as plt
sns.set(style="ticks", color_codes=True)
```


```python
tips = sns.load_dataset("tips")
```


```python
sns.catplot(x="total_bill", y="day", hue="sex",
            kind="violin", data=tips);
```


![png](violinplots_3_0.png)



```python
sns.catplot(x="total_bill", y="day", hue="sex",
            kind="violin", bw=.15, cut=0,
            data=tips);
```


![png](violinplots_4_0.png)



```python
sns.catplot(x="day", y="total_bill", hue="sex",
            kind="violin", split=True, data=tips);
```


![png](violinplots_5_0.png)



```python
sns.catplot(x="day", y="total_bill", hue="sex",
            kind="violin", inner="stick", split=True,
            palette="pastel", data=tips);
```


![png](violinplots_6_0.png)



```python
g = sns.catplot(x="day", y="total_bill", kind="violin", inner=None, data=tips)
sns.swarmplot(x="day", y="total_bill", color="k", size=3, data=tips, ax=g.ax);
```


![png](violinplots_7_0.png)

