---
title: "Aggregation And Representing Uncertainity"
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
fmri = sns.load_dataset("fmri")
sns.relplot(x="timepoint", y="signal", kind="line", data=fmri);
```


![png](agg-rep-unc_2_0.png)



```python
sns.relplot(x="timepoint", y="signal", ci=None, kind="line", data=fmri);
```


![png](agg-rep-unc_3_0.png)



```python
sns.relplot(x="timepoint", y="signal", kind="line", ci="sd", data=fmri);
```


![png](agg-rep-unc_4_0.png)



```python
sns.relplot(x="timepoint", y="signal", estimator=None, kind="line", data=fmri);
```


![png](agg-rep-unc_5_0.png)



```python

```


```python

```
