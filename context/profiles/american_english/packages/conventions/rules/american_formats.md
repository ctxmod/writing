# American Formats

Dates run month-day-year, spelled or numeric: October 4, 2026, or
10/4/2026 where the compact form is understood. Times use the
12-hour clock with meridiem styling — `a.m.`/`p.m.`, lowercase with
periods — so `9:30 a.m.` and `2:00 p.m.`; the 24-hour clock is a
military, medical, and technical register ("0800 hours") rather than
everyday prose. Currency writes the dollar sign attached before the
amount with no space (`$4.50`), and percentages are one word with the
symbol (`40%`) or spelled out in formal prose ("40 percent") — one
way per document.

## Rationale

Formats are the surface a reader's eye trips over first, and the
divergences are exactly where a British-trained writer defaults
wrong without noticing: the day-first instinct produces 4/10/2026 and
misdates the document for an American reader by four months. Keep the
numerals-and-words split from the shared number rules, and hold each
format family — dates, times, money, percent — to one style per
document; a page that mixes `9:30 a.m.` with `09:30` reads as
unfinished rather than varied.

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
