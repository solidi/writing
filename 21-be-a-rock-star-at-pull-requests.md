# Be a Rock Star at Pull Requests
## Tips for a successful collaborative code review
#beginners, #tutorial, #firstyearincode, #codequality

![Photo: Clément Hélardot/Unsplash](images/21-01.jpeg)

I've reviewed thousands of pull requests over my career. Here are my tips for building an inclusive learning environment while delivering value.

## For the Author and Reviewer

**Keep it small and iterative.** By focusing on the intent, it gives the ability for the reviewer to provide a timely, high bandwidth review. It's hard, but the author should resist batching work.

**Signal intentions with labels.** Whether it's with prefixes in the subject line or if the tool supports tagging, use these liberally to signal when work is in progress, the size of the review, or is associated with a milestone.

**Provide a clear context.** Define the problem and solution of the pull request [in the description](https://medium.com/hackernoon/no-description-provided-8d9e0f3a3abb). It will provide exceptional value to the review, and includes historical information for onboarding others.

**Review your commits and provide comments in the review.** Reduce the ambiguity by self reviewing your own newly minted pull request immediately. Provide proactive summary content to lines that need clarification so that the reviewer has a clear context.

**Be open to feedback, always.** The reviewer likely has good intentions. Take the feedback well by asking questions and making suggestive edits now, or deferring them in an agreed manner. Respectful reviews are [useful ones](https://testing.googleblog.com/2019/11/code-health-respectful-reviews-useful.html).

**Capture conversations in the tool.** Many times discussions had occurred around the pull request. However, that knowledge is missing for others. Follow up, and write the outcomes in the tool. This action will immensely add context to others.

**End with approval and summary comment to signal completion.** At the end of the review, add a summation paragraph. The feedback will give a recap, encouragement of the great work, and build trust between reviewer and author.

**An empathetic review is additive attribution.** Show that you care deeply for both the code and the author. Take your suggestive edits and file them on top of the pull request. The continued courtesy builds collaborative teams.

## For the Team

**Prefer pairing over pull requests.** Prefer pairing over pull requests. Pairing provides the same value as a pull request review with the benefit of real-time results. Work toward a system that, if significant pairing has occurred, the team should provide a way for those individuals to merge with advanced brevity.

**Make it easy for those to receive a timely review.** Make the ritual of code review easy for newcomers to get a timely review. Some teams I've seen have set precise time ranges for review, others have set SLA's. Either way, be inclusive and welcoming. The reviewer pulls. The author shouldn't need to push.

**Always look to improve the tooling to avoid nits.** High bandwidth pull requests lean on the direction of the codebase, not the format. Keep investing in tooling so that the human review shines. Every small comment (a nit), is an opportunity to automate away.

**Embrace TODO's.** The biggest gem of pull requests is potential improvement opportunities. Capture them, embrace them, *LOVE them*. And above all, keep track of them, and get them done at the next iteration.

**Iterate on a descriptive template.** Some teams have contributing philosophies to pull requests. I've seen groups work on clear checklists so that the pull request is comprehensively complete. Find an instrument that moves towards completeness.

**Make it easy to run the work locally.** Avoid surprises in failed builds. Emulate everything that happens in the pull request locally. Whether it's pre-commits, static analysis, or tests, move to make it dead simple for anyone to run the build in [one command](https://www.joelonsoftware.com/2000/08/09/the-joel-test-12-steps-to-better-code/).

**Encourage ratcheting over gatekeeping.** Keep the mindset that measures the health of the codebase and that abstractions are understandable. Do not expect perfection; expect learning and improvement on every review. Remember, there are [engineers](https://dev.to/solidi/what-is-a-software-engineer-anyway-3fb2) at all levels on the team. Are you growing them without frustration?

**Pull requests are about cross-pollination learning.** Respect other's efforts in their pull request. Context and opinion rules software engineering. Make these philosophies apparent to the author. Clear expectations make great partners. Starters could be a contribution guideline. Bug catching and code consistency are side effects of the review.

## Finally

**Keep it fun.** I once observed a team where they challenged themselves by writing highly clever haikus and prose in each summary. Doing this hundred (ah, thousands) of times developed a team of Hemingway's. Try adding to the playful habit. Engineering is all about curiosity and learning from play.

---

## Social Post

[dev.to](https://dev.to/solidi/be-a-rockstar-at-pull-requests-1e4f)
[medium](https://levelup.gitconnected.com/be-a-rock-star-at-pull-requests-d855308ce3d2)
[LinkedIn](https://www.linkedin.com/pulse/rock-star-pull-requests-douglas-w-arcuri/)
