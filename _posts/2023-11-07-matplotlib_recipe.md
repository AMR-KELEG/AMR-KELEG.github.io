---
layout: post
title: A recipe for matplotlib figures
date: 2023-11-07
description: How I make my figures fancier 😌
---

## General Setup

I use the following parameters for my plots.

```
import matplotlib
import matplotlib.pyplot as plt

# Set the font of the general labels to 7.
# Note: This generally works for my *CL papers,
# for which the default caption font size is 10.
font = {"size": 7}
matplotlib.rc("font", **font)

# Remove some of the sides of the plot's frame
matplotlib.rcParams["axes.spines.left"] = True
matplotlib.rcParams["axes.spines.right"] = False
matplotlib.rcParams["axes.spines.top"] = False
matplotlib.rcParams["axes.spines.bottom"] = False

# Allow using tex in labels and titles
# Note: This requires the system to have some tex dependencies installed
matplotlib.rcParams["text.latex.preamble"] = [r"\boldmath"]
```

## Figure Size

```
TODO
```

## Legend
I generally prefer frameless legends, setting the following flag `frameon=False`.

```
plt.legend(frameon=False)
```

A hack for changing the order of the labels.

```
# Check the labels for the current diagram
handles, labels = plt.gca().get_legend_handles_labels()

# Set the order after checking their default order in the plot
# This requires the knowledge of the default order 
# (i.e.: generating the plot before updating the order)
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

Using **tight layout** fixes the positions of labels and axes ticks in the exported figure

```
plt.savefig("fig1.pdf", bbox_inches="tight")
```

Note: Exported pdfs can not have transparent backgrounds, so I change the background for the plot into the color I am expecting as follows

```
TODO!
``` 

## Annotations

```
TODO!
```

## Some remarks about matplotlib

* `plt.gca()` returns the current active axis, which is useful for executing axes' commands.
