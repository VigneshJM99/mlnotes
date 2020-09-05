---
title: "Boxplots"
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
sns.catplot(x="day", y="total_bill", kind="box", data=tips);
```


![png](boxplots_3_0.png)



```python
sns.catplot(x="day", y="total_bill", hue="smoker", kind="box", data=tips);
```


![png](boxplots_4_0.png)



```python
tips["weekend"] = tips["day"].isin(["Sat", "Sun"])
sns.catplot(x="day", y="total_bill", hue="weekend",
            kind="box", dodge=False, data=tips);
```


![png](boxplots_5_0.png)



```python
diamonds = sns.load_dataset("diamonds")
sns.catplot(x="color", y="price", kind="boxen",
            data=diamonds.sort_values("color"));
```


![png](boxplots_6_0.png)



```python

```
