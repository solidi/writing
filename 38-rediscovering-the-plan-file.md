# Rediscovering the .plan File
#watercooler, #career, #motivation, #writing

At the end of the year, I published a [long-form post](https://medium.com/super-jump/building-a-popular-half-life-mod-during-the-rise-of-counter-strike-fec6a5b9fd8f?source=friends_link&sk=6d1427b3f1d832df06bd5b07aaa456bb) on discovering a computer programming career by building a game modification. In that article, I mentioned a communal practice whereby noting ideas and to-do lists originally served by the UNIX `finger` command. The command publicly exposes the content of a `.plan` file.

The demise of `finger` in the late 1990s, the practice was epitomized by [John Carmack] (https://garbagecollected.org/2017/10/24/the-carmack-plan/) who had a unique approach to crafting information within. His practice was romanticized in [Masters of Doom](https://github.com/solidi/learning-notes/blob/master/books/masters-of-doom.md) and mentioned in [Game Engine Black Book DOOM](https://fabiensanglard.net/gebbdoom/).

Since my article was published, I started a side project to rebuild that modification. My primary goal is to recapture the experience with the compatibility of the current state of the game. And in doing so, I have an interesting observation to share.

## What Is LEARNINGS.md?

Out of nostalgia, I started [a new .plan file](https://github.com/solidi/hl-mods/blob/master/workspace/plan/learnings.md) that captures the interesting minutiae within the small project. But with the demise of `finger`, I'm focusing every *meaningful* clarification from research, behavior, or a [*enter your favorite search engine*] result in a file I call `LEARNINGS.md` (see example below).

`LEARNINGS.md` is a chronological list that captures interesting findings from the developer's perspective. With some months into the project, it's been an investment of learning game development context, dockerization, build pipelining, Powershell scripting, and the oddities of cross-compilation of Linux, Windows, and macOS. Surprisingly it's a firehose of valuable technical findings. And it's being captured.

While I have yet to see this style out in the ether, I am confident that there are developers learnings learnings in their own way, organizing knowledge and making it searchable. Wiki's come to mind.

And in working on so many different projects, I wonder why this is such a late discovery for me, a small gem that can be shared with others while the sausage is made, highlighting all the things intrinsically *I should know*.

## Why I Like LEARNINGS.md

This `LEARNINGS.md` file is an unproven practice, but it encourages a helpful feedback loop in developing software. Here are a few reasons why I like the process:

1. `LEARNINGS.md` reinforces knowledge by writing down the findings. There is some friction to this habit; however, its benefit learning concepts *spatially in time*.
1. The `LEARNINGS.md` file is a place to look up information when remembering the learning, as concepts in development come up more than once. I've used it as a lookup to clarify the technical context, e.g., resources on how to operate docker on Windows within VirtualBox without Hyper-V.
1. The file is lightweight. `LEARNINGS.md` could become a small search index when its length becomes unwieldy.
1. `LEARNINGS.md` is a practice of *yak-shaving* search debriefs - when there are too many tabs open in [*your favorite browser*], I'll go ahead and walk each tab, determine if there was learning from that research, write it out in `LEARNINGS.md`, and then close the tab.
1. Finally, the `LEARNINGS.md` file is useful for the next engineer as a reference of solved knowledge.

## Spatial and Temporal Pedantic Reinforcement

I remember reading that `.plan` files were used to wax lyrical or write poems about growing old. And so I was reluctant to write about this practice because, just like a `.plan` file, it is a personal experience that will unlikely map to other's practices. 

However, in such an environment of [expert Googling](https://markodenic.com/use-google-like-a-pro/), I felt I had to keep track of the knowledge *somewhere*. And so I wrote.

This reminds me of an unknown quote:

> *The discovery of information is not really important. But information becomes important when it is appreciated.*

And when I'm in a jam not of not remembering the technical approach, I appreciated this file's existence. I like that it's there, a crutch, closer than [*enter your favorite search engine*]'s doormat. So I'll experiment with the `LEARNINGS.md` file and see where it takes me.

Realistically? The file will become a pedantic foxhole where link rot will thrive, and the poem I'll type is how *screwed* dependency management became.

---

{% gist https://gist.github.com/solidi/bc977d3ea51f01da287ee35ff6cc50b1 %}

---

## Social Post

A short on how I am experimenting on a `LEARNINGS.md` file that captures project findings in sequential order.

Thanks to Danielle Arcuri

[url](https://dev.to/solidi/rediscovering-the-plan-file-4k1i)

#learning #career #growth #watercooler #motivation #documentation

### Posted

1. hackernews
