# Software Context — Spoke

Voice guide for software, engineering, career, tools, and video-game-as-systems essays. Covers the register seen across essays 01–104 and any later piece in that key. Read [ai/writing-context.md](writing-context.md) first.

Most essays in this spoke also live in the author's collected book, _Deconstructive Software Ramblings: Essays from the Mind of an Engineering Manager_ (Dependent Studios LLC, December 2024; reprint November 2025). The book is the canonical edited form. When in doubt about an editorial choice (profanity asterisking, bracketed asides, citation handling, section grouping), defer to the book's conventions, captured below.

## When to load this file

- Role definition ("What is a [X] Anyway?").
- How-to pieces on practice, demos, PRs, remote work, onboarding, interviewing, shipping.
- Tool, language, or platform takes (Kotlin, IntelliJ, Git, versioning, etc.).
- Reflective career memoir.
- Listicles or observation catalogs from practice.
- Satirical or opinion pieces on developer culture.
- Video-game essays used as vehicles for systems thinking (e.g., 45, 46, 57, 67).

## Voice

- Reflective practitioner. Intellectually serious, conversationally casual.
- Peer at the coffee shop, not the podium.
- Opinionated, with receipts. Earns conclusions through observed evidence.
- Nostalgic when the nostalgia illuminates today. Never nostalgic as escape.
- Framework-builder. Names things so others can reuse them (Springboard, SECTAs, Decision Hypothesis, LatestVer, the Stew).

## Tone markers

- Funny in flashes, not as a running bit. One-word deadpan paragraphs earn their place ("Sh\*t.", "Yikes.", "Sigh.").
- Playful formality. Mock-academic phrasing deflated by a plain observation.
- Self-deprecation is a seasoning, not the meal.
- Satire targets industry tropes, not individuals.
- Factual density picks up when the subject is data or tooling; drops when the subject is the reader's day.

## Book taxonomy (Deconstructive Software Ramblings)

The book groups 64 essays into ten sections plus an epilogue. Each section opens with a single-word epigraph in dictionary form: `word (/pəˈnun.sɪ.ˈeɪ.ʃən/) part-of-speech. definition.` Use the section a piece would belong to as a routing signal: it tells you which canonical structure (A–F below) the essay is closest to and what its peers are.

| Section | Epigraph | Structure(s) | Examples |
|---|---|---|---|
| I. Gripes on Software Experiences | gripe (n.) | F (satire/rant) | 42, 52, 54, 60, 65, 73, 74 |
| II. Software Listicles | listicle (n.) | D (listicle) | 20, 21, 23, 36, 51, 53, 63, 64, 67 |
| III. Practices and Insight in Software | practice (n.) / insight (n.) | E (deep dive) | 02, 04, 05, 07, 08, 15, 41 |
| IV. Reading and Writing | read (v.) / write (v.) | C (memoir) + E | 19, 31, 38, 48, 68 |
| V. What is a … Anyway? | — | A (definitional) | 18, 22, 27, 29, 30, 33, 35, 40, 103 |
| VI. Interviewing | interview (n.) | B (imperative) | 09, 28, 39, 61 |
| VII. Being a Software Engineer | engineer (n.) | C + B | 11, 25, 55 |
| VIII. Being an Engineer Manager | manager (n.) | C + E | 01, 14, 24, 43, 44 |
| IX. Crossovers | crossover (n.) | C + E across domains | 10, 12, 17, 49, 50, 56, 57, 62, 66 |
| X. Reflections | reflection (n.) | C | 13, 16, 26, 71 |
| ∞. Epilogue | — | C | 47, 59 |

When drafting a new essay, name the section it would join. If it does not fit one, ask whether it is really a software essay at all.

## Canonical structures

### A. Definitional — "What is a [Role] Anyway?"
Short problem statement or opener. Then a series of bolded declarative sentences, each starting with "They", "It", or "The [role]", unpacking one facet per paragraph. Close with a tidy summary or social-post-ready list.
Examples: 18 tech lead, 22 engineering manager, 27 software engineer, 29 principal, 30 PM, 33 project manager, 35 staff, 40 SDET.

### B. Imperative — "How to [Verb] Your [Object]"
Anecdote or scene to open. Numbered list of practical moves, each with a short rationale. Close on encouragement or a meta-observation.
Examples: 20 demo, 21 PRs, 23 remote, 25 new role, 39 interview, 44 onboard, 48 HN, 53 vacation, 61 code workout.

