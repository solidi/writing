# History Context — Spoke

Voice guide for American history essays that are neither software nor toy-industry work. Covers regional incidents, industrial infrastructure, railroading, mining, mills, small-town lore, and the physical archaeology of recent-past America. Read [ai/writing-context.md](writing-context.md) first. Baseline exemplar: [109-the-chestuee-creek-l-n-derailment-of-1959.md](../109-the-chestuee-creek-l-n-derailment-of-1959.md). Second exemplar, documented-crime variant: [114-the-double-homicides-of-ridgewood-children-in-1964.md](../114-the-double-homicides-of-ridgewood-children-in-1964.md); see "Documented-crime variant (essay 114)" below for what transposes from 109 and what does not.

## When to load this file

- Railroad history: derailments, wrecks, hot-box incidents, line construction, company mergers, era transitions (steam → diesel, journal boxes → roller bearings).
- Regional or small-town history: mills, mines, dams, water towers, migrant labor, textiles, industrial rise and fade.
- Recent-past-America incident reconstruction that is **not** a toy story: an accident, a fire, a flood, a shooting, a labor dispute, a natural-resource spill.
- Physical archaeology: the author visits the site of a historical event and reports what remains on the ground.
- Named-crew or named-workman portraits (an engineer, a conductor, a foreman, a millwright).
- Cold War and mid-century industrial context when the primary subject is infrastructure, not toys or aerospace.
- Documented-crime history: a crime, or a pair of crimes, of the recent past reconstructed from newspapers and court outcomes, where the argument concerns how institutions responded (commitment versus trial, sealed records, press coverage). Maternal filicide, homicide clusters, and similar subjects that involve private citizens. Essay 114 is the exemplar.

If the subject touches the toy industry (Mattel aerospace adjacencies, Kenner incidents, inventor deaths), route to toy. If the subject is a cross-domain science-and-industry piece, promote the banner to `## ON SCIENCE AND INDUSTRY` and load toy on top. History-only work stays here.

## Voice

- Reverent-investigative, same lineage as the toy spoke, but tuned to **place** rather than **product**. The town, the creek, the mill, the line — these carry the through-line, not a corporate lineage.
- Regional storyteller register. The narrator sounds like someone who has stood on the ground, walked the rails, and talked to the property owner. That standing is the source of authority.
- Reverence for the working man. Named crewmen (engineer, fireman, brakeman, conductor, flagman) are treated with the same care the toy spoke reserves for named inventors. The fall of a laborer is reported factually and briefly, if at all; the body of the essay celebrates their work.
- Light Americana inflection is allowed. Biblical or folk phrasing lands in this register in a way it does not in software: "God was on their side that morning", "Ask, and it will be given to you". Use once or twice per essay, never as a running device.
- Skeptical toward corporate narratives, official records, and Interstate Commerce Commission silences. The absence of a federal report is itself a fact worth naming.
- "This author" is the preferred first-person form for investigative and interpretive moments, same as the toy spoke — three to six times per medium-length piece.

## Document anatomy (canonical layout)

Baseline is essay 109. Treat as the default skeleton; deviate with cause.

