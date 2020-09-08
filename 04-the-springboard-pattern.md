# The Springboard Pattern

> Software development is not a form of construction.
A few years ago at an agile demo a stakeholder made a special appearance. The team was closing in on a minimum viable product. The demonstration focused on sound effects and animations. The team revealed a configurable animation board to demo the effects quickly. The experiences were easy to launch consecutively; isolated and variably configured. The animation board did not depend on the larger system but the intention was to tie each animation in later.

While the team demoed, the stakeholder asked if the animation board could be evaluated for further experimentation. With this feedback the team noted the unrealized value and quickly wrote down what to explore next. Of course, this wasn’t the first time the team used the technique. Other similar discoveries were made during previous demos. The team was aware the feature isolation and containment was incredibly powerful both for their demos and for product value.

For us as engineers, naming things is really hard. Harder still is how to communicate things. To the above story, there exists no vocabulary to describe the effort of execution. There is no description for the iterative containment orchestration in software engineering.

So this is what I am to propose, a definition to describe the unique execution with its benefits and drawbacks. Developing and demoing in containment is an example of what I call the springboard pattern.

Let’s describe what the pattern is.

## What Is The Springboard Pattern?
The springboard pattern is known as a visual design pattern. Mobile operating systems that have constrained viewing areas have used the pattern widely. The app launcher is an example.


> The springboard visual design pattern used on app launchers.
Our introductory story and its animation board also fits this model. We can think of the animation board as the contained screen launcher and each animation as a contained app with its configurations.

When applied to software development, the springboard pattern acts as a guardrail to develop features in isolated pieces that are easily demonstrable on the platform. There are many benefits to engineering and product. The pattern is a way to operationally execute both iteratively and incrementally.

The springboard pattern is a way to keep dependencies in check and develop features on a cycle centered around product demonstrations. Here are the rules an engineer must follow while iterating.

The feature…

1. Is launched from a board that includes other features.
1. Can launch quickly with minimum setup.
1. Can launch on its own and in any order.
1. Can be configured to launch in any state.
1. Resists larger system coupling and dependencies.

If we follow these rules as a feature is developed, magic happens. This includes promotion of modularity, testability and build time, unrealized product ideation, engineer efficiency and advantages of the framework. Let’s discuss these next.

## Promotes Modularity
The springboard pattern insists features to be developed in isolation from one another. As each feature is developed, the team must do their best to develop the solution in containment.

Dependencies will certainly be used but the layers must be made to cleanly separate the feature for demonstration. The feature should be modularized and independent. As the iterations continue and demos succeed, the springboard item should then be integrated into the larger system. As this occurs, the team should continue to resist coupling and ensure the feature code cohesion is high. From start to finish, each item should have a weak measure of connascence.


> The springboard design pattern.
At any time during the cycle the pattern can be easily violated, diminishing the return of the modularization and to the springboard pattern. Therefore, the team must make prudent and deliberate decisions by leaning on tools of layering, wrapping, and flow of control using dependency inversion.

## Supports Testability And Build Time
The development of a demonstrable item from the springboard must be tested well. The unit tests that are developed will also serve as documentation of the module.

The concept of the springboard pattern is one that promotes testability. Its dependencies should be highly configurable. The feature should have available configurations available for its dependency injections. Thus this promotes ease of testing and mocking of all situations of the feature.

Build time also is maintained and the complexity of the codebase is normalized with each feature. Incoming features can be flagged not to be built and those features that are rejected from the demos are continuously removed.

Finally, a natural phenomenon of the springboard pattern can reveal and produce diagnostic test tooling of that individual feature. The feature had started a life without the larger system to prove only itself. The springboard can produce tools that test part of the feature in contra to the larger system as they are their own subsystems.

## Product Ideation And Engineer Efficiency
Opportunities happen when products are deconstructed into independent pieces. In the case of the introduction example, there appeared to be an unrealized product value in the use of an animation board.

Stakeholders refer to the features of their products as cohesive constructs and use vocabulary to describe them. Wouldn’t it be powerful to immediately find the feature without friction? The springboard gives us a learning library and allows for cross pollination between engineers and gives us a tool to quickly locate how each feature was built.


A simple springboard example with domain language.
As an additional benefit, the engineers work is always available to be demonstrated at a moments notice. The usual cost of the time to prepare for the demo (you are giving time for the engineers to prep, yes?) is offset by a more isolated solution.

Mileage may vary depending on domain and the reception from stakeholders. In the most pragmatic terms, products must predict less and experiment more. Having the features deconstructed and isolated may predict a different outcome or a reconfiguration of that product value.

## Framework Support
With the springboard pattern, there could be undiscovered efficiency benefits that coincide with features of the framework. The framework the team works with may vary. For this post, I’ll discuss Android in relation to the use of a springboard.

Recently in the Android ecosystem, Google has launched Instant Apps and discussed at length the incorporation and break out of new concepts in the area called feature modules. As we can see from above, everything that is demonstrable to stakeholders should be modular and isolated. As the work is developed, insulate each feature from major dependencies and optimize dependencies for every feature. Product may want to launch these features separate or together.

Another example on Android is the concept of isolated activities. Each activity should be able to launched in isolation taking only what it needs to survive an experience. If features are built in isolated activities, the software acquire pieces of an application that can be easily reconfigured to taste.

Finally with the latest versions of Android, its tooling have significantly improved. Independent modules allow for building abilities which significantly decrease build time. Setups that use flavored code organization may cause building delays especially if the product dimensions are extensive.

Before we conclude, there are drawbacks to consider.

## Drawbacks
There are possible drawbacks to this mode of execution. The team will have to make decisions that make the most sense to steer clear of over engineering.

The springboard approach may…

1. Violate YAGNI — “You ain’t gonna need it”. The team should build only what they need, and not a single line more.
1. Accelerate decisions — the best architectural decisions are the ones that are deferred. Operating this way may force harder code decisions sooner.
1. Increase complexity — additional logic to support layering and modularization may increase time to contribute and slightly longer development time.
However, keep in mind that the cost paid will most certainly provide a cost benefit for code that is consistent and adaptable. Adaptability needs room to breathe and the code and products deserve that breathing room.

Now let’s wrap this up.

## Spring Into Action
Developing for isolation and modularity is a practice all engineers should strive for. However, there had not been a pragmatic approach to these concepts and a way to describe how to execute on them. It is assumed engineers simply build this way but the reality is that they simply do not.

The springboard pattern in software development finally gives us a word to use to communicate our intention both in software execution. When adhering to this pattern, we manage complexity and increase optionality. As described above, the benefits are plenty, but be aware of the cost of drawbacks.

The springboard pattern takes effort and drive but the benefits could be incredible to the team and to their products. Center the pattern around the team demos and adhere to it.

---

## Social Post

How to organize new #software #features in #isolation? Use the springboard pattern.

- develop features on a cycle centered around product demonstrations 
- keep dependencies in check
- guardrail to develop features in isolated pieces that are easily demonstrable on the platform
- manage complexity and increase optionality
- operationally execute both iteratively and incrementally

Thanks to Shawn Carrillo, Alex Hart, and Hazem Saleh, and Konrad Stanik. 

https://medium.com/hackernoon/the-springboard-pattern-340e00379404

#softwaredevelopment #code #softwareengineering #learning #demos #productivity
