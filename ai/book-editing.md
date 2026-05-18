# Book Editing Context — Spoke

Production-side companion to [book-context.md](book-context.md). Where the book spoke covers **drafting and shaping** a book-form artifact, this file covers **auditing a typeset manuscript or published PDF** for the kinds of errors that only surface once the book is laid out: index page misses, alphabetical-order slips, endnote numbering drift, cross-reference rot.

This spoke loads on top of the subject spoke when the work is "the book exists, now find what's broken in it." It does not replace [book-context.md](book-context.md).

## When to load this file

- The author hands over a **typeset PDF** (post-galley, post-publish, or post-reprint candidate) and asks for a correctness sweep over a specific back-matter section.
- A pass over the **index**: page numbers, alphabetical ordering, sub-entry conventions, cross-reference targets.
- A pass over the **endnotes**: numbering monotonicity, dead URLs, missing chapter assignments, format drift.
- A pass over the **bibliography**: alphabetical ordering by surname, format consistency, books-only discipline (no URLs leaking in).
- A pass over **figure list / list of plates**: figure-letter notation consistency, page-number agreement with body text.
- The author asks "is this consistent with the book's stated conventions?" — load this file to know what to check against.

Always also load:

- [writing-context.md](writing-context.md) — base routing and voice.
- [book-context.md](book-context.md) — the book's editorial conventions (UTS vs. DSR deltas, citation discipline, index discipline, etc.). The editing pass enforces those rules; this file does not redefine them.
- The matching subject spoke — useful when an audit decision depends on whether the term is a person, product, place, or coinage.

## Stance

The author edits; the AI surfaces candidates. **Do not mutate the source PDF or the manuscript.** Produce tabular reports the author can act on by hand. Bucket findings by confidence so the author can triage. Be explicit about extraction-tool limitations rather than presenting false certainty.

## Index audit — page-number verification

The job: confirm that every `(entry, page)` pair in the index actually points at an occurrence of that entry in the body.

### Workflow

1. **Extract** the PDF to text per page. `pypdf` works for a first pass; consider `pdftotext -layout` if line-break structure matters (it does for cross-reference splitting).
2. **Build a printed-page → PDF-page-index map.** Books have front-matter pages, chapter title pages, and other shifts. For UTS, printed p.1 corresponds to PDF index 30, with a small additional discontinuity around chapter title pages (PDF 51–101). Verify the map by spot-checking a few known pages before trusting it.
3. **Identify the index region** and **the body region**. Exclude endnotes and the index itself from body-text searches — both contain the indexed terms by definition and will yield false positives. For UTS: endnotes printed 425–452 (PDF 453–480), index printed 453–465 (PDF 481–493).
4. **Parse the index into entries** of the shape `{head, subs: [(sub_name, [pages])]}`. A tokenizer that emits `WORD / NUM / PAREN / ',' / ';' / ':'` and a small state machine on top handles most lines.
5. **For each `(head, page)`**, search the body for the head term within ±5 pages of the claimed page. Match inverted names too: an entry "LastName, FirstName" must be searched as both `LastName, FirstName` and `FirstName LastName`.
6. **Bucket by confidence:**
    - **HIGH** — exactly one clean hit within ±5 pages on a page other than the indexed one, and no hit on the indexed page itself. Recommend the off-by-N correction.
    - **MEDIUM** — multiple plausible candidates within ±5; recommend the closest with the qualifier.
    - **LOW** — no clean match; flag for the author to check manually (often a figure caption, italicized phrase, or ligature mangling — see below).
7. **Report** as a markdown table with columns: Entry, Indexed page, Suggested page, Confidence, Note.

### Known pitfalls

- **Text extraction merges lines.** `pypdf` does not preserve index line breaks. Cross-references such as `X see Y. NewEntry, 173` collapse onto a single line and the parser may treat `NewEntry, 173` as a sub-entry of `X` rather than as a separate head. Filter or rerun with `pdftotext -layout` for those.
- **Ligature loss.** `ﬀ`, `ﬃ`, `ﬁ` extract unevenly. `Buﬀalo News` may become `Buf alo News` or `Bualo News`, which then fails to match `Buffalo` in the body. This shows up as false-LOW results and as false-positive alpha-order violations. Note explicitly in the report rather than re-querying.
- **Italics and figure captions.** Italicized phrases and embedded captions sometimes drop out of `pypdf` extraction. A LOW result on a term that you can see in the PDF is usually this.
- **Sub-entry leakage.** Phrases like `patent of`, `office of`, `recall of`, `assassination of`, `to`, `at`, `LLC` get parsed as standalone heads because the head/sub boundary is encoded in layout, not in text. Treat any "head" of length ≤ 3 words and lowercased verb-of / noun-of shape as suspect; exclude from the report unless the author asks.
- **Inverted names without commas.** A few names index as `Van Beek (family)` and `Van Beek, Barend`; the family-vs-individual convention is intentional — see below.

### Working artifacts

Scratch artifacts (`entries.json`, `pairs.json`, suggestion JSON) belong in `/tmp`, not in the repo. Each audit pass should be independently re-runnable from the PDF without depending on prior artifacts. Do not check audit scripts into the manuscript repo unless the author asks for a tools folder.

## Index audit — alphabetical ordering

The job: confirm the index is alphabetized consistently, and surface the human-introduced swaps and off-by-one letter slips that a manually built index always contains.

### Sort-key construction

- Lowercase the head.
- Strip to ASCII alphanumerics plus single spaces. Drop hyphens, commas, periods, apostrophes, parens.
- Collapse repeated spaces.
- Compare adjacent heads by the resulting key. Flag any `key[i] < key[i-1]`.

