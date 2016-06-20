---
date: 2016-06-20 10:53:56  
tags: python, opencv, numpy, data analysis  
author: James B. Ackman  
layout: post
title: Setup jupyter notebook/ipython  
---

## Install and setup anaconda python

Download [Anaconda](https://www.continuum.io/downloads) and run the installer.

From your command-line environment (e.g. Terminal on OS X, check out the [unix tricks/tutorial](https://gist.github.com/ackman678/6290329)), create a new python environment:

```bash
conda create --name py35 python=3 anaconda
```


## Install extra modules with conda

Next, activate your new environment and install a couple add on modules:  

```bash
source activate py35
conda install opencv
conda install tifffile -c conda-forge
conda install joblib
```

tifffile
: read in multi-page tiff files (time-lapse movies or multi-channel images)
: though tifffile.py is [already a part of scikit-image](https://github.com/scikit-image/scikit-image/blob/master/skimage/external/tifffile/tifffile.py), so this extra installation may not be necessary.

joblib
: a parallel computing module

## Run jupyter notebook/ipython

Then whenever you want to use your python 3 environment, first activate your environment (if it's not already active-- `source activate py35`) and enter: 

```bash
jupyter notebook
```

Then from the webserver [jupyter notebook/ipython](https://ipython.org/) session in your web browser click on new Python notebook:  
![]({{site.data_path}}/Screen_Shot_2016-06-20_at_11.16.24_AM.png)

This will open a new python session where you paste and run code (*control-enter* evaluates the current cell, *shift-enter* evaluates and moves to a new cell):  

```python
import cv2
import numpy as np

print("OpenCV Version : {0}".format(cv2.__version__))
print("Numpy Version : {0}".format(np.__version__))
```

>OpenCV Version : 3.1.0  
>Numpy Version : 1.10.4  


![]({{site.data_path}}/Screen_Shot_2016-06-20_at_11.13.40_AM.png)

To shut down your session go to *File --> Close and Halt*.

Then from your command-line shell from which the webserver is running, press *control-c* to interrupt/stop.

