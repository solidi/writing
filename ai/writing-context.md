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
4. Load [writing-editing.md](../writing-editing.md) for the universal banned-word and filter list. It applies to everything.
5. **Toy essays only**: before drafting, ask the author for a `quotes.md` (workspace-root file) to seed the quote pool. See the Quote intake protocol in [toy-context.md](toy-context.md). Toy essays are quote-driven; do not draft without one.
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

- 2026-05-02: Added the book spoke ([ai/book-context.md](ai/book-context.md)) and routing rules. Loaded only when the work is a book-shaped artifact (front/back matter, section epigraphs, soliloquy passages); blog essays continue to use only the subject spoke. Driven by the deep read of _Deconstructive Software Ramblings_ and forward-looking needs for the toy book.
- 2026-04-23: Initial hub created from corpus analysis of essays 01–101.