### C. Personal reflection / memoir
Scene or moment of realization. Personal story → professional parallel → extracted principle. Close on resolution, a lingering question, or an accepted tension.
Examples: 10 hobbies, 31 reading, 43 engineer exits, 47 ship, 59 remote pandemic, 62 listening alone, 65 clean code.

### D. Listicle / observation catalog
Hook ("I noticed a pattern"). 5–20 labeled items, each short. Synthesis or meta-question at the end.
Examples: 52 apps doing sh\*t, 64 not-so-small things, 67 video game concepts, 68 technically writing.

### E. Technical deep dive / tool review
Problem or tool in the first paragraph. Pros, cons, design analysis, historical context. Close on implications.
Examples: 02 IntelliJ SECTAs, 04 Springboard, 07 Decision Hypothesis, 38 .plan, 60 LatestVer.

### F. Satire / rant
Direct statement of annoyance. Specific grievances, sardonic observation. Close with a call-out or plea.
Examples: 42 reply all, 54 cancel update, 65 clean code goodbye.

## Signature stylistic devices (book-grade)

These appear consistently in the published book. Use them in new essays unless the piece is specifically a short web-only post.

- **Small-caps + bold opener.** First two to four words of the body in small caps and bold, completing the sentence in regular type. "**TYCO TOYS, INC. OPERATED** out of Mount Laurel, New Jersey." Used in roughly 40% of essays; near-universal in book versions. Toy and software both inherit it.
- **Bullet-arrow lists** (➜). Replace plain bullets when items deserve a visual anchor. Lead with a bolded noun phrase, then a sentence. "➜ **Equipment.** Buy the chair." Used heavily in listicles and inside long essays where a sub-list would otherwise drown in prose.
- **Triple-bullet section break** (● ● ●). Centers a thematic pivot inside an essay where a header would be too heavy. One per essay max.
- **Bracketed editorial wink** with a footnote dagger: `[which is to ship]†`, `[welcome back to five days a week in office, sorry]†`. Treat as a stage whisper to the reader. The dagger marks the aside as the author's, not the source's.
- **Italicized one-line rhetorical kick.** "_Is it?_" "_Feeling good beats feeling fast._" One per essay; lands a turn or a doubt.
- **Section epigraph in dictionary form.** When a draft groups essays into a sub-section, open with the epigraph: `gripe (/ɡrīp/) v. complain about something in a persistent, irritating way.`
- **"DSR" footer glyph.** Reserved for book context, not blog drafts.
- **Profanity discipline.** Always asterisked: `sh*t`, `batsh*t`, `dammit` left intact. Never spelled out, even in titles. "Apps Doing Sh*t". The asterisk is the point.

## Opening moves

- Cold-open scene: "I put in my earbuds and walked briskly to the train station." (59)
- Rhetorical question as title repeat: "What is a Tech Lead Anyway?" (18)
- Confession: "Lately, I'm writing fewer emails at work." (42)
- Observation: "Being a software engineering manager has its difficult people bits." (43)
- Naming move: "For software engineers, naming things is hard." (04)
- Meta: "Write to document what you're doing now." (68)

## Closing moves

- Philosophical landing: "Kotlin is here. I hope not another rewrite." (01)
- Open question back to the reader: "What have you experienced?" (52)
- Wry sigh: "Do astronauts receive updates while their rocket escapes the atmosphere? Sigh." (54)
- Practical conclusion earned by the body: 59 and 61.
- Quiet resolution: "And so, you and I listen to new music alone." (62)

## Sentence and paragraph rhythm

- Short declaratives in bursts. Then a longer orienting sentence. Then another burst.
- Em-dashes signal pivot or stakes. Parentheticals invite the reader close for a beat.
- Anaphora is a tool: repeat a subject-verb opener across three sentences for authority (16).
- Lists inserted mid-prose are fine; they speed the piece up, not slow it down.
- Paragraphs: 3–6 sentences in the middle, 1–2 sentences at turns or climaxes.

## Lists

- Numbered when order, procedure, or priority matters.
- Bulleted when the items are peers.
- Tables when comparing (60 versioning schemes).
- Inline "First, … Second, … Finally, …" when a list would break the narrative.
- Every list item earns its own line only if it earns its own idea.

## Humor devices

- Self-deprecation aimed at the narrator, never the reader.
- Mock-formality punctured by a plain observation.
- Absurd comparison grounded in a real grievance.
- Playful coinage (SECTA, float typing, the Stew). Coin, then use, then move on.
- One-word paragraphs for deadpan.
- Parenthetical hedge as wink ("(And yes, I am the only one asking silly questions.)" 26).