1. **Category banner** as a top-of-file H2: `## ON RAILROAD HISTORY` (or `## ON REGIONAL HISTORY`, `## ON INDUSTRIAL HISTORY`, `## ON AMERICAN HISTORY` — banner tracks the subject lane). A case study of a recurring human condition takes a **phenomenon banner** instead of a lane banner: `## ON MATERNAL PSYCHOSIS-RELATED CRIMES` (114), sibling to `## ON THE VICTIMS OF HISTORY` (112).
2. **Title** as H1. Incident-and-date title is the default: "The Chestuee Creek L&N Derailment of 1959".
3. **Subtitle** as H2 directly under the title — one declarative line that names the second-order consequence: "When Coal Spilled Into a Small Tennessee River, Convincing the Company to Invest In Roller Bearings". The subtitle is where the corporate-response thesis lives.
4. **Hero image** with a descriptive caption that carries a fact (publication, date, page number, restoration note). `images/NNN-01.jpeg`. AI-enhanced archival images are allowed; disclose in the caption ("The image was enhanced with AI").
5. **Opening reconstructed scene** — italicized bracket-tag stage direction, then a short dramatized scene with named crew and dialogue. See "Opening reconstructed scene" below.
6. **Horizontal rule** (`---`).
7. **Section 1 — Place and period.** The town, the creek, the mill, the era. **ALL CAPS BOLD lead phrase** of three to six words: `**ENGLEWOOD, TENNESSEE, IS**`. Etymology, founding, industry, migrant labor, the piece of infrastructure the essay hinges on.
8. **Section 2 — The incident.** Date, crew, cargo, mechanism of failure, immediate aftermath. Narrative-title section header (e.g., "The Incredible Derailment"). ALL CAPS BOLD opener.
9. **Section 3 — Cleanup or immediate response.** Duration, scale, disposal, official investigations (or the notable absence of one). ALL CAPS BOLD opener.
10. **Section 4 — Cause and mechanism.** The industrial or mechanical explanation. Diagram or Wikipedia figure welcome. Named suspicion (hobos, sabotage, wear) with hedging. ALL CAPS BOLD opener.
11. **Section 5 — Legacy and fade.** Corporate response (a capital purchase, a policy change, a fleet upgrade), the company's later dissolution, the town's current state, the visible remains today. ALL CAPS BOLD opener.
12. **Dedication line** as the final body element: `*- For [FirstName].*` — italicized, em-dash, first name only. Optional but characteristic.
13. **Horizontal rule.**
14. **Closing visual coda** — a YouTube embed, a period photograph, or an author site photo, with a one-sentence caption that names the coda's payoff. `![The black and yellow CSX logo is proudly displayed …](youtube-url)`.
15. **Horizontal rule.**
16. **Social Post block** — `## Social Post`, a two-to-three-sentence tee-up naming the crewman, the cargo, and the failure, one framing sentence, the hashtag set, then the Medium URL. Hashtag set is subject-specific: `#history #railroad #america #railfanning` for rail; `#history #mining #appalachia` for a mining piece; adjust the last tag to the regional/hobbyist community that will actually share the post.

There is **no book promo block**. History-spoke essays do not currently roll into an anthology and should not carry UTS scaffolding.

**Which anatomy items are incident-lane-specific.** Items 5 (reconstructed scene), 7–11 (place → incident → cleanup → mechanism → legacy), 12 (dedication), and 14 (video coda) belong to the railroad and industrial incident lane. Essay 114 kept items 1–4, the ALL CAPS BOLD openers, and the Social Post expectation, and replaced the rest; see "Documented-crime variant (essay 114)".

Image rhythm inside the body: 8–12 images per essay, one image per 2–4 paragraphs. Mix of archival (newspapers.com clippings, museum photos, period ads), reference (Wikipedia diagrams, patent figures if applicable, Google Maps screenshots for site location), and **author-taken contemporary photos of the site** (see "Site archaeology" below). Captions carry a parenthetical source: `(Source: [Chattanooga Daily Times](url))`, `(Source: Amberg Museum)`, `(Source: [Google Maps](url))`, `(Source: Author)`.

## Opening reconstructed scene — the signature move

The essay opens on the incident, dramatized, before the historical narration begins. Rules:

1. **Italicized bracket-tag stage direction** as the first line of body prose, framing time, weather, and motion: `[*With dawn breaking over the horizon, a freight train is hauling heavy through the forest.*]`. Square brackets around an italicized present-tense sentence.
2. **Named crew, dialogued in first person.** The engineer, fireman, brakeman, conductor are given lines. If a name is on the historical record (109: John Payne), use it. If not, name the role only ("said the fireman", "said the conductor").
3. **Sensory detail earns the scene:** soot on faces, glow of fire on the trucks, the sound of crashing metal, the howls of coyotes and rasping of katydids after the wreck settles. The reader should hear and smell the moment.
4. **Cut the scene before the historical section starts.** End on the moment of the incident's aftermath (settled sounds, crew reactions) or on a witnessed detail (falling into the creek). Then `---`, then the ALL CAPS BOLD historical opener.
5. **Same evidentiary discipline as toy-spoke imagined dialogue** — see [toy-context.md](toy-context.md) "Imagined dialogue — the protocol". The scene is a reconstruction grounded in the historical record: the crew count, the cargo, the location, the type of failure, the outcome must all trace to sources. Scene-setting (weather, gestures, specific words) may be imagined; claims of intent or foreknowledge must trace to a source. Disclose the reconstruction if the piece runs long or if the subject warrants it ("Reconstructed from newspaper accounts and the L&N investigation").

