# Mechanics rules in full

The rules [apostrophes_and_confusion_pairs.md](../rules/apostrophes_and_confusion_pairs.md), [at_sign_literals.md](../rules/at_sign_literals.md), [capitalization_ground_rules.md](../rules/capitalization_ground_rules.md), [sentence_boundaries.md](../rules/sentence_boundaries.md) state their obligations and tests in brief. This file holds each rule in full, with its rationale.

## Apostrophes and Confusion Pairs

Possessives take an apostrophe before the s for singular nouns
("the team's decision") and after the s for most plurals ("the teams'
decision"); pronoun possessives never take one ("its", "theirs",
"yours"). The three classic confusion pairs are contractions versus
possessive pronouns: "it's" only ever means "it is" or "it has";
"your" shows ownership, "you're" means "you are"; "their" shows
ownership, "they're" means "they are", "there" points.

### Rationale

These errors cost disproportionate trust because they sit on the
surface: a reader who spots "its" for "it is" stops checking whether
the argument is sound and starts checking for the next mistake. The
substitution test settles every pair in one move — read the sentence
with the expansion ("it is late" / "the committee delayed its
decision") and keep the spelling that survives. Watch the plurals of
abbreviations and years, which take no apostrophe
(`three PhDs`, `the 1990s`), and the possessive of compound nouns,
which lands on the whole unit ("my sister-in-law's car").

## Write Literal At Signs Safely

The at sign doubles as a citation trigger in this module's host
format. Mid-word, as in `alice@example.com`, it is ordinary prose:
the character before the `@` is a letter, so no citation candidate
starts. In trigger position — a sentence-initial handle or a
standalone mention — a bare `@` parses as the start of a citation
key, and an unresolvable key fails rendering with CTX-REF013.

### Rationale

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

## Capitalization Ground Rules

Capitalize the first word of every sentence, proper nouns and their
derived adjectives ("Nordic", "Shakespearean"), and titles when they
attach to a name ("Director Chen" but "the director"). Everything else
stays lowercase — job roles, product categories, seasons, directions
("head north"), and decades.

### Rationale

Capitalization is a signal, and signals lose value when overused: a
page of Title Case Every Noun forces the reader to weigh each capital
for significance it does not carry. Pick one heading convention per
document and hold it — sentence case ("How the indexer works") or
title case ("How the Indexer Works") are both defensible, but the
document must commit, including through subheadings. Acronyms expand
on first use ("continuous integration (CI)") and stay uppercase after;
brand-internal styling ("iPhone") survives as-is, since a trademark's
spelling is not the writer's to normalize. When unsure whether a word
is a proper noun, ask whether a specific, named referent exists —
"the university" is lowercase, "Uppsala University" is not.

## Sentence Boundaries

Every sentence ends where its grammar ends. The two boundary errors
are the comma splice — two independent clauses joined by only a comma
("the build passed, we shipped") — and the run-on, where clauses fuse
with no punctuation at all. Join independent clauses with a semicolon,
a comma plus a conjunction, or a full stop; anything else is a splice.
A colon never joins two clauses in running prose; the rule and its
exceptions are in [tone_and_register.md](../../basics/reference/tone_and_register.md).

### Rationale

Splices force the reader to guess which boundary the writer intended,
and the guesses diverge — one reader sees emphasis, another sees a
typo. Fragments sit on the other edge of the same line: a fragment
("Which worked. Mostly.") is legitimate as deliberate voice when the
context makes the missing part recoverable and the effect earns the
break; the accidental fragment — a long clause that lost its subject
somewhere mid-draft — is just an unreadable sentence. The audit is
mechanical: read the draft aloud sentence by sentence; where your
voice would insert a full stop but the punctuation offers only a
comma, there is the splice.
