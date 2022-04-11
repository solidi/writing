# On Kotlin: A Unit Test Conversion Guide
## Learnings Through Converting Thousands Of Java Unit Tests

Kotlin Island and the causeways that connect. We will take a drive through A-118 (Saint Petersburg Ring Road) during the reading. Courtesy: Google

This is not a typical explanation on applying Kotlin. It is also not a typically sized Medium post. It is to voice internal learnings through a story about how we are adopting Kotlin. It begins with unit tests.

If the information that follows helps just one engineer to better understand usage, it has served its purpose.
The first part will discuss the process behind our journey to Kotlin. Then, we will discuss the mechanical parts of unit test conversion. This will include what was observed, what was used and not used in the language. Finally, we will conclude with high level takeaways such as learnings, build speed and file size measurements.
This post assumes an understanding of unit testing. I would be happy to answer any questions in the comments below. Additionally, I am aware that some unit tests highlighted are not best practice. In the end, I hope it builds the curiosity of the uninitiated to discover this craft further.
Please bare with me. The post will contain an incomplete understanding of the Kotlin language and it may contain errors. This is because I am making an effort to learn Kotlin with our team.
I have to admit how quickly one can learn a language through unit testing.

Approaching Kotlin Island. Courtesy: Google

This conversion is just a starting point and there is much to learn. So before we dive in, let me set the stage on how we made the decision.

## Setting The Stage
Modularization As The Conversion Vehicle
As 2017 came to a close, our team began a migration to Kotlin. Our team had also started to move to a modular codebase to break up the heavy complexity of our monolithic app projects. These Android projects included many flavors from which tv and mobile applications were produced. We realized that modularization was the vehicle that we could utilize in our language migration.
Modularization of code has a lot of benefits even to Android. It includes the ability to obtain a consistent code style within each module. Consistency is an underrated property of many software engineering projects. In my opinion, code that is consistently wrong is always better than code that is inconsistently right! This is because a pivot later may be favorably trivial when code consistency is present. Optionality is possible when things have a predicted structural rhythm throughout.
We steered in this direction because consistency is critically linked to keep our organizational capacity high. Engineering expertise is usually constrained. Constraint is a property shared by many, perhaps all businesses. We decided to move forward with Kotlin in a consistent way without a drag on that organizational capacity. This is to mitigate risk of regressions and to help build the knowledge of the language. However, the cost to this strategy is the speed of adoption.
Our intention is to accelerate Kotlin conversion over time.

A-118 tunnel to Kotlin Island. Courtesy: Google

This started with our very large suite of many thousands of unit tests. The plan was simple at the high level. We would first migrate Android Java production code and JUnit tests from the app projects to their corresponding modules. From there, the unit tests would be converted to Kotlin. At the same time, we would develop an internal Kotlin style guide that would be amended and improved as unit tests were converted.

We would eventually follow up with production code of each module when the timing was correct. This includes the adoption of a shared team vision.

The first part of the process has already started and we have converted a decent percentage of unit tests. We have many more modules to go and have upwards of eight thousand unit tests. For those modules that have been converted or are uncovered, Kotlin will be the preferred language moving forward.

## The Book

In this profession it is important to invest a lot of time in learning. The key is to find the excitement and drive in the subject. I find a significant value in printed books to support learning and engage in the excitement.
Why books? Simple! Unlike Medium posts or the internet as an information source, a book is finite and completable. Completing things to obtain information and to increase a skill is underrated activity.

When completing a book, the initial goal of understanding the subject is achieved. The trick is to know what book(s) to invest in. Over time, you will find that investment takes on suggested parameters that must be fruitful and enjoyable to you.

My copy. The book is based on a foundation that will be stable for years to come.
As we discussed the Kotlin conversion process as a team, I bought the book Kotlin In Action (first edition). My interest peeked when I observed pull requests that adjusted an internal Kotlin style guide. I was skeptical, but after chewing through the first chapters in only a short matter of hours, I was impressed with its quality.

The Manning book is a well written program language guide and its size is very manageable. It is fitting that Kotlin, an island in Russia, would be covered initially by Manning. Manning is a virtual company based on Shelter Island, New York, a location that is close to me!

In this post, I plan to quote a few key areas of the book as I discuss the learnings to help reinforce the concepts. While the material covered is pragmatic, getting into the action is the only way to learn well. I’m very curious about those details.

