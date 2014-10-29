---
layout: minimal_post
title:  "Further adventures in Pythonism"
date:   2014-06-05
introduction: Over the last year or so, I’ve been porting all my analysis over to Python. Why, you ask? Perhaps because it’s a pleasure to use a language that’s clean and consistent. Perhaps because I’m tired of dying a little inside every time I have to process strings in Matlab. Either way, to borrow a concept used by Bible translators, one could almost say that I’ve discovered in Python my heart language for coding.
icon: "http://www.psychopy.org/_static/psychopyDocBanner2.gif"
---

<img src="http://www.psychopy.org/_static/psychopyDocBanner2.gif" style="float:left; margin-right: 20px"/> 
But there are a few sticking points. First of all, neuroscience is still a closed shop. A Matlab shop. Early adopters are asking for trouble. Second of all, I help enough people with coding that I can’t very well start pressuring them to switch over without some assurance that they can continue to perform all their usual tasks in the new system.

Which brings us to [PsychToolbox](http://psychtoolbox.org/). 

For the cogneuro and vision kids, PTB is the way we display our experimental stimuli with the temporal precision needed to synch up with very fast spiking dynamics. (At least we tell ourselves this; most system clocks are filthy liars.) And PTB is great. It’s well-maintained and supported by a huge community.

It also depends on Matlab. Which means I’d like to give it the boot, if possible.

Right now, there are a few alternatives in Python. There’s [expyriment](https://github.com/expyriment/expyriment), which is lightweight, but seems focused on experiment design logic I don’t mind handling myself, and [PsychoPy](http://www.psychopy.org/), which is heavier with dependencies, but comes with very PTB-like syntax and a GUI builder I can recommend to newer coders. There are a few others you can find online, but they don’t seem to be in active development.

So as a test case, I set out to port a working task of mine, a go/no-go variant, from PTB to PsychoPy. You can find the result here. What follows are some lessons learned in the process.

**First hard lesson: Download the self-contained app.** Seriously. After spending a shameful number of hours trying to install wxPython, pygame, and several other dependencies not available through pip in a virtualenv on my aging Macbook, I gave up. For a little while yet, according to the main developer, PsychoPy still needs 32-bit Python (again, those dependencies), so one way or t’other, you’d be stuck with juggling separate Python executables. On the flip side, if you download the .app file for OSX, all the depends and binaries come packaged in the .app file itself, so code just runs. Better, this can easily be installed on machines (like my Windows XP rig) with no pre-installed Python at all.

**Second hard lesson: Give in to coder.** I did a lot of whining early on about how I preferred to use my own code editor to PsychoPy’s Coder view, and I do think that having a single editor window (and single file examples) probably discourages code reuse and encourages sloppy programming practice. It also makes it harder to test your code. But as I said, I eventually came around to the idea of the standalone app as a blessing (“Here,” I’ll say to my colleagues, “just download this.”). I wound up using [my usual editor](http://www.sublimetext.com/) to structure the code as I wanted and just gave PsychoPy [a very simple program file](https://github.com/jmxpearson/pygonogo/blob/master/gonogo.py) that called my task class.

**Hard lesson the third: You will need OpenGL > 2.** Sigh. After all that coding, I discovered that the video card in my now-vintage electrophysiology rig is too old to begin the training. This should not be a problem for anything manufactured in the last few years (though see [this](http://www.psychopy.org/installation.html#recommended-hardware)), but it means that the code up on GitHub as of this writing is missing a few things, namely:

* Joystick support should be okay, but is untested.
* I use Plexon’s event queue to timestamp events. A really excellent Python wrapper for this functionality is [here](https://github.com/chrox/RealTimeElectrophy/tree/master/SpikeRecord/Plexon), but it’s not implemented in my code yet.
* When I’m not recording on Plexon, I send TTL pulses through the digital output on a National Instruments card. I’ve not implemented this yet, either, though [this](http://pythonhosted.org/PyDAQmx/) is likely where I’ll go when it’s time.

Bottom line: the code works. The PsychoPy API is nicely designed, and being able to work in Python allowed for a much better separation of concerns than Matlab. My code organization is described here. It may not be the ideal, but it’s a step in the right direction, I think.