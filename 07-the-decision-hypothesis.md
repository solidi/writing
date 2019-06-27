# The Decision Hypothesis
## The Mythical Man-Month Hinted At Software Decision Documents Decades Ago

> A Qumran Cave Scroll (iStock)

Some weeks ago, I completed a re-read of the Mythical Man Month (MM-M) by Frederick P. Brooks, Jr. This was my third sitting with the book over the course of years in software development.

MM-M is a dramatic piece of authoring excellence in our young craft. I consider it a constitution that continues to hide delightful discoveries. Anyone who practices software development will benefit if they read. However, to read once is not enough! Much pleasure and wisdom will come when reading numerous times. The work highlights forty five year old observations that hold true to this today.

This post will describe loose findings in MM-M that may hint on how we can document the why of software development decisions. It will also analyze a technique our team inconsistently deployed to capture software decisions.

## Chapter 10: The Documentary Hypothesis

In MM-M, Fred postulates scholarly labor to applied practical application in four short pages.

> Amid a wash of paper, a small number of documents become the critical pivots around which every project’s team revolves …

Fred goes on to describe neatly in three sections the required documents for computer product, university department and finally documents for a software project.

He concludes with the topic of why.

> First, writing the decisions down is essential… Second, the documents will communicate the decisions to others... Finally, … documents give … a data base and checklist.

From the quotes, Fred sets up the thinking and fundamentals of documentation that a developer should strive for. While he may have targeted documents such as schedule and requirements, how does this apply to a software project in terms of code?

## DECISIONS.md

Some years ago, there was discussion in our team to decide a mechanism on how to communicate the why of team decisions. We came up with a way to record the decisions that were made. The document was to provide attention to code direction, construct usage, structure and style in a way that explains the conclusion of such decisions.

Our guiding principle was that the documentation is code. If we absolutely had to document, do it in the version control system or as close to the software workspace as possible.

Then we found this post, every project should have a decisions making file, by Aliaksandr Kazlou. The post introduced the concept of a version controlled DECISIONS.md. It’s a brilliant write up and I suspect he is also a fan of MM-M.


> It’s clear in our DECISIONS.md that code organization and dependency management is dominant.

So, we followed and adopted it in our own way. I’ll share a short section of ours below.

```
# DECISIONS.md
...
## Logging

As a platform team, we have decided to utilize Timber [https://github.com/JakeWharton/timber] for all logging calls within the application. This is due to a few reasons. Our biggest gain is the removal of an overbearing Log wrapper we had to maintain. We wanted to get rid of its complexity.
Some other reasons for utilization of Timber are as follows:

* Automatic tagging.
* Easy extensibility.
* Better usability in unit testing.
...
```

Once adopted, we had problems with timeliness of DECISIONS.md since it required constant maintenance. We also observed two truths. First, software development decisions are relentless and constant. They can vary in intensity but are always present. Two, we have trouble having developers owning DECISIONS.md like its code by keeping it timely.

## Julius Wellhausen’s Work Was Lost To Many Hands

This post was inspired by observations between the team, MM-M, the many projects launched and maintained, and Aliaksandr’s post on DECISIONS.md. However, ultimately I decided to write this because of a lunch I recently had with a senior developer. The lunch brought it all together for me.

> Software decisions vary during a project, but prefers to be constant over time.

We debated about a pull request trend in our monolithic repo that seemed to be going awry with certain uses of @VisibleForTesting and others uses such as ReactiveX Subject. Additionally, a team decision was not made on the consistent use of @Nullable and @NonNull in preparation of our Kotlin production migration. Of course, the technical details are not as important and these issues are just the flavor of the week.

As we ate, there were many developers contributing and improving our code based on an idealistic development philosophy… but no philosophy is wrong if we are going in the same direction. A “wink” to Fred would suggest that Fragmentary or Supplementary Hypothesis is always in full effect when it comes to code contribution.

Sure enough, the conclusion of our lunch was that we had to present decisions and that the communication of these concerns were highly important. We have to start a discussion, a debate with data, and then update the DECISIONS.md document. Otherwise, the integrity of the tests and production code may degrade over time by violating conceptual integrity.