## Starting The Kotlin Conversion

Our team had been watching the community since the announcement. Over the summer and into the fall, I read through many great unit test guides for Kotlin. They covered most of the fundamentals, explored new test SDK’s and they highlighted reductions in code. However, I’d had not found a post that discussed the details about what happens when a team converts a large standing set of unit tests and, at the same time, learn the language from a senior engineer point of view.

Physical rhythm of the port. Courtesy: Google

What follows are my observations and trials while assisting the team by converting thousands of unit tests to Kotlin. Let’s discuss these in detail next.

## Unit Test Observations

The following will include a bulleted approach to some of the mechanics as we performed the conversion of unit tests. There are many great posts and video demos highlighting some of these techniques. Others are original ideas decided by the team.
These sections are borne out of team discussions and decisions. Not all practices are standard and some are considered unorthodox. Additionally, I will highlight usage and concepts of Kotlin that were unfamiliar to me.

## Import Style

The default style of imports of Kotlin are compact and consistent. There is encouragement of star imports and lack of line separations between packages.

While we agreed to reduce the empty lines, we did not agree to the star import. We believe that star imports hide the dependencies of classes.

Additional, static import does not exist because static is not present in the language.

```
// Before
import com.fasterxml.jackson.databind.JsonNode;
import com.google.common.base.Optional;
import org.junit.Test;
// After
import com.fasterxml.jackson.databind.JsonNode
import com.google.common.base.Optional
import com.nhaarman.mockito_kotlin.*
import org.junit.Test
```

We may have to revisit star imports later as it has additional behavioral context.
Note that this star import will make visible not only classes defined in the package, but also top level functions and properties. — Kotlin In Action, p. 27
imports are an underwhelming highlight, but apart from unit tests, this is exactly how I quickly understand code and their interdependencies.

## Eliminate Keywords

As we all know, the public and final keyword qualifiers in Kotlin are absent as they are implicitly default. Sometimes these may need to be explicit, such as dealing with types. The Manning book points out these keyword usages well.
Whereas Java’s classes and methods are open by default, Kotlin’s are final by default. — Kotlin In Action, p. 71
We decided to keep the default declaration of all properties and funs in test as public (implicit default). This helps reduce the noise of the tests. We avoid the use of private, internal and open where possible. The only exceptions are when scope change is required to avoid leaking the implementation (more on this later), or the use of const val on the top level to avoid difficult rename refactors and polluting autocomplete.
Just like the authors of the Kotlin language designed, the fewer keywords in a unit test, the higher the readability.

## Properties

One of the initial observations during our conversion of tests is the interesting ability to reduce our @Before methods with the use of properties. Properties appear to initialize without the worry of illegal forward references.

```
// Before
@InjectMocks
private PropertyItemsParser testSubject;
@Mock
private ContentParser contentParser;
@Mock
private PropertyThemeParser propertyThemeParser;
@Mock
private ApiConfig apiConfig;
@Before
public void setUp() throws Exception {
    MockitoAnnotations.initMocks(this);
    when(apiConfig.isInitialized()).thenReturn(true);
}
// After
val contentParser = mock<ContentParser>()
val propertyThemeParser = mock<PropertyThemeParser>()
val apiConfig = mock<ApiConfig>() {
    on { isInitialized } doReturn true
}
val testSubject = PropertyItemsParser(contentParser, propertyThemeParser, apiConfig)
```

Our team agreed on the approach above because it avoided the use of lateinit var and Mockito Annotations. Additionally, it eliminates the use of !!. This makes test setup immutable, readable, and allows for less lines of code.

Declaration intentions are clearer as there is less annotation magic. We decided to get rid of annotations like @InjectMocks, @Mocks, and other boiler plate code that assist the setup of our test subjects.

As an additional observation, the order in which these properties and init block are declared is important. A declared mock used for behavior modification of another mock (like returning it from doReturn), but is instantiated later in the file, may lead to runtime exceptions.

## Property Getter Block

Property get() and set() are welcomed additions.

Exit to the Port Moby Dik. Courtesy: Google

A lot of standard Java boilerplate, such as getters, setters, and the logic for assigning construction parameters to fields, is implicit to Kotlin and doesn’t clutter your source code. — Kotlin In Action, p. 11

