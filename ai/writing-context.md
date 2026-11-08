# Writing Context — Hub

The base voice file. Read this first for any essay session. Route to a spoke based on subject.

## How to use this file (for AI collaborators)

1. Read this file end-to-end before drafting.
2. Determine the subject:
   - Software, engineering, career, tools, video games, developer culture → also load [software-context.md](software-context.md).
   - American toy industry, inventors, incidents, patents, toy companies, Undercover Toy Stories entries, and national-tragedy pieces anchored on a consumer artifact → also load [toy-context.md](toy-context.md).
   - Railroad history, regional or industrial history, on-the-ground incident archaeology that is neither software nor toy work → also load [history-context.md](history-context.md). A documented crime or a pair of crimes of the recent past, told from newspapers and court outcomes with an institutional argument (essay 114), routes here too, under the spoke's documented-crime variant; apply its sensitivity defaults for private citizens and child victims. An annotated-footage or archive walkthrough, where a primary-source film or photo set is presented as captioned frames with identifications (essay 115), routes here as well, under the spoke's visual-essay variant.
   - Physical-gear buying guides and hobby product reviews — optics, cameras, turntables, knives, pens, instruments, tools — where the reader is choosing what to purchase → also load [review-context.md](review-context.md). Software-tool reviews stay in the software spoke.
   - Mixed or unclear → load the applicable spokes; the dominant subject wins; note the blend to the author before drafting.
3. Determine the form:
   - Single essay (blog post, dev.to / Medium piece, social post) → subject spoke is sufficient.
   - Visual essay (a sequence of captioned frames carries the content; about 500 words of prose bookend it; essay 115) → subject spoke plus its visual-essay section. The image-count, paragraph-length, and "one image earns its place" rules below do not govern the gallery; the caption is the unit.
   - Book-shaped artifact (front matter, back matter, section epigraphs, anthology-level editorial choices, personal soliloquy passages between sections) → also load [book-context.md](book-context.md) on top of the subject spoke.
   - Auditing a typeset / published PDF for correctness (index page numbers, alphabetical order, endnote numbering, bibliography order, figure list) → also load [book-editing.md](book-editing.md) on top of the subject spoke. This is the production-side companion to the book spoke; the book exists, and the job is to find what is broken in it.
4. Load [writing-editing.md](../writing-editing.md) for the universal banned-word and filter list. It applies to everything.
5. **Toy essays only**: before drafting, ask the author for a per-essay quote file at `quotes/NNN-*.md` (where `NNN` is the numeric token of the essay file). See the Quote intake protocol in [toy-context.md](toy-context.md). Toy essays are quote-driven; do not draft without one.
6. **Review essays only**: before drafting, walk the author through the seven porting questions in [review-context.md](review-context.md) ("Porting the spoke to a new product category"). Review essays are ownership-driven; do not recommend a product the author has neither owned, handled, nor sourced a review for.
7. Draft. Then run the banned-word pass before returning.
8. After the author publishes or approves the essay, ask: "What did we learn about the voice from this piece?" Capture the answer in the Learning log of whichever file it refines.

## Who the author is, on the page

- A practitioner. Software engineer by day, toy-industry archivist by avocation.
- First-person singular is the default. Second person appears in how-to mode. "This author" appears in toy investigations as a deliberate distancing device.
- **Guest bylines exist.** A piece written by someone other than Douglas W. Arcuri carries an italic `*Written by [Full Name]*` line under the hero image and a `.my.md` file suffix. Essay 111 is the first. Guest pieces take the house structure, not the house voice; see the Guest-author protocol in [review-context.md](review-context.md).
- Opinionated without preaching. Observes, names, frames. Rarely prescribes without cause.
- Trusts the reader. No hand-holding, no fake universality, no virtue signaling.

## Universal voice

- Concrete nouns over abstract ones. Proper nouns over generic ones. Prefer "Kenner" to "the company", prefer "IntelliJ" to "the IDE".
- Active voice. Agents do things. "We decided" beats "it was decided".
- Short declaratives carry the weight. One longer orienting sentence per paragraph earns its length.
- Commit to statements. Hedges drain the prose.
- Em-dashes for pivot or aside. Parentheticals for intimacy, used sparingly.
- Repetition for rhythm is fine. Repetition for bulk is not.

## Universal rules (hard constraints)

