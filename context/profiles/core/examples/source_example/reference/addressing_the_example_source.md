# Addressing the Example Source

The example package carries the module's citation teaching. This
reference explains the shapes it demonstrates: how the source's
citation key derives, the citation forms, how locators address
places inside a source, and what the rendered output does with all
of it. Every form is shown inside a code span — inert by the parser's
immunity rule — because the one place a live citation belongs is the
worked file beside this one.

## The citation key

The source's citation key is its derived qualified name:
`writing_core_source_example_example`. The chain walks the ownership
path — module `writing`, profile segment `core`, example package
segment `source_example`, source name `example` — with the structural
directory names (`profiles/`, `examples/`, `sources/`) excluded, and
joins the segments with underscores. A qualified key names exactly
one entity: names are validated unique across the active
composition, so a qualified citation can never tie.

Short keys are the convenience form: a key that is not itself a
qualified name resolves by outward first-match — the citing body's
own sources first, then its ownership ancestors nearest first, then
the rest of the active composition. This module exercises none:
one source, one key, no ambiguity to demonstrate.

## The citation forms

The supported pandoc forms, each with the example key:

- Parenthetical: `[@writing_core_source_example_example]`
- Narrative: `@writing_core_source_example_example`
- Suppress author: `[-@writing_core_source_example_example]`
- Prefix: `[@see @writing_core_source_example_example]`
- Suffix / locator: `[@writing_core_source_example_example, memo draft]`
- Multiple: `[@writing_core_source_example_example; @other_source]`
  — meaningful with two distinct keys, which this single-source
  module does not have
- Braced key: `@{key with spaces}` — braces win; `#` and `/` are
  never structural inside them
- Locator braces: `[@writing_core_source_example_example {…}]` —
  braced suffix data, carried verbatim

## Locators

Every file in a directory-form source carries an implicit path
locator: its path relative to the source root
(`chunks/01_memo_draft.md`, `summary/overview.md`, `SOURCE.md`).
Declared locators layer human-facing aliases on top — the
`<ctxmod_locator>` markup in a chunk body — and the suffix position
of a citation binds through them:
`[@writing_core_source_example_example, memo draft]` and
`[@writing_core_source_example_example#chunks/01_memo_draft.md]`
address the same file. Matching normalizes by case fold and
whitespace collapse, so `Memo Draft` and `memo  draft` bind the same
alias. A suffix matching no declared locator is not an error — it is
prose carried through, pandoc-style; only the `#path` form is
validated against the source tree. Declaring a file's own implicit
path as an alias is redundant and draws the CTX-REF018 warning.

## The render posture

A citation occurrence renders as a named footnote marker whose name
is the cited target's qualified name, the locator staying inline at
the site: `[@writing_core_source_example_example, memo draft]`
becomes `[^writing_core_source_example_example, memo draft]` in the
rendered body. The rendered `footnotes_list.yaml` is an ordered
mapping keyed by qualified name, with one entry per unique cited
target, sorted by qualified name — the ordering choice made for
render-diff stability, and because markers are the qualified name,
marker and entry align by construction. Entry content for a source
is interim: the raw `source.yaml` metadata serialized as inline JSON,
with `(inferred: <fields>)` appended when inference markers apply;
the CSL/Hayagriva rendering pipeline supersedes this interim form on
the roadmap. Locators never enter the list — they stay inline at
citation sites.

The example source itself declares no `inferred:` — synthetic
material has nothing unverified — so the `(inferred: …)` annotation
is taught here in code spans and appears in this module's rendered
output only when a future local source earns it. Honesty is the
rule: a field listed in `inferred:` names a value the author did not
verify, and the annotation keeps the rendered bibliography from
presenting it as verified.

## Immunity and the literal at sign

Nothing inside inline code spans or fenced code blocks parses as a
citation, a link, or locator markup; content returns byte-identical
through both render passes. The backslash escape `\@` is not a
citation candidate and the escape is preserved through the
round-trip, so a literal `@` in trigger position — a sentence-initial
handle, a standalone mention — needs a code span or an escape, and
mid-word addresses like `alice@example.com` need nothing because the
preceding character is a letter.
