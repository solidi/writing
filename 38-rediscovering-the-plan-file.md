# Rediscovering the .plan File
#watercooler, #career, #motivation, #writing

At the end of 2020, I published a [long-form post](https://medium.com/super-jump/building-a-popular-half-life-mod-during-the-rise-of-counter-strike-fec6a5b9fd8f?source=friends_link&sk=6d1427b3f1d832df06bd5b07aaa456bb) on discovering a computer programming career by building a game modification. In that article, I mentioned a communal practice whereby noting ideas and todos originally served by the UNIX `finger` command. The command publicly exposes the content of a `.plan` file.

At the demise of `finger`s life in the late 1990s, the practice was epitomized by [John Carmack] (https://garbagecollected.org/2017/10/24/the-carmack-plan/) which he had a unique approach to crafting information within. His practice was admired by the community and was later romanticized in [Masters of Doom](https://github.com/solidi/learning-notes/blob/master/books/masters-of-doom.md) and mentioned in [Game Engine Black Book DOOM](https://fabiensanglard.net/gebbdoom/).

Since my article was published, I started a side project to rebuild that modification. My primary goal is to rebuild the experience with the compatibility of the final game patch. And in doing so, I have an interesting observation to share.

## What is learnings.md?

Out of nostalgia, I started [a new .plan file](https://github.com/solidi/hl-mods/blob/master/workspace/plan/learnings.md) that captures the interesting minutiae within the small project. But with the demise of `finger`, I'm focusing every *meaningful* clarification from research, behavior, or a [*enter your favorite search engine*] result in a file I call `learnings.md` (see example below).

`learnings.md` is a chronological list that captures interesting findings from the developer's perspective. With some months into the project, it's been an investment of learning game development context, dockerization, build pipelining, Powershell scripting, and the oddities of cross-compilation of Linux, Windows, and macOS. Surprisingly it's a firehose of valuable technical findings. And it's being captured.

While I have never seen this style out in the ether, I am confident that there are developers out there doing this in their own way, organizing their found knowledge and making it highly searchable. Wiki's come to mind.

And in working on so many different projects, I wonder why this is such a late discovery for me, a small gem that can be shared with others while the sausage is made, highlighting all the things intrinsically *I should know*.

## Why I like learnings.md

This `learnings.md` file is an unproven practice, but I write since it's been a helpful feedback loop in a development environment. Here are a few reasons why I like it:

1. This `learnings.md` reinforces the learning through writing down the note. There is some friction to this habit; however, it's beneficial by way of remembering the learned concept *spatially in time*.
1. The `learnings.md` file is used as a primary place to look up information when attempting to remember the learning, as things in development come up more than once (that I forgot the core lesson or how-to). I've used it as a lookup to clarifying the technical context, e.g., resources on how to operate docker on Windows within VirtualBox without Hyper-V.
1. The file is lightweight. It could become a pivot to build out a small search index when its length becomes unwieldy.
1. It is a continual practice of *yak-shaving* search debriefs - when there are too many tabs open in [*enter your favorite browser*], I'll go ahead and walk each tab, determine if there was learning from that research, write it out in `learnings.md`, and then close the tab. Or close the tab outright, as there was no value.
1. Finally, I'll stretch to say a `learnings.md` file could be useful for the next engineer to review and walk the file to see what took hours of struggle to resolve (or not).

## Spatial and temporal pedantic reinforcement

I was reluctant to write about this practice because, just like a `.plan` file, it is a very personal experience that will unlikely map to other's practices. I remember reading once that `.plan` files were used to wax lyrical or write poems about growing old.

However, in such an environment of [expert Googling](https://markodenic.com/use-google-like-a-pro/), I felt I had to keep track of the knowledge *somewhere*. This reminds me of an unknown quote:

> *The discovery of information is not really important. But this information becomes important when it is appreciated.*

And when I seem in a jam vaguely remembering the technical once prior, I appreciated this file more than a handful of times. I like that it's there, a crutch, closer than [*enter your favorite search engine*]'s cozy doormat. So I'll experiment with the `learnings.md` file and see where it takes me.

Realistically? It will become a pedantic foxhole where link rot will thrive, and the poem I'll type is how *screwed* dependency management became.

---

{% gist https://gist.github.com/solidi/bc977d3ea51f01da287ee35ff6cc50b1 %}

---

## Social Post

A short on how I am experimenting on a `learnings.md` file that captures project findings in sequential order.

Thanks to Danielle Arcuri

[url](https://dev.to/solidi/rediscovering-the-plan-file-4k1i)

#learning #career #growth #watercooler #motivation #documentation

### Posted

1. hackernews