Not every history essay opens this way. A company-history or place-history piece may open with the town instead. But the reconstructed scene is the default for an incident piece and should be considered first.

## Site archaeology — the on-the-ground move

The distinguishing move of the history spoke is that the author walks the site and reports what remains. This is the equivalent of the toy spoke's patent scan: the primary-source move that anchors the essay's authority.

- **Access disclosure.** Name that the author was permitted access, or that the visit happened during a drought that revealed the creek bed, or that property lines limited the exploration. The reader learns immediately that the author was physically there.
- **Inventory the artifacts.** Coal shoals, rail ties, forged spikes, J-hooks, axles, gondola frames, journal boxes with doors missing. Count them, describe them, name their material state (fused to vegetation, half-buried, stored in a shed).
- **Photograph them.** Author-taken images earn `(Source: Author)` in the caption. Two to four site photos per essay is typical.
- **Report the property owner's role.** If a landowner told a story ("stored the supply of coal to coax stubborn campfires as he told tales of the crash"), quote or paraphrase it. This is where the regional oral tradition enters the piece.
- **Hedge what full exploration could not confirm.** "Full exploration could not take place due to property lines" is a clean way to close the archaeology beat and pivot to the documentary record.

## Documented-crime variant (essay 114)

Second history-spoke exemplar: "The Double Homicides of Ridgewood Children in 1964" (about 830 body words, three newspaper-front-page images, two inline links). Same lane as 109 — recent-past America, anchored to a place, built on newspapers, narrated by "this author". The subject is a crime and the argument is institutional: why two Queens mothers were committed rather than tried, whether that set a rule, and what changed by 2001 and 2023. Roughly half of 109's incident-lane machinery transposes.

### How 109's moves transpose

| 109 (incident lane) | 114 (documented-crime variant) |
|---|---|
| Italic bracket-tag reconstructed scene with named crew | **Absent.** A bold-caps thesis lead on the facts opens the essay, with no scene and no stage direction. The only dialogue is one sourced post-act line per principal: "Call a neighbor, I've broken my wrists." / "Oh, my God, I've shot myself." |
| Site archaeology, author photos | **Archive archaeology.** Front pages from a digitized local weekly (*Ridgewood Times* on Calameo) stand in for the site. Caption carries month, year, and a linked source. No address, no visit. |
| Mechanism with diagram | **Legal-institutional mechanism.** Court-appointed doctors find the defendant psychotic and unfit to stand trial; commitment replaces prosecution; the files are sealed. Named in 114, never cited (see open items). |
| Corporate response, dollar figure | **Institutional response and outcome.** Commitment of "various lengths", a misdemeanor Sullivan Act charge against the husband, a death year (2007). |
| Legacy and fade | **Precedent test, modern contrast, trend thesis.** Three sections; see below. |
| Dedication, video coda | None. |
| Social Post block | Owed. 114 carries the hashtag line under the subtitle and no `## Social Post` tail as committed. |

### Argument pattern: pair, outcome, precedent test, modern contrast, trend