## Sourcing and references

- Internet-native. Medium, dev.to, HN, Substack, GitHub, YouTube, official docs.
- Link density: short 2–5, medium 8–15, long 15–40.
- Citation density should rise with stakes. Gripes and rants cite lightly (3–5). Role definitions, management essays, and deep dives cite heavily (10–15+). The book pattern: external authority builds permission to advise senior moves.
- Books appear as nods to a stable shared canon. Confirmed by the book's Selected Bibliography: _The Mythical Man-Month_ (Brooks), _Code_ (Petzold), _Hackers_ (Levy), _Masters of Doom_ (Kushner), _The Pragmatic Programmer_ (Hunt & Thomas), _Programming Pearls_ (Bentley), _The Soul of a New Machine_ (Kidder), _Peopleware_ (DeMarco & Lister), _The Cathedral and the Bazaar_ (Raymond), _Hackers & Painters_ (Graham), _Zen and the Art of Motorcycle Maintenance_ (Pirsig), _The Manager's Path_ (Fournier), _High Output Management_ (Grove), _Designing Data-Intensive Applications_ (Kleppmann). Rarely quoted at length.
- People are named when they exemplify the point: Guido, Carmack, Uncle Bob, Rich Hickey, Jake Wharton.
- No bibliography in blog form. Inline links. No academic citation style. The book converts inline links to numbered endnotes; treat that as a pure print-format concern, not a voice change.
- Non-software inputs are legitimate: amateur radio, motorcycling, painting plastic models, retro game modding, YouTube subscriptions. Transposition (radio axiom → career mastery; T-CLOCS → code review) is a teaching method, not a tangent.

## Diction and signature vocabulary

- "Craft", "philosophy", "mental model", "visibility", "accretion", "connascence", "reify", "mise en place".
- First-person markers: "I've learned", "I've noticed", "To me", "Here's what I found".
- "What's in a [X]?" as a Shakespearean tee-up.
- Industry jargon is used when canonical, explained when novel.
- Avoid "obviously", "all engineers", "everyone knows". Use "in my experience", "some teams", "one pattern I've seen".

## POV and tense

- First-person singular is default.
- First-person plural for shared professional experience.
- Second-person for how-to mode.
- Third-person for definitional pieces about a role.
- Present tense for timeless claims. Past for anecdotes. Present perfect to bridge. Shift freely within a single essay when the beats demand it.

## Length and shape

- Most essays land short to medium. Deep dives and career memoirs stretch long.
- Section headers in medium-and-longer pieces. None or one in short pieces.
- Code blocks, screenshots, and small graphs when they show what prose cannot.

## Titles

- Playful is fine. Misleading is not.
- Patterns:
  - "What is a [X] Anyway?"
  - "How to [Verb] Your [Object]"
  - "[The] [Adjective] [Noun]"
  - Allusion to a canonical essay: "Reply All Considered Harmful" (Dijkstra nod).
  - Possessive coinage: "[Name]'s Law" — name the rule after the actor it indicts (102).
  - Vulgarity or dammit-energy when the piece is a rant, not otherwise.
- Subtitle optional; one clause.

## Do

- Commit to statements.
- Name the thing. Coin the term. Use it.
- Admit uncertainty when it exists. Say "I don't have the full answer; here's a pattern".
- Use concrete tools, languages, companies, people.
- Vary sentence length aggressively.
- Close on a turn, not a summary.
- Cross-link to sibling essays. For "What is a … Anyway?" pieces, link to the **published Medium / dev.to URL** (per [README.md](../README.md)) rather than the local `.md` path. The published URL is what readers follow.
- Add an object to a bare verb when the sentence reads thin. "Directors broker deals." beats "Directors broker." "The role rewards decision-making." beats "the role rewards the admission."
- Replace abstract closers with a concrete noun. "produces nothing but frustration" beats "produces nothing else."

## Don't

- Don't hedge into cowardice.
- Don't gatekeep with jargon without a first-use explanation.
- Don't preach from seniority.
- Don't clickbait.
- Don't end every essay with a motivational sendoff.
- Don't over-header short pieces.
- Don't stack "that", "just", "really", "actually". See [writing-editing.md](../writing-editing.md).

## Exemplar pieces to imitate

