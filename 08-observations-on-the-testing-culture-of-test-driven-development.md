# Observations on the testing culture of Test Driven Development

![A homage to “purple” wires installed by IBM field engineers decades ago. They were yellow.](https://miro.medium.com/max/1400/1*s1wnrbNeea89uz6GsPe6jw.png)

*This post is not a primer on Test Driven Development. It contains my observations of re-starting the discipline and the problem of unit testing craft.*

Kent Beck, a software engineering leader, is also the modern-day re-inventor of test-driven development (TDD). Kent also cowrote JUnit, a widely used testing framework, with Erich Gamma.

In his book, [XP Explained](https://www.pearson.com/us/higher-education/program/Beck-Extreme-Programming-Explained-Embrace-Change-2nd-Edition/PGM155384.html) (second edition), Kent describes that at the intersection of **values** and **practices**, form **principles**. When we iterate from the concept and plugin what we believe as a formula, we achieve a transformation.

```
[KISS, Quality, YAGNI, ...] + [Testing, Specs, ...] == [TDD, ...]
```

I have a profound respect for Kent’s life work not only because of his brilliant software creations but also his continued exploration of **trust**, **courage**, **feedback**, **simplicity**, and **vulnerability**. All attributes are paramount to the invention of Extreme Programming (XP).

TDD is a **principle** and a **discipline** that is followed by the XP community. The field has been present for nineteen years.

In this post, I will describe my opinion of where TDD stands in its adoption. Following this, we will explore intriguing personal observations as we perform TDD. Finally, we will conclude by postulating why TDD hasn’t become standard practice. Let’s begin.

## TDD, Studies, And Professionalism

Nineteen years in TDD is still debated as a discipline in the development community.
The first question an analytical person would ask, is “How many or what percentage of software professionals use TDD today?” If you asked Robert Martin (Uncle Bob), a friend of Kent Beck, the answer would be one hundred percent. Uncle Bob believes that it is infeasible to consider being a professional if test-driven development is not practiced. [1]

Uncle Bob has been the focus of the discipline for some years now, and it is natural to discuss him as a part of this write-up. Uncle Bob has defended TDD and has pushed the discipline’s boundaries significantly.

However, no one asks the follow-up question, “the definition of **practice** is the deliberate use of — but it does not specify the amount or percentage of, right?” My subjective estimation is that a majority of [software engineers](https://dev.to/solidi/what-is-a-software-engineer-anyway-3fb2) have not practiced TDD in a small timeframe.

The reality of the situation is that we **do not know**, since the practice percentage has not been studied widely. The only concrete measurement we have is a small collection of companies being gathered at [WeDoTDD](http://www.wedotdd.com/). WeDoTDD tracks these companies. Interviews are conducted with those who practice 100% of the time, but that list is small. It is also incomplete since searching reveals other larger shops are practicing — but perhaps not at full capacity.

If we don’t know how many are practicing, the next question is, “how effective is TDD based on measured benefits?”

There have been studies conducted over the years that have proven TDD’s effectiveness. Write-ups include well-recognized reports from [Microsoft](https://collaboration.csc.ncsu.edu/laurie/Papers/Unit_testing_cameraReady.pdf), [IBM](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.567.3740&rep=rep1&type=pdf), North Carolina University, and the [University of Helsinki](https://helda.helsinki.fi//bitstream/handle/10138/42741/2014_01_swqd_author_version.pdf?sequence=2).

![An impactful visual is taken from the Helsinki report.](https://miro.medium.com/max/1400/1*7TM_Dr62nyebITPsLWZBwA.png)

These reports prove to the degree that defect density is reduced by 40% to 60% in exchange for increased effort and execution time by 15% to 35%. These numbers have also begun to echo through books and new industries such as the DevOps community.

With these questions half answered, the final question is, “what should I expect as I start to perform TDD?” You are in luck because I have formulated my observations of TDD. Let’s review them next.

## 1. TDD Commands Verbalizing An Approach

As we practice TDD, we begin to experience the phenomena of “calling the shot.” In simple terms, the short acts of creating failing and passing tests will intellectually challenge the developer. They will say aloud, “I think this will pass” and “I do not think this will pass” or “I’m not sure, let me think after I try this approach.”

The developer’s IDE (integrated developer environment) has become a rubber duck begging for an intense conversation. At a minimum, TDD shops should be humming with this type of conversion.

> Think, then speak up about your immediate next move(s).

This type of reinforcement is key to communication, not only to predict your next action but also to reinforce the concepts of writing the most **straightforward** code to make a unit test pass. Of course, if the developer becomes silent, they are almost certainly wandering off the loop and must come back on the path.

## 2. TDD Commands Muscle Memory

As a developer moves forward with the first cycles of TDD, they will experience heavy fatigue by battling through high friction and awkward flow. The fatigue is right for any initiated but unlearned human activity. The developer will attempt to find shortcuts to improve the cycle because the goal is to reduce that awkwardness and to enhance muscle memory.

Muscle memory is the key to feeling good vibes and becoming fluid. TDD demands it because of execution repetition.

> Print out a shortcut cheat sheet. Learn only as many shortcuts in your IDE as you need to make your cycles efficient. Then, keep searching for more.

The developer will become an expert of shortcuts only in a matter of a few sittings, including building and running the test rig. With more practice, creating new artifacts, highlighting text, and navigating the IDE will become natural. Finally, we graduate to unlock all of the refactor shortcuts such as extraction, renaming, generation, pulling up, reformatting, and pushing down code.

## 3. TDD Commands Thinking At Least Slightly Forward

Each time a developer sits to start TDD, they must have a concrete short mental map on what is to be solved. In a traditional coding approach, this is not always true, as the mental map of the solution could be macro and exploratory. The developer does not know how to solve the problem but may know of a fuzzy goal. To get to that goal, unit tests are neglected in the process.

The start and end of the sitting should also be ritualized. First, think, and list. Play with it. List more. Then start, do, and then think. Check off. Repeat some times. Finally, think, and stop.

> Maintain your test list like a hawk. Check off items as you go. Never drive without one. Think!

The list may take some time to formulate and is not a part of the cycle. However, it should be prepared before the revolutions start. If you don’t have one, you may not know where you are going. Always have a map.

```kotlin
// A Test List
// "" -> does not validate
// "a" -> does not validate
// "aa" -> validates
// "racecar" -> validates
// "Racecar" -> validates
// print the validation
// have a blueberry ale
```

The developer must command a **test list**, as described by Kent Beck. The test list allows the direction of solving in the next immediate cycles. That test list should always be labored upon and updated moments before the cycles begin. Once the test list is solved minus the last step, the cycle stops on red with a failing test.

## 4. TDD Demands Communication With Others

As the above test list is filled out, specific steps become blocked because the commitment of work was not clear. The developer cannot figure out the test list. Or the reverse. They are generating a presumptive test list that has too many guesses about the missing requirement(s). The suggestion is to stop right there.

Driving without TDD will cause implementations of unneeded complexity to occur. TDD performed mindlessly is just as dangerous.

> Speak up loudly if the test list has gaps.

In TDD, the developer must understand what to build based on the owner’s picture of the requirement(s) and no more. If the need is unclear in context, the test list will start to break down. That break down will require a conversation. Direct conversions can quickly turn into trust and respect. The short feedback loops are now established.

## 5. TDD Demands Iterative Architecture

Initially proposed in the first edition of the XP book, Kent proposed that tests should drive architecture. However, over a few years, there have been stories about how sprint teams crash into walls about a few sprints in.

Of course, having tests drive all of the architecture is unwise. Uncle Bob had agreed with other experts that architecture driven by tests is “horse sh*t.” [1] Some larger map is required, but not too far above the distributed test lists that are being worked on in the field.

Kent also called this out many years ago in the [TDD By Example](https://www.safaribooksonline.com/library/view/test-driven-development/0321146530/) book. Concurrency and security are the two significant areas where TDD cannot drive, and the developer must be concerned separately. Loosely translated, concurrency via system design is on a different level and must be labored over iteratively and in concert with TDD. Concurrency is a reality today, as some architectures are driving toward reactive extensions, the zenith of concurrency construction.

> Create a larger map of organization. A vision that goes just a little bit ahead. Make sure you are steering with the team in the same way.

However, the essential idea is the **organization** of the system, which TDD cannot effectively handle alone. Unit tests test at a lower level. Iterative architecture and TDD orchestration is challenging in practice and demands trust among all team members, pair programming, and reliable code review. There is no exact way to do this, but it will become apparent that short iterative design sessions are needed in unison with the test lists in the field.

## 6: TDD Reveals Unit Test Frailty And Degenerative Implementation

Unit tests have a funny property about them, and TDD exposes that property. They cannot prove correctness. E.W. Dijkstra had labored over this and discussed the possibility of mathematical proofs in our profession to resolve the gap.

For example, the below solves all tests around a hypothetical imperfect palindrome that the business required. It was developed with TDD.

```kotlin
// Not an imperfect palindrome.
@Test
fun `Given "", then it does not validate`() {
    "".validate().shouldBeFalse()
}
@Test
fun `Given "a", then it does not validate`() {
    "a".validate().shouldBeFalse()
}
@Test
fun `Given "aa", then it validates`() {
    "aa".validate().shouldBeTrue()
}
@Test
fun `Given "abba", then it validates`() {
    "abba".validate().shouldBeTrue()
}
@Test
fun `Given "racecar", then it validates`() {
    "racecar".validate().shouldBeTrue()
}
@Test
fun `Given "Racecar", then it validates`() {
    "Racecar".validate().shouldBeTrue()
}
```

Indeed, these tests have holes. Unit tests are frail, even for the most trivial tasks. We can never prove correctness because if we had to, it would require intense mental labor, and the needed inputs would be unimaginable.

```kotlin
// Too generic of a solve based on tests provided
fun String.validate() = if (isEmpty() || length == 1) false else toLowerCase() == toLowerCase().reversed()
// Is the best implementation and solves all tests
fun String.validate() = length > 1
```

`length > 1` could be called **degenerative implementation**. It is just enough implementation to solve the problem at hand, but on its own tells us nothing about the problem we are trying to solve.

The question is, when does a developer stop writing the tests? The answer seems to be simple. When the **business is satisfied**, not when the code author is, this may hurt our **construction passion**, and we are **embarrassed by the simplicity**. These feelings are balanced by the good feelings of clean code and the ability to refactor with confidence later. Things feel tidy and clean.

> Be aware that the unit tests are fallible but are necessary. Understand their strength and weakness. [Property-based testing](https://hypothesis.readthedocs.io/en/latest/) and [mutation testing](http://pitest.org/) may help tie up this gap.

TDD has benefits, but it can take away building the sandcastles we do not need. It is a **constraint**, but it allows us to go faster, further, and with safety.

But! No matter how frail unit tests may seem, they are a core necessity. They are required to allow **fear** to turn into **courage**. Tests allow those to refactor the code mercifully and even better; it is a guide, **documentation**, for any other developer to immediately jump in and add value to a project that is well supported by unit testing.

## 7: TDD Reveals Assertion Completion Feedback Loop

Take a step back further. For the next two phenomena, we will visit strange re-occurrences. For the first occurrence, let’s take a quick look at FizzBuzz. Here is our test list.

```kotlin
// Print numbers 9 to 15. [OK]
// For numbers divisible by 3, print Fizz instead of the number.
// ...
```

We are a few steps in. We now have a failing test.

```kotlin
@Test
fun `Given numbers, replace those divisible by 3 with "Fizz"`() {
    val machine = FizzBuzz()
    assertEquals(machine.print(), "?")
}

class FizzBuzz {
    fun print(): String {
        var output = ""
        for (i in 9..15) {
            output += if (i % 3 == 0) {
                "Fizz "
            } else "${i} "
        }
        return output.trim()
    }
}

Expected <Fizz 10 11 Fizz 13 14 Fizz>, actual <?>.
```

Naturally, if we duplicate the expected assertion data to `assertEqualsIt`, it achieves the result, and the test passes.

> As we keep querying the test rig during implementation steps, failing unit tests set around data may correctly answer their own assertions. Perhaps we can call this voodoo testing.

Sometimes failing tests will [scream a correct result](https://blog.plover.com/math/divisibility-by-19.html) that is required to make the test pass. I do not know what to call these events, perhaps **voodoo testing**. Your mileage may vary based on your laziness and test etiquette, but I have seen this happen numerous times when working to have implementation achieve canned and expected **data sets**.

## 8: TDD Reveals The Transformation Priority Premise

In TDD, one can become trapped. There are situations where the developer can be entangled by the transformations applied to achieve implementation. At some point, the testing code becomes a bottleneck to move forward — an **impasse** forms. The developer has to back out and disarm by removing a portion of the tests to get out of the hole. The developer becomes exposed.

Uncle Bob likely has experienced these impasses in his career, and then he probably realized that the act of making a test pass must require a preferred order so that the risk of an impasse is reduced. At the same time, he also realized a premise. **As the tests get more specific, the code gets more generic**.

![The order of the transformations. One should always lower-ordered changes.](https://miro.medium.com/max/1400/1*7ixCT3Mc3gTAOd0YTM-_eA.png)

This list is called the [Transformation Priority Premise](https://8thlight.com/blog/uncle-bob/2013/05/27/TheTransformationPriorityPremise.html). There seems to be an order of refactoring risk one can choose to achieve by passing a test. The selected top transformation (the simplest) is usually the best option and will incur the least risk to create a situation of an impasse.

[TPP](http://blog.cleancoder.com/uncle-bob/2013/05/27/TheTransformationPriorityPremise.html), or perhaps **Uncle Bob’s Test Calculus**, is one of the most intriguing, technical, and exciting observations to date. Use it as a guide to keeping the code as simple as possible.

> Print out the TPP list and place it at your desk. Refer to it as you drive to avoid impasses. Embrace an order of simplicity.

Before we conclude, I’d like to answer my question, “what percentage of software professionals use TDD today?” My answer stands at “I think the group is small.” I want to explore this guess below with reasons why.

## Has TDD Taken Off?

Unfortunately, it hasn’t. The percentage is subjectively low, and the search for data continues. My experience in hiring, leading teams, and being an empathic developer myself, here are my observations.

### Reason 1: No Exposure To Real Testing Culture

My educated guess is that a majority of software developers have not had the experience of learning and working through a **testing culture**.

The definition of a testing culture is a place where developers are deliberately practicing testing. They are continuously mentoring those who are not skilled in the area. Each pairing and in every pull request is a feedback loop on building individuals to become great at testing. There is also significant support up the engineering leadership chain. All managers believe in testing. When deadlines and times get tough, the test discipline is not dropped — it is maintained.

Those that have gone through a testing culture, like me, are lucky to have those observations. We can apply the experience to future projects.

## Reason 2: Unclear Educational Resources

Some have attempted to write books on the subject, such as [xUnit Patterns](http://xunitpatterns.com/) and [Effective Unit Testing](https://www.manning.com/books/effective-unit-testing). However, there seems to be no place that clearly defines what and why to test. Most resources out there do not clearly describe the craft of assertion and verification.

Open source projects are also hit or miss with useful unit tests. In these unfamiliar projects, the very first thing I do is look for tests. My disappointment is almost inevitable. I can also remember the very few instances of excitement when tests are present but also readable.

## Reason 3: No Focus In Universities

My observation of candidates over the years fresh out of university reveals a well-known assumption: little to no discipline in testing rigor. Every developer I know has learned testing afterward, some on their own, but most going through a previous testing culture experience.

## Reason 4: A Career Of High Test Passion Required

It also takes passion for being interested in testing and for understanding the details and benefits over an extensive period. You have to be hungry and obsess on clean code and doing the craft better.

Most want to get things working, achieving only half of what Kent Beck said: “First make it work, then make it right.” I empathize that to get things working is a tough battle in itself.

Testing is hard to do well, so let’s conclude on that thought.

## Conclusion

Kent’s proposal in XP included a simple formulation of **instinct**, **thought**, and **experience**. These three levels are stepping stones to execution quality measured by a **threshold**. Kent’s model explains a problem with TDD.

The threshold for clean test execution is high, in that it eclipses a baseline of experience. The majority will never become above water, and those that do are lucky — have experience from the elusive testing culture.

![From XP Explained. Initially, about design quality, imagine a higher threshold line.](https://miro.medium.com/max/1400/1*7tA4AMlNkSI0lLrCoQyYkg.png)

Software is tough enough to build and organize. Testing takes it to a whole new level of enlightenment.

Early on, I had an **instinct** that testing is essential, but my test culture **experience** came later. It took years of **thought** in my career, but without that experience of test culture, I would not have emerged above that threshold.

I believe that many developers also have this thought but cannot see the real benefit of test culture due to a lack of specific **experience**.

> TDD discipline has struggled to take off due in part to the high learning curve of testing. Even armed with veteran testing knowledge and experience, TDD requires a headspace that is unique and challenging.

Amplify this. TDD demands all that **thought** and **experience**, and more. It is not easy and is a skill. I think it is because it commands the developer’s throughput to the maximum, continuously and relentlessly. We are all **vulnerable** in the process, and few developers like being in this position.

```kotlin
@Test
fun `Given software, when we build, then we expect tests`() {
    build(software) shoudHave tests
}
```

However, TDD is an intriguing discipline and **is a tool to lean on**. Its **phenomena** should be studied in detail. If anything else, the discipline makes for better developers as the practice contains benefits that can strengthen the individual and the collective group.

---

*Inspiration for this post was due in part by [Danny Preussler](https://medium.com/u/1331e67af4e1?source=post_page-----a9b5144f868----------------------). As I re-explore the discipline, he has started running comprehensive Android TDD workshops. [Check out his recent deck here](https://speakerdeck.com/dpreussler/tdd-on-android-mobos-2018).*

[1] [Jim Coplien and Bob Martin Debate TDD](https://www.youtube.com/watch?v=KtHQGs3zFAM)

---

## Social Post

Personal observations of practing TDD stands and where it stands.

Alt: What is TDD and why it hasn't developed critical mass? (2018)

- Review studies of TDD effectivness
- Explores the steps of TDD
- Examens the observations of what happens in TDD
- Why TDD hasn't taken off in adoption

Thanks to Hazem Saleh and Danny Preussler

https://medium.com/free-code-camp/8-observations-on-test-driven-development-a9b5144f868

#softwaredevelopment #code #softwareengineering #software #career #learning #testing #productivity

