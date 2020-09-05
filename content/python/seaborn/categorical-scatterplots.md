---
title: "Categorical scatterplots"
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
sns.catplot(x="day", y="total_bill", data=tips);
```


![png](categorical-scatterplots_2_0.png)



```python
sns.catplot(x="day", y="total_bill", jitter=False, data=tips);
```


![png](categorical-scatterplots_3_0.png)



```python
sns.catplot(x="day", y="total_bill", kind="swarm", data=tips);
```


![png](categorical-scatterplots_4_0.png)



```python
sns.catplot(x="day", y="total_bill", hue="sex", kind="swarm", data=tips);
```


![png](categorical-scatterplots_5_0.png)



```python
sns.catplot(x="size", y="total_bill", kind="swarm",
            data=tips.query("size != 3"));
```


![png](categorical-scatterplots_6_0.png)



```python
sns.catplot(x="smoker", y="tip", order=["No", "Yes"], data=tips);
```


![png](categorical-scatterplots_7_0.png)



```python
sns.catplot(x="total_bill", y="day", hue="time", kind="swarm", data=tips);
```


![png](categorical-scatterplots_8_0.png)

