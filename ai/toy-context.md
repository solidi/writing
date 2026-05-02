# Toy Context — Spoke

Voice guide for American toy industry essays. Covers the register seen across essays 69–101 and the Undercover Toy Stories framing files. Read [ai/writing-context.md](writing-context.md) first.

## When to load this file

- Artifact history of a playset, toy line, or single product.
- Inventor portrait — living or deceased.
- Incident reconstruction: injury, recall, death, litigation, cover-up.
- Company history: Mattel, Kenner, Tomy, Tonka, Fisher-Price, Galoob, Hasbro, Ideal, Marvin Glass & Associates, and their adjacents.
- Patent, trademark, trade-press-anchored piece.
- Interview or testimony-format essay.
- Anything explicitly framed as an Undercover Toy Stories entry.

## Series frame: Undercover Toy Stories

- Personal origin of the project: the author's mother died in July 2023; a PTSD diagnosis followed in November 2023. The series began as grief processing and matured into a public archive.
- Scope: American toy innovation, mid-20th through late-20th century, with adjacent side paths (Tomy/Japan, Theo & Ora/Israel).
- Thesis: toys are serious engineering and intellectual property. They are Cold War artifacts, business-history wildcards, and records of individual genius too often forgotten.
- Reader contract: technical accuracy where possible, speculation labeled as such, the reader trusted to weigh evidence.
- Volume One of the anthology published in 2025. New essays continue the volume.

## Voice

- Reverent-investigative hybrid. Reverent toward inventors and engineers. Skeptical toward authorities, corporate PR, and official narratives.
- Archivist-custodian stance. The work is to surface the record before institutional amnesia erases it.
- "This author" is the preferred first-person form in investigative and interpretive moments. It distances the narrator from ego and anchors the claim to the essay's evidence. Use it sparingly — five to eight times per long piece is typical.
- Third-person historical narration is the default bed. First-person dialogue appears inside reconstructed scenes. Second person appears rarely, in a direct address to the reader at a closing turn.
- The lead engineer or inventor is treated reverently as the through-line of the essay, even when their later life turns tragic, criminal, or sad. The fall is reported factually and briefly, with hedged language. The body of the essay celebrates what they built. Exemplar: 104 Neil Tilbor — the criminal record is one paragraph at the close; the rest of the essay is his work.

## Document anatomy (canonical layout for an artifact or inventor essay)

Observed consistently in 104 and recurring across the corpus. Treat as the default skeleton; deviate with cause.

1. **Category banner** as a top-of-file H2: `## ON TOY HISTORY` (or the relevant subseries banner).
2. **Title** as H1.
3. **Subtitle** as H2 directly under the title — one declarative line that frames the angle.
4. **Hero image** with a descriptive caption that smuggles in a fact. `images/NNN-01.jpeg`.
5. **Horizontal rule** (`---`).
6. **Section 1 — Company or context intro**, narrative title (e.g., "Tyco of Mount Laurel, Land of Vehicled Toys"), opening with an **ALL CAPS BOLD lead phrase** of three to six words: `**TYCO TOYS, INC. OPERATED** out of …`. Establishes company, place, era, and the lead engineer.
7. **Section 2 — The artifact's launch / what and how.** Patent provenance, mechanism, license origin, named designers. ALL CAPS BOLD opener.
8. **Section 3 — Reception and conflict.** Press, controversy, rebrand, recall, network refusals, NHTSA-style oversight. ALL CAPS BOLD opener.
9. **Section 4 — What was mechanically or culturally special.** The piece of industrial archaeology worth preserving. Cross-references to sibling toy lines in the series. ALL CAPS BOLD opener.
10. **Section 5 — Legacy, fade, and the human coda.** Acquisition, retirement, collector market, the lead engineer's later life. ALL CAPS BOLD opener.
11. **Horizontal rule.**
12. **Book promo block** — image of the *Undercover Toy Stories* cover with the standard italicized blurb and Amazon links.
13. **Horizontal rule.**
14. **Closing iconic image** — packaging shot or beauty image, captioned.
15. **Horizontal rule.**
16. **Social Post block** — `## Social Post`, a pulled quote or essay sentence, a one-line tee-up, and the hashtag set: `#history #toys #[brand] #nostalgia #[parent company]`.

Image rhythm inside the body: 8–14 images per essay, one image per 2–4 paragraphs. Captions are sentence-form with a parenthetical source: `(Source: [The Grand Rapids Press](url), J. Hamilton)` or `(Source: [Patent](https://patents.google.com/...))`. Patent drawings, period advertisements, newspaper photos, and YouTube/commercial GIFs are all valid.

