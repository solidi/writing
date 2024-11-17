# Deception: Degenerate A/B Testing
## Questionable A/B Tests Using Dark Patterns

![](images/05-01.png)

Picture a normal triangle in your head. Now picture a triangle without its area. Can you? In mathematics, a **degenerate triangle** is defined as follows:

> A degenerate triangle is formed by three collinear points. It doesn’t look like a triangle, it looks like a line segment.

![A triangle approaching degeneracy.](images/05-02.png)

It’s as if the three angles of the triangle are flattened. In theory, the triangle exists, but all that remains are overlapping linear lines.

While this essay is not about mathematics, it will attempt to classify certain A/B testing methodology as *degenerate* using patterns that approach a line of user deception, also known as *dark patterns*. Then, we will review questionable large scale tests in the tech industry. Finally, we will conclude by giving recommendations on avoiding this deception by making clear statements to our users.

Before we begin, let’s discuss what A/B testing is.

## What Is A/B Testing?

A/B testing is loosely based on statistical mathematics and theoretical *psychological* experimentation. There is a control “A” and a variation “B.” An author of a test sends these two types to a controlled percentage of users for a variation of time in the product under test. The percentage and groups of users can be controlled by *targeting*.

Once the A/B test is completed, the data is analyzed. The analysis allows the team to [steer the product in a direction](https://dev.to/solidi/what-is-a-product-manager-anyway-3pc4) based on the results. These data points are inferred by the team, driving performance indicators such as *customer retention* and *growth*, *call to action*, *revenue*, *conversion*, or to find new indicators.

Traditionally A/B testing acts on user experience, visual design, or the customer journey of the targeted system to reduce user *friction* and maximize *engagement*. Most tests are on the *surface* where the colors, layouts, or navigation flow/behavior are altered.

![A basic A/B test example. Note the difference in button color.](images/05-03.png)

[A/B testing](https://hbr.org/2017/06/a-refresher-on-ab-testing) has gained a particular *perception*. Consultancies have formed businesses around the discipline, just how they formed around search engine optimization (SEO). SEO was popular in the 2000s. A/B testing is now popular in the 2010s. While SEO was beholden to secret algorithms that can immediately change from direct control of companies like Google, A/B test logic is owned wholly by the authors who execute them to meet goals for their stakeholders.

Data collection and tooling has increased dramatically over the past few years. The authors of A/B tests have the power to walk a fine line on a code of ethics. Let’s explore this next by defining high-level dark patterns, with the first classification leverages urgent platform tools.

## Pattern 1: Act on Urgency

Those that have used Android or iOS applications know well what a notification badge is. Notification badges are visual indicators on the app icon that cue the user to important events. The badge is usually a brightly colored circle with a number associated with the notifications waiting.

![A typical, highly visible notification badge.](images/05-04.png)

### Example

Imagine if we push a badge with a deceptive count to represent subjective notification activity. Even when the user is logged out, they'll receive badges without user activity. The badge is engagement bait.

For those who are targeted, users will repeatedly engage with the application to understand what was urgent. They'll engage many times, increasing chances of an outcome, because of their presence.

### Motto: “Urgent Notification”

On mobile platforms, that notification badge is one of many routes to execute an interesting A/B test. The platform-tools will vary, but each platform has high-level indicators for engagement that users are comfortable and knowledgeable with. The users are wired to respond and engage.

Next, we will fake things.

## Pattern 2: Fake It Until We Build It

Of course, there are many parts of a digital product that haven’t been built completely yet. However, we want to increase engagement in some way.

### Example

Recently, a group of users navigated a site looking to watch a particular movie genre. As the users typed in the search result, they were steered to partial matches.

The users engaged further with similar content.

### Motto: “Canned Search Results”

Developing the final polished product is something we can fake, including search results. Instead of investing heavily in the perfect feature, we assemble the results into simple categories based on previous research.

![Results when the user searches on a subjective statement that is not quantifiable.](images/05-05.png)

Now, let’s test with scarcity.

## Pattern 3: Make Things Scarce

Manipulating critical numbers such as item stock, content number, and ratings are well known to consumer marketing. While these tricks  work temporarily, they will backfire.

We do have the power to adjust numbers to increase the outcome of engagement–to a point.

### Example

Recently a group of users had been shopping on a website—and the customers are experienced with commerce sites.

Let’s say that one of those items that the customer absolutely needed was in stock, but only "one left." Of course, this will motivate the  user to act–purchasing  in a timely manner.

The next day the user returned to the site to research another similar purchase—sixteen items were available. Their trust will quickly erode.

### Motto: “Everything is the Last Item”

This idea can be extended to whatever the product desires–and is an infringement of consumer protections. Low space, stock, rating, and a lot of things are adjustable. If your team owns a video platform, “expiring” content is another angle. Finally, anything as a number can be rounded.

![A great layout with many numbers encapsulated.](images/05-06.png)

Next, let’s test by giving away.

## Pattern 4: Give Platform Expectedly or Unexpectedly

Sometimes if we give or take away major items of the platform, it may manipulate the engagement.

### Example

A group of users was recently on an application that offered paid content behind a paywall. This app was freemium in nature.

Access became “unlocked,” and a group of users could view content for free without the paid subscription. Then time passed, and it was gone.

Some users liked the content–and so they purchased the product.

### Motto: “Curious Engagement Through Shock”

Opening the gates in an A/B test could be a potential opportunity to engage users. The process here is to select known identities to engage them further.

![A paywall can have many testable options.](images/05-07.gif)

Additionally, moving or closing things unexpectedly will stimulate engagement and increase returns. If services that are relied on are missing, those users will return frequently until it re-establishes.

Finally, we can hide things.

## Pattern 5: Platform Information Hiding

One final example is the creative use of information. Here, we conduct an A/B test that manipulates information relevant to the users at the proper time and context. We either shift the information upstream or manipulate it so that it is diluted. We reduce the *friction* of information to obtain a result. Sometimes lack of information is that friction.

### Example

An example is a service that relies on the live location of the available liveries in the area — maybe those parked or on break, increasing information will deliver engagement.

![Plenty of levels of information to reduce friction.](images/05-08.png)

### Group: “Shift, Adjust and Filter Information”

We will try to adjust information or direct the user into a desired action by either giving or taking information away at measured points. Taking it a step further in tests, information manipulation can be targeted to identified groups of users.

This wraps up the pattern examples. **Urgency**, **faking**, **scarcity**, **giving**, **hiding** are subjectively divisive. Are they unethical?

## Degenerate Tests May Be Unethical Tests

In mathematics, a degenerate triangle exists in the overarching term of degeneracy cases:

> A **degenerate** case is a limiting case in which an element of a class of objects is qualitatively different from the rest of the class and hence belongs to another, usually simpler, class. **Degeneracy** is the condition of being a **degenerate** case.

The degenerate triangle is deceptive, and so are the patterns defined above. All tests are doable without the user understanding it had happened nor platforms catching authors in the act. These A/B tests are a degenerate class of the typical e-commerce tricks such as *urgency*, *scarcity*, and *human fallacy*. These techniques are, in most cases, harmless but act on *deception*. The question posed here is when the human is unknowingly participating, is it ethical to run these tests?

The question may have already been answered because large technology companies have published their results.

## A/B/Code/Deception Testing

Some years ago, both Facebook and OkCupid deceived their users by running controversial A/B tests surrounding content engagement by companion matching. Then, they posted the results to the public. Opponents suggested that manipulating emotions and incorrectly matching incompatible date companions was wrong. This started a very long chain of responses from the [community](https://techcrunch.com/2014/06/29/ethics-in-a-data-driven-world/).

![The increasing data and tooling power will be the deciding factor. [Post here](https://www.gwern.net/docs/psychology/okcupid/weexperimentonhumanbeings.html).](images/05-09.png)

One excellent research paper focused on this test fallout. You can read it [here](https://journals.sagepub.com/doi/pdf/10.1177/1747016116680664). Raquel Benbunan-Fitch dubbed these as A/B/C/D testing, where she states:

> This is a deep form of testing, which I propose to call **Code/Deception** or **C/D** experimentation to distinguish it from the surface level testing associated with A/B testing.

Are the tests ethical? Well, the debate rages on.

The position of this author is to communicate to your customers. Let me suggest ways in which we can state our testing code of conduct.

## Ethics May Start By Saying We Are "Ethical"

While the industry is attempting to figure out how to roll out and scale A/B testing to their advantage, I’d like to define how we can avoid these types of C/D tests. Here are a few ideas that are centered around communicating the use of live user testing.

1. Clearly specifying an A/B testing section in a Terms of Service.
1. Publish an ethical statement and guiding principles of A/B testing.
1. Visually indicating an A/B test is being performed with an opt-out.

The messaging presented is up to the stakeholders, and should be plain language. The boundaries of testing must be clear.

For item three, test evangelists would agree that this behavior would highly disrupt the results, and the test would not be valid. The test author does not expect the user to feel that they are in a test “A” or “B” mode. The author wants the user to act as normal to measure correctly.

While that might be true, we would still want to give the option at an appropriate time, in user preferences or sign-up. We want to measure and satisfy the user's concern which is the *product's value.*

---

In the future, state and government agencies will define C/D testing limitations as public knowledge increases and problematic tests are uncovered. Companies may be caught performing highly degenerate tests that none of us could fathom.

What would be the consequence of being deceptive? At this time, there are **no examples** of crossing a line. We have the power to ask whether to *associate* with the authoring team that *knowingly* deploys these questionable tests or *opt-out* of these deceptive practices.

![Impactful wisdom by [Daniel Weber](https://news.ycombinator.com/item?id=8230442).](images/05-10.png)

Time will tell how deceptive testing shakes out. Data, tooling and their alignment will continue to increase testing power. Increased public awareness will spur hard questions.

If there is one lasting advice, try not to deceive... too much.

---

*If you are interested in more information on the subject of dark patterns, check out [https://darkpatterns.org/](https://darkpatterns.org/).*

---

## Social Post

Every dark #pattern is the brutal end of blindly following #A/B #tests.
Alt title: 5 dark patterns of A/B testing (2017)

- What is A/B testing?
- Five dark patterns that are questionable in A/B testing.
- More on A/B/Code/Deception testing.
- Being ethical with tests by clearly communicating expectations.

Thanks to Hazem Saleh and Dan Leonardis.

[medium](https://medium.com/hackernoon/deception-degenerate-a-b-testing-ecce6635000e)
[linkedin](https://www.linkedin.com/pulse/deception-degenerate-ab-testing-douglas-w-arcuri/)

#engagement #learning #testing #analytics #ethics #softwaredevelopment

### Posted

1. hackernews
1. r/programming
1. r/softwarengineering
1. r/ProductManagement
