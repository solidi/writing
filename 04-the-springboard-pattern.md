# The Springboard Pattern
## How to build new features in isolation
#programming, #beginners, #tutorial, #productivity

![Software development is not a form of construction.](images/04-01.png)

A few years ago, at an agile demo, a stakeholder made a special appearance. The team was closing in on a minimum viable product. The demonstration focused on sound effects and animations. The group revealed a configurable animation board to demo the results quickly. The experiences were easy to launch consecutively, isolated, and variably configured. The animation board did not depend on the more extensive system, but the intention was to tie each animation later.

While the team demoed, the stakeholder asked if we evaluate the animation board for further experimentation. With this feedback, the group noted the ***unrealized*** value and quickly wrote down what to explore next. Of course, this wasn’t the first time the team used the technique. We made similar discoveries in [future demos](https://dev.to/solidi/how-to-crush-your-next-team-demo-2bb5). The team was aware the feature containment were incredibly powerful both for their demos and for product value.

For us as engineers, naming things is hard. Harder still is how to communicate something. To the above story, there exists no vocabulary to describe the effort of execution. There is no description for the iterative containment orchestration in ***software engineering***.

So this is what I propose, a definition to describe the unique execution with its benefits and drawbacks. Developing and demoing in containment is an example of what I call the **springboard pattern**.

Let’s describe what the pattern is.

## What Is The Springboard Pattern?

The springboard pattern is known as a ***visual design*** pattern. Mobile operating systems that constrain viewing areas have used the pattern widely. The app launcher is an example.

![Above are examples of the springboard visual design pattern within app launchers.](images/04-02.png)

Our introductory story and its animation board also fit this model. We can think of the animation board as the contained screen launcher and each animation as an organized app with its configurations.

When applied to software development, the springboard pattern acts as a guardrail to develop features in isolated pieces that are easily ***demonstrable*** on the platform. There are many benefits to engineering and product. The design is a way to execute both iteratively and incrementally operationally.

The springboard pattern is a way to keep dependencies in check and develop features on a cycle centered around ***product demonstrations***. Here are the rules an engineer must follow while iterating.

The feature:

1. It launches from a board that includes other features.
1. Can launch quickly with minimum setup.
1. It can launch on its own and in any order.
1. The configuration is possible to launch in any state.
1. The feature resists larger system coupling and dependencies.

If we follow these rules during feature development, magic happens. Benefits include the promotion of modularity, testability, and build-time. Additional improvements include [product ideation](https://dev.to/solidi/what-is-a-product-manager-anyway-3pc4) that is unrealized, engineer efficiency, and advantages of the framework. Let’s discuss these next.

## Promotes Modularity

The springboard pattern insists on developing features in isolation from one another. In each design segment, the team must do their best to create a solution in ***containment***.

Dependencies will always be present, but the layers separate the feature for demonstration cleanly. The feature should be modularized and independent. As the iterations continue and demos succeed, the springboard items integrate into the extensive system. As this occurs, the team should continue to resist coupling and ensure the feature code cohesion is high. From start to finish, each item should have a weak measure of ***connascence***.

![The springboard design pattern.](images/04-03.png)

At any time during the cycle, pattern violation can diminish the return of the modularization. Therefore, the team must make ***prudent and deliberate*** decisions by leaning on tools of layering, wrapping, and flow of control using dependency inversion.

## Supports Testability And Build Time

The development of a demonstrable item from the springboard demands testability. The unit tests will also serve as documentation of the module.

The concept of the springboard pattern is one that promotes testability. Its dependencies should be highly configurable. The feature should have available configurations available for its ***dependency injections***. Thus this supports ease of testing and mocking of all situations of the component.

Build time also is maintained, and the complexity of the codebase is normalized with each feature. Incoming features can be ***flagged*** to be unbuilt by the toolset. Features that are rejected from demos are continuously removed.

Finally, a natural phenomenon of the springboard pattern can reveal ***diagnostic test tooling*** of that unique feature. The feature had started life without the extensive system. The springboard can make tools that test part of the feature in contra to the more comprehensive system as they are their subsystems.

## Product Ideation And Engineer Efficiency

Opportunities happen when products are deconstructed into independent pieces. In the case of the introduction example, there appeared to be an unrealized product value in the use of an animation board.

Stakeholders refer to the features of their products as cohesive constructs and use vocabulary to describe them. Wouldn’t it be powerful to find the part without friction immediately? The springboard gives us a ***learning library*** and allows for ***cross-pollination*** between engineers and gives us a tool to locate each feature quickly.

![Above is a screenshot of a springboard example with the use of the domain language.](images/04-04.png)

As an additional benefit, the engineer’s work is ***always available*** for demonstration at a moment’s notice. An isolated solution offsets the typical cost of the time to prepare for the demo (you are giving time for the engineers to prep, yes?).

Mileage may vary depending on the domain and the reception from stakeholders. In the most pragmatic terms, products must predict less and experiment more. Having the features deconstructed and isolated may indicate a different outcome or a reconfiguration of that product value.

## Framework Support

With the springboard pattern, there could be undiscovered ***efficiency*** benefits that coincide with features of the framework. The framework the team works with may vary. For this post, I’ll discuss Android concerning the use of a springboard.

Recently in the Android ecosystem, Google has launched [Instant Apps](https://developer.android.com/topic/instant-apps/index.html) and discussed at length the incorporation and break out of new concepts in the area called ***feature modules***. As we can see from above, everything that is demonstrable to stakeholders should be modular and isolated. As development continues, insulate each feature from significant dependencies and optimize them for every feature. The product team may want to launch these features separately or together.

Another example of Android is the concept of isolated ***activities***. Each activity should be able to launch in isolation, taking what it needs to survive an experience. If features are built-in isolated activities, reconfiguration of the pieces of an application is possible.

Finally, with the latest versions of Android, its tooling have significantly improved. Independent modules allow for building abilities, which significantly reduce build time. Setups that use a ***flavored*** code organization may cause building delays, especially if the product dimensions are extensive.

Before we conclude, there are drawbacks to consider.

## Drawbacks

There are possible drawbacks to this mode of execution. The team will have to make decisions that make the most sense to steer clear of over-engineering.

The springboard approach may:

1. **Violate YAGNI** — “[You ain’t gonna need it](https://martinfowler.com/bliki/Yagni.html).” The team should build what they need, and not a single line more.
1. **Accelerate decisions** — deferring architectural choices is an excellent strategy to keep complexity manageable. Operating this way may force challenging code decisions sooner.
1. **Increase complexity** — additional logic to support layering and modularization may increase development time.

However, keep in mind that the cost paid will most certainly provide a cost-benefit for code that is consistent and adaptable. ***Adaptability*** needs room to breathe. The code and products deserve that breathing room.

Now let’s wrap this up.

## Spring Into Action

Developing for isolation and modularity is a practice all engineers should strive for. However, there had not been a pragmatic approach to these concepts and a way to describe how to execute on them. It is assumed engineers build this way, but the reality is that they do not.

The ***springboard pattern*** in software development finally gives us a word to communicate our intention both in software execution. When adhering to this pattern, we manage ***complexity*** and increase ***optionality***. As described above, the benefits are plenty, but be aware of the cost of drawbacks.

The springboard pattern takes effort and drive, but the benefits could be incredible to the team and their products. Center the way around the team demos and adhere to it.

---

## Social Post

How to organize new #software #features in #isolation? Use the springboard pattern.
Alt title: How to organize and build features in isolation? (2017)

- develop features on a cycle centered around product demonstrations 
- keep dependencies in check
- guardrail to develop features in isolated pieces that are easily demonstrable on the platform
- manage complexity and increase optionality
- operationally execute both iteratively and incrementally

Thanks to Shawn Carrillo, Alex Hart, and Hazem Saleh, and Konrad Stanik. 

[medium](https://medium.com/hackernoon/the-springboard-pattern-340e00379404)
[linkedin](https://www.linkedin.com/pulse/springboard-pattern-douglas-w-arcuri/)
[dev.to](https://dev.to/solidi/the-springboard-pattern-3o04)
[twitter mention](https://twitter.com/CodeNewbies/status/1686907485846642688)
[twitter mention 2](https://twitter.com/ThePracticalDev/status/1687196893036658689)

#softwaredevelopment #code #softwareengineering #learning #demos #productivity