- Follow [writing-editing.md](../writing-editing.md). The banned-word list is the single source of truth; do not duplicate it here.
- Screenreader pass before returning a draft.
- "And", "or", "of", "can", "-ly" filters applied.
- Escher-sentence and tautology scan.
- Active-voice flip pass.
- Prefer a proper noun to a vague pronoun where the reference is recoverable.
- **Titles may take a deliberate banned-word exception; body prose may not.** A banned word survives in a title when it carries the reader-facing promise of the piece and every correction reads as marketing (essay 111: "Without Spending a lot of Money"). The word stays on the list. Flag the exception to the author rather than granting it yourself.

## Length and shape

- Short: under 500 words. Medium: 500–1500. Long: 1500–3500. Very long: 3500+.
- Section headers serve pacing, not marketing. Short essays often use none. Long ones use hierarchy.
- One image earns its place only when it shows a thing prose cannot.
- **Visual essays measure in frames, not words.** 115 runs about 500 words of prose around 62 images and about 1,770 words of captions; the captions carry roughly three-quarters of the text. Budget the caption median (about 25 words) and the frame count (50–65), then the prose.

## Title conventions across the corpus

- Definitional: "What is a [Role] Anyway?"
- Imperative: "How to [Energetic Verb] Your [Object]"
- Observational: "The [Adjective] [Noun]"
- Provocation or allusion: "Reply All Considered Harmful", "Apps Doing Sh*t"
- Person-name title: "Tom Osborne on Kenner's M.A.S.K."
- Incident title: "A Tragic American Toy Story"
- Pair-incident title: "The Double Homicides of Ridgewood Children in 1964". Count word + crime noun + place + victims + year. The count word counts incidents, so define it in the first sentence.
- Hobby-entry guide: "How to Become a Knowledgeable [Category] Enthusiast Without [Constraint]"
- Trait title: "Having [Quality]". A gerund-participial phrase naming a human quality the reader either carries or lacks. No question mark, no role noun. Sibling to the definitional "What is a [Role] Anyway?" family.
- Year-prefix title: "2001: The Tale of an American Peter Rabbit". The year does the dating work so the subtitle can carry the anniversary or the angle. Mirrors the UTS chapter-by-year convention.
- Borrowed-title allusion: the essay's title rewrites the title of the artifact it is about (*The Tale of Peter Rabbit* → "The Tale of an American Peter Rabbit"). The inserted word carries the thesis.
- Index-and-artifact title: "FDNY Heroes: Critical Timestamps in the Naudet 9/11 Film". The people honored, a colon, then the indexing device (timestamps, frames, quotes) and the artifact it indexes. The title names the finding aid, and the subtitle carries the news hook ("A Raw Copy of the Documentary Was Released on YouTube"). Visual-essay form (115).
- Subtitle after the colon is welcome. One clause. No bombast.

## Routing table

| Signal | Route |
|---|---|
| Role definition, career advice, team practice | software |
| Trait or behavior definition ("Having [X]", a named human quality) | software |
| Tool review, language take, IDE or platform piece | software |
| Video game essay used to teach a systems idea | software |
| Developer culture, blog-scene commentary, HN/Medium/dev.to-adjacent | software |
| Toy artifact history, playset origin, product lifecycle | toy |
| Inventor portrait (deceased or living) | toy |
| Incident reconstruction, recall, injury, corporate cover-up (toy industry) | toy |
| Patent, trademark, or trade-press-rooted piece | toy |
| Undercover Toy Stories series entry | toy |
| Grief, memoir, or personal motivation of the archive project | toy |
| National tragedy or mass-casualty event witnessed through a consumer artifact (plush, book, doll) | toy |
| Braided anonymized-scene reconstruction built from testimony, biography, and patents | toy |
| Railroad history: derailment, wreck, line, era transition | history |
| Regional or small-town history: mill, mine, dam, textile lineage | history |
| Industrial infrastructure history (non-toy) | history |
| Incident reconstruction where the author walked the site | history |
| Documented crime or crime pair of the recent past, argued through institutional response (commitment, trial, sealed records, press) | history (documented-crime variant) |
| Pair-of-incidents essay that tests a shared outcome against contemporaneous counter-cases | history |
| Violent crime involving private citizens or child victims | history + sensitivity defaults (no scene of the act, no addresses) |
| Named-crewman or named-workman portrait (engineer, conductor, foreman) | history |
| Annotated primary-source film, footage, or photo archive: timestamped frames, identifications, quotes from a memoir | history (visual-essay variant) |
| Newly released or soon-to-vanish archival media, with the essay as the finding aid | history (visual-essay variant) + as-of stamp and archive link |
| Responders or other public-service figures identified in footage of a mass-casualty event | history + sensitivity defaults (name responders, never civilians) |
| Physical-gear buying guide: which model to buy, at what price, for what use | review |
| Hobby-entry guide: becoming knowledgeable in a gear category on a budget | review |
| Spec-literacy piece teaching a reader to read a product's numbers | review |
| Contrarian take against a hobby community's received wisdom on gear | review |
| Vintage or secondary-market guide for a collectible product category | review |
| Software tool, IDE, language, or developer-product review | software (structure E), **not** review |
| Toy or toy-adjacent collectible, treated as history rather than purchase advice | toy, **not** review |
| Front matter, back matter, section epigraphs, anthology editorial work | **+ book** (on top of subject spoke) |
| Personal soliloquy bridging essays in a collected volume | **+ book** |
| Praise / Even More Praise pages, About the Author, Acknowledgments | **+ book** |
| Index audit (page numbers, alphabetical order), endnote audit, bibliography audit on a typeset PDF | **+ book-editing** (on top of subject spoke) |
| Post-publish correctness sweep on a printed or print-ready manuscript | **+ book-editing** |

