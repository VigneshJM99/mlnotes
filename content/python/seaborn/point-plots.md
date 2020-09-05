---
title: "Point plots"
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
```


```python
sns.catplot(x="sex", y="survived", hue="class", kind="point", data=titanic);
```


![png](point-plots_3_0.png)



```python
sns.catplot(x="class", y="survived", hue="sex",
            palette={"male": "g", "female": "m"},
            markers=["^", "o"], linestyles=["-", "--"],
            kind="point", data=titanic);
```


![png](point-plots_4_0.png)