## Fred Concluded With Self Documentation

In MM-M, it is plain to see that Fred had a difficult time grappling with separate documentation. He supported its value, but pondered why developers do not do it well. In the end, he gave direction in some way that I consider pragmatic.

> Most documentation fails in giving too little overview. The trees are described, the bark and leaves are commented, but there is no map of the forest. To write a useful prose description, stand way back and come in slowly…

The biggest contrast about written language to Fred are the following.

> English, or any other human language, is not naturally a precision instrument for such definitions. Therefore the manual writer must strain himself and his language to achieve the precision needed.

However…

> With English prose one can show structural principles, delineate structure in stages or levels, and give examples. One can readily mark exceptions and emphasize contrasts. Most important, one can explain why.

> Developers do not like to document. Mundane external processes hurt developer happiness. [ 1 ]

Fred finally breaks down and writes a chapter on marrying documentation to code.

> Yet our practice in programming documentation violates our own teaching. We typically attempt to maintain a machine-readable form of a program and an independent set of human-readable documentation, consisting of prose and flow charts.
The results in fact confirm our teachings about the folly of separate files. Program documentation is notoriously poor, and its maintenance is worse. Changes made in the program do not promptly, accurately, and invariably appear in the paper.
The solution, I think, is to merge the files, to incorporate the documentation in the source program. This is at once a powerful incentive toward proper maintenance, and an insurance that the documentation will always be handy to the program user. Such programs are called self-documenting.

Fred was close to a solution, but he did not accomplish the follow through with code as documentation. It appears that human language and machine language repeal each other, just as if two magnets are forced together at the same pole. More energy is required to keep the connection as they move closer.

Forty five years later, tests are the documentation on specification. However they too cannot explain why code exists as it does. There is a high value to keep that why, to allow the system to pivot and survive. Therefore, some documentation has its place in the workspace.

## Code Cannot Explain The Why To Humans

Every project will have plenty of software decisions that will demand constant attention at varying intensities. The recommendation is to document the major software development decisions continuously, carefully, in one place. Try a technique like DECISIONS.md.

This document could serve the team by encouraging new debate and focusing the resolution to a highly transparent file revision. This is because this small process focuses developers comfortably at a concrete point that is neutral. An imperfect electronic arbiter.

> Decreasing code complexity and increasing code consistency appears to be the whys.

Finally, we must explain the why of our software decisions because the code has a daft ability to poorly communicate its origins. Tribal knowledge, hallway conversations, team dynamics change and fade. Version controls are changed and history is broken. All that remain are the many contributors that graphed the pieces together over short periods of time.

> The decision hypothesis:
> Amid constant software decisions, those of complexity and consistency become the critical pivots around which every software system survives. The decision document is a key to its revelation.

## References

[ 1 ] Daniel Graziotin, Fabian Fagerholm, Xiaofeng Wang, and Pekka Abrahamsson. On the Unhappiness of Software Developers.

## Author’s Notes

In MM-M, Chapter 10: The Documentary Hypothesis is focused on the manager actor. Creativity liberty was taken to refocus the conversation on the software team and their documents by combining thoughts on Chapter 6: Passing The Word and Chapter 15: The Other Face.

Fred’s “The Documentary Hypothesis” discuss documents such as budget, organization charts, and schedule. To many software engineering teams, these documents are considered taboo to distribute directly to them. However, these documents are data and decisions that partially or wholly control the variable inputs of all software projects — time, scope, developers, and quality.

> [From Chapter 3: The Surgical Team] … Mills’s concept in transformation of programming “from private art to public practice” and making all the computer runs visible to all team members and identifying all programs and data as team property, not private property.

Since software development teams are always under constraint, there are parallels drawn to code consistency, complexity and why the team constructed things they way they did. We should question why certain documents that drive software projects are hidden, possibly to have the team debate and drive the variables differently so that better software could flourish. However, this was not the goal of my initial contemplation. Thanks to Hazem Saleh for pointing this out and the summation that many books could be written on this fascinating exploration.

Finally, thanks to James Shvarts for the inspiration. One thing that will never fade are overpriced sandwich shops.