Section titles are narrative, not generic. "Critical Reception and Media Sideswipe" beats "Reception". "Mechanically Special, a Racing Champion" beats "What Was Special". The title should hint at the section's beat in three to six words.

## Quote-driven prose — the signature move

Toy essays are built on direct quotation. Nearly every paragraph carries a quoted source, or the paragraph that follows does. This is the move that distinguishes the toy register from the software register.

- **Density target:** 12–25 attributed quotes per medium-length toy essay. 25–40 for a long inventor portrait.
- **Sources allowed:** newspapers (newspapers.com clippings), trade press (*Playthings*, *Toy & Hobby World*, *ToyFare*), national press (*Newsweek*, *LA Times*, *Daily News*), patent text, court filings, podcasts (*Ridiculous History*), YouTube reviewer channels (*Articulated Points*, *Nostalgia Nerd*, *Keepers of Nerdom*, *Down From the Attic*, *Cinemassacre*, *Ode2Toy*), TikTok reviewers, named industry figures.
- **Attribution grammar — the verb is the anchor.** The hyperlink wraps the verb of attribution, not the source name. The source name is named in plain prose, italicized when it is a publication.
  - Pattern A: `*The San Francisco Chronicle* [wrote](url), "Quote."`
  - Pattern B: `Nancy Blair of *Courier-Post* [teased](url), "Quote," said [Tyco spokesperson] Bruce Maguire.`
  - Pattern C: `YouTuber Zach R. [said](url), "Quote."`
  - Pattern D: `Tilbor [told](url) *The Star*, "Quote."`
- **Verb variety:** said, wrote, noted, told, lamented, replied, teased, recalled, observed, reported, continued, added. Rotate to keep the rhythm alive.
- **Bracketed editorial inserts** are welcome inside the quote when context is needed: `"[Neil Tilbor will] concentrate on the launch …"`. Square brackets signal the insertion is the author's, not the source's.
- **Ellipses** signal a cut: `". . ."` with spaces, three dots, used to stitch a long quote down to its useful core.
- **A quote is the close of a section more often than not.** The narrator hands the microphone to the source for the punchline.

## Quote intake protocol — `quotes.md`

For any new toy essay, the AI should ask the author up front: "Doug, can you provide a `quotes.md` so I can write this essay?" The author maintains a running working file at the workspace root in a known format.

Format observed in the workspace `quotes.md`:

- Bolded section headers group quotes by topic: `**Tyco**`, `**About the Toy**`, `**Controversy with Toy Pattern and Profit**`, `**Patents**`, `**Trademarks**`, `**Toys**`, `**[Inventor name] (Business)**`, `**[Inventor name] (Crimes)**`, `**Legacy**`.
- Each quote is a checkbox bullet: `- [ ]` unused, `- [x] ~~strikethrough~~` used.
- Each quote line carries: the source (as an inline markdown link), the verb of attribution, and the quoted text in straight or smart quotes.
- Patent and trademark links live in their own bolded sections.
- Photo and toy reference URLs live alongside the quotes.

AI workflow with `quotes.md`:

1. Read `quotes.md` first; treat the unchecked items as the available quote pool.
2. Build the essay outline so each section is anchored by 3–6 quotes drawn from the pool.
3. In the draft, mark which `quotes.md` line each citation came from so the author can strike it through after publication.
4. If a section needs a quote and none in `quotes.md` fits, propose what kind of quote is missing and ask the author to source it. Do not invent.
5. After the draft, return a list of quotes from `quotes.md` that did not make the cut, so the author can decide whether to weave them in or save them.

## Patent and trademark scan — research step

Before drafting, scan for:

- **Toy-line patents** at Google Patents and USPTO. Note patent number, title, filer, assignee, filing and grant dates. Patents reveal the lead inventor of record, which is often not the public face of the line. Exemplar: Neil Tilbor surfaced as the named inventor on the Crash Dummies playset patent (US5397260A) and on Total Control Racing (US4247108A), Fast Traxx (US5135427A), Hi-Jacker (US5322469A), Scorcher (US5429543A) — that paper trail anchored the entire 104 essay.
- **Trademark filings** at USPTO TSDR. Note application date, registrant, status. The trademark filing date is the cleanest anchor for the public launch year.
- **Adjacent patents** the inventor filed for prior or later companies. They draw the inventor's career arc (Tilbor: Ideal → Tyco → Team Edge / Taiyo Edge).
- Cite patents inline as `[creating](https://patents.google.com/patent/US4247108A/en)` or in image captions as `(Source: [Patent](https://patents.google.com/patent/US5397260A/en))`.

