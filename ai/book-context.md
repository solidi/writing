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
- **UTS** — _Undercover Toy Stories: An Anthology of Real American Inventions_ (Dependent Studios LLC, 2025). Toy-history anthology. Three Parts plus three Appendices, no numbered epilogue. ~9,800 manuscript lines, ~1,270 endnotes.

DSR and UTS are sibling books with deliberately different registers. **DSR is informal; UTS is formal.** When the two books disagree on a convention, the disagreement is usually load-bearing for the spoke that owns the subject. The table below records confirmed deltas; defer to it before generalizing a DSR pattern onto UTS or vice versa.

| Convention | DSR | UTS |
|---|---|---|
| Section header | `Section One` / `I. [Theme]` | `PART I: [THEME]` (small caps in body) |
| Section epigraph | Dictionary-form definition: `gripe (/ɡrīp/) v. …` | Block quotation from a cited book or interview, attributed in ALL CAPS: `RUTH HANDLER, NYT 1959.` |
| Closing structure | Numbered Epilogue marked `∞.` | Three Appendices (A/B/C) + a "TIMELESS" bridging chapter; no `∞.` marker |
| Profanity | Asterisked (`sh*t`) | Absent. Strict-formal register throughout. |
| Editorial dagger `†` | Used for author asides | Not used. Asides are pushed into footnotes. |
| Bracketed wink asides | Common in body and front matter | Rare. Brackets reserved for clarifying inserts inside quotations. |
| Social Post block | Stripped from book; lives in blog version | Stripped from book; lives in blog version |
| Praise page | Real-but-inverted device (hostile reader quotes + one sincere closer) | Not present in the published manuscript. Do not assume one. |
| Bibliography | Software canon (Brooks, Petzold, Kushner, etc.) | Toy / Cold War / archive canon (Stern & Schoenhaus, Gerber, Lord, Oppenheimer, Douglass, Rich, Feynman, Coster, Paxton, Valone, Boellstorff & Soderman, etc.) |
| Index | Concepts > people > products | People + companies + products + places + patents + incidents, very dense (~500 entries) |
| About the Author | Career-arc bio, ~100 words, professional register | Grief-forward bio, ~70 words, "researcher and citizen journalist", names mother's death from long COVID |
| Grief frame | Absent | Explicit in front and back matter; subtext in essays |
| Appendices | None | Three. Appendix A is a standalone ~18,000-word investigative monograph. |
| Public-records device | None | Appendix C catalogs FOIA / CPRA returns and refusals as a literary device |

When in doubt about a convention, defer to the spoke that owns the subject (software vs. toy). When the two books _agree_, treat the convention as load-bearing for any future book.

## Front-matter pattern

The two books share a skeleton but differ on individual slots. Confirmed slots, in order:

1. **Praise for the Author** — DSR uses the real-but-inverted device. UTS omits a praise page entirely. New books should choose deliberately.
2. **Also by the Author** — single line per prior title. Italicized.
3. **Title page** — book title hard-broken, all caps; subtitle on one line.
4. **Copyright page** — author, copyright years, publisher (Dependent Studios LLC), permissions email, production note (typeface, software), trademark disclaimer, ISBN, LCCN, edition / printing line.
5. **Dedication** — short, paired by relationship. DSR: mentor + parent. UTS: grief-forward, oriented toward the family that survived the loss.
6. **Epigraph(s)** — DSR opens with a single first-person epigraph attributed to the narrator-as-character. UTS opens with a quotation from an outside source (Ruth Handler, NYT 1959).
7. **Contents** — section / part list with chapters and page numbers. UTS contents lists chapters by **year** (Ch. 1959, Ch. 1968, Ch. 2009, etc.) rather than sequential numbers.
8. **Foreword** — DSR has one, written by Hazem Saleh (a credentialed peer). UTS does not have a Foreword; it goes straight from front matter into a Preface and Introduction in the author's own voice. Forewords are optional.
9. **Preface / Introduction / How to Use This Book** — DSR uses Introduction + How to Use. UTS uses Preface + Introduction (no How to Use). Pick the combination that suits the book's stance: instructional (DSR) vs. archival (UTS).
10. **List of Figures** — UTS uses figure-letter notation (`A.1`, `AA.2`) for appendix and personal-photo plates. DSR has no formal list of figures.

## Back-matter pattern

