# Writing Context — Hub

The base voice file. Read this first for any essay session. Route to a spoke based on subject.

## How to use this file (for AI collaborators)

1. Read this file end-to-end before drafting.
2. Determine the subject:
   - Software, engineering, career, tools, video games, developer culture → also load [software-context.md](software-context.md).
   - American toy industry, inventors, incidents, patents, toy companies, Undercover Toy Stories entries → also load [toy-context.md](toy-context.md).
   - Mixed or unclear → load both; the dominant subject wins; note the blend to the author before drafting.
3. Determine the form:
   - Single essay (blog post, dev.to / Medium piece, social post) → subject spoke is sufficient.
   - Book-shaped artifact (front matter, back matter, section epigraphs, anthology-level editorial choices, personal soliloquy passages between sections) → also load [book-context.md](book-context.md) on top of the subject spoke.
   - Auditing a typeset / published PDF for correctness (index page numbers, alphabetical order, endnote numbering, bibliography order, figure list) → also load [book-editing.md](book-editing.md) on top of the subject spoke. This is the production-side companion to the book spoke; the book exists, and the job is to find what is broken in it.
4. Load [writing-editing.md](../writing-editing.md) for the universal banned-word and filter list. It applies to everything.
5. **Toy essays only**: before drafting, ask the author for a per-essay quote file at `quotes/NNN-*.md` (where `NNN` is the numeric token of the essay file). See the Quote intake protocol in [toy-context.md](toy-context.md). Toy essays are quote-driven; do not draft without one.
6. Draft. Then run the banned-word pass before returning.
7. After the author publishes or approves the essay, ask: "What did we learn about the voice from this piece?" Capture the answer in the Learning log of whichever file it refines.

## Who the author is, on the page

- A practitioner. Software engineer by day, toy-industry archivist by avocation.
- First-person singular is the default. Second person appears in how-to mode. "This author" appears in toy investigations as a deliberate distancing device.
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

## Length and shape

- Short: under 500 words. Medium: 500–1500. Long: 1500–3500. Very long: 3500+.
- Section headers serve pacing, not marketing. Short essays often use none. Long ones use hierarchy.
- One image earns its place only when it shows a thing prose cannot.

## Title conventions across the corpus

- Definitional: "What is a [Role] Anyway?"
- Imperative: "How to [Energetic Verb] Your [Object]"
- Observational: "The [Adjective] [Noun]"
- Provocation or allusion: "Reply All Considered Harmful", "Apps Doing Sh*t"
- Person-name title: "Tom Osborne on Kenner's M.A.S.K."
- Incident title: "A Tragic American Toy Story"
- Subtitle after the colon is welcome. One clause. No bombast.

## Routing table

| Signal | Route |
|---|---|
| Role definition, career advice, team practice | software |
| Tool review, language take, IDE or platform piece | software |
| Video game essay used to teach a systems idea | software |
| Developer culture, blog-scene commentary, HN/Medium/dev.to-adjacent | software |
| Toy artifact history, playset origin, product lifecycle | toy |
| Inventor portrait (deceased or living) | toy |
| Incident reconstruction, recall, injury, corporate cover-up | toy |
| Patent, trademark, or trade-press-rooted piece | toy |
| Undercover Toy Stories series entry | toy |
| Grief, memoir, or personal motivation of the archive project | toy |
| Front matter, back matter, section epigraphs, anthology editorial work | **+ book** (on top of subject spoke) |
| Personal soliloquy bridging essays in a collected volume | **+ book** |
| Praise / Even More Praise pages, About the Author, Acknowledgments | **+ book** |
| Index audit (page numbers, alphabetical order), endnote audit, bibliography audit on a typeset PDF | **+ book-editing** (on top of subject spoke) |
| Post-publish correctness sweep on a printed or print-ready manuscript | **+ book-editing** |

## Cross-domain bridge essays

Some essays sit between voices. They are allowed. Flag the blend at the top of the draft.

- Video-game-as-software-lesson (e.g., Secret of Mana, GoldenEye, River City Ransom): software voice dominates.
- Toy-as-career-reflection (hypothetical): toy voice dominates, but the author's first-person may surface.

## Post-essay write-back protocol

After an essay is approved, the AI asks one of these, in order, then writes the answer into the correct Learning log:

1. Any new pattern worth adding (opening move, closing move, structural template)?
2. Any word or phrase to add to or remove from the banned list (proposed; author decides)?
3. Any sharper exemplar to replace a weaker one in a spoke?
4. Any voice miss that the author fixed in edits, so we can avoid it next time?

Promotion rule: once a pattern appears in the Learning log three times, promote it into the main sections of the relevant file.

## Learning log

<!-- Append dated bullets. Newest at top. Promote recurring patterns into the body above. -->

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
