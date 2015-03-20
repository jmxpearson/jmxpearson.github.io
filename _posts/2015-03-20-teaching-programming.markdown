---
layout: minimal_post
title:  "Teaching Programming"
date:   2015-03-20 12:00:00
---
I just finished teaching another short course in programming, this time for our undergraduate neuro majors at Duke. As mentioned [elsewhere](/teaching), I'm excited by the work [Software Carpentry](http://software-carpentry.org) has been doing, especially in designing lessons for programming novices. However, when it came time to run my own class, I found myself doing some redesign.

This mostly stems from a few dissatisfactions I have with the SWC lessons on Python. Or perhaps more accurately, my misgivings about the applicability of these lessons to the students I'm teaching. Again, our students are not coders, for the most part. They're not computer science students. That's just not where their interests lie. They want to be doctors or neuroscientists, or maybe they just like biology, but whatever the reason, they didn't take this course in hopes of doing lots of math and spending most of their time thinking about for loops.

And the SWC [lessons](http://software-carpentry.org/lessons.html) are targeted at just these learners. A lot of smart folks have worked very hard on them. So what am I complaining about?

Perhaps I should be looking harder at the [Data Carpentry](http://datacarpentry.org/) material. After all, most of our students (including graduate students) will spend 90% of their time running other people's code. And rightly so. Having spent most of the last year, off and on, reproducing time-frequency analyses that are easily available elsewhere, it's hard not to feel that this was an enormous waste of time. And I *like* to code. 

So what I really want my students to be able to do is use libraries. To be able to load data in, do high-level exploration and plotting in Pandas, and worry about the tricky stuff as they need it. Yet the SWC materials, like most conventional treatments, start with the basics &mdash; variables, types, for loops, etc. Of course, this stuff is important. It's arguable you won't get very far without understanding it. And yes, if you don't understand that Pandas usually returns copies and NumPy returns views and that there is a difference, you're in for a world of hurt, but (dare I say it) *most of the time*, with a well-designed language like Python, stuff behaves the way you expect it to. 

Or maybe my expectations are warped from years of programming.

At any rate, I decided to try a different approach, one with its own problems. I asked a friend of mine, recently learning R, what she found most motivating in the R seminars she's attended, and she told me exactly what I suspected: being able to load in, explore, and plot real data is motivating. The [Art of R Programming](http://www.nostarch.com/artofr.htm) is not. 

So I put the cart before the horse. I taught Pandas first, then NumPy, then for loops and dicts ([notebooks](http://nbviewer.ipython.org/github/jmxpearson/DIBS_materials/tree/master/python/)). This may turn out to have been a terrible idea, but we were able to plot real data on the first day, and that's some kind of a win.

And again, my rough understanding is that this is a difference in emphasis between Data Carpentry and Software Carpentry: the former is for people who want to use libraries to analyze data, the latter more for people who have to build things themselves. I suspect this is a difference in degree, not in kind, but I was encouraged to find that Kevin Sheppard had taken [a similar approach](https://www.kevinsheppard.com/images/0/09/Python_introduction.pdf). In fact, were it not for the difference in domain knowledge, his book, which teaches data structures like NumPy arrays before objects, would likely become my go-to recommendation for students wanting to follow up on what we covered.

Moving forward, I'm considering the idea of parceling these lectures out into small modules. I'm loathe to reproduce the many, many, many introductory lessons on Python out there, but a series of quick "getting started" notebooks on typical types of neuroscience data (perhaps one per analysis type) seems like a way for students to dip in and out and get a sense of what they need to know.

At any rate, if you're reading and have suggestions, feel free to submit pull requests to the [repos](https://github.com/jmxpearson/DIBS_materials). At some point, if it gets polished enough, I might wind up submitting them as an alternate lesson to SWC.