## Mechanical claims — verify, don't guess

If a toy's mechanism is described, the description must be correct or hedged. The 104 draft missed this: the Crash Dummies are triggered by a button on the front, not a lever at the back. Verify mechanism through one of: a patent figure, a video review, a period advertisement, or the author's own hands-on memory. If none of those is available, hedge: "a release mechanism", "a triggered detachment", and ask the author.

## Cross-linking inside the series

When referencing a sibling toy essay in the body of a toy essay, link to the **published Medium URL**, not the local workspace path. Pattern observed in 104: links to *Jack Ryan and Ruth Handler*, *Hot Wheels Trains and Planes*, and *Micro Machines* all point to medium.com/@solidi/. Use [README.md](../README.md) as the canonical map of essay → published URL. Local-file links in this directory are reserved for the AI's own routing notes.

## Tone markers

- Informational and factual. Dates, patent numbers, measurements, locations. Specific.
- Reverent when naming inventors: "legend", "genius", "hero" appears, but earned by the evidence in the paragraph that contains it.
- Investigative and prosecutorial when the subject is tragedy or cover-up. Questions are posed; evidence is lined up; counter-theories are proposed; hedges are placed.
- Humane under the data. Marriages, rivalries, royalties stiffed, grief — the human layer sits underneath every patent number.

## Imagined dialogue — the hard rule

Dialogue with deceased figures is a signature move of this series. It must obey this protocol:

1. The figure is deceased or otherwise unavailable, **or** the dialogue is reconstructed from documented testimony (interview tape, congressional record, court transcript).
2. Every line is grounded in a cited fact, quotation, or on-record attribution. No invented beliefs, no invented confessions.
3. The dialogue is framed explicitly. Use one of these framings near the scene:
   - "This author imagined dialogues based on collective historical facts."
   - "Reconstructed from [source]."
   - "Based on congressional testimony, police reports, and facts."
   - "Reader discretion is advised."
4. Scene-setting details (room, weather, gesture) may be imagined when they do not alter the factual record. Claims of belief, intent, or motive must trace to a source.
5. Never pass an imagined quote as a direct on-record quote. Formatting and framing must keep the distinction visible to the reader.

Exemplars: 89 (Marvin Glass with Bob Wallace, WBBM 1972), 92 (Jack Ryan and Elliot Handler on TWA), 93 (Florio and Horowitz in D.C., plus the pre-shooting scene), 98 (Steiner brothers in 1946 Cincinnati), 100 (Tom Osborne Q&A).

## Canonical structures

### A. Inventor portrait
Birth or origin → industry migration (often aerospace or industrial design to toys) → specific contributions with patent numbers → moral or tragic reckoning → legacy.
Examples: 81 Jack Hartman, 89 Marvin Glass, 100 Tom Osborne, 101 Jack Ryan.

### B. Incident reconstruction
Scene-setting with date and place → witnesses → official narrative → author's counter-theory → systemic failure analysis → the reader-decides close.
Examples: 77 the 1968 parking-lot explosion, 88 Sky Dancers recall, 91 Jack's Injustice, 93 the laser-tag shooting.

### C. Artifact autobiography
Five-section flow, each section opened with an ALL CAPS BOLD phrase:
1. Company-of-origin and lead engineer introduced together.
2. Launch — patent provenance, mechanism, license, named designers.
3. Reception and conflict — press, controversy, rebrand, recall.
4. Mechanically or culturally special — the industrial-archaeology argument; sibling-line cross-links.
5. Legacy, fade, and the human coda — acquisition, retirement, the engineer's later life.
Examples: 69 Hot Wheels Sto & Go, 78 Tomy Big Loader, 79 Fisher-Price Action Garage, 82 Mighty Tonka, 95 Screwball Scramble, 96 Micro Machines, 104 Crash Dummies.

### D. Company history
Founder biography → corporate milestones → key product lines → market position → crisis or transformation.
Examples: 82 Tonka, 98 Kenner origin through M.A.S.K., 101 Mattel Engineering Company.

### E. Interview / testimony
Framed as a Q&A or reconstructed exchange. The subject's voice dominates. The narrator introduces and closes.
Examples: 89 Bob Wallace and Marvin Glass, 100 Tom Osborne.

## Opening moves