## Cross-domain bridge essays

Some essays sit between voices. They are allowed. Flag the blend at the top of the draft.

- Video-game-as-software-lesson (e.g., Secret of Mana, GoldenEye, River City Ransom): software voice dominates.
- Toy-as-career-reflection (hypothetical): toy voice dominates, but the author's first-person may surface.
- Toy-industry incident that is also a regional infrastructure event (e.g., a factory fire in a mill town): toy voice dominates; borrow the history spoke's site-archaeology move if the author walked the site.
- Railroad or regional-industry piece that touches a toy line (e.g., Hot Wheels Trains, Tomy Big Loader as industrial artifacts): history voice for the on-the-ground reporting; toy voice for the product history.
- Crime history with a legal or policy thesis (e.g., 114, maternal filicide and the commit-versus-try question): history voice dominates for place, newspapers, and "this author"; borrow the toy spoke's private-citizen anonymity discipline and the 112 numbered-footnote tail for sealed or contested records. No software or toy voice.
- Toy or consumer artifact as witness to a national tragedy (e.g., a Peter Rabbit plush aboard United 175): toy voice dominates for the artifact's provenance and IP history; the history spoke's site-and-object discipline supplies the reconstruction. The event is never the subject — the object is.
- Gear review that runs through the manufacturing history of the category (e.g., why Chinese porro-prism production improved): review voice dominates; borrow the history spoke's mechanism-explanation discipline for the technical passage.
- Hobby-as-career-reflection (e.g., a CQ-style piece where the gear is the vehicle for a mastery argument): software voice dominates, per essay 10; the review spoke supplies the gear vocabulary only.
- Visual essay on a mass-casualty event, built from released footage (e.g., 115, the Naudet film): history voice dominates for the banner, "this author", and the sourcing discipline. Borrow the toy spoke's displacement restraint from 112 (the act is never narrated; a flat fate line carries it) and 114's flat-declarative rule for violence. No reconstructed scene: the footage is the scene. The event is never the subject; the people identified in the frames are.

## Post-essay write-back protocol

After an essay is approved, the AI asks one of these, in order, then writes the answer into the correct Learning log:

1. Any new pattern worth adding (opening move, closing move, structural template)?
2. Any word or phrase to add to or remove from the banned list (proposed; author decides)?
3. Any sharper exemplar to replace a weaker one in a spoke?
4. Any voice miss that the author fixed in edits, so we can avoid it next time?

Promotion rule: once a pattern appears in the Learning log three times, promote it into the main sections of the relevant file.

## Learning log

<!-- Append dated bullets. Newest at top. Promote recurring patterns into the body above. -->

