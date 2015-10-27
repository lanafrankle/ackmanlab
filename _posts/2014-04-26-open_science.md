---
title: Open science
layout: post
Date: 2014-04-26 04:50:10  
Tags: science, research, peer review, literature, opinion, open source, software development, markdown, data sharing, database  
---

[open data repository](http://datadryad.org) used for cboettingers publications.

[ropen science hackathon](http://simplystatistics.org/2014/04/10/the-ropensci-hackathon-ropenhack/). ropenscience is a big grant that cboettinger is part of.

[R ipython notebook bindings project](https://github.com/takluyver/IRkernel)

[hacker school sounds awesome](https://www.hackerschool.com)

On application page:  

>Write a program that prints out the numbers 1 to 100 (inclusive). If the number is divisible by 3, print Crackle instead of the number. If it's divisible by 5, print Pop. If it's divisible by both 3 and 5, print CracklePop. You can use any language.


[plotly library](https://github.com/ropensci/plotly) for interactive graphs in webbrowser. With python, R, matlab.

[http://software-carpentry.org/v4/data/mgmt.html](http://software-carpentry.org/v4/data/mgmt.html)


# Data visualization

Cool gist hack. A [bl.ocks.org](http://bl.ocks.org) is a viewer for github gists if you have it titled index.html. People have used this to render beautiful plots and graphs using [D3](http://d3js.org).

D3 uses vocabulary that comes from webstandards of html, css, and svg. An alternative project is [Processing.js](http://processing.org/examples/), which can do alot, but is a whole new vocabulary. 

* Actually here is an implementation of OpenCV in processing.js](https://github.com/atduskgreg/opencv-processing)
* Processing seems to be big in artistic, computational visualizations

D3 basically uses html, css, and svg to produce nice graphics for quantitative data.

Check out this [beautiful matrix with different ordering options](http://bost.ocks.org/mike/miserables/) rendered using D3 on a Les miserables co-occurence dataset from Donald Knuth.

Mike Bostock is the author [github/mbostock](https://github.com/mbostock/d3/wiki/Gallery)


[boxplot visualization using d3](http://bl.ocks.org/mbostock/40615020)



Contour plots of the volcano dataset using [R --> json --> D3](http://vis.supstat.com/2012/11/contour-plots-with-d3-and-r/).

[Why we don't yet have interactive graphics](http://www.biostat.wisc.edu/~kbroman/talks/InteractiveGraphs/). Comments on hadley wickham working on interactive versions of ggplot. D3 is the best option right now, but pretty low level and several thins that need to be learned, like javascript. 

http://timelyportfolio.github.io/gridSVG_intro/


[Simple examples combing R, gridSVG package and d3.js](http://timelyportfolio.github.io/gridSVG_intro/) to make interactive graphics (tool tips on a scatterplot) from any grid based graphics in R (lattice or ggplot2)


[Shiny package](http://shiny.rstudio.com/gallery) by RStudio might be the way to go for now with my R plots.   e.g. [here is a matrix with hierarchal clustering](http://shiny.rstudio.com/gallery/absolutely-positioned-panels.html) on the sides. Could have toggles for different orders.  Same with the graphs.





# Open models database

http://physiomeproject.org/software/cm

http://models.physiomeproject.org/welcome

[output to different languages, incl C, fortran, matlab, python](http://models.physiomeproject.org/e/44/tabak_mascagni_bertram_2010.cellml/@@cellml_codegen)

[model of spontaneous activity in developing networks](http://models.physiomeproject.org/e/44/tabak_mascagni_bertram_2010.cellml/@@docgen)

Curated from 
>Joel Tabak, Michael Mascagni, Richard Bertram, 2010, Journal of Neurophysiology, volume 103, 2208-2221. PubMed ID: 20164396




#  Data management tools

2015-02-25 17:01:22


## Permanent repositories

Both of these are supported exports from [rOpenScience](http://ropensci.org)

[DataONE](https://www.dataone.org/best-practices).  Collab between NSF, UC Santa Barbra, Univ New Mexico, Oak Ridge, etc. Like fig share but bigger more flexible?
http://figshare.com


[DMPTool](https://dmp.cdlib.org) from UC Digital Library for creating data management plans for funding agencies-- for collection and storage during and after projects.

UC3 from University of California Digital Library






# Hierarchical information visualization

[MySQL Workbench](http://dev.mysql.com/downloads/workbench/) is [highly recommended](http://apple.stackexchange.com/questions/82592/is-there-a-good-sql-diagram-editor-drawing-mac-app-tool)

But people have also used [Omnigraffle](https://www.omnigroup.com/omnigraffle/), a classic graphviz based drawling/outlining/layout program for Mac OSX?  Lots of nice graphics stencils (including programming, hardware, software, site design) at [graffletopia](https://www.graffletopia.com/categories/programming)

Stencil for drawing [IDEF1X compliant data models using IEEE notation (crows feet)](https://www.graffletopia.com/stencils/588):

![](/assets/Screen_Shot_2015-08-10_at_11.38.16_AM.png)


Some people have used it for [MySQL visualization](http://mabblog.com/blog/2012/03/scripting-omnigraffle-mysql-json-visualization/) and export an omnigraffle hierarchy

[Gist for a Python script to convert MySQL table to omnigraffle](https://gist.github.com/iloveitaly/1486762).  Uses appscript for the omnigraffle Applescript bindings in the Pro version.

Here is a [gist for a ruby script that uses OSX scripting bridge to pull hierarchical omnigraffle document data to JSON](https://gist.github.com/iloveitaly/1487305)





# Synapse

Talk (2013) by Stephen Friend at 10th annual Allen Brain Institute symposium (at youtube) on need for github for science. Introduces [Synapse'](http://sagebase.org/synapse/) is a platform which is supposed to be just that.

![](/figures/Screen_Shot_2015-08-28_at_2.29.53_PM.png)
![](/figures/Screen_Shot_2015-08-28_at_2.29.04_PM.png)
![](/figures/Screen_Shot_2015-08-28_at_2.28.56_PM.png)
![](figures/Screen_Shot_2015-08-28_at_2.28.48_PM.png)
![](figures/Screen_Shot_2015-08-28_at_2.28.43_PM.png)


[Core code is on Github](http://gitub.com/Sage-Bionetworks/)

[https://www.synapse.org/#!Wiki:syn2305384/ENTITY](https://www.synapse.org/#!Wiki:syn2305384/ENTITY)

>for biomedical data scientists we have created an environment that aids these users in sharing all of their digital research assets including data, code, and analysis results. These assets can be broadly shared and accessed through a unified set of RESTful APIs – through which Synapse provides integration points in R, Python, and the Linux shell in order to enable dissemination of findings across common analytical environments.   

> Furthermore, Synapse provides advanced capabilities for formally tracking the relationship between these digital assets through the Synapse provenance system, and for documenting and disseminating their work in ways that others can reproduce and reuse. These capabilities are key in supporting larger research teams, such as the 200+ scientists that collaborated through Synapse as part of the TCGA Pan Cancer Analysis Working Group.

>Second, for clinical and biological scientists we have focused on developing Synapse as a community hub that creates a partnership between computational / analytical users and the more biologically / clinically minded scientists. In particular, the Synapse web portal is designed to enhance this communication and grow communities of scientists with diverse skill sets that can work together to interpret complex and diverse biomedical data sets.



Sage Bionetworks also makes 'Bridge Server'.  Pages on Confluence and Github:  

>Sage Bionetworks’ Bridge Server is designed to securely manage data captured from IRB-approved human health research studies conducted through mobile technology platforms.





[NeuroDebian linux distro](http://neuro.debian.net/index.html#how-to-use-this-repository) with python psychophysics, electrophysiology, mri, and dataset access software installed. 


[scalable mouse brain atlas](http://scalablebrainatlas.incf.org/main/index.php?)


[map of developing human brain, atlas](http://www.brainspan.org/static/atlas)  Same vtk visualization of connectivity as in mouse brain atlas.


[Jupyter, Docker Sage notebook like interface for teaching](https://developer.rackspace.com/blog/deploying-jupyterhub-for-education/). More info and python hacking tips for cognitive neuroscience and teaching at a [octopress blog at berkeley](http://www.jesshamrick.com/2014/03/24/deploying-jupyterhub-for-education/)

[the new ipython, jupyter](http://jupyter.org/about.html)


