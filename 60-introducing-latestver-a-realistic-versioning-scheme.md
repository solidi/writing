# SemVer is Dead. Long Live SemVer!
#watercooler, #semver, #versioning, #systems

> *This post is my opinion on versioning software. After a questioning dive into acknowledging fantastic alternative schemes, it introduces [latestVer](https://latestver.org/), my myopic software versioning technique. Please share with your friends!*

Often, a swell versioning scheme appears on a link aggregator. I mutter, "*yeah, that's great.*" Then I'll add it to a collection that has become a shrine of excellent thinking. In between, an opinion will come along on approaching versioning. Of the few posts I read, [the cargo cult of versioning](http://akkartik.name/post/versioning) made me rise off the chair and clap—until the author recanted the phrase I enjoyed.

> You could even remove the version altogether and use the commit hash on rare occasions when we need a version identifier.

Sigh, *correctness*, but is there truth behind the author's words?

## What's Versioned Out There?

Fast-forward years from the write-up, [SemVer 2.0.0](https://semver.org/) remains the standard. Things stay as they are—a journey to communicate the intention of a change in a tangle of dependencies. If one is a maintainer, one receives pokes about improvements. If a manager, their game is to reduce risks. If a lead on a passion project, eighty-four versions of the software have elapsed on a Saturday, with one hundred seventy-nine regressions, which no one will find. And if an adopter updates a library, it's typically to the latest, knowing the risks even with a suite of ten-thousand tests.

Since I am a consumer of someone else's work (like everyone else), I'll avoid bumping the library today or bump it slightly through constrained pinning until I must update it to the latest. I don't have much time to decode the version numbers. It's a linear function where risk *increases* with time. Each bump means a subjectively *more* perfect implementation enveloped with possible dreadful outcomes.

So with versioning stuff, it depends on the intent of the change. Numbers don't communicate intentions well. Even when Rich Hickey says, "change behavior, rename!" it often fails to decode the message. Regardless, I'll *pin* versions in the hope no one will [force me to update](https://dev.to/solidi/cancel-this-app-update-dammit-5f6j) until I don't have the option. I'll throw my hands up, declaring that nothing is complete in the software, even [when someone else states it's complete](https://vivqu.com/blog/2022/09/25/outdated-apps/). If finished, the code expires because labor is consistently involved, costing scarce human, social, or monetary capital to keep it running. We are all at the mercy of becoming outdated.

But we, as a community, try to do better. I'll continue to search for a modern version scheme that communicates sounder. So this got me contemplating. What is out there, encoded in its thinking? Let me share my incomplete child list of SemVer, the current defacto versioning standard. I will share brief opinions about them. By the way, I love all of these and tip my hat to these thinkers.

| Label | Depiction | Introduced | Where to Use | Reality |
| ----------- | ----------- | ----------- | ----------- | ----------- |
| [SemVer](https://semver.org/) | The "Standard" | 2013 | At the Job | Here to stay |
| [BreakVer](https://github.com/ptaoussanis/encore/blob/master/BREAK-VERSIONING.md) | Clear intentions | 2014 | Not at the job | Patches can break things |
| [RomVer](http://blog.legacyteam.info/2015/12/romver-romantic-versioning/) | Human in the highest | 2015 | Not at the job | To err is to break some APIs |
| [CSemVer](https://csemver.org/) | Limits are good | 2015 | Not at the job | SQL statements in versions |
| [SimVer](https://simver.org/) | Clear statements | 2015 | Not at the job | Even closer to reality |
| [MonoVer](https://perlancar.wordpress.com/2016/05/19/using-monotoning-versioning-in-perl/) | Fewer placeholders | 2016 | Not at the job | The fewer numbers, the better |
| [ComVer](https://gitlab.com/staltz/comver)| Clear statements too | 2016 | Not at the job | Confused with simVer |
| [CMSVer](https://github.com/ms-studio/CMSver) | Specific to content | 2017 | Not at the job | Only if dealing with a CMS!
| [WendtVer](https://wendtver.org/) | Tens, tens, tens | 2018 | Not at the job | Odometer goes on and on |
| [Zer0Ver](https://0ver.org/) | Cool, lots of zeros | 2018 | Not at the job | Defines the incomplete nature of software |
| [PandenticVer](https://mikeralphson.github.io/pedantic-versioning/) | *Sigh*, no | 2018 | Not at the job | Politics, I guess |
| [ChronVer](https://chronver.org/) | A life on a calendar | 2019 | Not at the job | What month is it? |
| [CalVer](http://calver.org/) | Make me remember the date | 2019 | Not at the job | Technology marches on |
| [FibVer](https://github.com/kkokosa/fibver) | Matches the agile thinking | 2019 | Not at the job | Too many flashbacks to interviews gone sideways |
| [SentimentalVer](http://sentimentalversioning.org/) | Become a stoic | 2020 | Not at the job | How I feel about my failed essays |
| [HyVer](https://github.com/kstenerud/hyver) | Good | 2020 | Not at the job | Closer to reality |
| [HashVer](https://miniscruff.github.io/hashver/) | Not very clear | 2020 | Not at the job | A good choice for lots of commits |
| [MakeVer](https://github.com/orlandol/makever) | For the C/C++ crowd | 2021 | Not at the job | Headers for versioning |
| [GitDateVer](https://taylorbrazelton.com/2022/06/06/2022-06-06-bye-bye-semantic-versioning-say-hello-to-gitdate/) | Make me remember the date | 2022 | Not at the job | Makes me feel old |
[SemancatVer](https://avatao.com/blog-semancat-versioning/) | Love those cats | ? | Not at the job | I'm allergic to cats |
| [SetVer](https://github.com/RocketRace/setver) | Set patterns | 2022 | Not at the job | Wildly satisfying |
| [LatestVer](https://latestver.org/) | The reality | 2022 | At the job | Cool, this one is mine |

## Introducing LatestVer

For the authors above, while having good intentions, new versioning schemes are at the fringes. I've rarely seen these in the wild, maybe [zer0Ver](https://0ver.org/) or [calVer](http://calver.org/), smiling when I do. Creating a new versioning system requires creative thinking *and* invoking a community change which takes exponential marketing. SemVer surrounds my work, and I'll label my libraries the same. But there is something meta that occurs as I interact with the labeling. Something first-ordered.

As an adopter, I do not sweat over minor versions. It's always about the best, the latest, the major, and the now. If I am building something new, I shop for the latest. Since dependencies are a land of extreme abundance, it is unlikely I will pin my hopes on an out-of-date library. So, while I construct in a "shiny thing" matter, perhaps what is happening in my trenches is occurring elsewhere. As a consumer, I choose the latest version while making a new thing. Otherwise, I place myself, the team, and the project in explicit protection until the pinned forcefield depletes, and I must do something. There is rarely an in-between. SemVer is correct thinking, but in this consideration, anything that increments on the far side is what matters to me.

So what is this pattern? Let's call my realistic library versioning scheme **latestVer**. [LatestVer](https://latestver.org/) is a simplistic approach to versioning. Choose whatever system—numbers, dates, or hashes. Let's call it a *LABEL*. Then ensure the adopters follow the latest version. The reality is that consumers will be looking elsewhere anyway, challenged by pull requests of technical superiors, or dealing with well-intended contributors. Whatever happens, the author and adopter must bump up to the **latestVer** before an ever-present dystopian cybersecurity vulnerability future. Implementers, including myself, will not have time to understand what has changed until getting into the weeds. When I unpack the work, the latest is what matters.

**[LatestVer](https://latestver.org/)** is a shortsighted but truthful versioning scheme. As an author, it encourages "[accretion](http://blog.ezyang.com/2016/12/thoughts-about-spec-ulation-rich-hickey/)" as Rich Hickey said. As an adopter, it is my reality. Understandably I cannot speak for all since there are strict guidelines for implementing dependencies in different environments. But for those in my part of the world where philosophies are unrestricted, it's a general heave-ho, and **latestVer's** motto captures the mood well.

> If I'm not on latestVer, let me get there soon. Otherwise, I'll be forced there as a priority by something out of my control. If unfixed, I'll drop the library for its alternative. And when building anything new, it's always the latest.

Seldom do I have to cherry-pick a specific "in-between" version that will raise a project from a sinking hole. A feeling sets in while I do it, corresponding vaguely to purchasing something expensive but of little value. Feeling regret, I'll bootstrap my way to the latest, finding the courage to drive in the newest version of *their* shiny thing at the cost of my mental labor. In the end, it feels so good to have something new.

I love **latestVer** because it's my reality of the working software. Do you experience the same? [If so, I wrote its specification to rally around](https://latestver.org/).

## Social Post

#Semantic #version is dead. Long live #SemVer! I'm happy to announce that my new versioning #scheme, #Latest #Versioning ( #LatestVer), has launched. See https://latestver.org/

Thanks to John Elden Revano for editing and support.

#software #development #creation

[url](https://dev.to/solidi/semver-is-dead-long-live-semver-4lh4)