This is a **letter-by-letter** sort consistent with UTS practice. If a future book adopts strict word-by-word (space sorts before letters), revisit the key function.

### Intentional conventions that look like violations

A raw violation list will contain false positives the author has placed on purpose. Filter these out **before** presenting the report, and call out borderline cases as a separate "convention check" section for the author to decide.

- **Numbers-first.** `2001: A Space Odyssey`, `3D printing` precede the letter A. Not a violation.
- **Family-before-individual.** `Gentile (family)` before `Gentile, Andrew`. `Hassenfeld (family)` before `Hassenfeld, Alan`. `Mowbray (family)` before `Mowbray, Anna`. `Van Beek (family)` before `Van Beek, Barend`. Strict alpha would put the individual first; UTS uses family-first as a deliberate genealogical grouping.
- **Parent-before-specific.** `Mattel (company)` before `Mattel Engineering Co.`. `LEGO (toy)` before `LEGO Group`. `Photon (toy)` before `Photon Marketing Ltd.`. `Ghostbusters (toy)` before `Ghostbusters II`. The shorter/parent term carries the entry; the longer specifics file beneath.
- **Series order.** `Big Loader (toy)` then `Big Big Loader (toy)` then `Big Big Big Loader (toy)`. This is product-sequence order from Tomy, not an alphabetical pass that broke three times in a row. Verify against the product line before flagging.
- **Subsidiary parentheticals.** `Daily News (Louisiana)` and `Daily News (New York)` sort by the parenthetical when the head is identical. UTS appears to file by parenthetical alphabetically.

### Reporting format

Two tables, in order:

1. **Out-of-order entries to fix** — clear letter-swap and off-by-one slips. Columns: `Misordered entry`, `Currently sits after`, `Should sit before`. Group by index page when the page is recoverable from layout; otherwise present in document order.
2. **Convention check** — borderline cases that look like violations but may be intentional. Columns: `Entry`, `Sits after`, `Comment`. Frame as questions for the author, not as corrections.

End with a short caveats paragraph naming the extraction-tool limitations that affected this pass (ligatures, run-on cross-references, etc.).

## Endnote audit (forward-looking — not yet exercised)

When the time comes:

- **Numbering monotonicity.** Endnotes should march `[1] [2] [3] …` with no gaps and no repeats. Across the whole book, not per chapter (see [book-context.md](book-context.md) Citation discipline).
- **Body-to-back agreement.** Every `[N]` in the body must have a matching numbered endnote in the back. Every numbered endnote in the back must be cited at least once in the body.
- **URL form.** `https://` plain text, no tracking parameters, no shortener URLs, no `medium.com/@…` short forms. UTS endnotes are not hyperlinks in print; treat the printed form as canonical.
- **Books in endnotes are short-form** (`Author, _Title_, ch. N`). Full bibliographic entries belong in the Selected Bibliography only. Flag any endnote that duplicates a full bibliographic record.
- **Dagger vs. bracket.** UTS does not use `†`. If any leak in from a DSR-mode draft, flag.

## Bibliography audit (forward-looking)

- Alphabetical by author surname. Build the same lowercase-alphanumeric sort key as for the index and check monotonicity.
- Books only. Any entry that is a URL, podcast, article, or forum post is misfiled and belongs in Endnotes.
- Format consistency: surname, given name, then italicized title. Match the dominant pattern of the existing list; do not invent a new one.
- 30–60 entries for a single-author anthology. Outside that range, flag as a count-check for the author.

## Figure list / plates audit (forward-looking)

- UTS uses figure-letter notation: `A.1`, `A.2`, `AA.1`, etc. Confirm the sequence is monotonic per appendix or per personal-photo group.
- Every figure in the list must appear in the body with a matching caption.
- Every captioned figure in the body must appear in the list.

## Acknowledgments / About the Author audit

Lighter pass; mostly a consistency check against [book-context.md](book-context.md):

- About the Author opens with `**FIRSTNAME M. LASTNAME**` in bold small caps.
- UTS-form bio identity claim: `researcher and citizen journalist`.
- No book promotion inside the bio.
- Acknowledgments do not introduce new coinages.

## Do

- Surface; do not mutate. The author edits the manuscript by hand from the report.
- Bucket by confidence. HIGH / MEDIUM / LOW for page numbers; "fix" vs. "convention check" for alpha order.
- Name the extraction-tool limitations in every report. Ligatures, missed italics, run-on cross-references are recurring causes of noise.
- Re-use scratch artifacts inside one session; rebuild them next session. The PDF is the source of truth.
- When in doubt about whether a violation is intentional, ask before listing it as a fix.

## Don't

- Don't propose edits to the source PDF or to the manuscript files. Audit, then hand off.
- Don't run the same extraction twice in a session for the same section. The bottleneck is human review, not extraction.
- Don't pad confidence. A LOW finding is more useful than a falsely-confident HIGH that wastes the author's checking time.
- Don't quietly "fix" parser artifacts in the report by re-labeling sub-entries as heads. Drop them and say so in the caveats.
- Don't extend the audit scope mid-pass. Index page numbers and index alphabetical order are two separate passes with two separate reports.

## Learning log

<!-- Append dated bullets. Newest at top. Promote recurring patterns into the body above. -->

- 2026-05-17: Spoke created from the UTS post-publish-edits-9.pdf index audit. Two passes were performed: (1) page-number verification across the index (printed pp. 453–465), producing 13 HIGH-confidence corrections, 7 MEDIUM, 3 LOW; (2) alphabetical-order verification, producing ~85 clear out-of-order entries plus a short list of convention-check borderline cases (family-vs-individual, parent-vs-specific, series order). Workflow, pitfalls, sort-key construction, and the convention-vs-violation filter list were all promoted into the body above from that session.
