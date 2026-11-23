# Write Literal At Signs Safely

The at sign doubles as a citation trigger in this module's host
format. Mid-word, as in `alice@example.com`, it is ordinary prose:
the character before the `@` is a letter, so no citation candidate
starts. In trigger position — a sentence-initial handle or a
standalone mention — a bare `@` parses as the start of a citation
key, and an unresolvable key fails rendering with CTX-REF013.

In trigger position, write the at sign as a code span when the token is a name, an address or citation syntax (`@ctxmod`), and as the escape `\@` inside plain prose. Before publishing, search for every `@`; each hit must be mid-word, inside a code span, or backslash-escaped.

Rationale: [mechanics_rationale.md](../reference/mechanics_rationale.md).
