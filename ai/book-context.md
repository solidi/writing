# Book Context — Spoke

Voice and form guide for **book-shaped artifacts**: anthologies, collected essays, memoirs, and themed compilations published as printed (or print-equivalent) volumes. This spoke loads on top of the subject spoke, not in place of it.

## When to load this file

- Drafting or editing **front matter**: praise pages, title/copyright page, dedication, epigraphs, foreword, introduction, "How to Use This Book".
- Drafting or editing **back matter**: epilogue, acknowledgments, endnotes, selected bibliography, index, about the author, back-cover copy, "Even More Praise" pages.
- Designing **section architecture**: choosing the number of sections, naming them, writing dictionary-form epigraphs, ordering essays into a deliberate arc.
- Converting a blog essay into book form (link conversion, profanity discipline, bracketed asides, footer glyphs).
- Writing personal soliloquy passages that bridge sections (the author addressing the reader directly between essays).

Always also load:

- [writing-context.md](writing-context.md) — base voice.
- The matching subject spoke: [software-context.md](software-context.md) for software/career anthologies; [toy-context.md](toy-context.md) for toy-history anthologies.

## Anchor works

- **DSR** — _Deconstructive Software Ramblings: Essays from the Mind of an Engineering Manager_ (Dependent Studios LLC, December 2024; reprint November 2025). Software anthology. 64 essays in 10 sections + epilogue. ISBN 979-8-9919267-0-6.
- **UTS** — _Undercover Toy Stories: An Anthology of Real American Inventions_ (2025). Toy-history anthology. Sectional structure expected to follow DSR's editorial conventions.

When DSR and UTS disagree on a convention, defer to the spoke that owns the subject (software vs. toy). When they agree, treat the convention as load-bearing for any future book.

## Front-matter pattern

Order, top to bottom, in the printed book:

1. **Praise for the Author** — page of pull-quoted reader/admin/peer comments. See _Praise page strategy_ below.
2. **Also by the Author** — single line per prior title. Italicized.
3. **Title page** — book title in three lines, all caps, hard-broken; subtitle one line, mixed case, italic optional.
4. **Copyright page** — author, copyright years, publisher (Dependent Studios LLC), permissions email (`douglaswarcuri@gmail.com`), production note (Google Docs, EB Garamond body, Courier New code), trademark disclaimer, ISBN, LCCN, edition/printing line.
5. **Dedication** — two short dedications max, paired by relationship (mentor-figure + family-figure works). One sentence each. No "for".
6. **Epigraph** — single quoted line, attributed in brackets to the narrator-as-character: `"There are no adults in this conference room. I'll prove it!" [The author writes his opinions—later—on the Internet.]`
7. **Contents** — section + chapter list with page numbers. Front matter and back matter included with roman/decorative page references.
8. **Foreword** — written by a credentialed peer (DSR: Hazem Saleh). Not the author. Title cased simply: "Forward" or "Foreword".
9. **Introduction** — first-person, scene-driven, ends with a turn that sets up the rest of the book.
10. **How to Use This Book** — short. Permission to skip around. Concrete suggestions ("park it on the coffee table", "read on support rotation"). Always closes by pointing to the canonical online home (`github.com/solidi/writing`).

## Back-matter pattern

