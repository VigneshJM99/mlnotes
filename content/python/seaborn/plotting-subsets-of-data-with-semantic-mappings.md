---
title: "Plotting subsets of data with semantic mappings"
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
sns.relplot(x="timepoint", y="signal", hue="event", kind="line", data=fmri);
```


![png](plotting-subsets-of-data-with-semantic-mappings_2_0.png)



```python
sns.relplot(x="timepoint", y="signal", hue="region", style="event",
            kind="line", data=fmri);
```


![png](plotting-subsets-of-data-with-semantic-mappings_3_0.png)



```python
sns.relplot(x="timepoint", y="signal", hue="region", style="event",
            dashes=False, markers=True, kind="line", data=fmri);
```


![png](plotting-subsets-of-data-with-semantic-mappings_4_0.png)



```python
sns.relplot(x="timepoint", y="signal", hue="event", style="event",
            kind="line", data=fmri);
```


![png](plotting-subsets-of-data-with-semantic-mappings_5_0.png)



```python
sns.relplot(x="timepoint", y="signal", hue="region",
            units="subject", estimator=None,
            kind="line", data=fmri.query("event == 'stim'"));
```


![png](plotting-subsets-of-data-with-semantic-mappings_6_0.png)



```python
dots = sns.load_dataset("dots").query("align == 'dots'")
sns.relplot(x="time", y="firing_rate",
            hue="coherence", style="choice",
            kind="line", data=dots);
```


![png](plotting-subsets-of-data-with-semantic-mappings_7_0.png)



```python
dots = sns.load_dataset("dots").query("align == 'dots'")
sns.relplot(x="time", y="firing_rate",
            hue="coherence", style="choice",
            kind="line", data=dots);

```


![png](plotting-subsets-of-data-with-semantic-mappings_8_0.png)



```python
palette = sns.cubehelix_palette(light=.8, n_colors=6)
sns.relplot(x="time", y="firing_rate",
            hue="coherence", style="choice",
            palette=palette,
            kind="line", data=dots);
```


![png](plotting-subsets-of-data-with-semantic-mappings_9_0.png)



```python
from matplotlib.colors import LogNorm
palette = sns.cubehelix_palette(light=.7, n_colors=6)
sns.relplot(x="time", y="firing_rate",
            hue="coherence", style="choice",
            hue_norm=LogNorm(),
            kind="line", data=dots);
```


![png](plotting-subsets-of-data-with-semantic-mappings_10_0.png)



```python
sns.relplot(x="time", y="firing_rate",
            size="coherence", style="choice",
            kind="line", data=dots);
```


![png](plotting-subsets-of-data-with-semantic-mappings_11_0.png)



```python
sns.relplot(x="time", y="firing_rate",
           hue="coherence", size="choice",
           palette=palette,
           kind="line", data=dots);
```


![png](plotting-subsets-of-data-with-semantic-mappings_12_0.png)



```python

```