We sometimes use explicit get() and set() on our properties for our tests. However, there are times we may need to perform an initial operation on the testSubject or others. It is possible to have get() as a function block which was described in Kotlin In Action as the “backing property technique”.

Here you use the backing property technique. … You need to use two properties … — Kotlin In Action, p 191.

```
// Before
@InjectMocks
private SelectionConverter testSubject;
@Before
public void setUp() throws Exception {
    MockitoAnnotations.initMocks(this);
    Whitebox.setInternalState(testSubject, "mapper", mapper);
}
// After
val testSubject: SelectionConverter
    get() {
        val converter = SelectionConverter(contentParser)
        Whitebox.setInternalState(converter, "mapper", mapper)
        return converter
    }
```

Here, I am not using a backing field to avoid a declaration of another property. As long as testSubject is not called more than once in a test, this should do no harm. Each test should run in an isolated state. This, coupled with data class, reduced @Before blocks even further.
Let us review annotations next.
Use-Site and Declare-Site Annotations
Parts of the book mentioned the concept of use-site and declared-site. In simple terms, a construct is used at the site of code in which it wants to modify, or declared at the site of the declaration (like a class) to be reused many times.
This comes into play when we want to annotate a property but with a particular context that is not present in code. Frankly, this is neither use or declaration! It’s more like implicit-site.
While the use of annotations on our legacy unit tests related mostly to mocking, use-site declarations were involved with the occasional need for @Rule. The rule needs to be public. It needs to be applied on get() of the property.

```
// Before
@Rule
public TemporaryFolder temporaryFolder = new TemporaryFolder();
// After
@get:Rule
val temporaryFolder = TemporaryFolder()
```

This very topic was covered in chapter 10 and defines more uses apart from get:. Stack Overflow has a good one on the subject here.
@Before Or Init
There is an open question on the use of init block or the @Before block within unit tests. For those tests that do need initial setup, we are sticking to @Before but there seems to be no difference, superficially, on the usage. Both are called before each test.

```
// This
init {
    setInternalState(testSubject, "objectMapper", objectMapper)
}
// Or This
@Before fun setUp() {
    setInternalState(testSubject, "objectMapper", objectMapper)
}
```

Some would suggest to use @Before in context of testing since it highlights the possible need for @After if required.

```
// Don't Do This
init {
    PowerMockito.mockStatic(ObjectMapper::class.java)
}
```

Although our team is migrating away from PowerMock, the use of it within the init block will compile but will not work correctly.
Parametric Polymorphism
Some of our classes under test use parametric polymorphism. Conversion of these classes under test caused some additional type declarations. This was actually a bummer, but the safety is the benefit. It also has to do with the absence of the raw type.
Unlike Java, Kotlin always requires type arguments to be either specified explicitly or inferred by the compiler. … Because Kotlin has had generics from the beginning, it doesn’t support raw types, and the type arguments must always be defined. — Kotlin In Action, p. 224

```
// Before
@Mock
private ApiAsyncTask task;
// After
val taskString = mock<ApiAsyncTask<ApiConfig, String>>()
val taskSetting = mock<ApiAsyncTask<ApiConfig, Setting>>()
```

We had numerous unit tests requiring different generic types. We were coerced to declare new properties separately.

An exit to Kronstadt. Courtesy: Google

Since Kotlin 1.1, typealias makes working with drawn out types a little easier and less verbose. The above can become:

```
typealias TestTask<T> = ApiAsyncTask<ApiConfig, T>
val taskString = mock<TestTask<String>>()
val taskSettings = mock<TestTask<Setting>>()
```

## Heredoc And Companions

Also known as multi-lined triple quotes, in combination with string templating, it gives a powerful way to feed unit tests which we had a few of.

```
// Before
private static final String VALID_SAMPLE_RESPONSE = "{"""
 + "\"response1\" : “ + "\"" + RESPONSE_1 + "\"" + ", "
 + "\"response2\": “ + RESPONSE_2
 + "}";
// After
private const val VALID_SAMPLE_RESPONSE = """
{
    "response1": "${RESPONSE_1}",
    "response2": "${RESPONSE_2}"
}
"""
```

