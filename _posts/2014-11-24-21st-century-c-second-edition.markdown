---
layout: minimal_post
title:  "21st Century C (Second Edition) by Ben Klemens; O'Reilly Media"
date:   2014-11-24 21:30:00
---
<img src="http://akamaicovers.oreilly.com/images/9781491903896/thumb.gif" style="float:left; margin-right: 20px; margin-bottom: 10px"/> Disclaimer: I received a free copy of this work under the O'Reilly Blogger Review Program.

Over the course of fifth, sixth, and seventh centuries, during the period known as Late Antiquity, much of the learning known to the Roman world was lost to Western Europe. Though the monasteries copied and preserved selected strands of the classical tradition, other subjects, particularly mathematics and philosophy, gradually lost touch with their imperial antecedents. Educated men no longer knew Greek, then no longer knew the Latin of Cicero. Until the Arabs reintroduced Aristotle and Euclid in the early Renaissance, Western intellectual culture continued to build on foundations it knew almost entirely as legend.

In much the same way, the world of modern computing is based on the two great languages of its own classical period -- C and Fortran. Whatever operating system you happen to be using, it is written in C, or some latter-day variant of it. Whatever scientific programming you are doing, it is likely built on the collective efforts of forty years of Fortran optimization. And yet I don't "speak" Fortran beyond the barest rudiments from a course more than a decade ago, and I stopped coding C with any regularity sometime around 2007.

Ben Klemens, in the second edition of his _21st Century C_, sets out to rectify this tragedy. It is a tragedy, he insists, because for all the advances in computing over the last couple of decades, a few hard truths remain:

* C is still faster than your language of choice
* If you are working seriously with hardware or operating systems, you are going to have to pay the piper

Just as importantly, Klemens argues, the experience of coding C does not have to be as painful as we've all been led to believe (or experienced). If you have spent hours tracking down bugs with `printf`, if the sight of `malloc` and `free` peppered throughout code gives you hacker's vertigo, there is hope for you, and it's all traceable to another hard truth:

**C: You're doing it wrong.**

This, Klemens, explains, is because most of us have learned our C through outdated textbooks focused on coding practices from the time C was designed, not as it exists now. The language has continued to evolve, as has the ecosystem of tools, and those of us who would not dream of working without Python's NumPy or SciPy nonetheless sit down to code without the benefit of a comparably strong C toolchain.

So what will you learn in _21st Century C_? Among other highlights:

* How to use the debugger (in this case, `gdb`).
* How to package your code to be compiled on others' machines (Automake, Autotools, etc.)
* How to use macros to create functions with variable-length inputs.
* How to spare yourself the worst pains of memory management.
* How to use structs to get goodies like named argument lists, default inputs, object-like data structures, and other features you thought were impossible in C.
* An appendix that boils down C syntax to the bare essentials you need to know, without a lot of unneeded complexity.

This is a very good book. Even better than the first edition, which I purchased. Klemens is opinionated on matters of style, and I suppose there are lots of ways to disagree with him, but when you're new to the terrain, subscribing to one strong opinion is often better than having no opinion at all. While not comprehensive on all the topics it attempts to cover (many of them worthy of book-length treatments in their own right), it is a clear-eyed and cogent reintroduction to an increasingly neglected language by an author with extensive experience creating modern C libraries with modern tools. It remains my go-to source for contemporary C practice.

A few negatives I should note, though: You do need to have experience with C. I found the chapters on structs and pointers much easier to follow, since these are fairly common features. Despite reading the relevant chapter in both the first and the second editions, I still find Autotools baffling, though I suspect that if I had a pressing need to distribute some C code, the material would have stuck better. I think there are better treatments of git out there, and it's peripheral enough to the main thrust of the text that it might have been easier to drop this.

But those are only minor complaints. For any student looking to get a handle on the modern C toolchain, this is a friendly and efficient introduction.