- 2026-11-08: Pattern study of essay 115 ("FDNY Heroes: Critical Timestamps in the Naudet 9/11 Film"). Routed to the history spoke by lane (`## ON AMERICAN HISTORY`, recent-past America, "this author", a named-people ethic), and the first **visual essay** in the corpus: 62 images (a hero plus 61 captioned film frames) and about 1,770 caption words against about 500 prose words. Analyzed as an untracked draft; the README already links the Medium post. Full anatomy, caption grammar, sensitivity rules, proofing results, and open items live in [history-context.md](history-context.md) ("Visual-essay variant (essay 115)" and its Learning log). Cross-spoke rules captured:
  - **In a visual essay the caption is the paragraph.** Each caption is a self-contained unit: linked timestamp, identification, one action, a fate or a quote, a page cite. Run the banned-word caps (`was`, `this`, `that`, `had`, one per paragraph) per caption, not per essay. 115 ran `was` ×27 across 62 captions, six of them with two or more, because the fate line ("was killed") demands a passive. Flip it: "died when the North Tower collapsed", "the collapse killed".
  - **The hyperlinked timecode is the citation.** A third hyperlink convention beside the toy/history verb-of-attribution and the review product name: the reader audits the claim by clicking `[m:ss](url&t=Ns)`. The label and the `t=` value must agree. In 115, 13 of 61 links drift 1–17 seconds from their label and one pair (1:45:36, 1:45:39) shares a `t=`. Derive one from the other mechanically; never type both.
  - **Foreknowledge is the narrative engine.** "Only Tardio and Pfeifer would survive." "Everybody in this huddle would be killed." The essay never narrates the dying; the reader knows what the people in the frame do not. Fate goes in one flat declarative with no adjectives, the 114 restraint carried into a new form. Portable to any archival walkthrough: the caption states what the frame cannot yet know.
  - **Name the responders, never the civilians.** Public-service figures in a documented event are named with rank, unit, and fate; civilians and the people who fell or jumped stay unnamed and undescribed. A sibling to the 112 anonymize-the-private-citizen rule, and the inverse of its reveal block: here the names are the point. Link each named line-of-duty death to a memorial page (115 does it once, for Halloran, out of about 35 names).
  - **Put a key before the gallery.** One paragraph says whose overlay or edit the viewer is seeing, what the page numbers cite (*Ordinary Heroes*), and who helped, with handles linked. Credit community contributors by name; here that is the pre911wtc1 clock overlay and @BrettClement-89.
  - **Two clocks need a one-sentence key.** 115's frames carry a burned-in wall clock (a third party's overlay) while the captions carry video runtime. Neither is explained. The offset is not constant (8:40:46 at 12:23, 8:42:45 at 1:45:39), which means about two minutes of the raw tape are cuts. The overlay is also approximate: the "Flight 175 impacts" frame reads 09:03:00.3, eleven seconds before the commonly cited 9:03:11, and the "Flight 11 impacts" frame reads 08:46:36.7 and shows the aftermath. Label the frame, not the event, or move the link to the sound.
  - **Essays about a vanishing artifact take an as-of stamp and an archive.** 115 lives only as long as one YouTube upload ("It likely won't last long"). Stamp the claim ("As of November 2026, the upload remained live"), capture the page and video with archive.org, and say plainly that the frames now outlive the source. Extends the 114 live-case rule from trials to media.
  - **Correcting the community record is a deliverable.** "Hurley is often misidentified as Ronald Horenor." For an identification piece, a sourced correction is the contribution; keep one per essay, say who is usually mistaken for whom, and cite the basis.
  - **One position in one sentence, then a concession.** "In this author's view, the source film should remain up out of respect for its historical impact" is the first stance on a publishing or legal question in the history spoke. Keep it to one sentence under "this author" and follow it with the downside ("copyright protections may eventually take everything down"). Do not argue fair use in the body; the title and the gallery are the argument.
  - **Caption proofing, second data point (114 was the first).** 115's typos sit almost entirely in captions: `enterance`, `Exteremly`, `injuried`, `communcations`, `Cheif` ×2, `enroute`, a missing period (`Lt Vincent`), an unclosed quotation mark (1:16:32), and a wrong referent (`Chief Orio`, which names Orio Palmer by his first name). A third occurrence promotes "read every caption aloud; run a find on every rank, surname, and unit" into the universal rules.
  - **Unit-in-parentheses placement is a referent rule.** "Capt. Dennis Tardio speaking to Pfeifer (Engine 7)" parses as Pfeifer's unit. Place the parenthetical immediately after the person it belongs to. Universal for any caption that identifies several people.
  - **Dashes in a history-lane piece stay spaced.** 115 mixes spaced (" - Capt. Patrick Brown") and unspaced ("impact-testing", "perspective-for young or old-to watch") hyphens as dashes. Pick the spoke's spaced hyphen; apply it everywhere.
  - **A post-gallery epilogue can carry the last fact.** 115 ends the prose on the FBI agents who took the tape and returned it weeks later, then on a call to watch, then on a viewer's comment as the coda. The author's voice steps back at the end; the crowd speaks last. Cite the FBI quotation by page.
