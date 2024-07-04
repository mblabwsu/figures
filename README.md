# figures
Example code to make figures for publications

To make publication quality figures in matplotlib takes a bit of work, but is well worth the effort. 

```
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib as mpl
import matplotlib.pyplot as plt
from scipy import stats

settings = {
    'figure.dpi': 300,
    'figure.subplot.left': 0,
    'figure.subplot.right': 1,
    'figure.subplot.top': 1,
    'figure.subplot.bottom': 0,
    'figure.subplot.hspace': 0.0,
    'figure.subplot.wspace': 0.0,
    'font.family': 'Arial',
    'font.size': 6.5,
    'lines.linewidth': 0.5,
    'lines.markersize': 3,
    'patch.linewidth': 0.5,
    'axes.linewidth': 0.5,
    'axes.spines.bottom': 'on',
    'axes.spines.left': 'on',
    'axes.spines.top': 'off',
    'axes.spines.right': 'off',
    'axes.labelweight': 'normal',
    'axes.xmargin': 0.02,
    'axes.ymargin': 0.02,
    'axes.grid': 'off',
    'axes.labelpad': 2,
    'axes.titlepad': 2,
    #'axes.prop_cycle': cycler(color=['r', 'g', 'b', 'y']),
    'xtick.major.size': 2.5,
    'ytick.major.size': 2.5,
    'xtick.major.width': 0.5,
    'ytick.major.width': 0.5,
    'xtick.major.pad': 1.5,
    'ytick.major.pad': 1.5,
    'legend.frameon': True,
    # 'legend.edgecolor': gray,
    # 'legend.columnspacing': 
    'pdf.fonttype': 42,
    'ps.fonttype': 42,
    }


mpl.rcParams.update(mpl.rcParamsDefault)
for k,v in settings.items():
    mpl.rcParams[k] = settings[k]

# Choose a color pallette with sns.set_pallette(pallette_name)
# alternatively, use the pallette keyword in plots to set specific colors
# Palletes can be found here
# https://seaborn.pydata.org/generated/seaborn.color_palette.html
# Deep is a popular pallette
# Other options:
# deep, muted, pastel, bright, colorblind, dark
# Set2, rainbow, seismic, tab10, tab20, tab20c
sns.set_palette('deep')

```

