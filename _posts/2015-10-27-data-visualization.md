---
title: Data Visualization
author: James B. Ackman
layout: post
date: 2014-04-26 04:50:10  
update: 2015-10-27 14:27:22  
tags: open science, research, open source, software development, markdown, data sharing, database, visualization  
---


Web development tools for interactive data visualization. These are notes originally from a previous [post]({% post_url 2014-04-26-open_science %}).

Cool gist hack. A [bl.ocks.org](http://bl.ocks.org) is a viewer for github gists if you have it titled index.html. People have used this to render beautiful plots and graphs using [D3](http://d3js.org).

D3 uses vocabulary that comes from webstandards of html, css, and svg. An alternative project is [Processing.js](http://processing.org/examples/), which can do alot, but is a whole different set of methods. 

* Here is an implementation of OpenCV in processing.js](https://github.com/atduskgreg/opencv-processing)
* Processing is big in artistic, computational visualizations

D3 basically uses html, css, and svg to produce nice graphics for quantitative data.

Check out this [beautiful matrix with different ordering options](http://bost.ocks.org/mike/miserables/) rendered using D3 on a Les miserables co-occurence dataset from Donald Knuth.

Mike Bostock is the author [github/mbostock](https://github.com/mbostock/d3/wiki/Gallery)

[boxplot visualizations using d3](http://bl.ocks.org/mbostock/)


## Web visualization with R bindings

[plotly library](https://github.com/ropensci/plotly) for interactive graphs in webbrowser. With python, R, matlab.

Contour plots of the volcano dataset using [R --> json --> D3](http://vis.supstat.com/2012/11/contour-plots-with-d3-and-r/).

[Why we don't yet have interactive graphics](http://www.biostat.wisc.edu/~kbroman/talks/InteractiveGraphs/). Comments about Hadley Wickham working on interactive versions of ggplot. D3 is the best option right now, but javascript based. 

http://timelyportfolio.github.io/gridSVG_intro/


[Simple examples combing R, gridSVG package and d3.js](http://timelyportfolio.github.io/gridSVG_intro/) to make interactive graphics (tool tips on a scatterplot) from any grid based graphics in R (lattice or ggplot2)


[Shiny package](http://shiny.rstudio.com/gallery) by RStudio might be the way to go for now with R plots. e.g. [here is a matrix with hierarchical clustering](http://shiny.rstudio.com/gallery/absolutely-positioned-panels.html) on the sides. Could have toggles for different orders.  Same with the graphs.