1. **Epilogue** (DSR only) — one or two short essays separated from the numbered sections, marked with `∞.` rather than a section number. Do not port to other books unless the structure earns it.
2. **Appendices** (UTS) — lettered A, B, C. Appendix A may be book-length on its own; treat appendices as a venue for original investigative research that does not fit essay form.
3. **Acknowledgments** — sparse in DSR, expansive in UTS. UTS names ~31 individuals across librarians, museums, government employees, named industry insiders, fellow researchers, therapist, family, and father. Both forms are valid; pick by project scope.
4. **Endnotes** — superscript `[N]` in body, full URL or citation in the back. Numbered straight through, not per chapter. Plain-text URLs (no hyperlinks). DSR: ~450. UTS: ~1,270. Toy investigations cite more heavily than software essays.
5. **Selected Bibliography** — alphabetical. Books only; URLs and articles stay in endnotes. DSR: ~30–40 entries. UTS: ~47 entries.
6. **Index** — DSR weighting: concepts heavy, people moderate, products light. UTS weighting: people, companies, products, places, patents, incidents — all dense (~500 entries). Choose by reader use case.
7. **About the Author** — brief. Voice can shift book-to-book (see Author identity in subject spokes).
8. **(Optional) Even More Praise** — DSR-only device. Not used in UTS.
9. **(Optional) Suggested Future Volume** — UTS appends a list of speculative future essay titles signaling the project will continue. Useful for series anchors.

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

DSR and UTS use different section grammars. Both are valid; pick by subject.

### DSR pattern (informal anthology)

- **Number of sections.** Ten plus an epilogue. Use seven to twelve numbered sections; fewer reads thin, more reads encyclopedic.
- **Section header.** In the body, the spelled-out form: `Section One`. In the contents, Roman numeral + period + section name: `I. Gripes on Software Experiences`.
- **Section epigraph.** Dictionary-form definition, italicized, single line:
  - `gripe (/ɡrīp/) v. complain about something in a persistent, irritating way.`
  - The pronunciation guide uses IPA-ish slashes. The part of speech is abbreviated (n., v., adj., adv.). The definition is one clause, lowercase, ends with a period.
- **Section ordering as arc.** DSR ascends from gripes (junior frustrations) through role definitions (mid-career) into management (senior) and closes on reflection and shipping. The order is narrative.
- **Epilogue marker.** `∞.` instead of a numeral. Holds two essays at most.

### UTS pattern (formal anthology / archive)

- **Number of parts.** Three Parts plus Appendices A–C. Parts are larger and fewer than DSR sections; each Part contains a chronological run of chapters.
- **Part header.** ALL CAPS, prefixed with `PART I:` / `PART II:` / `PART III:`. Example: `PART I: A TIME FOR TOY STORIES`.
- **Part epigraph.** A block quotation from a cited source, with an ALL-CAPS attribution line below. Examples seen in UTS:
  - `"With our [toy-making] system, Ruth said whimsically, we might just as well be turning out real airplanes or missiles." RUTH HANDLER, NYT 1959, p. 23.`
  - `"Unlike geology, archaeology explores what we can understand as 'near history.' …" TOM BOELLSTORFF & BRAXTON SODERMAN, INTELLIVISION (MIT PRESS, 2024), p. 19.`
- **Chapter naming by year.** UTS chapters are named for the year they investigate: `Ch. 1959`, `Ch. 1968`, `Ch. 2009`, etc. This anchors the book as a chronological archive rather than a topical anthology. A dateless coda chapter is named `TIMELESS`.
- **Bridging chapter.** UTS uses a single "TIMELESS" chapter to pivot from the Part I survey into the Part II investigative deep dive. The bridging chapter is structural, not content-only; it earns its title.
- **Appendices over epilogue.** UTS replaces a numbered epilogue with three lettered appendices that carry original research (monograph-length investigation, expanded timeline, public-records inventory).

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

