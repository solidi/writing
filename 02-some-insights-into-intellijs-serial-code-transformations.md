# Some insights into IntelliJ’s Serial Code Transformations
## Questioning Editor Enhancements and Their Consequences

Our integrated development environment has introduced user interface improvements that may have profound impact and opportunity in the way we code. We will call these serial code transformations.

## Introduction

As I was chatting on Workplace with our SVP of Engineering about his new post on Kotlin, our conversation shifted from his trials as a young engineer to how terrifyingly awesome the recent integrated development environment (IDE) experience has become. With thirty plus years under his belt, he had seen many IDE environments from visual to textual and back again.

It goes without saying that the IDE has been and still is the extension of the developer’s hands. The IDE and its tooling are what make developers productive. From the individual to the collective, IDEs have the power to cradle and support larger team efforts. One of the many great examples is what transpired over at Uber. The IDE played a key role to that success.

While there are many environments to choose from, my focus will revolve around JetBrains’ IntelliJ. I chose IntelliJ because there is an interesting improvement trend unfolding that I’d like to explore in its user interface. We will discuss three recent additions added to IntelliJ 2016.2, 2016.3 and 2018.1. There could be more to come in the 2018 version series.

We will review these user interface improvements with the perceived pros of readability, proper labeling, and discoverability. We will also review the cons of visual noise, code quality consequences, and nondeterministic code.

I’ll label these additions as serial code transformations (SECTAs). Before we focus on the transformations, let’s next explore IntelliJ’s historical origin and then its tooling strengths.

## A Brief History On IntelliJ

IntelliJ’s strength has been in supporting Java. Since IntelliJ’s inception in the new Millenium and the rise of Java, IntelliJ had entered to compete in the IDE space against NetBeans and JBuilder.

The story of JBuilder is long. However, in the end it has been swallowed by Eclipse. As Eclipse took over JBuilder, NetBeans began jockeying as the preferred IDE for Java.

Over the years, major domains controlled by Java rose. This brought about power popularity struggles. One such major case was when JetBrains paired with Google and then Android development transitioned from Eclipse to IntelliJ. There are many reasons why this happened. Gradle support was absent.

With IntelliJ’s rise, NetBeans’ popularity waned with the transition from Sun to Oracle. With recent problems such as NetBeans parent abandoning it, the future of NetBeans now lies in Apache’s hands.

NetBeans still holds a slice of Java server side development. IntelliJ is now the popular go-to for most Java, Scala, Groovy and Kotlin ideation. A new chunk of engagement had been from Android and some Java server sided development in its ultimate edition. JetBrains has also started down the route of supporting iOS development.

With IntelliJ pulling ahead above all IDEs in the space, JetBrains continues to improve. IntelliJ’s implementation of clever code completion, build system plugin integrations, code and flow control analysis, and other major integration points like version control and testing make it difficult to find a developer who hasn’t used it. Most of them praise the software.

## IntelliJ’s North Star

Historically, IntelliJ has had a very public north star. IntelliJ’s authors want engineers to “develop with pleasure.” This pleasure had a lot to do with their development of refactoring tooling since its inception. Without question the refactor tooling has been improved (mercifully) in the past ten years.

Their terrifying advanced hotkeys are also true to that pleasure. This is a highly welcomed addition to all the incrementing intelligent code completion now dubbed “deep intelligence.”

One of my earlier experiences with IntelliJ’s pleasure was in the refactoring tooling. I was a witness to those like Robert Martin (Uncle Bob) and his blazingly fast refactors in such videos as the bowling game kata. The IDE was essentially doing all the work. Extracting, rearranging, and abstracting, all with keyed shortcuts. Simply memorize the shortcuts and where to place the cursor and let the tooling refactor with pleasure.

As with all tools in the IDE, the refactoring tooling changes code that we commit for the better, as long as it is steered with engineering principles. Couple that with great lint tooling, code analysis, and now flow control, and it gives you the power to modify code intelligently and quickly.

In the past few iterations of IntelliJ, JetBrains had introduced new under-the-radar improvements to further the pleasure. JetBrains has labeled them under their “User Interface” improvements section, but I’ll label these as serial code transformations. The first few have been added within the past six to nine months.

What are SECTAs? Let’s review some examples next.

## Our First SECTA

