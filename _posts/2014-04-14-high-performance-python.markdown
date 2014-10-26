---
layout: post
title:  "High Performance Python by Micha Gorelick and Ian Ozsvald; O'Reilly Media"
date:   2014-04-14 
---
Disclaimer: I received a free review copy of this work through the O’Reilly Blogger Review Program.

<img src="http://akamaicovers.oreilly.com/images/9781491900727/rc_cat.gif" style="float:left; margin-right: 20px"/> In the worlds of scientific computing and data science, it’s hard to dispute that Python is the language of the moment. With an ever-increasing user community and quality package support, the NumPy/SciPy/Pandas stack is beginning to give platforms like Matlab and R a run for their money.

But Python has its drawbacks. It can be slow in data-intensive analysis, especially compared with compiled languages. The GIL, the global interpreter lock, is a barrier to parallel algorithms analysis. Thus the proliferation of tools — Cython, Jython, Numba, a host of parallelizing libraries — designed to help Python compete with industrial tools and level up when confronted with tasks demanding intensive data crunching.

At the moment, though, there’s a dearth of instructional material out there for these new tools, especially for those without much experience programming close to the metal. Lots of working scientists out there might like to optimize one or two key functions in their algorithms, but the prospect of rewriting an entire program in Java or C++ can seem like a bridge too far.

All of which is to say that I suspect there is a hefty demand for a book like High Performance Python. It could easily become the go-to manual for optimizing Python code in the scientific community.

As of now, though, this is more promise than reality. The version of the text I reviewed is still preliminary in both presentation and coverage, so I’m writing this to encourage people to keep an eye out as the work develops.

The Good: Gorelick and Ozsvald are trying for a pretty systematic introduction to performance optimization. Many will skip the introduction to computer architecture to get straight to the code, but shouldn’t. The chapter on profiling shows even novice users how they can begin locating bottlenecks in their own code. Chapter 3, comparing lists and tuples, might not be the first section readers like myself flip to, but is an important step in thinking carefully about the efficiency of data structures.

The Bad: The presentation still needs work. Right now, the text has more of a “too many trees, too little forest” feel. I suspect this will change as the authors finish chapters and continue editing, but given the intrinsic breadth and complexity of the topic, I would appreciate more summarizing, rules of thumb, and guidance. The chapter on profiling, moving so quickly from one option to another, can feel a little overwhelming, and less experienced users might want more helping sorting out how to proceed. On a smaller count, the quality of the figures is not terribly high. Much of the labeling is unreadable.

On balance, though, this book is extremely promising. Even given the flaws in its current form, it may still end up as the standard resource for Python optimization. I am looking forward to watching as it evolves.