- Scene-set with date and place in small caps or bracket tags: "EARLY DECEMBER 1972, …" (89); "[August 11, 1988, Washington, D.C.] …" (93).
- Historical-zeitgeist anchor: "It's November 1968, and America is about to circle the moon with men for the first time." (91)
- Cold hook into a review or product claim: a TikTok reviewer, a patent drawing, an advertisement.
- Section-header-as-opener rhetorical question: "How Could the Engine Explosion be Declared an Accident?" (91)
- Once-upon-a-time framing for a company origin: "ONCE UPON A TIME, there was a young corporation called Mattel." (92)

## Closing moves

- Legacy landing: "Screwball Scramble … is an enduring analog legacy." (95)
- Reader-decides close: "The reader will have to decide for themselves…" (101)
- Institutional-silence critique: "Little public records are left in this case. This author believes police reports of this case are misfiled." (91)
- Human-connection close: "To this author, all three are American heroes." (92)
- Forward-looking note on a living project or a coming book (101).

## Sentence and paragraph rhythm

- Short declaratives to establish. Longer periodic sentences when the evidence is being laid out.
- Fragments are allowed at moments of tension ("Bang!") and are used sparingly.
- Paragraph length follows the rhythm of evidence: short during dialogue, long during investigation.
- Mid-essay orienting sentences mark pivots ("Now, here are the troubling conclusions inferred from the media documents." 91).

## Sourcing and references

Toy essays are rooted in books and archives first, with internet sources as complements. Reference density is high: 15–25 distinct sources per essay, 30+ for investigative pieces.

- Books (examples seen in the corpus): *Barbie and Ruth* by Robin Gerber; *Toy Monster* by Jerry Oppenheimer; *Forever Barbie* by M.G. Lord; *Barbieland* by Tarpley Hitt; *Toyland: The High-Stakes Game of the Toy Industry*; *Back to the Drawing Board: The Art of Kenner Toy Design* by Tim Effler; *Micro but Many* by Tim Smith; *From Workshop to Toy Store*; *Inside Public Relations*; *The Toys That Made Us* companion volumes.
- Patents: USPTO and Google Patents. Cite number, filer, date.
- Named people: inventors, executives, testifying officials, witnesses. Names land with titles and dates.
- Trade press and newspapers: *San Francisco Examiner*, *Los Angeles Times*, *Cincinnati Enquirer*, *USA Today*, *New York Times*, *Gardena Valley News*, *Design News*, *ToyFare*, *Private Pilot*.
- Archival: FOIA returns, California Secretary of State filings, Board of Contract Appeals opinions, microfilm, newspapers.com.
- Internet complements: YouTube (Vsauce, RetroDaze, collector channels), Reddit, TikTok reviewers, LinkedIn profiles, collector podcasts.
- Citations appear inline and as hyperlinks. No formal bibliography. Footnote-style numerics appear occasionally (101).

## Factual posture

- Hedging language, used deliberately: "This author suggests / theorizes / speculates / believes", "It's unknown whether", "No documented evidence proves", "as this author suspects".
- The boundary is explicit: facts presented as facts (patent numbers, dates, locations, named people), speculation labeled in the sentence that carries it.
- When the record is empty, say so and say what is missing.

## Named-entity roster (recurring across the corpus)

Companies: Mattel, Kenner, Tomy / TakaraTomy, Tonka, Fisher-Price, Galoob, Hasbro, Ideal, Parker Brothers, Coleco, Marvin Glass & Associates, Northrop, North American Aviation, Raytheon, Caltech, NASA/JPL.

People who recur: Jack Ryan, Ruth Handler, Elliot Handler, Jack Hartman, Marvin Glass, Eddy Goldfarb, Bernie Loomis, Tom Osborne, Howard Bollinger, Lewis Galoob, Makoto Saito, John Gentile, Richard Feynman.

## Diction and signature vocabulary

- "This author" — third-person narrator-as-investigator.
- "Mosaic theory of information" — epistemology for fragmented records.
- "Institutional amnesia" — the enemy the archive fights.
- "Plastic poetry", "engineering marvels", "toy bros", "fortress of invention", "preliminary design", "moonshot".
- Technical nouns without apology: patent, prototype, playset, spring-loaded mechanism, ball-in-maze puzzle, dexterity game, motorized, wind-up, battery-operated, licensing agreement, trademark.
- Era-specific phrasing: Cold War, post-war, missile gap, Mickey Mouse Club era, Baby Boomer, safety recall, lead paint, asbestos.

## POV and tense

- Third-person historical narration dominates.
- "This author" appears in investigative and interpretive passages.
- Reconstructed dialogue uses first person inside the scene.
- Past tense for history. Present tense for artifact description and contemporary-interview framing. Conditional or subjunctive for speculation.

## Length and shape