- **Profanity.** DSR asterisks (`sh*t`, `batsh*t`); the asterisk is the joke. UTS strips strong language entirely; the register is formal. Choose the convention by the book's stance — do not import DSR's asterisking into a UTS-style work.
- **Inline links → endnotes.** Every blog hyperlink is converted to a superscript `[N]` and the URL goes plain-text into the Endnotes section. No hyperlink survives in print. UTS endnote density runs ~1,270 across the volume; DSR runs ~450. Density follows the book's evidentiary stance.
- **Editorial dagger (`†`).** DSR-only device. Reserved for the author's bracketed asides: `[which is to ship]†`. UTS does not use it; asides are pushed into endnotes. In drafts, plain `[brackets]` are fine — the dagger is a typesetting concern.
- **Section breaks within an essay.** DSR uses `● ● ●` (three centered bullets) for a thematic pivot. UTS uses bordered horizontal-rule breaks and named sub-sections. One break per essay maximum.
- **Small-caps + bold opener.** First two to four words of the body in small caps and bold: `**TYCO TOYS, INC. OPERATED** out of Mount Laurel, New Jersey.` Near-universal in book versions of essays from both books.
- **Italic one-line kicker.** A single italicized rhetorical sentence (`_Is it?_`) lands a turn. DSR uses this often; UTS uses it sparingly because the formal register resists it.
- **Bullet-arrow lists** (`➜`). DSR-friendly when items deserve a visual anchor. UTS prefers numbered lists or prose enumeration in keeping with archive-speak.
- **Footer glyph.** DSR uses `DSR`. UTS does not adopt a footer glyph. Do not import a footer glyph unless the book earns its own.
- **Tense and link prose.** Where a blog essay says "I [linked yesterday] about X", strip the temporal hook. The book reader is not in the same week as the blog reader.
- **Cross-link prose.** "See also Ch. 1968" beats "I wrote about this on Medium". Use the in-book chapter reference, not the URL. UTS chapter references use the year (`Ch. 1968`); DSR uses the chapter number.
- **Social Post block.** Stripped entirely in both books. Social posts live with the blog version, not the book.
- **Book-promo block.** The Amazon-link block that closes a blog toy essay is removed in the book itself (the book is the promo). For a third book, replace with a clean Suggested-Future-Volume teaser, UTS-style.

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
- Confirmed canon for the **software book (DSR)**: _The Mythical Man-Month_, _Code_, _Hackers_, _Masters of Doom_, _The Pragmatic Programmer_, _Programming Pearls_, _The Soul of a New Machine_, _Peopleware_, _The Cathedral and the Bazaar_, _Hackers & Painters_, _Zen and the Art of Motorcycle Maintenance_, _The Manager's Path_, _High Output Management_, _Designing Data-Intensive Applications_.
- Confirmed canon for the **toy book (UTS)** — ~47 entries, interdisciplinary on purpose. Anchors include:
  - Toy-industry trade and biography: Stern & Schoenhaus _Toyland_, Gerber _Barbie and Ruth_ and _Barbie: Her Inspiration, History, and Legacy_, Lord _Forever Barbie_, Oppenheimer _Toy Monster_, Miller _Toy Wars_ and _Kid Number One_, Clark _The Real Toy Story_, Lobel _You Don't Own Me_, Schneider _Children's Television_.
  - Toy makers' memoirs and trade-press: Handler _Dream Doll_, Elliot Handler _The impossible really is possible_, Sweet & Wecker _Mastering the Universe_, Breslow _A Game Maker's Life_, Paxton _A World Without Reality_, Murfin _Daisy_.
  - Cold War / aerospace / investigation: Rich _Skunk Works_, Douglass _JFK and the Unspeakable_, Marrs _Crossfire_, Engelhardt _End of Victory Culture_, Valone _Papp Noble Gas Engine Report_, Feynman _Surely You're Joking_ and _What Do You Care_.
  - Holocaust memory and psychology: Coster _We All Wore Stars_, Jamison _Night Falls Fast_.
  - Platform studies and contemporary criticism: Boellstorff & Soderman _Intellivision_, McCullough _How the Internet Happened_, Goldberg _Radical Play_, Packard _The Hidden Persuaders_, Kline _Out of the Garden_, Sutton-Smith _Toys As Culture_.
  - Reference and history: Roberts & Scher _Toys of the 50s, 60s and 70s_, Wulffson _Toys!_, Jaffe _The History of Toys_, Fletcher _Exploring the History of Childhood and Play_, Andersen _The LEGO Story_, Dennis & Laumann _Tonka_, Leffingwell, Palmer, Vanbogart, Pascal & Zarnock on Hot Wheels.
  - Safety and litigation: Swartz _Toys That Don't Care_ and _Toys That Kill_.
  - Outliers that signal the book's stance: Trump & Schwartz _Trump: The Art of the Deal_; A.C. Gilbert / McClintock _The Man Who Lives In Paradise_.