Multiline strings give you a perfect solution for including the expected output as part of your test. — Kotlin In Action, p. 63
I’m still scratching my head as to why it was not labeled heredoc.
The team also decided to the avoid the use of companion objects in unit tests to cut down on unnecessary object creation. Instead, top level const vals were used where possible.

```
// Not This

class ClientUrlTest {
    ...
    companion object {
        const val INVALID_URL = "invalid"
    }
}
// This
private const val INVALID_URL = "invalid"

class ClientUrlTest { ... }
```

Additionally, the standard style and position of companion objects are expected at the bottom of the class that contains it, which may reduce the readability of tests.

## Throw Out Throws

A lot of our tests in Java had throws appended on the end of the test methods. After conversion, we realized that Kotlin did not differ between checked and unchecked exceptions.@Throws(Exception::class) appeared meaningless on tests. We threw all of them out.
… Kotlin doesn’t differentiate between checked and unchecked expressions. — Kotlin In Action, p. 41
We then realized later that it didn’t make sense to have throws even in Java. I call this the conversion benefits effect. These benefits give additional credence to adopting a new language that every engineer should understand and desire.
These effects will be highlighted in detail later.

## Reduced Matchers

As you may have noticed, use of mocks is abundant in our tests. We typically lean on any for those parameters we do not care for. For example, we use matchers from Mockito such as anyString(), anyInt() and any(Class.class).
With the conversion of the tests to Kotlin, we were able to reduce and lean on inference. This is thanks to Kotlin-Mockito and their heavy use of reified types.

```
// Before
when(task.addCallback(any(Task.Callback.class))).thenReturn(task);
// After
whenever(task.addCallback(any())).thenReturn(task)
```

## Remove Null Tests

We admit that we had null pointer unit tests throughout our codebase. With the conversion to Kotlin, testing these became impossible with our use of the @NonNull annotations in Java.

Bridging supports. Courtesy: Google

Therefore, we had to let go of some tests and become more exposed until we adopt Kotlin production code. For example:

```
@Test(expected = NullPointerException::class)
fun `Given a null locale, when I get language and region, then I expect an exception`() {
    // GIVEN
    val languageDevice: Locale? = null
    // WHEN
    LocaleCodeUtils.getLanguageAndRegionFromLocale(languageDevice!!)
}
```

The above unit test is not testing the true intention. You cannot force a null type into getLanguageAndRegionFromLocale since its locale is marked with @NonNull. However due to the assertion !!, it allows it!

## Escaping Identifiers

We noted numerous escaped method names like `when` and `is` . We did everything we could to remove these and replace Mockito and Hamcrest to Mockito-Kotlin (mentioned previously) and Kluent, a tidy way to propose assertions on values using infix.

```
// Before
// GIVEN
`when`(objectMapper.readTree(body.`in`())).thenReturn(rootNode)
// After
// GIVEN
whenever(objectMapper.readTree(body.`in`())).thenReturn(rootNode)
```

Some of tests still contain these back ticks. Retrofit contains methods like `body.in`() from import retrofit.mime.TypedInput.

## ShouldEqual

Speaking of Kluent, we converted most of our assert and assertThat lines to use this SDK.
The team suggested to favor shouldEqual for most comparisons. For any single lined comparisons of empty or true/false, we thought it was more readable with the method invocation.
```
// Before
assertThat(descriptionResult, is(“description”));
assertThat(miscResult, isEmptyString());
// After
descriptionResult shouldEqual “description”
miscResult.shouldBeEmpty()
```

## Assertion Blocks

While we chat about assertions, there were tests that included blocks of assertThat statements. We converted them using the apply extension method from the standard library.

Additionally, for inOrder statements, we converted to the proper extension function as provided by Mockito-Kotlin.

```
// Before
assertThat(property.urlKey(), is(urlKey));
assertThat(property.title(), is(title));
assertThat(property.icons(), is(propertyIcons));
InOrder inOrder = inOrder(singletonTask);
inOrder.verify(singletonTask).removeCallback(taggedCallback);
        inOrder.verify(singletonTask).addCallback(callback);
// After
property.apply {
    urlKey() shouldEqual urlKey
    title() shouldEqual title
    icons() shouldEqual propertyIcons
}
inOrder(singletonTask) {
    verify(singletonTask).removeCallback(taggedCallback)
    verify(singletonTask).addCallback(callback)
}
```

