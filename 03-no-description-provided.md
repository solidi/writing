# No Description Provided

Some months ago, one of my colleagues suggested a book. Out of curiosity I read and completed Sapiens: A Brief History Of HumanKind.

It was a fascinating read with many points to consider. With themes interweaving throughout the chapters, one theme continued to bubble up that was thought provocative but easy to understand.

Yuval described that in order for humans in large groups to cooperate, they must create orderly patterns that are understood and valued. As described, a mythical glue.

I questioned, is there such a glue that is effectively applied to our engineering profession? Do we as engineering professionals have a mythical glue we value?

## Everything In A Pull Request

Without question the pull request, or code review, has become the life line of every development team who interact and contribute. Pull requests are where the team culture is embodied in some way. In a sense, this is how the team communicates and makes decisions.

As Yuval described free market systems, money and other constructs that are believed and valued, we as engineering professionals believe in pull requests. We all understand what code review is and what values it provides.

Or do we?

With travels to many other code reviews, something's not quite right. There are no descriptions that cleanly point out the intent of change. For those that do describe the change, they appear messy and inconsistent.

The value, the glue, is diluted and does not bind well. What’s the value of a pull request when the problem is not described?


Perhaps the engineer was in a rush? The commit message was no better and the commit diff was unclear.
The most important aspect of software engineering is to describe the intent of change. We must describe the why. This is what we must do as professionals.

Since our profession is distributed globally, ear shot conversations will not do. Tribal team knowledge will not suffice either. The description must be textual as record.

So, what is the solution?

## Call For A Unified Pull Request Template

The community has toiled with pull requests for some time. There have been numerous posts in the community to do them better.

Some of the best examples provide preferred templates that guide the contributor to answer certain questions. This is a good way to suss out a description of change.

However the community has not found an answer to forge descriptive pull requests. Many professional teams often skip descriptions missing out on great opportunities to strengthen our glue.

## An Example

At a normal cadence engineering teams have to update external dependencies. The mode in-which these updates occur are usually done in mystery.


What are we trying to solve? What’s the gain?
Google “Butterknife”. This is a view dependency injection SDK for Android. However, why the bump? What are we trying to solve?


A clear problem and solution. Find the template here.
Okay, now we understand. The team understands the opportunities to improve.

The description identifies the problem, the solution and why. We can take the template further with topics such as testing, code coverage, measurement changes and further unique ways to automate and communicate concrete change.

The definition of a unified template must start with a problem and solution. It would behoove a team to realize how to communicate change through the use of a template and kindly decline those pull requests that do not present them.

As an additional bonus the template gives gravity to a slam-dunk atomic merge commit message in a continuous integration and delivery system.

## Commits May Be Overkill

Commits lack value if subject titles and descriptions are unclear.


https://xkcd.com/1296/
Indeed, there have been numerous posts written about these problems over the years. The most direct solution to non-descriptive commits is to follow the 50/72 rule. This rule encourages subject and body messaging delivered in a specific way.

However most engineers do not follow 50/72. Some engineers think it's okay to place periods at the end of subject titles. Their commits are riddled with ticket systems and for some seasoned engineers these commits lie outright without malicious intent. Commit messages are almost too hard to get right. Writing the code was easier.

There is a philosophical argument that questions the value of the commit even if written cleanly. Should we care for the steps or should we care only for the pull request merge, as long as it is well shaped and not overbearing for any one engineer to understand?

One would argue that in most professional engineering teams the merge out of the pull request is the most important description. Not the small iterations that came to form it. The reasoning is simple. We are not machines that can accurately remember more than seven commits at any one time, plus or minus two. There are those teams that also squash and rebase so the commits were trivial to begin with.

There is no right answer to this quandary. The only true constant is the pull request template, the opportunity described, and if it is recorded in a version control system.

## A Value Is The Description

Pull requests take time just as much as writing clean code that follows consistent patterns. The code should be fully covered with tests. We value the pull requests because they serve cross pollination in engineering teams as well as protection of user experiences that are valued to business, agency, or whatever.

Engineers are required to solve difficult problems. The first step is to write what the problem is, why, and how we went about solving it. Sometimes in steps over a course of chained pull requests.

There are two hard things in computer science: cache invalidation, naming things and off-by-one errors.
— Unknown
Naming things is hard. However, describing things is harder and rife with errors. As professionals it is our duty to describe the intent of change with context to the best of our ability.

The most correct code is that which is not written but the most correct description is one that is.
The argument here is if we do not make our best attempt at the description of change the context is lost. This does a disservice not only to future contributors, but to the business partners, agencies, and others.

So how do we embody and capture the value of context description so other engineering professionals understand?

## Extending Uncle Bob’s Programmer’s Oath

There are conversations happening in our community about our engineering profession as an organized body. We should look no further than Uncle Bob sending these smoke signals.

For some time now he has urged for us as engineers, or programmers, to embody a set of concrete principles otherwise government agencies will do it for us.

Uncle Bob’s argument consists of comparisons to other professional groups. One such example describes just how patients died from lack of sterilization in the medical profession, a swath of people will die inadvertently as software eats the world. Unknown to the medical professionals is as unknown to the engineering professionals until it’s too late.

To correct these problems the medical professionals organized and formed guidelines that were adhered to like sterilization techniques. These medical professionals were able to hand the agencies their mottos and hence they made their own rules. So too is what Uncle Bob is asking from us.

He will be proven correct and it will happen in our lifetime. However the question is are we ready to take this on as an organized group of professionals? To answer this dilemma, Uncle Bob created the Programmer’s Oath.


There are very strong points above in the oath. Uncle Bob has created a strong glue for us. However he missed a fundamental rule and I wish to offer an extension.

> 10. I will communicate to the best of my ability the intent of change with as much context as possible.

The point with rule number ten is to enforce all other rules in the oath. We are writers that are expected to communicate to the best of our written abilities.

The mystical glue that binds us as software engineers are many. One such glue is that we value the pull request. Let’s do our part to describe in detail the context of the problem and solution so that others can contribute promptly and to protect our users. It starts with thinking and describing “what” the problem is. Then we must describe the solution with the new opportunities at hand. Ultimately communicating intent of change should be adhered to by all engineering professionals.