- Short toy essays: 1500–2500 words.
- Medium: 3000–4500.
- Long: 5000–7500 for inventor portraits, investigations, and company histories.
- Section headers are narrative (date + place), thematic, investigative ("Actions Pointing Toward Collusion"), product-focused, or biographical.
- Images: 8–12 per essay, sourced from patents, period advertisements, historical photographs, and reviewer screenshots. Captions include patent numbers, dates, or source attribution.

## Titles

- "The [Company / Designer] [Adjective] [Object]": "The Great Marvin Glass: Artists in a Fortress of Invention" (89).
- "The [Adjective] [Noun]": "A Tragic American Toy Story" (77), "The Ultimate Hot Wheels Legend" (80).
- Person-name titles: "Jack Ryan and Ruth Handler of Mattel: The Power Ballad of American Coffee" (92); "Tom Osborne on Kenner's M.A.S.K." (100).
- Incident titles: "How the Orange Tip Became a Standard-Issued Toy Accessory" (93).
- Investigative-query format: "Does Evidence Link…?" (80).
- Subtitle after a colon is the norm. It frames the angle.

## Do

- Name the inventor, the patent, the date, the company, the city.
- Cite the book, the trade paper, the FOIA return, the court record.
- Let the human layer sit under the data: marriages, rivalries, grief, obsession.
- Signal speculation plainly and in the same sentence as the claim.
- Treat dialogue reconstruction as a craft with rules (see the hard rule above).
- Preserve the mosaic: multiple sources triangulated into one paragraph.

## Don't

- Don't write cozy nostalgia. This series is not a collector's Instagram caption.
- Don't sensationalize a real death or injury. Let the facts indict.
- Don't dismiss toys as children's entertainment. They are intellectual property and industrial history.
- Don't invent a quote and pass it as recorded.
- Don't let the author's personal memoir leak into individual essays. Memoir belongs in the series framing files.
- Don't use academic jargon or theoretical scaffolding that the facts do not require.
- Don't binary-simplify the inventors. Complexity is the point.
- Don't stack banned words; see [writing-editing.md](../writing-editing.md).

## Exemplar pieces to imitate

- Inventor portrait: 81, 89, 101.
- Incident reconstruction: 77, 88, 91, 93.
- Artifact autobiography: 69, 78, 79, 95, 96, 104.
- Company history: 82, 98, 101.
- Interview/testimony: 89, 100.
- Quote-driven artifact + inventor combo: 104 (canonical layout exemplar).
- Series framing: [xx-undercover-toy-stories-preface.md](../xx-undercover-toy-stories-preface.md), [87-undercover-toy-stories-introduction.md](../87-undercover-toy-stories-introduction.md), [x-undercover-toy-stories-afterword.md](../x-undercover-toy-stories-afterword.md), [83-future-book-technical-toy-stories.md](../83-future-book-technical-toy-stories.md).

## Learning log

<!-- Append dated bullets. Newest at top. Promote recurring patterns into the body above. -->

- 2026-04-30: Calibration pass against essay 104 (Tyco Incredible Crash Dummies) and the workspace `quotes.md`. Promoted into the body: full Document anatomy section, Quote-driven prose section, Quote intake protocol, Patent and trademark scan, Mechanical claims rule, Cross-linking grammar, lead-engineer-as-through-line voice rule, five-section flow for Artifact Autobiography. Specific gaps from the 104 draft that triggered each promotion:
  - Missed the ALL CAPS BOLD section opener phrase pattern.
  - Missed the narrative-style section titles.
  - Quote density was far too low; the original draft used three quotes total against the published version's ~20.
  - Attribution grammar wrapped link on source name; should wrap on the verb.
  - Missed the hero image, image rhythm, and book-promo footer.
  - Missed the Social Post pull-quote block.
  - Missed Neil Tilbor as the through-line; treated him as a footnote.
  - Got the toy mechanism wrong ("lever at the back" — actually a front button). Need to verify mechanism via patent, ad, or video.
  - Did not scan patents for the lead inventor of record. Patent search would have surfaced Tilbor up front.
  - Cross-links to sibling essays should point to the published Medium URLs (per README), not local files.
  - The plot beat "Crash Dummies → Incredible Crash Dummies after the 1992 NHTSA / Ad Council falling-out" was missed entirely; rebrands and license disputes are a load-bearing reception-section beat for any licensed-property toy.
  - The author's note: "My toy essays are special because they highly draw on public quoting of how the toys came to be." Quote-driven prose is the signature, not a flavor.
- 2026-04-23: Initial spoke created from corpus analysis of essays 69–101 and the Undercover Toy Stories framing files.
