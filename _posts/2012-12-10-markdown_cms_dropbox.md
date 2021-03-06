---
author: James Ackman  
title: Write with Markdown  
layout: post  
date: 2016-01-28 13:23:28  
date original: 2012-12-10  
tags: markdown, cms, dropbox, website, lab, notebook, html5, git, open science, openscience  
---

Markdown is a set of simple rules for writing text documents. Benefits include:  

* Plain text (future proof!)
* Simple [syntax](http://daringfireball.net/projects/markdown/syntax), human readable
* Wide community support and usage (e.g. GitHub, Tumblr, etc) by both bloggers and programmers
* Supported by wikis (like MediaWiki) and many tools (see below) for producing content rich in links, graphics, tables, references, and more.


## Writing for the web, not the desktop

All the content we now produce lives mostly on the web and *sometimes* on paper. So when it comes to designing and creating content we should [move away from the world of 'paper document' layouts](http://www.tedcurran.net/2012/10/why-write-for-paper-or-how-i-learned-to-stop-worrying-and-love-html/) -- i.e we should stop forcing our initially created content into 8.5" x 11" or A4 page layouts. Instead, write documents (mixed with text, images, links, etc) with a simple set of structured rules (e.g. Markdown) which then allows for flexible conversion downstream into multiple types of documents: html, pdf, Word, etc.

[Why markdown](http://www.tedcurran.net/2012/09/using-markdown-a-quicker-way-to-write-for-the-web/)


## Markdown tools

* [Multimarkdown](http://fletcherpenney.net/multimarkdown/) is an extended version of markdown with nice citation and table support. Very nice for academic writing needs.
* [pandoc](http://pandoc.org/) Universal document converter to/from different formats. For example markup languages (e.g. Markdown, MediaWiki, reStructuredText), LaTeX, html, LibreOffice, Microsoft Word...
* github, jekyll, octopress: version control + collaboration, site generation, content management.
* Many easy to use GUI apps exist for rendering Markdown on OSX, iOS, Android, Linux, Windows
	* [Marked](http://marked2app.com/) is one. Powerful and super flexible markdown/multimarkdown document previewer/exporter. Highly recommended if you are on Mac OSX.
		* Manuscript preparation [using multiple .md documents in Marked](http://marked2app.com/help/Multi-File_Documents.html)
			* Option for paper writing with or without Scrivener
* App called Drafts featured at lifehacker for iOS. Powerful and flexible. Also simplenote, **nvAlt** for Mac, resophNotes for Windows


Additional tools workflow examples:  

* Wiki cms powered by MediaWiki for a lab:  
	- [Wiki educator example lab webpage](http://wikieducator.org/User:Cooper_lab)
* [Remembering stuff workflow by Brett Terpstra](http://brettterpstra.com/forget-about-it-or-not/)
	- [Project system on gitHub](http://ttscoff.github.com/QuickQuestion/)
* [nvAlt on Tumbler](http://www.tumblr.com/tagged/nvalt)
* Personal wiki software list [personal wiki info](http://physbank.referata.com/wiki/Personal_Wiki_Software)
	- [DesktopWiki](http://c2.com/cgi/wiki?DesktopWiki)	
* [instiki](http://golem.ph.utexas.edu/wiki/instiki/show/HomePage)
* [azimuth](http://www.azimuthproject.org/azimuth/show/Self-organization)



### Dropbox CMS

Notes from an [article on lifehacker](http://lifehacker.com/5860139/host-web-pages-for-free-within-dropbox-with-droppages-or-pancakeio) on dropbox public website cms services.

With all these services they are best for small websites, not for big organizations or ones with lots of page hits as there is a dropbox limit per day and your account can get suspended.

* [Pancake](http://Pancake.io/)
	- Preview common files like word, pdf documents right in browser
	- works with html, js, css, and plain text
	- 'free to sign up'
* [DropPages](http://droppages.com/)
	- markdown friendly
	- content gzipped and cached for best performance possible.
* [VoodooPad](http://flyingmeat.com/voodoopad/)
	- Personal wiki
	- MacOS and iOS
	- tons of export options
	- sketching
	- unix shell scripting executiable
	- markdown friendly
	- project management



## Lab notebooks in markdown 

Open science initiative using git, github, R, knitr.  Git based **distributed version control** is key to this sort of open project (software - science - data - documentation - manuscript) workflow. [A more technical explanation of git magic](http://www-cs-students.stanford.edu/~blynn/gitmagic/ch08.html).

Since a large number of scientific projects these days require substantial data analysis with interactive programming languages like R and python, mixing a structured markup language like markdown with the program interpreter is a very powerful way forward to helping achieve truly reproducible research (together with version control). Tools like [jupyter/ipython notebook](http://jupyter.org/), Rstudio, and [ropensci](http://ropensci.org) do exactly this and can be very helpful in this regard.


Here is an [example lab-notebook from C. Boettiger](http://carlboettiger.info/lab-notebook.html) with [github project hosting]((https://github.com/cboettig).

[nvAlt git selective note sharing](http://afitnerd.com/2011/07/28/notational-velocity-git-team-note-sharing/)





## Markdown to html5 presentations

### Popular html presentation solutions

[from tedcurran.net](http://www.tedcurran.net/2013/02/making-html5-presentations-in-the-cloud-with-markdown-rvl-io/):  

>Highly technical GitHub dwellers have long used HTML5 presentations like Impress,js, Reveal.js, and Google’s HTML5 Rocks Presentations to impress fellow hackers with lean, well designed code and hand-tooled design.

[slid.es](http://slides.com/)

Some are trying to emulate the non-linear prezi format. Some give traditional slide based formatting to markdown documents.

impress.js

[reveal.js](http://lab.hakim.se/reveal-js/#/)  [download latest release](https://github.com/hakimel/reveal.js/releases)

[MarkdownPresenter](https://github.com/chrishulbert/MarkdownPresenter)



### Reveal.js example

Define slides in index.html using external markdown. Notice the separator could be changed to something else, like a markdown hr:  "^\n---\n"

	<section data-markdown="example.md"  
	         data-separator="^\n\n\n"  
	         data-vertical="^\n\n"  
	         data-notes="^Note:"  
	         data-charset="iso-8859-15">
	</section>

From [reveal.js github readme](https://github.com/hakimel/reveal.js/#full-setup)

Some reveal.js features, like external markdown and speaker notes, require that presentations run from a local web server. The following instructions will set up such a server as well as all of the development tasks needed to make edits to the reveal.js source code.

Install Node.js

Install Grunt

Clone the reveal.js repository

	$ git clone https://github.com/hakimel/reveal.js.git

Navigate to the reveal.js folder

	$ cd reveal.js

Install dependencies

	$ npm install

Serve the presentation and monitor source files for changes

	$ grunt serve

Open http://localhost:8000 to view your presentation

You can change the port by using grunt serve --port 8001.






### R html presentation solution

[http://slidify.org](http://slidify.org):  Rmarkdown, Rpubs, Rstudio, github, dropbox

 >Built by Slidify. Styled with Bootstrap. Hosted on GitHub. Icons from Font-Awesome. Web fonts from Google. Inspired by Ruhoh

#### Usage example

	library(devtools)
	install_github('slidify', 'ramnathv')
	install_github('slidifyLibraries', 'ramnathv')
	library(slidify)
	author(slidifyDemo)

Then edit front-matter:

	Title: Slidify Demo
	Subtitle: HTML5 slides from R markdown
	author: name
	job: R hacker

Then make slides after ln 19 `--- .class #id`:

	## Slide 1
	
	Animated list
	> 1. Point 1
	> 2. Point 2
	> 3. Point 3
	
	---
	
	## Motion chart
	
	```{ r echo = F, results = "asis", message = F}
	
	require(googleVis)
	M1 = gvisMotionChart(fruits, idvar = "fruit", timevar = "year')
	print(M1, tag = "chart")
	```

Then click `knit HTML` and it will bring up an html preview.

Can add a line in the front matter for posting to github repo:

	mode   : selfcontained # {standalone, draft}
	github:	
	  user: ramnathv
	  repo: slidifyDemo

Then click `knit HTML` again.

Then publish from Rstudio command line to github:

	publish('ramnathv', 'slidifyDemo')

Or delete the mode and github lines in the header and add:

	mode: standalone

Then click `knit HTML` again.

Then you can click the publish button in the html preview window and it will let you upload documents to Rpubs and enter document details.




## More R markdown awesomeness

The [rpubs](http://www.rpubs.com) site is a place to publish R documents.  Some people have released reports here, small starting community but mostly looks like nice resource for examples.

[Example report of politician voting on defense bills with open data set](http://www.rpubs.com/ghuiber/moneytalks)

[Example of network visualization in R](http://www.rpubs.com/Felix/7699)

[googleVis package examples](http://www.rpubs.com/estopub/7697)

[R markdown](http://www.rstudio.com/ide/docs/r_markdown)

[R markdown notebook](http://www.rstudio.com/ide/docs/authoring/markdown_notebooks)



### Rstudio googleVis example

2013-08-20 14:18:19

	demo(googleVis)
	
![]({{site.data_path}}/Screen_Shot_2013-08-20_at_2.13.36_PM.png)


Fruits dataframe

```
> Fruits
	    Fruit Year Location Sales Expenses Profit       Date
	1  Apples 2008     West    98       78     20 2008-12-31
	2  Apples 2009     West   111       79     32 2009-12-31
	3  Apples 2010     West    89       76     13 2010-12-31
	4 Oranges 2008     East    96       81     15 2008-12-31
	5 Bananas 2008     East    85       76      9 2008-12-31
	6 Oranges 2009     East    93       80     13 2009-12-31
	7 Bananas 2009     East    94       78     16 2009-12-31
	8 Oranges 2010     East    98       91      7 2010-12-31
	9 Bananas 2010     East    81       71     10 2010-12-31
```