## About the Author

The bio is intentionally short. The voice can shift book-to-book; both observed forms are valid.

- DSR form (career arc, ~100 words): Open with the author's name in **bold small caps**: `**DOUGLAS W. ARCURI** resides …`. Geography → present role → prior career → off-hours practice. One oblique family reference at most.
- UTS form (grief-forward, ~70 words): Open with the same bold-small-caps name. Identity claim first (`is a researcher and citizen journalist`). Childhood-memory anchor. Loss disclosed and dated. Project framed as recovery work. Geography last.
- Either form: no book promotion in the bio. The book itself is the promotion.

## Appendices (UTS-confirmed device)

For a book that carries original investigative research too long for essay form, lettered appendices are the right venue.

- **Appendix A** — a standalone investigative monograph. UTS Appendix A runs ~18,000 words on Mattel Engineering Company / Papp engine / Jack Hartman's death. Footnoted to the same density as the main body or higher.
- **Appendix B** — a curated timeline or expanded reference. UTS Appendix B is "Memorable Moments in Future Toyland," extending Stern & Schoenhaus's 1990 timeline into 2025.
- **Appendix C** — the **public-records appendix**. UTS catalogs FOIA / CPRA returns and refusals chapter by chapter. Bureaucratic opacity becomes literary tension. Specific to investigative non-fiction; do not import into a software-book context.

Appendices are signed front-of-section with their own header (`Appendix A / On Mattel Engineering Company`). They carry their own internal section structure. They are not numbered chapters and they are not part of the Parts.

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

- 2026-05-02: Deep read of the published _Undercover Toy Stories_ manuscript (~9,800 lines, ~1,270 endnotes). Substantial corrections to earlier DSR-extrapolated speculation. Promoted into the body: the DSR-vs-UTS delta table; UTS Part / chapter-by-year structure; UTS book-quote epigraphs (replacing the DSR dictionary-form epigraph as a universal); UTS-formal register (no asterisked profanity, no `†` daggers, no `●●●` breaks); UTS Acknowledgments scope (~31 named individuals plus institutions); the UTS About-the-Author grief-forward variant; the Appendix A/B/C device, with Appendix A as a standalone investigative monograph and Appendix C as a public-records literary device; Suggested Future Volume as a series-anchor back-matter slot; UTS bibliography (~47 entries) added as confirmed toy canon. Specific items not yet promoted but worth keeping:
  - **"TIMELESS" bridging chapter** — between Part I (chronological survey) and Part II (deep investigation), one chapter named TIMELESS does the structural pivot. A bridging chapter is a useful pattern for any future sectioned book.
  - **Chronology-by-year naming.** UTS chapters use the year of the artifact or incident as the chapter title (`Ch. 1959`, `Ch. 1968`, `Ch. 2009`). This is an indexing decision: a reader who knows the year can find the chapter without knowing the topic. Worth considering for a future book whose subjects sit naturally on a timeline.
  - **Appendix C is unique to investigative non-fiction.** FOIA and CPRA responses (responsive and unresponsive both) are catalogued by chapter. Bureaucratic refusal as evidence is a UTS-original device.
  - **"Researcher and citizen journalist"** is the bio identity-claim that opens the UTS bio. Use the same identity-claim slot for any future investigative volume — it does work that "engineering manager" cannot.
  - **Praise page may be omitted entirely.** UTS does not include one. The DSR real-but-inverted device is portable but not mandatory; a strict-formal book can simply skip it.
  - **Foreword may be omitted entirely.** UTS does not have one. A peer Foreword is a DSR move; an investigative book can rely on its Preface and Introduction in the author's own voice.
  - **No Even More Praise back page in UTS.** That device is DSR-only.

- 2026-05-02: Spoke created from a deep read of _Deconstructive Software Ramblings_ (manuscript) and from forward-looking notes for the toy-history book (UTS) which is expected to share book-form conventions while inheriting the toy-context voice. The praise-page inversion, dictionary-form section epigraphs, dagger-vs-bracket citation split, ●●● break, small-caps openers, and the brevity discipline of "About the Author" are all DSR-confirmed and portable.