Pleasant views on the crossing. Courtesy: Google

Our team is debating whether with or apply is better. I’m in the former camp.
[On with and apply] If you don’t care about the result, these functions are interchangeable. — Kotlin In Action, p. 292

## Illegal Identifiers in Backticks

One of the biggest wins for Kotlin unit testing is that we could write complete sentences to describe tests out of the box.
However, as we converted our tests we noted IDE problems understanding infix notation with certain characters. We decided to suppress the issue with the use of @Suppress("IllegalIdentifier") at each test class declaration.

As you can see, most of our unit tests follow the pattern of the Given-When-Then approach. However, we still use comments to declare the sections.

We will briefly mention Spek later.

## Immutable and Mutable Split

During the conversion of some tests, the compiler complained about the use of Map<> where methods of put() where used.
As explained in the Kotlin In Action book, the Kotlin team decided to split up these collections into immutable and mutable collections.
… every Java collection interface has two representations in Kotlin: a read-only one and a mutable one … — Kotlin In Action, p. 163
My understanding is the decision was made to assist inference of what’s happening in code.

```
// Before
val taskMap = mock<Map<ApiTag, Task>>()
// After
val taskMap = mock<MutableMap<ApiTag, Task>()
whateverOrNull()
```

On the same topic of duality, another pattern that is prevalent in the standard library, and mocking frameworks like Mockito-Kotlin, is the concept of OrNull().
Since Kotlin deals with types that contain and do not contain null values, emphasis of locating null may be necessary.
[On handling null] The functions isEmptyOrNull and isBlankOrNull can be called with the receiver type String?. — Kotlin In Action, p. 147
In tests that involve Java, there is observance of platform types. Platform types are easy to spot in code completion, they yell loudly such as String! or Object!.
Since there is type inter-op that is required, scenarios of mocks of anyOrNull() began to appear.

```
// Before
{   
    // GIVEN
    when(asyncTaskFactory.create(
         any(DoInBackgroundTaskInternal.class),
         nullable(ApiAsyncTask.Callback.class))
         .thenReturn(newAsyncTask);
}
// After
{
    // GIVEN
    whenever(asyncTaskFactory.create<ApiConfig>(
             anyOrNull(),
             anyOrNull()))
             .thenReturn(newAsyncTask)
}
```

The use of any() above would compile but would miss the mocked intention. This caused failed tests and conversion headaches.
Mocking Final Classes
During our conversion we hit aproblem where all classes in Kotlin are implicitly final.
Here, some of our tests included the declaration of stubs (typically abstract classes). The Convert Java File to Kotlin File tool did not mark these classes as open. The simple solution was to mark them as such.

```
// Before
class TestTaskManager() : TaskManager
...
org.mockito.exceptions.base.MockitoException: 
Cannot mock/spy class com.example.rest.tasks.async.TaskManager$TestTaskManager
Mockito cannot mock/spy because :
 — final or anonymous class
// After
open class TestTaskManager() : TaskManager
```

After some brief research on the subject, this issue was discussed in the community and a new plugin is now available.
It is widely known that when dealing with the code conversion tool, it does not always result in compilable code.

## Parameterized Tests

Although we have only a handful of parameterized unit tests in our suites, discussion happened regarding its conversion and approach.
The two rallying opinions appear to be either Kotlin/JUnit based, or a slightly cleaner version using JUnitParameters.

```
// Kotlin/JUnit
@RunWith(Parameterized::class)
class SentenceCaseTest(val input: String, val expected: String) {
    companion object {
        @JvmStatic 
        @Parameterized.Parameters
        fun data(): Collection<Array<Any>> {
            return listOf(arrayOf("word", "Word"),            
                          arrayOf("Yes", "yes"))
        }
    }
    @Test fun test() {
        input.toSentenceCase() shouldEqual expected    
    }
}
// JUnitParamsRunner
@RunWith(JUnitParamsRunner::class)
class SentenceCaseTest {
    @Test 
    @Parameters
    fun test(input: String, expected: String) {
        input.toSentenceCase() shouldEqual expected
    }
    fun parametersForTest() = arrayOf(arrayOf("word", "Word"),            
                              arrayOf("Yes", "yes"))
}
```

An original Kotlin thread started the topic of conversion within our team, here.

## Problems In Understanding