1. **Epilogue** — one or two short essays separated from the numbered sections, marked with `∞.` rather than a section number. Lands the arc.
2. **Acknowledgments** — sparse. Editor first, then specific peer inspirations by name and reason, then family obliquely. No alphabetical thank-you list.
3. **Endnotes** — superscript `[N]` in body, full URL or citation in the back. Numbered straight through, not per chapter. Plain-text URLs (no hyperlinks). See _Citation discipline_ below.
4. **Selected Bibliography** — alphabetical. Books only; URLs and articles stay in endnotes. 30–60 entries.
5. **Index** — concepts and named people heavily; products and companies lightly. Coinages (Springboard, Claude's Law, the Stew, LatestVer) get their own entries.
6. **About the Author** — ~100 words. Geography, day job, prior career, off-hours practice. No personal/family detail beyond a single oblique reference. Brevity is the move.
7. **(Optional) Even More Praise** — see _Praise page strategy_.

## Praise page strategy

DSR's front-matter praise page is **real but inverted**. Quotes lead with reader hostility, mod-removal notices, platform friction, and a reader misreading the author as AI; one genuine compliment lands at the bottom. The joke is that it is the literal truth.

Rules:

- Use real quotes only. Never fabricate. Pull from comments, removal notices, DMs.
- Order by escalation: misreading → snark → ban → rebuke → policy quote → genuine compliment.
- Attribution is a generic role: `—A reader`, `—An admin`, `—Software Lead Weekly`. Names appear only when the source is professional and named in print elsewhere.
- The single genuine compliment closes the page. It earns its weight by sitting under the noise.
- An optional **"Even More Praise for the Author"** page can sit in the back matter to extend the device. Same rules.

This pattern is portable. The toy book may invert the device differently — collector forum gripes, Reddit removals, eBay seller complaints — but the structure (escalating hostility, single sincere closer) holds.

## Section architecture

- **Number of sections.** DSR uses ten plus an epilogue. Use seven to twelve numbered sections; fewer reads thin, more reads encyclopedic.
- **Section header.** Roman numeral + period + name: `Section One`, then `I. Gripes on Software Experiences` in the contents. Title in body uses the spelled-out form.
- **Section epigraph.** Dictionary-form definition, italicized, single line:
  - `gripe (/ɡrīp/) v. complain about something in a persistent, irritating way.`
  - `listicle (/ˈlistək(ə)l/) n. a piece of writing presented in the form of a list.`
  - The pronunciation guide uses IPA-ish slashes. The part of speech is abbreviated (n., v., adj., adv.). The definition is one clause, lowercase, ends with a period.
  - For the toy book, expect: `incident (n.)`, `inventor (n.)`, `patent (n.)`, `archive (n.)`, `mascot (n.)`, etc.
- **Section ordering as arc.** The order is not topical; it is narrative. DSR ascends from gripes (junior frustrations) through role definitions (mid-career) into management (senior) and closes on reflection and shipping. The toy book should similarly carry its own arc: e.g., artifact → inventor → incident → archive → grief.
- **Epilogue marker.** Use `∞.` instead of a numeral. Holds two essays at most.

## Personal soliloquy passages

The author's voice as **narrator** (not as essayist) appears in:

- The **Introduction** — scene-opened, first-person, ends on a turn.
- **How to Use This Book** — direct address ("this author suggests"), second-person warmth ("you got this"), bracketed wink asides.
- **Section preambles** (optional) — one short paragraph under the section epigraph, in italic if used. UTS may use this more heavily than DSR did.
- The **Epilogue** — quietest register in the book. No coinages. No advice. Land the feeling.
- The **Acknowledgments** — sparse, named, specific.

Soliloquy rules:

- "This author" appears as a deliberate distancing device, especially in toy-history pieces. Pair with first-person elsewhere; do not mix within a single paragraph.
- Keep soliloquies short. The reader bought essays; the soliloquy earns its space by framing them, not competing with them.
- One bracketed wink per soliloquy maximum. The device dilutes if used twice.
- The Epilogue does not ask a question. It closes.

## Editorial conventions (blog → book)

When converting a blog essay for inclusion in a book:

- **Profanity asterisked.** `sh*t`, `batsh*t`. `dammit` stays intact. Asterisking applies in titles too. The asterisk is the joke.
- **Inline links → endnotes.** Strip every `<a>` and replace with a superscript `[N]`. The URL goes plain-text into the Endnotes section. No hyperlink survives in print.
- **Editorial dagger (`†`).** Reserved for the author's bracketed asides: `[which is to ship]†`. The `†` distinguishes the aside from a citation. Drafts can use plain `[brackets]`; insert the dagger only at typesetting.
- **Section breaks within an essay.** Use `● ● ●` (three centered bullets) for a thematic pivot inside a long piece where a new header would be too heavy. One per essay maximum.
- **Small-caps + bold opener.** First two to four words of the body in small caps and bold. `**TYCO TOYS, INC. OPERATED** out of Mount Laurel, New Jersey.` Near-universal in book versions of essays from both books.
- **Italic one-line kicker.** A single italicized rhetorical sentence (`_Is it?_`) lands a turn. One per essay.
- **Bullet-arrow lists** (`➔`). Replace plain bullets when items deserve a visual anchor. Lead with a bolded noun phrase.
- **DSR footer glyph.** Not portable to other books. The toy book should adopt its own one-letter footer glyph (`UTS`?) only if it earns the recurrence.
- **Tense and link prose.** Where a blog essay says "I [linked yesterday] about X", strip the temporal hook. The book reader is not in the same week as the blog reader.
- **Cross-link prose.** "See also essay 22" beats "I wrote about this on Medium". Use the in-book chapter number, not the URL.

## Citation discipline

- **Numbering.** Straight-through `[1]…[N]` across the whole book. Do not restart per chapter.
- **Two marker types.**
  - `[N]` — external source. Lands in Endnotes.
  - `†` — editorial aside, author's voice. Stays inline in the body, paired with a bracketed phrase.
- **URL form.** `https://example.com/path` in plain text. No tracking parameters. No `medium.com/@solidi/...` short URLs — use the full canonical link.
- **Density by stakes.**
  - Gripes and rants: 3–5 endnotes.
  - Listicles and how-tos: 5–10.
  - Role definitions, management essays, deep dives: 10–15+.
  - Long-form case-study essays (DSR essay 34, Half-Life mod): 25+.
- **Books in endnotes** are short-form (`Brooks, _Mythical Man-Month_, ch. 11`). Full bibliographic entry lives in Selected Bibliography only.
- **Wikipedia and standard references** (Big O, Dijkstra, common acronyms) appear unmarked in the body. They earn no endnote.

## Index discipline

- **Index concepts heavily.** Abstractions, correctness, decisions, delegation, mentorship, philosophy, shipping. The reader looking for "how does the author think about X" finds X.
- **Index named people** when they appear as exemplars or sources. Carmack, Brooks, Bentley, Guido, Tilbor.
- **Index coinages.** Springboard, Decision Hypothesis, the Stew, LatestVer, SECTA, Claude's Law. The coinage is the indexable noun.
- **Index lightly for products and companies.** A line per appearance, not a sub-tree.
- **Do not over-index family or personal references.** A single oblique entry is enough.

## Selected Bibliography conventions

- Alphabetical by author surname.
- Books only. Articles, podcasts, videos, and forum posts stay in Endnotes.
- 30–60 entries.
- Confirmed canon for the software book (carry forward to any reissue): _The Mythical Man-Month_, _Code_, _Hackers_, _Masters of Doom_, _The Pragmatic Programmer_, _Programming Pearls_, _The Soul of a New Machine_, _Peopleware_, _The Cathedral and the Bazaar_, _Hackers & Painters_, _Zen and the Art of Motorcycle Maintenance_, _The Manager's Path_, _High Output Management_, _Designing Data-Intensive Applications_.
- The toy book should declare its own canon — e.g., _Toy Wars_, _The Toys That Made Us_ companion volumes, FTC and CPSC reports, Patent and Trademark Office records, period trade press (_Playthings_, _Toy & Hobby World_).

## About the Author

- ~100 words. Brevity is load-bearing.
- Open with the author's name in **bold small caps**: `**DOUGLAS W. ARCURI** resides …`
- Geography → present role → prior career → off-hours practice. In that order.
- One oblique family reference at most ("with his family on Long Island").
- No book promotion in the bio. The book itself is the promotion.

## Cover and back-matter copy

DSR ships without a traditional back-cover blurb. The "Even More Praise" page does the back-cover work. If a future book wants a conventional blurb:

- Three short paragraphs maximum.
- First paragraph names the genre and the promise.
- Second paragraph names a specific essay or chapter as a hook.
- Third paragraph closes on the author's stance, not on the reader's benefit.
- Pull-quotes, if used, follow the praise-page rules (real, attributed minimally, escalation order).

## Do

- Treat the book form as an editorial object, not a content object. The essays already exist; the book is the framing.
- Pick the section arc before placing essays into sections. The arc is the argument.
- Coin a one-line dictionary epigraph for every section. If you cannot, the section is not a section yet.
- Preserve failure narratives (the HN ban, the Cold Ice mod failure, the recall, the lawsuit). They earn the wins.
- Let the soliloquy passages be quiet. Save the firepower for the essays.

## Don't

- Don't sand off frustration. The author writes openly partly as a relief valve; book editing should preserve the original heat.
- Don't sanitize the praise page into flattery. The inversion is the device.
- Don't restart endnote numbering per chapter.
- Don't promote the book inside the book. The "About the Author" and "Also by the Author" lines do all promotion.
- Don't add a motivational sendoff to the Epilogue. Land it; do not exhort.
- Don't introduce a new coinage in the front matter or back matter. Coinages live in the essays.

## Learning log

<!-- Append dated bullets. Newest at top. Promote recurring patterns into the body above. -->

- 2026-05-02: Spoke created from a deep read of _Deconstructive Software Ramblings_ (manuscript) and from forward-looking notes for the toy-history book (UTS) which is expected to share book-form conventions while inheriting the toy-context voice. The praise-page inversion, dictionary-form section epigraphs, dagger-vs-bracket citation split, ●●● break, small-caps openers, and the brevity discipline of "About the Author" are all DSR-confirmed and portable.
