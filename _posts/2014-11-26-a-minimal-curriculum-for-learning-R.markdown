---
layout: minimal_post
title:  "A minimal curriculum for learning R"
date:   2014-11-26 20:30:00
---
<img src="http://www.duke.edu/~jmp33/assets/Rlogo.png" style="float:left; margin-right: 20px; margin-bottom: 10px" width="150px"/> I like R. At least, well enough. I find the common lore to be true: the language is inconsistent and crufty, objects are bizarre, the data structures can be hard to work with. But the package system is excellent, with significantly better support for advanced statistical methods and analysis of categorical data. It's clear that several of my favorite Python packages, [pandas](http://pandas.pydata.org/) and [statsmodels](http://statsmodels.sourceforge.net/) in particular, deliberately borrow from the best R has to offer, and [ggplot2](http://ggplot2.org/) produces, in my opinion, the best-looking off-the-shelf plots available. So collected here for the benefit of my friends learning R, is my shortlist of R learning recommendations.

* Download [RStudio](http://www.rstudio.com/). Much better than the default R IDE, including integrated support for R markdown/knitr/sweave.

* I don't have a swear-by introduction to R programming. I mostly learned by Googling, since there are really great resources out there particular to your field, whatever that field is. A lot of people like [The Art of R Programming](http://www.nostarch.com/artofr.htm). These people are generally doing more serious R coding than simple data analysis, but this is where I would go for a better understanding of the R language itself.

* Use everything [Hadley Wickham](https://github.com/hadley) writes. Seriously. The following packages are, in my opinion, far easier to use and more consistent than those available in base R:
    - [ggplot2](http://ggplot2.org/) for plotting
    - [dplyr](http://cran.rstudio.com/web/packages/dplyr/vignettes/introduction.html) for selecting, filtering, and transforming data
    - [reshape2](https://github.com/hadley/reshape) for manipulating data into "tidy" format (see below)

* Note: the dplyr and reshape2 packages supersede plyr and reshape, but the following articles are well worth reading to better understand the thinking underlying their design:
    - An introduction to the concept of [tidy data](http://vita.had.co.nz/papers/tidy-data.pdf) and what it means for organizing data into tables.
    - The paper on [split-apply-combine](http://vita.had.co.nz/papers/plyr.pdf). Written as an expostion of the plyr package, but more important for showing how a certain approach to data analysis and transformation can unify a lot of the confusing multiplicity of features in base R.
    - The introduction to [reshape](http://www.had.co.nz/reshape/introduction.pdf). Again, reshape has been superseded by reshape2, but this explains the rationale shared by both.

None of this will teach you what analyses to run on your data, and it's light on the nuts and bolts of actual statistical analysis. But it will give you a better toolchain with which to clean, organize, and massage your data, which, if the pundits are to be believed, is ~80% of the work of being a data scientist.

Once you get this far, I think it's easy enough to download whatever package is relevant to your analysis of choice (and surely there is one), get your data in order, and run it. As always, doing the real work is up to you.