To wrap up the conversion process, we will cover items that seemed difficult at first.

A side side stop. Courtesy: Google

Indecent Exposure

In the last section we spoke of test stubs. Many were embedded in their test classes. Numerous properties we defined had problems with I call scope leakage.

The simple solution was to down-scope using either internal or private, or the reverse by increasing the scope of the test stub to public. There appeared to be no preferred answer since we are dealing with isolated unit tests.
I make mention of this small observation because it took me a while to understand what was happening and why. This post helped.
Returning Itself
In Mockito-Kotlin, it was not clear how to return a mock of itself. The simple resolution was to use it.

```
// Before
@Mock
private RestAdapter.Builder restAdapterBuilder;
@Before
public void setup() {
    when(restAdapterBuilder.setEndpoint(anyString()))
    .thenReturn(restAdapterBuilder);
    when(restAdapterBuilder.setClient(any(OkClient.class)))
    .thenReturn(restAdapterBuilder);
}
// After
val restAdapterBuilder = mock<RestAdapter.Builder>() {
    on { setEndpoint(any<String>()) } doReturn it
    on { setClient(any<OkClient>()) } doReturn it
}
```

This approach reduced lines and unnecessary backing properties. To see more on this subject, check out this link.
doAnswer
I’d admit that we use doAnswers in our testing. The question was the direct conversion of code.

```
// Before
doAnswer(new Answer() {
    public Object answer(InvocationOnMock invocation) {
        Object[] args = invocation.getArguments();
        ((ResponseMetaData.Builder) args[1]).status("status");
        return null;
    }
}).when(
    responseMetadataParser)
    .parseMetadataStatus(any(JsonNode.class), 
    any(ResponseMetaData.Builder.class));
// After
doAnswer({
        val args = it.arguments
        (args[1] as ResponseMetaData.Builder).status("status")
        null
}).whenever(
    responseMetadataParser)
    .parseMetadataStatus(any(), any())
```

Note the differences. This includes the removal ofnew Answer(), the lambda receiver with null with no return, and the it parameter.
More information about this conversion can be found here.

## Star Projection
Just like Java wildcards, star projection (it’s analogue in Kotlin) is not well understood by me. However, the difference with Kotlin’s revamped type system is that they are more prevalent in client code.
My observation include its particular use in unit tests like the case below.

```
class TestTaskManager() {
    override fun onCreateSingletonTask(): ApiTask<*> {
        return mock<ApiTask<*>>()
    }
}
```

The star projection and the type it holds is simply passed through without a care of what it is. Based on the book, this is generally how it is described.

You can use star-projection syntax when the information about type arguments isn’t important: you don’t use any methods that refer to the type parameter in the signature, or you only read the data and you don’t care about its specific type. — Kotlin In Action, p. 249
On mocks dealing with types, although the code converter tool substituted the type for the star projection, the compiler complained about needing specific types. Where possible we subsisted with Any, but many of these had to be converted to particular type.
“Oh… You Don’t Need This”
Our pull request process had caught unconventional Kotlin style smells, including annoyances such as unneeded explicit type parameters. These nits became somewhat repetitive.
After some searching, the solution was to include klint and to turn up the live code inspections in Android Studio 3.0 from default to their highest levels.

All Kotlin live code inspections on, with the exception of KDoc.
This revealed some other small issues related to cleaner code quality. It turned out to be more useful than originally thought and helped direct us on how to write Kotlin idiomatic code just a little bit better.
I suggest those that are learning to turn these up very high to quickly learn.
This wraps up the code observations of the conversion process. Next, I want to mention what language constructs were particularly absent during the conversion.
Unused Constructs
During the conversion of the unit tests, I noted items in the Kotlin language that were largely unused.
Exploiting functions as top level or multiple test classes for different organization for tests.
Extension (except for with / apply) and functional extensions such as map, filter, flatMap.
Destructuring and function types.
Minor use of object singletons for test stubs but avoided the use of companion objects.
Conventions except the use of access with the index operator [n] .
Delegation, inlining, variance.
Very little Java inter-op, but some usage of @JvmStatic.
I want to point out that our tests did not call for these interesting constructions. Perhaps with some thought, these could be harnessed to do unit tests better as long as it is readable and understandable to all.
One of those features are extension functions. I think many can leverage extension functions to make unit tests slightly more readable by replacing static calls.
For example, if we had this extension function defined to wrap the Whitebox static call:
fun <T : Any> T.setInternalState(fieldName: String, value: Any) = Whitebox.setInternalState(this, fieldName, value)
We could re-write:
Whitebox.setInternalState(testSubject, "isNew", false)
to simply:
testSubject.setInternalState("isNew", false)
This approach is similar to how we avoid using unnecessary keyword modifiers in our tests. Ultimately, we are focused on further reducing the noise in the unit tests.
You can now see that extension functions are a powerful way to extend the APIs of existing libraries and to adapt them to the idioms of your new language… — Kotlin In Action, p. 63
We also avoided use of larger frameworks that harness DSL’s. We decided against the use of the following:
Spek
KotlinTest
JUnit 5
This may change over time. The main argument was consistency and keeping the unit test conversion complexity down.
With all of the conversion discussion, what are the takeaways? Let’s discuss these next.
Takeaways

