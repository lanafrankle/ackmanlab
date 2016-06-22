---
date: 2016-06-20 10:53:56  
tags: python, opencv, numpy, data analysis  
author: James B. Ackman  
layout: post
title: Setup jupyter notebook/ipython  
---

## Install and setup anaconda python

Download [Anaconda](https://www.continuum.io/downloads) and run the installer. This can be done using the graphical installer on a local laptop/workstation or if you are logged into a linux computing server use: 

```bash
# change the following url to the most recent one from https://repo.continuum.io/archive/
wget http://repo.continuum.io/archive/Anaconda3-4.0.0-Linux-x86_64.sh #download the installer
bash Anaconda3-4.0.0-Linux-x86_64.sh #run the installer script
export PATH=/afs/cats.ucsc.edu/users/n/jackman/anaconda3/bin:$PATH #append to your path so you can use conda to create environment below
```

Then from your command-line environment (e.g. linux Terminal on OS X, check out the [unix tricks/tutorial](https://gist.github.com/ackman678/6290329)), create a new python environment:

```bash
conda create --name py35 python=3 anaconda
#conda create --name py27 python=2.7 anaconda #if you want to install python 2.7 use this line instead. useful for opencv usage on linux cluster
```


## Install extra modules with conda

Next, activate your new environment and install a couple add on modules:  

```bash
source activate py35
conda install opencv
conda install h5py
conda install tifffile -c conda-forge
conda install joblib
```

opencv  
: computer vision library  
: [tutorial](http://docs.opencv.org/3.0-beta/doc/py_tutorials/py_tutorials.html)  

h5py  
: read/write support for hdf5  
: read matlab v7.3 files  
: fixes other hdf5 dependencies (like cv2)  

tifffile  
: read in multi-page tiff files (time-lapse movies or multi-channel images)  
: though tifffile.py is [already a part of scikit-image](https://github.com/scikit-image/scikit-image/blob/master/skimage/external/tifffile/tifffile.py), so this extra installation may not be necessary.  

joblib  
: a parallel computing module  
: useful with multicore compute nodes  

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

