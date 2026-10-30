# Write Literal At Signs Safely

The at sign doubles as a citation trigger in this module's host
format. Mid-word, as in `alice@example.com`, it is ordinary prose:
the character before the `@` is a letter, so no citation candidate
starts. In trigger position — a sentence-initial handle or a
standalone mention — a bare `@` parses as the start of a citation
key, and an unresolvable key fails rendering with CTX-REF013.

## Rationale

The false-positive class is exactly the handles-and-addresses
vocabulary general writing naturally contains. Two safe spellings
exist, and both survive rendering byte-identical: a code span, and
the backslash escape `\@`. Reach for the code span when the token is
a name or address (`@ctxmod`, `updates@example.org`) or when you are
showing citation syntax; reach for the escape when the sign sits
inside a longer stretch of plain prose where backticks would mislead
the reader about formatting.

Code spans and fenced code blocks are immune zones: nothing between
backticks parses as a citation, a link, or locator markup, so any
doubtful `@` inside one is safe by construction. The audit before
publishing is a search for every `@` in the document; each hit must
be mid-word, inside a code span, or backslash-escaped.