A nicely constructed pedestrian crossing. Courtesy: Google
Here are some key takeaways — the thought provoking stuff — through which conversion of tests provided.
Fundamentals: Inference
Converting our unit tests felt like a game of golf where code reduction happened on almost every function, line, and at every type declaration without introducing readability issues.
Thanks to Kotlin’s support for type inference, most of the extra verbosity associated with static typing disappears, because you don’t need to declare types explicitly. — Kotlin In Action, p. 6
This was all thanks to inference. The Kotlin languages authors put a lot of work into it.
The simple rule you can follow is to always start without the types; if the compiler complains, specify them. — Kotlin In Action, p. 108
With inference comes expression bodies.
Fundamentals: Expression Bodies
Indeed, there are parts of the Kotlin In Action book that suggest not all one liners are readable.
[Relating to expression bodies] Having the return type … written explicit helps you quickly grasp what can be returned. — Kotlin In Action, p. 20
However, the power of the expression can go a long way if it is readable. For example, check this idiomatic before and after from a conversion on a recent unit test.

```
// Before
val sampleSubTypes: List<String>
    get() {
        val excludeIds = ArrayList<String>()
        excludeIds.add(SAMPLE_SUBTYPE)
        return excludeIds
    }
// After
val sampleSubTypes = listOf(SAMPLE_SUBTYPE)
```

The difference between a statement and an expression is that an expression has a value, which can be used as part of another expression… — Kotlin In Action, p. 19
Side Effect: Conversion Benefits
As discussed in the section on Throws, converting unit tests to Kotlin also gave the team opportunities to improve and clean up the campsite further. They included:
Correctness: Fixed tests that were not exercising the intended target.
Build Speed: Removed Robolectric and PowerMock where they were not needed.
Cruft Clean Up: Cleaned up test step, annotations and throws that were unnecessary or unneeded.
Readability: Further enhanced test style such as increased readability of tests in either // Given or // Then sections by use of method extraction.
Readability Again: Restating the tests in sentences revealed missing assumptions in their names.
While overlooked, this is no small improvement indirectly caused by the conversion to Kotlin. This benefit is achieved only if a codebase is being converted.
Suggestion: Testing Style
As described, there are many great posts on unit testing with Kotlin. A few years worth. So I researched explicitly about test style.
We listened to Jake Wharton’s special appearance on the Fragmented podcast ep 105. The Kotlin community is working hard to standardize a style guide and as I write this, JetBrains just released their own. However, the community guideline was revealed a few months ago for Android — basically Jake’s doc.
Interestingly, there was a part of the podcast where Jake mention the @Test annotation. He suggested that it should be on the same line as the method infix, unless there are accompanied annotation parameters.
Kotlin In Action suggests the same style on p 255.

```
import org.junit.*
class MyTest {
    @Test fun testTrue() {
         Assert.assertTrue(true)
    }
}
However, just two pages later on p. 257
class HasTempFolder {
    @get:Rule
    val folder = TemporaryFolder()
    @Test
    fun testUsingTempFolder() {
        ...
    }
}
```

