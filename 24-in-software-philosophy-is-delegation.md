# In Software, Philosophy is Delegation
## A short story on how humans in software transmit direction

![Photo: Stephen Dawson/Unsplash](images/24-1.jpeg)

Over my software career, I’ve built software apps and systems. More recently, as an engineering manager, I’ve had led teams that do the same. While activities were ongoing, I’ve noticed a pattern — a phenomenon. **Teams get their work done guided by philosophies.** This write identifies this behavior, questions its origin, and how it’s a powerful force through repetition. Let me highlight an example next.

## A Short Story About a Dashboard

Recently, one of my teams had a featured product heading to production. It was evident they needed to monitor the system before deployment. However, the goal was unclear. What are they optimizing?

Some weeks into it, I began repeating to the team that in this monitoring, *we should trace the customer’s pain throughout the system* (the philosophy). We would tease out the essential contexts and artifacts of the customer that made sense in an easily digestible format (the framework).

Of course, there wasn’t a meeting stating this precisely, just a lot of informal discussions and consensus-building naturally. A pattern was emerging, and it became the philosophy because of stickiness.

### Principles Support Philosophy

As work was underway, I’d test out the dashboard. The team readjusted when we discussed the [SLAP principle](http://principles-wiki.net/principles:single_level_of_abstraction). It was hard to reason what was on the screen because the context was mixed. Taking this feedback, the group split infrastructure health and customer pain.

What I learned is principles (unchanging rules) help guide the philosophy and framework. Reevaluation is needed every so often. And the team continues to move it forward without the manager being there.

In my opinion, this is a natural phenomenon of building software in teams. These types of events happened many times in my career. And the origins are difficult to pinpoint.

### Philosophy is Direction

In my experience, teams typically desire a single direction, *not directions*. In software engineering, defining direction is difficult because [the process is intangible](https://medium.com/hackernoon/software-is-unlike-construction-c0284ee4b723). Software is a young profession, and there are many trade-offs. So how does one clarify an approach?

All people (the team, engineers, managers, architects, designers, and [product managers](https://dev.to/solidi/what-is-a-product-manager-anyway-3pc4)) develop direction. The path should summarize multiple discussions between all involved parties (engineers, leads, product people, designers, and stakeholders). Someone in the group will catch onto the philosophy and drive it. And that direction should be an agreement between the parties.

In my opinion, it may be beneficial that the [engineering manager](https://dev.to/solidi/what-is-an-engineering-manager-anyway-4and) steers this ritual. Taking on the actual work may be a no-no (such as building the framework); the last thing the team wants is a manager blocking them. In exchange, they can identify and rally the philosophy.

## Where do These Philosophies Originate?

The environment in which we work and the constraints around us shape philosophies. We are optimizing for something. Knowing how to drive is where intuition and synthesis are needed. The inputs are broad, but the software requires discreteness. *Philosophy is theoretical and sticky, and the framework is practical and bedrock*.

In the case above, we realized the items flowing through our pipes in a B2B context were highly constrained, leading to the reasoning we can map customer pain on one monitor. Additional inputs came from the environment around us. One such example is heightened organizational sensitivity of observability throughout all systems — and the abundance of external support.

Philosophies crystalize delegation effectively because if a team believes, they will work furiously in that direction. Like [software delegation](https://wiki.c2.com/?WhatIsDelegation), ***a team’s signature resolves by design.*** This design is the [commander’s intent](https://hbr.org/2010/11/dont-play-golf-in-a-football-g). Software engineering is often opinionated, so philosophies matter. *They are virtual commanders*.

By stating the philosophy, every engineer in the team has a unified mental model. They work through a potential framework to satisfy it. And if there is disagreement, the philosophy needs to be retooled. Ideally, anyone on the team can reshape and re-delegate.

What are the origins of philosophies? They are sourced by those that aggregate knowledge. Those that have the experience can then bring forward a library of available pivots.

## Philosophies are Portable and Repeatable

In a previous role, we would go around stating, “let’s keep our apps as dumb as possible.” I realized this was a philosophy. It had an immense impact on qualitative construction through delegation.

And recently, I’ve had a conversation with an engineer about unit tests. What we realized is that the philosophy of testing our software had shifted. No longer was it about “every [pull request](https://dev.to/solidi/be-a-rockstar-at-pull-requests-1e4f) has unit tests,” but it was “test to the design, not the implementation” — and that framework of integration tests made way more sense in the environment. The structure was to solve the problem faced by engineers in a monolith by the sheer exhaustion of dealing with overly mocked unit tests.

To the point, in software, ***philosophies appear portable and repeatable***. I have a growing list discovered in each project. Only experience will unlock these opinions in the dimensions of technical, product, design, and meta (how teams do their work).

## Conclusion

Finally, I’d like to leave with a thought about how I’ve seen software built. Metaphorically, someone in the group muttered something resoundingly impactful about plans in a software system. [Without wood, hammers, and nails](https://mitpress.mit.edu/books/software-arts) in the office, ***philosophy is a virtual foreperson and delegates in software engineering***.

---

## Another Example of the Phenomenon

Philosophies and frameworks are born out of problems that need solving — another example in the video below. Louis Castle explains avoiding artificial idiocy (theory) and layering the edge cases (framework) to make an RTS way pathing game mechanics smart enough. As he explains, subtly, "always tell(ing) people if you spend more time making sure it doesn’t do something stupid, it will look smart."

Those that believe in a way are repeating the mantra over and over again. *By doing this, by definition, is a philosophy that transmits and delegates*.

[War Stories on Command and Conquer](https://www.youtube.com/watch?v=S-VAL7Epn3o&t=412s)

---

## Social Post

On how teams do their work in software:

- Teams get their work done guided by philosophies.
- Philosophy is Direction.
- A team's signature resolves by design.
- Philosophies appear portable and repeatable.
- Philosophy is a virtual foreperson and delegates in software engineering.

Thanks to Hazem Saleh

#effectiveness #teamwork #philosophy #softwaredevelopment
