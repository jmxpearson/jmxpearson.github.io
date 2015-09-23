---
layout: minimal_post
title:  "Signal and Noise"
date:   2015-09-22 23:00:00
---
> You know why nobody likes statisticians? Because we're the lawyers of science.
>
> &mdash; name withheld

<figure>
<video width="480" height="360" controls>
  <source src="http://www.duke.edu/~jmp33/assets/projection.mp4" type="video/mp4">
Your browser does not support the video tag.
</video> 
<figcaption>Signal from noise?</figcaption>
</figure>
I am not a statistician. In polite company, I don't even get to pretend to be. But I do admit, in moments of weakness, to envying their style. After all, the quote on my [about page](/about) is from a statistician, and one expressing a most un-physicist view of models, at that. And how completely action hero sang-froid do you have to be to tell an entire group (nay, [multiple groups](http://www.nature.com/nrn/journal/v14/n5/abs/nrn3475.html)!) of scientists that [they are doing it wrong](http://amstat.tandfonline.com/doi/abs/10.1080/09332480.2005.10722754?journalCode=ucha20)? To tell them that, cold skeptics they may be, but they are almost surely deluding themselves? That, friend, is some strong judo. Because when you have implacable math and God Almighty on your side, it doesn't matter whether the rest of us like it: you are almost surely right.

There's something faintly prophetic in that.

All of which is to say that times are trying on the non-statisticians among us. There is both a growing conviction that pyschology is in the grips of a reproducibility crisis and an as-yet subliminal fear that we are fast reaching the resolution limit of many of our current generation of cognitive neuroscience tools. Consider EEG: it's been around for decades; the equipment is (relatively) cheap; all the easy stuff has been done. To get this sort of work published in the modern era, you have to be incredibly clever and more than a little persuasive.

I'm willing to bet we are fast approaching this "late phase" for fMRI, as well. Perhaps that's my highly biased outsider's perspective, but consider the rapidly accelerating arms race in fMRI analysis: only a few years ago, MVPA was exotic sorcery; now, it's commonplace sorcery. In part, this is a byproduct of a scientific sociology in which new, shiny analysis tools seem to spring fully-formed from the heads of a few key Zeuses. But I also suspect it's due to the fact that the BOLD signal has an incredibly low signal-to-noise ratio, and that as the questions asked in fMRI experiements are necessarily getting more sophisticated (because again, so many of the easy ones have been answered), there is less and less signal left to work with. 

So we have just as little signal as we ever had, but more ways than ever to fit the noise. I suppose there's nothing really new there. And no remedy in sight, unless we all take [Cynthia Dwork's advice](http://www.sciencemag.org/content/349/6248/636.short) and start adding noise to our data before analyzing it.[^1] 

But what's the harm, I hear you asking? Don't we just cross-validate everything? Doesn't the machine learning approach account for this?

To which I say yes, it does, provided
1. you are not doing unsupervised learning (i.e., pattern identification without ground truth labels)
2. you are not allowed to interpret your features, only talk about predictive accuracy
3. you are fitting parsimonious models that, at least in part, compensate for the fact that you are further dirtying your dataset by adaptively fitting multiple model classes, etc.

Of course, 3 is not super terrible, even theoretically, unless your set of models is really big. And everybody knows 1. But man, oh man, beware option 2. Because we are nothing if not [pattern-finding machines](https://en.wikipedia.org/wiki/Pareidolia), and even if our models are discriminative, not generative, we are still going to interpret those features and try to make meaning out of what should just be pure black-box prediction. 

Which brings me around, finally, to that movie at the top of the page. A [simple little demo](https://github.com/jmxpearson/cloudmorph) in which a well-chosen rotation of high-dimensional data yields a hidden pattern. In which we extract a key insight lurking in our apparently messy data. In which, by the power of fancy analysis, we find a striking, interpretable signal in what is, in fact *100% pure noise*.[^2]

Yup. Because if I have enough dimensions, I can find anything.

I am surprised how little this idea is appreciated even in the theory-savvy quarters of the neuroscience world. I suppose it's possible that, for the first time, we are actually starting to have widespread availability of simultaneous high-dimensional data, and these are just the mistakes we are all going to make. But when I was in graduate school, even physicists were aware of the conventional wisdom from topology: one dimensional is trivial, two exactly solvable, three and four are where the action is, meaning all the really hard proofs. And five and above? Well, it depends, but basically, matters become simpler again because there's enough "room" in high dimensions to smooth away anything complex.

So that 30k voxel response map? That 300-dimensional neural firing vector? How is that *not* going to look interesting when we boil it down to the top \\(n\\) PCA or ICA components, the things *guaranteed* to look like structure?

But there's hope, at least. There really is signal in the brain. There are ways to keep from fooling ourselves. The statisticians, no surprise, have worried a lot about this. The best of the neuro folks? Them, too. 

I suspect the word will percolate eventually. It usually does. In the meantime, I suspect we're due for a few more jeremiads. And as I said, I have some sympathy. Nobody ever asked for a Cassandra. It's not exactly the Dale Carnegie way.

But hey, when you're right, you're right...


[^1]: In fact, I think this is a really, really, really good idea, being equivalent in spirit to admitting that, unless your effect size is big enough to be visible in a simple analysis, it's probably not real. Not that I haven't flouted this principle myself.

[^2]: I don't believe I'm the first to make such a little movie. In fact, I overhead the idea standing in line for registration at CoSyNe workshops, attributed to a prominent theoretical neuroscientist. When/if I eventually confirm, I'll update here.