While this is a style we quickly adopted, potentially saving fifty to one hundred lines for well tested classes, a standard is absent in the community style guide.
This continues to be a problem for all of us.
I think there should be one. We would love to see a testing style guide section within the community Kotlin style guide.
Biggest Learning: Internal DSL Support
While our team did not chose to use a testing framework, the conversion of unit tests had revealed that Kotlin has superior support for DSL conversion.
Kotlin has the power to achieve internal domain specification languages. Here is the DSL formulation as I understand it:
[On Kotlin] A general language with lambda receivers and invoke convention means the ability to support internal DSL’s. Internal DSL’s give the ability for higher level readability and understandability through the use of structured grammar, but the additional benefit — that declared languages cannot provide easily — is type safely through compilation.
This is the most exciting aspect of Kotlin with respect to unit testing. It is also covered with examples in chapter 11 of Kotlin In Action.
The community is active with tackling this subject. RxTest is just the latest example of how internal DSL support can build specific domain grammar to test.

```
// Example of RxTest
Observable.just("Hello RxTest!")
    .test {
        it shouldEmit "Hello RxTest!"
        it should complete()
        it shouldHave noErrors()
    }
```

For those multi-year old testing frameworks in Java, they too could invest time to make a domain language. RESTMock could be a great candidate for this exploration.
Other Learnings
Converting to Kotlin had many benefits such as learning new skills and increasing developer happiness, but these indicators were difficult to measure.
We paid attention to basic key performance indicators on how fast the unit tests ran in comparison to the original Java tests and how many lines we would save.
Since we aren’t finished with the conversion, it will be some time until we understand the impact. However, I do have two measurements to share based on one module we recently converted.
Setup
We have basic tooling to help us measure these indicators. Leaning on ./gradlew clean test --profile by starting a daemon and running the job numerous times. Then, we started recording the runs and finally averaging the total build time.
Testing was profiled with AGP 3.0.0, Gradle 4.1 and Kotlin 1.1.61.
Build and Test Speed
In an ideal world we would love Kotlin to run as fast as Java compilation. However, during some initial pull requests we had a trending comparison that favored the unit test run time of Java over Kotlin.
The trend continues. With our latest module converted, unit test total build speed increased about 25%. This is based on a clean state on our continuous integration system.

26.47% total build time, which includes unit test run time, increased with Kotlin in this module.
For example, the module in question has approximately 475 unit tests. The original run time of the tests from a cleaned state is approximately 25 seconds. When we converted the tests to become idiomatic Kotlin, the run time was approximately 32 seconds.

Actual unit test run time is flat, slightly favoring Kotlin by 0.15%.
It appears that Kotlin compilation added to the total build times. Since the module also includes auto-parcel, we had to add kapt. The addition of kapt annotation processing compounded the profile time.

Kapt added an average of 10% to the total build time.
There are options to remove the use of kapt. Migrating away from annotations as a whole is an opinion, albeit a painful one. In the case of auto-parcel, @Parcelize is available.

Kotlin compilation time is generally higher by three times.
If we have a test suite that contains approximately eight thousand tests, does this scale linearly? Certainly unlikely as modularization invites parallelization. Even so, this could be a potential problem. Are there ways to reduce or improve the speed?

Kotlin clean times were also consistently higher by 24%; although the time dealt with in this module is minuscule.
It is logical to me that the speed is slower because Kotlin is generally atop of Java. The key will be reduce that friction at every point.
Speed is an open question, with a lot of confusion and hopes around build caching. However that too has problems with build determinism.
This topic hasn’t stopped us and we remain hopeful that tooling will improve. My bet is it will.

## Lines Saved

While the unit test build time was not encouraging, the lines saved certainly was. The lines saved in this particular module was not insignificant. We had a reduction from 6,500 test code lines to approximately 5,500 lines, a reduction of 14.5%.

This is excellent and we very much welcome it since we all believe that fewer lines means less mistakes. It also underscores the succinctness that Kotlin provides, and the efficiency of doing much more with less.

## Conclusion

Let’s turn around, there has to be more to see! :) Courtesy, Google.
I really do appreciate this language and are eager to learn more. I look forward to better approaches as Kotlin may provide because the potential is very high. The tools, especially the IDE, are laid out to do it all better.
Our teams will continue to learn and convert.
Also, a shout out to Dmitry Jemerov and Svetlana Isakova on the authors of the book, Kotlin In Action. It was a pleasure.

---

## Social Post

[medium](https://proandroiddev.com/on-kotlin-a-unit-test-conversion-guide-71e0597bb45d)