- 2026-11-01: Pattern study of essay 114 ("The Double Homicides of Ridgewood Children in 1964"). Routed to the history spoke as its second exemplar and first documented-crime piece; the full analysis, transposition table, sensitivity defaults, and open-items list live in [history-context.md](history-context.md) ("Documented-crime variant (essay 114)" and its Learning log). Cross-spoke rules captured:
  - **Pair-incident essays: test the shared outcome against verified counter-cases.** Two incidents with one outcome look like a rule. List contemporaneous cases with the opposite outcome (name, year, state, sentence), each sourced; the pair becomes an exception and the exception carries the thesis. Portable to any spoke: two recalls, two derailments, two platform deprecations. A counter-case that cannot be sourced is cut, and a substitute whose outcome matches the pair's quietly reverses the test (114 after `a75a224`).
  - **Dual-subject essays saturate `both`.** 114 used `both` ten times in about 830 words (seven after the author's cuts), plus `was` ×12–13. The structure invites it. Name the pair, use "each", or split the sentence per subject; do not reach for the banned word as connective tissue.
  - **Live-case essays take an as-of stamp.** "Today, … ended in a mistrial on [date]" dates itself. Write "As of [month year]", hedge any forecast in the same sentence, and log a revisit. Applies equally to a software deprecation, a pending recall, or a trial.
  - **Captions are the leakiest proofing zone.** The author's `Corrections` commit on 114 fixed five typos, three of them in image captions (two possessives, one month name), and one surname that had drifted (`Hofmiester`). Run a find on every surname variant and read every caption aloud before publish.
  - **Banners can name a phenomenon, not only a lane.** `## ON MATERNAL PSYCHOSIS-RELATED CRIMES` (114) joins `## ON THE VICTIMS OF HISTORY` (112) and `## ON SCIENCE AND INDUSTRY` (105). Use a phenomenon banner for a case study of a recurring human condition; keep a lane banner when the place or industry is the subject.
  - **Sensitive subjects earn restraint by omission.** 114 drops the reconstructed scene, the address, the site photo, and the diagnosis, and spends its harshest vocabulary on the media rather than on the women. The toy spoke's private-citizen rule (anonymity in-scene) extends to the history spoke as a default; see the sensitivity list in the history spoke. Pending author confirmation that the omission was deliberate.
  - **A commit that says `Corrections` is a write-back signal.** When a post-draft commit touches only typos, log the class of error here (caption, surname, month) so the next draft front-loads the check.
  - **Source it or cut it; do not hedge it.** After the first analysis flagged unsourced counter-cases, the author's `Remove unverified trials` commit deleted them outright rather than softening them, consistent with "Commit to statements. Hedges drain the prose." A replacement that changes the argument forces a re-read of the header, the lead sentence, and the paragraph after it (114: the Young substitute was committed rather than tried and no longer fits "Did Not Set Precedent"). Detail in the history spoke's follow-up log entry.
  - **User-contributed pages are pointers.** A Find a Grave memorial can anchor a name and a date; pair it with a newspaper or court source for the claim.

- 2026-09-03: Pattern study of essay 113 ("Having Killer Instinct"). Software-spoke piece, and the first **trait definition** in the corpus: the "What is a … Anyway?" machinery pointed at a human quality instead of a job title. Cross-spoke rules captured:
  - **Private sources take a role noun and singular *they*; public sources take a name and a link.** 113 opens from a one-on-one — "my manager described a human trait" — and never names them. The reaction-extension family (102, 110) opens from a public post, names the author, and links it. Match the attribution to the source's exposure. A colleague who spoke in a private room is anonymized permanently, with no reveal block (the 112 anonymize-then-name move applies to reconstructions of documented events, not to workplace conversation).
  - **Defuse a loaded borrowed term in one sentence, immediately after defining it.** "While the term sounds aggressive, in management it denotes urgency, pragmatism, and accountability—not ruthlessness toward teammates." Definition-by-negation buys permission to use the term for the rest of the piece. Reach for it whenever the title word carries a connotation the essay does not intend (killer, ruthless, brutal, cheap, obsolete).
  - **Composite scenarios are the software spoke's primary-source substitute when the material is confidential.** Every spoke has an evidence move (toy = the patent scan, history = site archaeology, review = ownership disclosure, software = lived practice). When lived practice cannot be cited without exposing an employer or a coworker, 113 substitutes the invented composite case: a **Scenario** paragraph and an **Action** paragraph, generic enough to be no one and specific enough to be recognized. This is a software-spoke license only. Toy and history essays demand documented sources; never invent a scenario there.
  - **Reportorial frame when the idea came from above.** "From what I learned, killer instinct refers to …" keeps the narrator a student rather than an authority. Role definitions define from the author's own seat; borrowed-vocabulary essays report first, then extend. The humility is what stops a secondhand frame from reading as appropriation.
  - **Close on the sentence the archetype says, not on a summary.** 113 ends with the question a person with the trait asks out loud, in quotation marks, one word italicized for stress. Portable to any essay that has spent its body describing a kind of person.

- 2026-09-02: Pattern study of essay 112 ("2001: The Tale of an American Peter Rabbit"). Toy-spoke piece by routing, but it opens a new form in the corpus: the **braided scene mosaic**, where an artifact bears witness to a mass-casualty event. Sits beside essay 92 in method — reconstructed dialogue, patents as evidence, an object as the through-line — and departs from it in one decisive way: 92 names everyone in the scenes, 112 names no one until the reveal. Universal patterns captured, applicable to any spoke:
  - **Anonymize the scene, name in the reveal.** When the human subjects of a reconstruction are private citizens rather than public figures, run the scenes with role nouns ("a parent", "the child", "a person") and singular *they*, then hand the reader every name, age, and date in one italicized documentation block near the end. The reader inhabits the roles before learning whose they were. Named-figure reconstructions (92, 89, 93) keep names in-scene; private-citizen reconstructions do not.
  - **Epigraphs partition an essay, not only a book.** 112 runs four bold-italic epigraph blocks with an attribution line, spaced through the body as act breaks. Previously a book-spoke device; it is portable to a long essay whose sections are scenes rather than arguments. Form: `***Quote.***` newline `- Attributor, Source (Year), p. N.`
  - **Bracketed italic stage directions with sound design.** Each scene opens `[*Two parents thinking about their children, among scenes of reporters with the sound of light rain.*]`. Cues carry a sound bed (AM radio, an oud, birds, rain) and can close it (`[*Oud music fades.*]`). Radio-play scaffolding. Use when the essay is scene-driven and the narrator has stepped out.
  - **Motif chain replaces chronology as the spine.** 112's scenes jump 1893 → 1999 → 2001 → 2026 with no transitional prose. What binds them is recurring objects: rabbits, chrysanthemums, a September sky, lost shoes and jackets, gardens and warrens, aircraft overhead, overeating. When a braided essay stops working, the fix is a stronger motif, not a stronger transition.
  - **Displacement carries the atrocity.** The essay never depicts an impact, a collapse, or a death. It stops at "I'm going to hang up now." The violence lands later on a dead rabbit in a suburban backyard. For any subject that would be exploitative to render directly, displace the image onto a small object and let the reader complete it.
  - **Numbered footnotes as a blog-form tail.** Superscripts ¹–⁶ in the body, italicized notes after the closing media, each carrying a page number, an archive link, or a named denial. Reach for this instead of inline hyperlinks when the claims are contested, legally sensitive, or drawn from print sources with pagination. Inline links stay for the ordinary case.
  - **Dedication line, now confirmed as a signature (second instance after 105's `*- For Gene.*`).** 112 closes the body with `[For George. *Based on true stories.*]`. The bracket can carry a blanket reconstruction disclosure alongside the dedication. Promoting to the body of the toy spoke.
  - **`## AI Review` tail block.** 112 carries a mood-and-tone summary at the very bottom. Working scaffold for the author, not published matter. Leave it in the draft; strip it at publish time and confirm with the author.

- 2026-09-02: Added the review spoke ([review-context.md](review-context.md)) and routing rules, built from essay 111, the binocular buying guide. New class of writing: the deep product review in a niche hobby domain, where the reader has money in hand and the essay's job is to spend it well. Cross-spoke rules captured:
  - **Every spoke has a primary-source move, and they are not interchangeable.** Toy = the patent scan. History = site archaeology. Review = **ownership disclosure** ("I own a Flyant 12x25 that cost under $100"). Software = lived practice. Identify the spoke's evidence move before drafting; a piece without it reads as summary.
  - **The hyperlink attaches to different things in different spokes.** Toy and history wrap the **verb of attribution** because the link proves a claim. Review wraps the **product name** because the reader is meant to click and buy. Do not carry one convention into the other.
  - **"This author" is spoke-specific, not corpus-wide.** It is the toy and history distancing device. Review voice is first-person singular and unhedged; the value of the piece is a named person putting their taste on the line.
  - **A constraint named in the title is a structural obligation.** 111's "Without Spending a lot of Money" is enforced as "under $100" in six separate sections. Whenever a title makes a promise (a price, a timebox, a word count), honor it visibly in the body rather than once at the top. Author ruled on the banned-word collision here: "a lot" stays on the list, and the 111 title keeps it as a rare exception, because the colloquialism is the promise.
  - **First guest-authored piece in the corpus.** Bylined `*Written by Douglas J. Arcuri*`, saved as `.my.md`. Guest pieces take the house structure but keep the guest's diction; run the banned-word pass and propose the cuts as a list rather than rewriting silently. Mechanical fixes (title case, unit spacing, en-dash ranges, stray zero-width characters) are unilateral.
  - **Review essays need a pre-draft intake, same as toy essays need a quote file.** Seven questions in the review spoke: price ceiling, doctrinal fork, false luxury, the one calculation, use cases, what the author owns, the traps.

- 2026-07-18: Pattern study of essay 110 ("Ways People Respond to Problems"). Second data point in the **reaction / extension of a public artifact** family (first was 102). Cross-spoke rule captured for future work regardless of subject:
  - **When replying to a numbered / enumerated external artifact, extend its numbering rather than start a rival list.** The tribute-plus-participation posture wins over the corrective posture on the open web. Applies equally to a toy-industry checklist, a railroad-history taxonomy, or a software listicle. Detail in [software-context.md](software-context.md) Learning log (2026-07-18).
  - **Reaction essays stay short.** Body under ~250 words when the essay is an extension of someone else's public post. If the reply grows past that, it is a standalone piece that happens to cite the source, not an extension.
  - **Title mirrors the source's title, minus the count.** "Three ways people respond to a problem" → "Ways People Respond to Problems". Signals family relationship without copying.

- 2026-07-13: Added the history spoke ([history-context.md](history-context.md)) and routing rules. Loaded when the subject is railroad history, regional or industrial history, or on-the-ground incident archaeology that is neither software nor toy work. Baseline exemplar: essay 109, the Chestuee Creek L&N derailment of 1959. The history spoke inherits the toy spoke's investigative discipline (imagined-dialogue protocol, mechanism-must-be-verified rule, mosaic sourcing, "this author" as the investigative first-person) but has its own signatures: place-first ALL CAPS BOLD opener, italicized-bracket reconstructed opening scene, site archaeology as the primary-source move, dollar-figure corporate response, dedication line as final body element, YouTube coda in place of a book promo block, and a subject-tuned hashtag set. No UTS scaffolding on history-spoke essays.

- 2026-06-06: Delta from essay 107 author edits — universal close-and-pivot patterns.
  - **Self-deprecation by personal admission, not by asterisked profanity.** Reflective essays close warmer when the narrator quietly admits to *being* the thing the essay just named ("And that was me, last week."). The asterisked `Sh*t.` / `Sigh.` / `Yikes.` sign-off is rant register, not reflection register. Match the close to the temperature of the body. If the essay observes more than it gripes, the personal admission lands; if the essay gripes more than it observes, the asterisk lands.
  - **Soften meta-frame pivots.** A drafted close that says "Except that is not what the 5x manager actually is" reads as the writer reaching into the frame to break it for the reader. Published 107 replaced it with "Perhaps not always." — the same pivot, but the reader is trusted to feel the turn. Cut "Except", "But really", "The truth is" when introducing a frame-break; substitute a one-line concession ("Perhaps not always.", "Maybe.", "Not quite.") and let the next paragraph do the work.
  - **Compare-contrast structure does its own rhythm.** When the essay's spine is explicit A vs. B comparison (paragraph bolded with `**They [verb]**` clauses), prefer comparative joiners ("while", "whereas") inside each paragraph instead of staccato two-sentence chops. The bolded sentence-openers already supply the cadence; doubling it with chopped clauses reads as a drum machine. Save staccato for moments that need emphasis (the last beat, the close).
  - **Coined-frame essay close: escalate, don't collapse.** When the essay coins a frame and then complicates it, tee up the *next* tier of the same frame instead of rejecting the frame. "Perhaps there are 10x managers out there, after all" is recursive escalation; "the five attributes aren't really the point" is frame-collapse. Recursion lets the coinage survive the joke; collapse kills the coinage on the way out.

- 2026-05-30: Delta from essay 106 author edits — universal patterns.
  - **Paragraph length cap for Medium-bound essays: 3–4 sentences.** Internet readers scan; a 5–6-sentence block reads as a wall. Long quote-bearing paragraphs are the worst offender — when the quote runs long, keep narrator sentences short, and break to a new paragraph after the quote rather than continuing in the same block. Captured in detail in [toy-context.md](toy-context.md).
  - **Brief in-line product / artifact descriptors on first mention.** A 4–10-word appositive whenever a brand, toy, or product is named, even when the reader is assumed to know it. "Madballs, grotesque, squishy balls that children threw at each other" beats "Madballs". Trust the reader's recognition; don't trust the reader's memory of the *thing*. Universal — applies to software essays too (a tool, a framework, an IDE feature).
  - **Find the hidden thesis before drafting the close.** The public reason for an outcome (boycott, layoff, cancellation, deprecation) is rarely the real reason. Doctrine, parent-company values, internal politics, and culture clashes usually are. Pre-draft prompt: "What is the underlying-values thesis under the public narrative?" Toy-spoke captures the canonical 106 example (Kenner vs. Hasbro on SMB).

- 2026-05-17: Added the book-editing spoke ([book-editing.md](book-editing.md)) and routing rules. Loaded when the work is a correctness sweep on a typeset PDF (index audit, endnote numbering, bibliography order, figure list). The drafting spoke ([book-context.md](book-context.md)) covers *how the book is built*; the editing spoke covers *how to find what is broken once it exists*. Driven by the UTS post-publish-edits-9.pdf index audit session.
- 2026-05-12: Delta from essay 105 author edits — universal rules refined.
  - **Short sentences need subject-verb-object completeness.** The banned-word list pushes toward fragments. Author rejected noun-only fragments ("A Mattel executive.", "A magazine sat at his fingertips." was kept, but standalone "Richard Feynman stood at his elbow." was kept while "A Mattel executive." was struck). Rule: rhythm-short is fine; nominalized-short is not. Short declarative sentences must have a verb of their own; do not lean on the preceding sentence to complete the thought.
  - **Date stacking inside a paragraph.** When two or more dated events appear in the same paragraph, the first event gets the calendar date; subsequent events use relative intervals ("Four months later", "Two months after that"). Reads faster, reduces month-name repetition, and lets the rhythm of the paragraph carry the chronology.
  - **Once a hedge has framed a claim, don't reinforce it in the next sentence.** Drop the second framing sentence. The reader takes the hedge on the first pass.
- 2026-05-08: Drafting note from essay 105 (toy-spoke piece, but the universal filters did the heavy lifting). Awaiting author review.
  - **Banned-word filters apply to narration, not quoted material.** A quote-driven essay accumulates banned words inside its quotes that the narrator cannot edit out. The filter pass should treat the narrator's prose as the editable surface and leave the quote text alone. The cap on `was` / `had` / `this` / `that` / `can` / `would` per paragraph still binds; the remediation is to flip narrator passives to active in advance, not to disturb the quote.
  - **Active-voice flip pass should run before the banned-word pass on quote-heavy essays.** Sequence matters. Flipping passives early frees up cap budget per paragraph for unavoidable quoted instances of `was` / `had`.
- 2026-05-02: Added the book spoke ([book-context.md](book-context.md)) and routing rules. Loaded only when the work is a book-shaped artifact (front/back matter, section epigraphs, soliloquy passages); blog essays continue to use only the subject spoke. Driven by the deep read of _Deconstructive Software Ramblings_ and forward-looking needs for the toy book.
- 2026-04-23: Initial hub created from corpus analysis of essays 01–101.
