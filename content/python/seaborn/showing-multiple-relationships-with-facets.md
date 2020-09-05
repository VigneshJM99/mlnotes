---
title: "Showing multiple relationships with facets"
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
sns.relplot(x="total_bill", y="tip", hue="smoker",
            col="time", data=tips);
```


![png](showing-multiple-relationships-with-facets_2_0.png)



```python
fmri = sns.load_dataset("fmri")
sns.relplot(x="timepoint", y="signal", hue="subject",
            col="region", row="event", height=3,
            kind="line", estimator=None, data=fmri);
```


![png](showing-multiple-relationships-with-facets_3_0.png)



```python
sns.relplot(x="timepoint", y="signal", hue="event", style="event",
            col="subject", col_wrap=5,
            height=3, aspect=.75, linewidth=2.5,
            kind="line", data=fmri.query("region == 'frontal'"));
```


![png](showing-multiple-relationships-with-facets_4_0.png)

