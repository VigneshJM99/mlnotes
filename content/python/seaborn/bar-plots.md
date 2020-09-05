---
title: "Bar plots"
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
titanic = sns.load_dataset("titanic")
sns.catplot(x="sex", y="survived", hue="class", kind="bar", data=titanic);
```


![png](bar-plots_2_0.png)



```python
sns.catplot(x="deck", kind="count", palette="ch:.25", data=titanic);
```


![png](bar-plots_3_0.png)



```python
sns.catplot(y="deck", hue="class", kind="count",
            palette="pastel", edgecolor=".6",
            data=titanic);
```


![png](bar-plots_4_0.png)