- Definitional: 18, 27, 29.
- How-to: 20, 21, 48.
- Memoir: 43, 47, 59.
- Listicle: 52, 67.
- Deep dive: 04, 07, 60.
- Rant: 42, 65.
- Video-game-as-systems: 45, 57, 67.
- Coinage / law-naming: 102 (Claude's Law).
- Long-form modding memoir: 34 (Half-Life mod).
- Crossover transposition: 50 (motorcycling), 49 (hobbies), 66 (YouTube).

## Author identity (load-bearing facts)

- Douglas W. Arcuri. Long Island, New York. Engineering manager at SaaS / tech software companies; earlier career in mobile video streaming for media companies.
- Off-hours: writes business history (toy industry), rides motorcycles, paints plastic auto models, ships retro game mods.
- First book: _Deconstructive Software Ramblings_ (2024). Second: _Undercover Toy Stories_ (2025).
- The author writes openly partly as a stated relief valve against burnout; do not sand off frustration in an edit. Frustration is part of the voice.
- Hazem Saleh wrote the foreword to DSR; Danny Preussler and James Shvarts are credited inspirations; Aida Issayeva edits. Name them only when they are actually load-bearing for a piece.

## Learning log

<!-- Append dated bullets. Newest at top. Promote recurring patterns into the body above. -->

- 2026-05-02: Deep read of the published manuscript of _Deconstructive Software Ramblings_ (DSR), the author's collected book of essays 01–68 plus reorganization. Promoted into the body: book taxonomy table, signature stylistic devices (small-caps openers, ➔ bullet-arrow lists, ●●● section breaks, bracketed editorial wink with †, italicized one-line kickers, dictionary-form section epigraphs, asterisked profanity), citation-density-by-stakes rule, expanded shared canon list from the actual Selected Bibliography, and an Author identity block. Additional patterns worth keeping in mind but not yet promoted:
  - **The book is a disguised career-arc memoir.** Section order ascends: Gripes → Listicles → Practices → Reading/Writing → Role definitions → Interviewing → Engineer → Manager → Crossovers → Reflections → Epilogue. New essays should know which rung they sit on.
  - **Examples beat abstractions.** Essay 34 (Half-Life mod) is the longest piece in the corpus and uses narrative case-study form, not theory. When teaching a hard idea, find the long story first.
  - **Failure is credibility.** The Cold Ice failure, the HN ban after the HN-frontpage essay, the "stroke while reading" reader quote — all preserved. Do not sand failures out; they earn the wins.
  - **The "Even More Praise for the Author" device.** The book's back-matter praise page is real but inverted: hostile reader quotes, mod-removal notices, one genuine compliment. The joke lands because it is the literal truth. Available as an opener move for a meta-essay on writing or platforms (consider for any future essay 19-style piece).
  - **Editorial dagger (`†`) vs. citation bracket (`[1]`).** In book form, `†` marks an author aside; `[N]` marks an external source. Drafts can ignore the dagger and use plain brackets `[like this]`; the daggered form is print-only.
  - **Index discipline.** The book indexes concepts and named people heavily, products lightly. When coining a term in a new essay (Springboard, SECTA, Decision Hypothesis, Claude's Law, the Stew, LatestVer, the Manager Stew), the term is the indexable noun. Coin → use → reuse → it lands in an index someday.
  - **"Ship" is the load-bearing verb.** Essays 47, 59, and 64 turn it into a thesis. When a draft has lost its spine, ask whether the thesis collapses to "ship".
  - **Pandemic-era dating.** Essays 23, 45, 59, 63 anchor the post-2020 office-renegotiation moment. Future essays referencing remote work should treat that period as historical, not current.

- 2026-04-30: Pattern study of essay 102 (Claude's Law). A new sub-genre lives here: the **agentic-coding reflection**. It is short (~350 words), memoir-shaped, and ends in a coined law. Specific moves to imitate:
  - **Trigger from a public artifact.** Open with an external prompt — an HN post, a list, a public law library. "I came across the post on Hacker News titled …". The artifact gives the essay something to react to and a place to send the reader.
  - **Greybeard foil.** Stage a canonical old law against a present-day agentic moment. The collision is the engine. In 102 it is _Go To Statement Considered Harmful_ vs. an agent committing `goto`s. Always link the original (web.archive.org if needed).
  - **Self-implication.** The narrator confesses they let the agent's choice land — "I committed the code and let the second AI review it." The piece earns its coinage by admitting complicity, not by scolding the tool.
  - **Quote scaffolding.** Block-quote the narrator's own HN comment, then a stranger's reply, then the coined line. Three quoted beats, each indented, each shorter than the last. The escalation lands the punchline.
  - **Scriptural inversion.** A King James cadence repurposed for tech satire ("Render therefore unto Caesar … and unto Claude …"). Use sparingly; one allusion per essay, and only when the source phrasing genuinely rhymes with the modern observation.
  - **Coin, italicize, define in one line.** "_**Claude's Law**: The code that is written by the agent is the most correct way to write it._" Bold the name, italicize the whole line, keep the definition to a single declarative. No hedge.
  - **Direct address as closer.** Naming the person who maintains the canon ("Dr. Milan Milanović, if you see this, please consider adding it …") earns a wry intimacy that a generic call-to-action cannot. Pair with a small private admission ("And yeah, I updated my style context file …") to break the fourth wall and keep the narrator honest.
  - **Social Post block.** Lead with the most quotable line in quotes, hashtag the actors (#Caesar, #Claude), then the topical hashtags, then the dev.to URL. Title-case hashtags per the 103 calibration.
  - **Length discipline.** Coinage essays stay short. The law is the payload; the scene is the wrapper. Resist adding a second example.

- 2026-04-30: Calibration pass against the published version of essay 103 (Engineering Director). Promoted into the body: cross-link rule (use published URLs), "add an object to a bare verb" rule, "concrete noun over abstract closer" rule. Specific deltas from my draft to the published version:
  - **Opening flip.** "I've worked with engineering directors as an engineer and as a manager" → "As a manager, I've worked with amazing engineering directors." The role the author held leads. The adjective "amazing" warms the opening without flattering the narrator.
  - **Cross-essay links.** Most-prominent role links go to the published dev.to URLs (`/what-is-an-engineering-manager-anyway-4and`, `/what-is-a-software-engineer-anyway-3fb2`); secondary links can stay as local `.md` paths during drafting. Published-URL discipline mirrors the toy spoke.
  - **Articles for rhythm.** "Engineers ship software, managers guide teams, and directors coach managers" → "Engineers ship the software, managers guide their teams, and directors coach the managers while setting the vision." The articles soften the staccato; the trailing clause adds the missing director-specific verb.
  - **Concrete noun beats abstract closer.** "A poorly shaped one produces nothing else" → "… produces nothing but frustration." "the role rewards the admission" → "the role rewards decision-making." Name the noun.
  - **Bare verbs gain objects.** "Directors broker." → "Directors broker deals." The bare verb sounded clipped; the object lands the bold-sentence opener.
  - **Verb variety in the rhythm trio.** "An engineer's loop runs in minutes. A manager's in weeks. A director's in halves and years." → "… A manager's last weeks. A director's cycle goes a year." The published version varied the verb ("runs", "last", "goes") and dropped the slightly poetic "halves and years" for plainer time. Vary the verb across the trio.
  - **Pluralization smooths.** "the project at the edge of their skill" → "projects at the edge of their skills."
  - **Broaden where credit lands.** "so credit lands with the manager" → "so credit lands with the leads and teams." Directors hand credit two layers down, not one.
  - **Hashtag capitalization.** Use Title Case in hashtags in the Social Post block: `#Engineering #Director`, not `#engineering #director`.
  - **Possessive small-word pickups.** "Patience is the price of admission" → "Patience is the price of their admission." Small possessives anchor the subject of the sentence to the role being defined.
- 2026-04-23: Hyperlink discipline for definitional essays. Key terms are linked to (a) prior essays in the corpus (see README for the canonical URL list) and (b) outside canon when the term is borrowed. Exemplar: essay 35 links "free electrons", "holistic results", "tech lead", "principal engineers", "product manager". Apply the same density to new "What is … Anyway?" pieces. Cross-link to at least 3 of the sibling role essays (18, 22, 27, 29, 30, 33, 35, 40) where the concept naturally touches them.
- 2026-04-23: Synonym discipline. Within a single essay, rotate high-frequency role nouns (director/manager/engineer) and action verbs (deliver/ship/execute) across paragraphs. Repeat for rhythm, not for fill.
- 2026-04-23: Sentence construction. Prefer the fuller periodic form over cute compression when a comparison is at stake. "noise **that is apt to** derail delivery" over "noise **apt to** derail delivery". The small word keeps the reader from stumbling.
- 2026-04-23: Avoid superlative adjectives on the narrator's peers. "the technologist in the room" reads better than "the sharpest technologist in the room". The superlative reads as ego; dropping it keeps the observation flat.
- 2026-04-23: Italic one-liner coinages at the close can feel tacked on. Let the final paragraph do the landing. A separate italicized epigraph after the body is optional, not required.
- 2026-04-23: Initial spoke created from corpus analysis of essays 01–68.