One of the more recent code reviews that came up at camp was the use of booleans as parameters in methods.

Of course, we know that adding a boolean parameter to a method could be considered a code smell. It signals that this method may have two distinct options, and thus violates the SRP rule.

It can be difficult to understand the usage of a primitive boolean type. As the boolean is being passed through method calls, the developer has to dig to see the signature and the parameter name to understand the usage at a distance. In many cases this breaks mental concentration.

The decision to disallow a boolean parameter could be dogmatic if the codebase already has other methods using a similar pattern. Also, it depends on the usage. A method that uses a boolean without splitting fundamental two paths way could be acceptable.

Lets say we agreed to add the boolean. How do we fix the developer visibility through the method calls? The answer here is that we do not. IntelliJ solves this problem with a SECTA.

Our first SECTA is called a parameter hint. IntelliJ adds visible labeled metadata that doesn’t exist in code. However it appears to be inline code.

As a visual example, notice the gray non-monospaced label “append” next to true below. This is a parameter hint.


“append” is an example of IntelliJ’s parameter hints.
When I first saw these parameter hints some months ago, I thought a special debug mode had inadvertently been turned on.

IntelliJ now ships with parameter hints turned on by default, so many developers are becoming familiar with the style. They are continuing to improve it with the expansion of hints to other parts of the code and filtering of hints where restraint is required.

## Our Second SECTA

Sometime ago, Uncle Bob took on the quest to define a final programming language. In his exploration, he discovered many thought-provoking ideas and concepts. When he described what the ideal language’s attributes should be, he questioned if there could be a better way to declare inequality than !=.

Now there is. A recent example was introduced at Google I/O this year at the Intro To Kotlin session. Enter code ligatures, also known as font ligatures.

Hadi Hariri, the host of the I/O session, had introduced the use of code ligatures at previous Kotlin demos. He had now done so at a major developer conference.

Code ligatures have been around for a few years with many IDEs supporting them in some way. Many require the use of plugins. However, none have adopted the ligature to the point of mass popularity, and few have direct support for them. This trend is changing, and it’s coming to a IDE near you.

Code ligatures are different and radical — this new tool transforms code while the developer types the code.

At the moment, code ligatures are turned off by default in IntelliJ. However, I believe that IntelliJ is about to change this at scale so that they become more popular. Hadi is on a mission to do this.

Code ligatures are shocking to those who have developed for some time. See the example below.


Live demonstration by Hadi Hariri of a code ligature in Kotlin.
As an example, the code ligature changes != into ≠. There are many other replacement examples. The goal of code ligature is readability. To see more examples, see FiraCode. IntelliJ has implemented FiraCode as the preferred font ligature.

When Hadi demoed the code ligature above, I was in the audience. I looked over at one of the engineers and I mouthed “WHAT?” There was an audible shock wave throughout the session when it first appeared on the screen.

Hadi did not use a unicode trick or a shortcut to a new symbol. IntelliJ performed the glyph exchange automatically.

## Our Third SECTA

Annotations are statements that serve metadata to improve or describe the behavior of co-located code. They were introduced widely in programming languages within the last twenty years. The most famous is the Java annotation and the C# attribute.

Since the annotation’s inception, JetBrains realized its benefits and applied them to IntelliJ. They also introduced interesting ideas. For example, they realized problems with null when interacting with class libraries. Since these libraries could not be edited, they proposed improving usage of such libraries by implementing ideas like the external annotation system.

While there is a continuing debate about the effectiveness of the annotation in these languages, it has been extensively iterated upon by companies like JetBrains.

For example, annotations were introduced to help call out and reduce the amount of Java NullPointer exceptions in code. IntelliJ also introduced a static analysis tool that infers nullity. This tool was developed to scan code in an ad hoc matter. Then it would annotate areas of the code where null concerns were present. These annotations became a part of a project’s source control.

However, IntelliJ improved this concept by taking the next step with automatic inline inference of nullity. Instead of running the tool and committing the annotations in code, it is now dynamic and happening in real time.


@NotNull is both inlined and inferred. It does not exist in the code, but is a construct that is handled by the IDE.
As seen above, the @NotNull annotation does not exist in code. It appears with an IDE option turned on. As a developer types code, these annotations appear. Nullity checking is now constantly vigilant about changing code.

