---
layout: minimal_post
title:  "Data Science at the Command Line by Jeroen Janssens; O'Reilly Media"
date:   2014-10-29 23:30:00
---
<img src="http://akamaicovers.oreilly.com/images/9781491947852/thumb.gif" style="float:left; margin-right: 20px; margin-bottom: 10px"/> Disclaimer: I received a free copy of this work under the O'Reilly Blogger Review Program.

I don't have a neck beard. My .vimrc file doesn't break 20 lines. I know only a handful of options to `ls`, `find`, and `grep`, and so the number of people whose bash fu is better than mine is several orders of magnitude too large for my opinion on matters of the command line to carry any weight. (He uses bash, they're snickering...)

But I know a little about working with data. And I'd like to get better. And I don't mind if someone shows me a few new tricks now and then, especially if they come buffet-style, where I can pick and choose as the problem demands.

As a result, I immensely enjoyed Jeroen Janssens's _Data Science at the Command Line_. First of all, because the style is engaging, practical, and readable. Well-chosen case studies, useful caveats, and just enough of each tool to point you in the right direction, but not to overwhelm you with options.

Even better, the book is a great resource for command-line tools that don't ship with *nix proper: learning about `csvkit` alone was probably worth the price of admission. As was the chapter on streamlining the process of turning R and Python scripts into shell-usable tools, because, okay, many of us should know to do this, but how many _actually do_? For many of us, this book might be the extra nudge.

Best of all, Janssens's approach isn't to convert you to a command-line-only workflow. On that count, he seems to be a realist. His goal is to make you incrementally better, perhaps a little faster, and at least in my case, I'll call it a success.

Of course, the difficulty is that few people will really make the commitment (or should) to working exclusively at the command line. It doesn't necessarily scale well, and the more involved programs Janssens puts together are perversely cryptic compared to their equivalents in Python. Effective for quick-and-dirty interactive exploration, I'm sure, but not great moments in maintainable code.

Along the same lines, the choice to supply readers with a virtual machine rather than lengthy installation instructions for all the tools discussed in the book is a decision that makes life great for novice and author but no less difficult for the actual data scientist, who will not want to be doing any heavy lifting in a VM. To that end, sources are all listed in the appendix, but many of the tools, Janssens admits, are tricky installs, and that bodes ill for their widespread adoption when compared with a more streamlined package ecosystems like R's.

In summary, this short book is well worth a read for anyone looking to improve his command line skills, especially those with data-centric needs. As both an introduction to shell-centric analysis and the wider world of modern lightweight tools, it's a valuable addition to the data scientist's bookshelf.