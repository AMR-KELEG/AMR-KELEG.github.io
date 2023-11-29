---
layout: post
title: A recipe for matplotlib figures
date: 2023-11-07
description: How I make my figures fancier 😌
---

## General setup
```
import matplotlib
import matplotlib.pyplot as plt

font = {"size": 7}
matplotlib.rc("font", **font)
matplotlib.rcParams["axes.spines.left"] = True
matplotlib.rcParams["axes.spines.right"] = False
matplotlib.rcParams["axes.spines.top"] = False
matplotlib.rcParams["axes.spines.bottom"] = False
matplotlib.rcParams["text.latex.preamble"] = [r"\boldmath"]
```

## Legend
- Using `frameon=False` is genrally nicer

```
plt.legend(frameon=False)
```

- A hack for changing the order of the labels
```
# Check the labels for the current diagram
handles, labels = plt.gca().get_legend_handles_labels()

# Set the order after checking their default order in the plot
order = [2, 1, 0, 3, 4]

plt.legend(
    [handles[idx] for idx in order],
    [labels[idx] for idx in order],
    title="LEGEND_TITLE",
    frameon=False,
    prop={"size": 6}, # The size of the text within the legend
    handlelength=0.8,
)
```

## Exporting to pdf
- Using **tight layout** fixes the positions of labels and axes ticks in the exported figure
```
plt.savefig("fig1.pdf", bbox_inches="tight")
```

- Note: Exported pdfs can not have transparent backgrounds, so I change the background for the plot into the color I am expecting as follows
```
TODO!
``` 

## Some remarks about matplotlib
- `plt.gca()` returns the current active axis.
