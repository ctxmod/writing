# Accessible Content

Documentation is read through screen readers, magnifiers, keyboard
navigation, translation tools, and search snippets as often as it is
read on a page. The writer controls most of what those readers get:
alternative text, link text, headings, and the words around tables and
color. The applicable standard is the W3C's Web Content Accessibility
Guidelines (WCAG) 2.2, a W3C Recommendation since 5 October 2023,
whose current version is dated 12 December 2024; WCAG 3.0 is still a
working draft and is not yet a conformance target. The success
criteria named below are WCAG 2.2's.

## Alternative text

Every image gets alternative text chosen by the image's job, following
the W3C images tutorial's decision tree (SC 1.1.1 Non-text Content,
level A):

| The image… | Alternative text |
| --- | --- |
| carries information (a screenshot of the setting to change, a photo the text discusses) | a short phrase giving what the reader needs from it, not "image of" |
| is a link or button | the destination or the action ("Download the report"), not the picture |
| is decorative, or repeats text already beside it | empty (`alt=""`), so a screen reader skips it |
| shows text | that text, word for word, unless the same text is already on the page |
| is a chart or diagram | a short identification in the alternative text, and the data or the explanation in the page itself: a table, a list, or the surrounding prose |

A caption and alternative text do different jobs: the caption
interprets the figure for every reader, the alternative text replaces
it for one who cannot see it. Where the caption already says what the
image shows, the alternative text can be short; it never simply
repeats the caption.

## Link text

Link text says where the link goes or what it does, so a reader who
lists the page's links, as screen-reader users often do, can choose
among them (SC 2.4.4 Link Purpose (In Context), level A, requires the
purpose to be clear from the link text with its surrounding sentence;
SC 2.4.9, level AAA, from the link text alone). Link the words that
name the target, "authentication guide", never "click here" or "this
page"; when the link downloads a file, the link text names its format
and size ("annual report, PDF, 2 MB"). Two links with the same text
go to the same place. The navigation reference carries the link
patterns.

## Structure that assistive technology reads

- **Headings are real headings.** Use the format's heading markup in
  order, without skipping levels for looks, and make each heading
  describe its section (SC 1.3.1 Info and Relationships, level A;
  SC 2.4.6 Headings and Labels, level AA). Bold text styled to look
  like a heading is invisible to heading navigation.
- **Lists and tables are marked up as lists and tables.** A data table
  has a header row; a table used only to lay text out in columns is
  replaced by headings or lists.
- **Color is never the only signal.** "The failed steps are shown in
  red" excludes readers who cannot tell red apart; add a word, a
  symbol, or a pattern (SC 1.4.1 Use of Color, level A). The diagram
  standards apply the same rule to diagrams.
- **Instructions do not depend on shape or position alone.** "Click the
  round button on the right" fails when the layout reflows or is read
  aloud; name the control by its label (SC 1.3.3 Sensory
  Characteristics, level A).
- **The language is declared.** The document states its language, and
  passages in another language are marked as such, so a screen reader
  pronounces them correctly (SC 3.1.1 and 3.1.2, levels A and AA).

## Documents beyond the web page

The same duties hold for PDF and word-processor output, where they
depend on the export: a PDF is accessible only when it is tagged
(PDF/UA is the ISO standard for it), and a word-processor document
keeps its accessibility only when headings, lists, and alternative
text are set through the application's styles and image properties
rather than by direct formatting. Plain language serves the same
readers from the other side: WCAG's reading-level criterion (SC 3.1.5,
level AAA) and the ISO 24495-1 plain language standard in the core
profile's basics package both aim at readers who can find,
understand, and use what they read.

## Sources

- https://www.w3.org/TR/WCAG22/ — WCAG 2.2, W3C Recommendation (first
  published 5 October 2023; current version 12 December 2024): success
  criteria 1.1.1, 1.3.1, 1.3.3, 1.4.1, 2.4.4, 2.4.6, 2.4.9, 3.1.1,
  3.1.2, 3.1.5; accessed 2026-11-23.
- https://www.w3.org/WAI/tutorials/images/decision-tree/ — W3C WAI alt
  decision tree, updated 13 May 2024; accessed 2026-11-23.
- https://www.w3.org/WAI/WCAG22/Understanding/link-purpose-in-context.html
  — Understanding SC 2.4.4 Link Purpose (In Context), level A;
  accessed 2026-11-23.
- https://www.w3.org/TR/wcag-3.0/ — WCAG 3.0 working draft (latest
  draft dated 10 September 2026); accessed 2026-11-23.
