# American surface conventions in full

The rules [american_formats.md](../rules/american_formats.md), [american_punctuation.md](../rules/american_punctuation.md), [american_spellings.md](../rules/american_spellings.md) state their obligations and tests in brief. This file holds each rule in full, with its rationale and worked examples.

## American Formats

Dates run month-day-year, spelled or numeric: October 4, 2026, or
10/4/2026 where the compact form is understood. Times use the
12-hour clock with meridiem styling — `a.m.`/`p.m.`, lowercase with
periods — so `9:30 a.m.` and `2:00 p.m.`; the 24-hour clock is a
military, medical, and technical register ("0800 hours") rather than
everyday prose. Currency writes the dollar sign attached before the
amount with no space (`$4.50`), and percentages are one word with the
symbol (`40%`) or spelled out in formal prose ("40 percent") — one
way per document.

### Rationale

Formats are the surface a reader's eye trips over first, and the
divergences are exactly where a British-trained writer defaults
wrong without noticing: the day-first instinct writes 4 October 2026
as 4/10/2026, which an American reader takes for April 10, almost six
months off. Keep the numerals-and-words split from the shared number
rules, and hold each format family — dates, times, money, percent —
to one style per document; a page that mixes `9:30 a.m.` with
`09:30` reads as unfinished rather than varied.

A date a reader sees is written out with the month as a word, in body
text and in any visible "Published" or "Updated" line; ISO dates
(`2025-04-15`) belong in frontmatter and other machine fields, where
software reads them. A text that has been substantively revised shows
its publication date and its update date as two separate dates:

> The essay was first published on April 15, 2025. (body text)
>
> Published April 15, 2025 · Updated May 2, 2025 (visible byline or footer)
>
> `published: 2025-04-15` (frontmatter)

A numeric range takes an unspaced en dash: `2018–2024`, `pages 12–18`.

## American Punctuation

Double quotation marks are the American default, with singles for
quotes inside quotes ("She called it 'unfinishable,' and she was
right"). Commas and periods sit inside the closing quotation mark as
a matter of convention, not logic: He said the plan was "dead on
arrival," and he was correct. The serial comma is standard — include
it ("red, white, and blue") — and the only defensible exception is a
publication whose established style drops it, never an ad hoc one.

### Rationale

The inside-the-quotes rule is arbitrary — it does not track whether
the comma belongs to the quotation — but it is uniform, and uniformity
is the value: readers of American prose parse the convention without
thinking, and every exception forces them to stop and check. The
serial comma earns its standard status by preventing ambiguity
("my parents, Ayn Rand and God"); dropping it saves one character and
risks the misreading. Watch quoted questions and exclamations, where
the mark genuinely belongs to the quotation and stays inside even
when the sentence continues: She asked, "Is it live?" before every
deploy.

### Dashes

American English uses the unspaced em dash (`word—word`, U+2014) for
a break in a sentence, and keeps the en dash (U+2013) for numeric
ranges (`2018–2024`, `pages 12–18`). A dash is allowed wherever it
passes the dash test: does it create a meaningful interruption,
reversal, or delayed qualification that the alternatives would
weaken? Compare it against a comma, a colon, parentheses, and a full
stop, and keep the dash only if each of them would weaken the turn.
There is no quota, but frequency is a warning sign during editing:
several dashes in one paragraph, or a dash in most paragraphs, usually
means the dashes are standing in for sentence construction.

Passes, because the dash carries a delayed qualification that a comma
would flatten: The model was accurate—on the cases it had already seen.

Fails, because commas carry the inserted list just as well: I work
close to the product—designers, product owners, users—and treat
maintainability as part of the delivery. Repaired: I work close to the
product, with designers, product owners, and users, and treat
maintainability as part of the delivery.

A translated title may keep a dash if the turn still works in English;
the punctuation is decided again from the meaning of the rebuilt
sentence, never carried over mechanically.

## American Spellings, Chosen Once

American spelling is a set of consistent choices, not a list to
sample from. The core sets: `-ize` as the default verb ending
(`organize`, `recognize`, `realize`); `-er` where British has `-re`
(`center`, `meter`, `theater`, `fiber`); no `-our` — American writes
`color`, `behavior`, `labor`, `neighbor`; and `-se` where the
noun/verb split needs it (`practice` for both noun and verb,
`license` for both, `defense`). The `-l` doubling does not happen
before vowel suffixes: `traveled`, `canceled`, `modeling`,
`counselor`.

### Rationale

Mixed spelling systems read as unchecked output, and the American
set's traps are the inverse of the British ones: the `-l` words that
stay single (`traveled`, `marveled`) and the noun/verb pairs that do
not split (`practice`, `license`) are where drafts drift, because the
words are shared with the other variety. Where a proper name or an
established technical term fixes another spelling (`Colour Revision`
as a product name, a quoted British text), the fixed spelling wins
over the house set.

The test is consistency within a document: a text that mixes
"organise" with "organize", or "colour" with "behavior", reads as
unedited, whichever variety it leans towards. American spelling is
also the convention of the software industry and of most international
technical markets, which makes it the usual choice for English
technical and commercial text written outside an English-speaking
country.