1. **The pair.** Two incidents in chronological order, one image and one quote each, in one unheaded opening block. Two cases that share an outcome look like a rule.
2. **Outcomes.** What happened to the people afterward, with the absence of a record named as a fact ("Both cases have files under permanent seal and will never see the light of day." — the same move as 109's missing ICC report).
3. **The precedent test.** List contemporaneous counter-cases with name, year, state, and sentence (Maggie Young, 1955, Georgia; Dorothy Mae Stephens, 1958, California; both life sentences). The pair is then an exception, and the exception carries the thesis. The test ports to any two-incident essay: two derailments, two mill fires, two dam failures.
4. **Place as legal climate.** The state replaces the creek and the mill as the through-line. Name the state beside every comparison case, then rank the climates: New York and Massachusetts as compassionate, Georgia, pre-liberalization California, and Texas as harsh. The explanation takes the "this author suspects" hedge in the same sentence.
5. **Modern contrast.** Andrea Yates (2001) and Lindsay Clancy (2023) show the same crime under today's coverage, with one image.
6. **Trend thesis.** A short closing section whose header is a prediction ("Trial-and-Error Cases Will Persist") and whose two paragraphs name the causes: deinstitutionalization and media voyeurism.

### Headers in the variant

Headers are **claims**, five or six words, verb-bearing: "Ridgewood Murders Did Not Set Precedent", "Trial-and-Error Cases Will Persist". Use them when the section argues. Keep 109's adjective-plus-noun narrative headers when the section narrates. The outcomes header ("Outcomes of These Maternal Filicide Cases") is a plain noun phrase. The opening block has no header, as in a short essay.

### Voice and restraint

- **"Mrs." plus surname** after a first full-name mention, for every woman in the essay across both eras (Hofmeister, Calia, Young, Stephens, Yates, Clancy). The honorific keeps a flat, period-correct distance. Full names return at the head of a section or when a case is introduced.
- **Violence in one or two flat declaratives, no adjectives.** The toilet-brush and gunshot sentences carry the weight without modifiers. The harsh vocabulary ("horrific media spectacles", "media voyeurism", "grossly polarized") is aimed at the coverage, not at the women. Moral targeting is part of the voice: the media is the accused, the mothers are the case.
- **One quote per principal, unremarked.** Each mother's first words after the act concern her own injury ("I've broken my wrists", "I've shot myself"). The essay lets the asymmetry stand. Hold that restraint.
- **Clinical language is attributed, never supplied.** "Found by court-appointed doctors to be actively psychotic and suicidal." Do not add a diagnosis (postpartum, bipolar) that no source states, even when the circumstances invite one.
- **One-sentence paragraph as the absence beat.** The sealed-files line stands alone. Use it for the single fact the record refuses to give.
- **Spaced hyphen as the rendered dash** (" - "), as in 109. The one software piece to close the dash up is 113 ("accountability—not ruthlessness"); history and toy essays keep the spaced form.

### Sensitivity defaults for crimes involving private citizens and children

Observed in 114, aligned with the toy spoke's private-citizen rule ([toy-context.md](toy-context.md), "Imagined dialogue", rule 5). Treat as defaults until the author states otherwise.

- **No reconstructed scene of the act.** The bracket-tag opener is suspended; 109's imagined-dialogue protocol does not extend to a parent harming a child. Sourced quotes only.
- **No addresses and no site visit.** The family and surviving relatives may be living; the archive image is the evidence.
- **Child victims are not named in the 1964 cases; survivors are named by role** ("her young boy, 10 months old"). Naming is inconsistent in 114 (a modern victim, Callan, is named). Pick one rule per essay: unnamed throughout, or named only where wide public coverage already did and consistently so.
- **Do not turn silence in the record into a life story.** "Believed to have lived full lives" and "did not commit further crimes" outrun what the records state. Prefer "records show" with a cited source, or "no further record."
- **Stamp live cases with an as-of date.** "Today, Lindsay Clancy's first trial ended in a mistrial on September 4, 2026" goes stale. Write "As of [month year]" and log the revisit.
- **Forecasts on a live case take the hedge in-sentence and a revisit note.** 114's closing prediction ("this author expects that either outcome will end in *not guilty by reason of insanity*") is acceptable only with the framing and a scheduled recheck.

### Sourcing in the variant

- Digitized local weeklies (Calameo-hosted archives) replace newspapers.com as the primary source. Link the image caption.
- National dailies named in prose without a link (*The New York Times*, AP) are a gap. Link the verb of attribution to the specific article.
- For legally sensitive or print-sourced claims — sealed files, a death year, a misdemeanor charge, the sentences in the counter-cases — use the numbered-footnote tail from essay 112 ([writing-context.md](writing-context.md), 2026-09-02 log) rather than a bare assertion.
- Reference density in 114 is two links in 830 words against the spoke's 10–20 per medium essay. A brief can run lighter, but every named counter-case and every sealed-record claim needs a source.

### Length

Brief tier: 700–1200 words. 114 sits here. The incident lane's 1200-word floor does not apply to a case-pair brief.

## Sources

History essays lean heavier on newspapers.com and local community records than the toy spoke leans on trade press, but the shape is the same: mosaic-triangulation, cited inline.

- **Newspapers, primary evidence.** newspapers.com clippings are the workhorse. Cite the publication (italicized) and hyperlink the verb: `the *Knoxville News-Sentinel* [wrote](https://www.newspapers.com/image/…), "Quote."` Pattern matches the toy spoke.
- **Local town records.** The town's official website ("townofenglewood.com/history"), the local historical society, county museums.
- **Community history on social platforms.** Regional Facebook pages (Tennessee Overhill), regional history blogs (Resin Car Works), local YouTubers. Cite them as sources; they carry the oral tradition.
- **Federal records and their absence.** Interstate Commerce Commission report searches, NTSB / FRA archives, USGS maps, census data. When a federal report is missing, name that fact and speculate on why ("likely because no one was hurt and property damage was minimal").
- **Reference.** Wikipedia is allowed as a diagram source and a technical-mechanism reference — link to the specific article (`[hot box](https://en.wikipedia.org/wiki/Hot_box_(rail))`), not to a general topic. Google Maps for site location. Museum photographs for period equipment.
- **YouTube coda.** The essay's closing image is often a YouTube embed from a regional railfan or documentarian (Rob Wild for 109). One-sentence caption names what the video shows and why it earns the tail slot.

Citations appear inline as hyperlinks in blog form. No formal bibliography. Reference density: 10–20 distinct sources per medium-length history essay.

## Mechanism explanation — verify, don't guess

When a mechanical failure is the pivot of the essay, the mechanism must be described correctly or hedged. Same rule as the toy spoke.

- Cite the technical reference (Wikipedia, patent, engineering manual, period trade paper).
- Include a diagram if one is available. Journal box diagrams, boiler cutaways, gondola figures, roller-bearing exploded views.
- Name the part in the caption ("A journal box is seen in the lower right hand of the diagram.").
- Explain the failure in one clean paragraph: what the part does, what went wrong, why the design was later replaced. The 109 hot-box → roller-bearing transition is the canonical example.
- Corporate-response thesis lives at the end of this section: the failure drove a capital investment ($33M in roller bearings for L&N, ~$380M in today's dollars). Naming the dollar figure and its present-day equivalent is a hallmark move.

## Sentence and paragraph rhythm

- Short declaratives to establish, longer periodic sentences when the technical explanation is being laid out. Same as toy spoke.
- Fragments allowed at moments of tension inside the reconstructed scene ("Hot box, HOT BOX!"). Rare in the narrative sections.
- Paragraph length cap for Medium-bound essays: 3–4 sentences (per the universal 2026-05-30 rule).
- Mid-essay orienting sentences mark pivots ("What is not negligible is the number of lasting artifacts of the incident.", "God was on their side that morning …").

## Titles

- **Incident-and-date** is the default: "The Chestuee Creek L&N Derailment of 1959".
- **Corporate-response subtitle**: "When Coal Spilled Into a Small Tennessee River, Convincing the Company to Invest In Roller Bearings". The subtitle names the second-order consequence, not the incident itself.
- **Place-and-object** for a company or infrastructure piece: "The Louisville & Nashville Steam Fleet of the 1950s" (hypothetical).
- **Named-crewman** for a laborer portrait: "John Payne, L&N Engineer" (hypothetical).
- Subtitle after a colon is the norm. One clause. No bombast.
- **Place-victims-year** for a documented-crime pair: "The Double Homicides of Ridgewood Children in 1964" (114). A count word ("Double") counts **incidents**, not victims; 114's own tally implies more child deaths than two, so define the count in the first sentence ("A RARE DOUBLE-TRAGEDY occurred …") and keep the title a headline, not a body count.
- **"When …" subtitle.** 109 and 114 both open the subtitle with "When". 109's names the second-order consequence; 114's ("When Two Mothers Murdered Their Kids Months Apart") restates the first-order incident and leaves the consequence to the section headers. Prefer the 109 form: the subtitle is where the thesis lives. A candidate for 114: "When Two Mothers Murdered Their Kids Months Apart, New York Chose Commitment Over Trial".
- **Hashtag line under the subtitle** (`#crime, #murder, #america, #newyork, #history` in 114; `#CurrentEvents, #History, …` in 105). Comma-separated, directly beneath the H2, before the hero image. Investigative-lane pieces carry it; the `## Social Post` set below stays space-separated.

## Diction and signature vocabulary

- **Rail-specific nouns without apology:** journal box, wadding, hot box, gondola, box car, coal car, hopper, boxcar, tender, cab, truck, axle, roller bearing, J-hook, rail tie, spike, ballast, embankment, right-of-way, siding, wye, division, subdivision, freight, consist, hostler, hostling, deadhead.
- **Rail crew roles:** engineer, fireman, brakeman, conductor, flagman, dispatcher, tower operator, section hand.
- **Period phrasing:** hobo, jungle fire, migrant worker, Depression-era, post-war, Cold War, dieselization, roller-bearing conversion.
- **Regional and folk phrasing:** "hauling heavy", "the rails are going up", "hot box, HOT BOX!", "God was on their side", "Ask, and it will be given to you". Used sparingly; earns the piece's regional authority.
- **Investigative phrasing:** "This author suspects", "It's not known", "No documented evidence proves", "hedged speculation", "no report was filed" — same discipline as the toy spoke.
- **Reverent framings for a regional event:** "this legend of the [X]", "the incredible derailment", "the coal spill". The word "legend" is earned when the event has passed into oral tradition; do not use it for a well-documented federal-report incident.

## POV and tense

- **Reconstructed scene:** present tense in the bracket-tag stage direction, past tense in the narrative dialogue itself.
- **Historical narration:** past tense, third-person.
- **Site archaeology:** past tense for the visit; present tense allowed for what still exists on the ground ("Half the truck was forever fused to vegetation, as a square journal box port is visible without its door.").
- **Corporate-response and legacy sections:** past tense; conditional or subjunctive for speculation.
- **"This author"** in interpretive and evidentiary moments, same as toy spoke.

## Length and shape

- Short: 1200–2000 words.
- Medium: 2000–3500 (109 sits here).
- Long: 3500–6000 for a multi-incident investigation or a company history piece.
- Brief: 700–1200 for a documented-crime case pair (114, about 830 body words). Medium in the hub's tier table, below the incident lane's Short floor.
- Section headers are narrative and short — "The Incredible Derailment", "The Rushed Clean Up", "A Hot Box Derailment", "A Legacy of Textiles and Rails". Three to six words. Adjective + noun is the most common shape. Argument sections in the crime variant take claim headers instead.

## Do

- Walk the site if you can. Report what remains.
- Name the crew. Name the town. Name the creek. Name the equipment.
- Cite the newspapers, the local historical societies, the community pages.
- Explain the mechanism. Include a diagram.
- Name the corporate response and price-tag it in present-day dollars.
- Signal speculation plainly and in the same sentence as the claim.
- Close with a dedication if the essay is owed to a person who guided the research or the visit.
- Test a pair of incidents against contemporaneous counter-cases before calling the shared outcome a pattern (documented-crime variant).
- Name the state beside every comparison case; jurisdiction is the place.
- Close every history essay with a `## Social Post` block, including the crime variant.
## Don't

- Don't apply UTS scaffolding (book promo block, "researcher and citizen journalist" bio claim, Undercover Toy Stories cross-references) to a history-spoke essay. Different corpus.
- Don't invent a federal report. Naming the absence is fine; fabricating a citation is not.
- Don't romanticize labor conditions or the hobo economy. Regional lore is welcome; sentimental gloss is not.
- Don't lean on the reconstructed opening scene for facts the historical record does not support. The scene dramatizes the record; it does not replace it.
- Don't drop the mechanism explanation. A history-spoke incident essay without a technical pivot reads as a newspaper rewrite. In the crime variant the mechanism is legal-institutional (the competency finding, the commitment, the seal); name it and cite the statute or the rule of the period. Verify the statute before naming it; do not guess a section number.
- Don't dramatize a violent act against a child, and don't supply a diagnosis the sources do not state.
- Don't publish a home address or a site photo for a private-citizen crime.
- Don't claim "the only" or "the first" in American history without a hedge or a source. 114's "the only incidents in American history to occur in the same city, in the same year, with similar outcomes" is an unprovable superlative.

## Learning log

<!-- Append dated bullets. Newest at top. Promote recurring patterns into the body above. -->

- 2026-11-01: Pattern study of essay 114 ("The Double Homicides of Ridgewood Children in 1964"), the second history-spoke essay and the first documented-crime piece. Analyzed at commit `a513194` ("Corrections"). Routes to history by lane (recent-past America, place-anchored, newspaper-sourced, "this author"); it opens the **documented-crime variant** documented above. Answers the 2026-07-13 question of which 109 patterns generalize:
  - **Generalized (promote candidates, one data point each beyond 109):** ALL CAPS BOLD lead phrase on every section opener (`**A RARE DOUBLE-TRAGEDY**`, `**BOTH OF THESE**`, `**DURING THE 1960s,**`, `**THE HOFMEISTER AND CALIA**`); "When …" subtitle; "this author" for interpretation and forecast (twice in about 830 words, so proportionally on pace); archival image captions with a parenthetical linked source; naming the absence of a record (sealed files); no UTS scaffolding; spaced-hyphen dash.
  - **109-specific (did not carry):** the reconstructed opening scene, site archaeology, mechanism-with-diagram, the dollar-figure corporate response, the dedication, the video coda, adjective-plus-noun headers, 8–12 images, 10–20 sources. The variant section above records each replacement.
  - **New moves:** the precedent test (counter-cases that turn a shared outcome into an exception), place as legal climate, claim-bearing headers, phenomenon banner, "Mrs." plus surname across eras, harsh vocabulary aimed at the media rather than the subjects, one unremarked quote per principal, attributed-not-supplied clinical language.
  - **Banned-word scan of the committed text (narrator prose, about 830 words):** `both` ×10, `was` ×12, `this` ×7, `that` ×7, `actively` ×3, `later` ×3, `Unfortunately` ×1, `finally`, `immediately`, `only`, `once`, `had`, `now`. Two consecutive paragraphs open with "Today,". The dual-subject structure drives `both`: any two-case essay saturates it. Remedy: name the pair ("Mrs. Hofmeister and Mrs. Calia"), use "each", or split the sentence per woman. Paragraphs run one to four sentences with one exception, the Young/Stephens block, which runs five across a soft line break (a missing blank line).
  - **Author's corrections (`a513194`): five fixes, three in image captions.** Two possessives (`Hofmeisters` → `Hofmeister's`, `Calia` → `Calia's`) and one month (`Janurary` → `January`) landed in captions; the other two were body spellings (`catasphories`, and `Hofmiester` drifting from `Hofmeister`). Rule: captions are the leakiest zone; search every surname variant and every caption possessive before publish.
  - **Open items for the author (not edited; the analysis only recorded them):**
    - Structure: no hero image under the subtitle (the first image falls after paragraph four); no `---` before "Trial-and-Error Cases Will Persist"; no `## Social Post` tail; subtitle states the incident instead of the consequence.
    - Facts to verify: Ridgewood is a neighborhood in the borough of Queens, not a borough; Andrea Yates was found not guilty by reason of insanity at her 2006 retrial rather than "accepting" a verdict; the sentences and states for Maggie Young (1955) and Dorothy Mae Stephens (1958) need a source; "Records show" the 2007 death year needs a source; the Sullivan Act misdemeanor needs a source; the superlative "the only incidents in American history …" needs a hedge or a source.
    - Sourcing: two inline links in the whole essay; the third caption (*The Boston Globe*) is unlinked; *The New York Times* and AP coverage is named without a link. Candidate for the 112 numbered-footnote tail.
    - Consistency: Callan is the one child victim named; the 1964 children are not. "Lived full lives" and "did not commit further crimes" outrun the cited record.
    - Time-sensitive: the Clancy mistrial date (September 4, 2026) and the closing forecast of a not-guilty-by-reason-of-insanity outcome; stamp as-of and recheck before republishing.
    - Thesis support: "trial-and-error" in the final header is evidenced only by Yates's overturned conviction and Clancy's mistrial, and the closing section never connects them. The legal mechanism (competency finding, commitment, sealed files) is named but not cited.
  - **Pending write-back questions for the author** (per the hub's protocol): Was dropping the reconstructed scene a deliberate rule for child-victim subjects? Is the "Mrs." honorific deliberate? Should the phenomenon-banner family (105, 112, 114) continue? Which sharper exemplar, if any, should replace 114 as the crime-variant baseline?

- 2026-07-13: Spoke created from essay 109, the Chestuee Creek L&N derailment. Baseline patterns captured: place-first ALL CAPS BOLD opener, italicized-bracket reconstructed opening scene with named crew, site archaeology as the primary-source move, mechanism explanation with diagram and dollar-figure corporate response, dedication line as final body element, YouTube coda in place of the toy-spoke book promo block. Awaiting a second history-spoke essay to test which patterns generalize and which are 109-specific.