These are beautiful automatic orchestrations of code analysis. The appearance of the annotation is fascinating.

While the automatic appearance of the annotation could be helpful and perhaps may reduce issues with our code, it cannot be easily captured in source.

Like magic, if the option is unchecked, all of the generated annotations go away as well.


The power of code impact is in the checkmark.
Now that we have a good understanding of these transformations, let’s analyze the pros and cons.

## The Pros Of SECTAs

The pros of SECTAs are straightforward and clear.

### Method parameter and operator readability
The developer can lean on the IDE to see clearly the intent of the parameters and operator statements. This is also true for boolean parameters, since they are not, as values, self describing.

### Improves stability of the software
Since inferred annotations like @NotNull and @Nullable are being analyzed and added constantly, the software may become more stable over time by avoiding poor choices of null parameter usage.

### Method discoverability
Parameter hints can help with quick discovery on how to use the method calls if the parameter names are highly described. The hints provide natural discovery on how to use the method.

### Potential for something wonderful
What is so wonderful about SECTAs is that there is a possibility to build upon them visually. Serially transforming the code along with the developer’s work helps with readability. I will discuss more of its wonderful potential in the final section.

## The Cons Of SECTAs

SECTAs can have very impactful cons. Lets discuss them.

### Visual noise and clutter
Having parameter hints throughout the code may make concentration difficult for authors who already have a mental model of the areas of code that they are currently working in. It may visually clutter the workspace and make development less pleasurable.

For those developers who have been trained to read the usual character combinations for equality, assignment, indirection and other operators, the use of the code ligatures could be initially awkward. Some will continue to prefer the traditional usage.

### Code quality consequences
One could argue that the use of parameter hints is a route to bike-shedding. But we no longer debate about the architecture or the use of a boolean as we once did. This is because the readability of the boolean is no longer a concern. The IDE simply handles the transformation. It makes a possibly poor design decision expressive and clear.

### Nondeterministic code concerns
By their nature, SECTAs are virtual and depend on the IDE software version. This is difficult for version control, as it can not capture the IDE environment context effectively. Code that was once the truth in the environment may not read the same with an IDE upgrade. When the IDE is upgraded or changed, there could be consequences to shifting or missing implementation of the transformations.

For code ligatures, IDEs are beginning to transform operational symbols. These symbols also do not exist in code. They are glyph transformations on the code to make it more expressive based on a font. Even if the font is changing the symbol, it’s changing the truth of the code.

A very recent and public mistake on nondeterministic tooling was recently discovered with Gradle’s variant versions. It has been suggested by the community not to use variant versions.

## The Future

When we see and use SECTAs, we should question and explore them. Watch closely for new transformations. I’m sure more will be introduced over the next versions of IntelliJ.

It’s worth mentioning that these SECTAs are in fact serial. I named them such because textual code is by nature serially imperative. We expect to read from top to bottom and expect something to happen as we read.

With the cons in mind, are serial code transformations a slippery slope to something more insidious?

I’m not sure. In many ways, we are moving into the world of “mixed reality” in our code editors, and this is the start. Metadata is laid over text to help us navigate and read transformative and expressive code that may not have been on it’s own or because of a language limitation.

What’s more, it’s not breakpoints, bread crumbing, or code folding that we should question. What we should question is direct assistance on the visual readability and understandability of what we write in real time.

We may be fine with serial code transformations if IDEs standardize.

If the IDE authors continually add transformations, do the nuances between languages begin to disappear? It’s way too early to say, but it would be highly interesting and fun if the tooling could make language dialect boundaries blend. Layering SECTAs could prove very powerful.

However, to balance the excitement, these code transformations may not allow us to say that the code we have committed is the truth. Maybe there could be a way to make the transformations deterministic. An answer to this question could be a major discovery in our field.

Should we allow these tools to add to or transform what is actually in the code? Maybe. In a lot of ways, tools do this visually (and in fact some languages are visual). But it’s something profound to layer visually over serially textual code that we all love to write.

More fundamentally, if the IDE continues to iterate on these SECTAs, does our language selection matter less? This is an interesting and thought-provoking question, and I’m very curious to see where it shakes out over the next few years. Hopefully IntelliJ can take that step to help every single developer to better express their creative desire to make code work well.
