# Docs Prose Style Basics

The house style for documentation prose in four commitments: second
person, present tense, sentence-case headings, and a consistent code
style. Each removes a decision the reader otherwise pays for.

## Second person

Address the reader as "you": "You need a signing key", "Run the
check". Second person maps instructions onto the reader's hands.
Avoid "we" for the reader's actions ("we then delete the file" —
whose file?), which flips between the writer's product team and the
reader unpredictably; reserve "we" for the product's own behavior
("the indexer refuses duplicates") only when "the indexer" cannot
carry it. Never "the user" for the person reading — that is a third
person standing in the corner of a room the reader is alone in.

## Present tense

Documentation describes how the product behaves, and behavior is
present-tense: "The command prints the digest", not "The command
will print the digest". Future tense creeps in as hedging ("will
now proceed to") and adds a syllable of doubt to every step; past
tense belongs to release notes and changelogs, which narrate
events, not to pages that describe standing behavior.

## Sentence-case headings

Headings in sentence case — capitalize the first word and proper
nouns only ("Rotate the signing key", "Set up a secondary region").
Sentence case keeps headings scannable without title-case decoding,
distinguishes proper nouns honestly, and survives autocomplete and
search better than Title Case With Every Word Capitalized. Hold the
convention through every level, including subheadings inside
procedures.

## Consistent code style

One code-span style for one kind of thing: commands, flags, file
names, and UI literals in code spans; placeholders marked and named
(`ctxmod render <query>`); language-tagged fenced blocks for
multi-line code (`sh`, `yaml`), never bare indented blocks mixed
with tagged ones. Output shown to the reader is distinguished from
input to type (`$` prompts, comment annotations) and kept truthful —
an output example that no longer matches the real output is a bug
report waiting to be filed. Inline code stays inline: a one-line
fragment does not need a fence, and a fence does not need to
interrupt a step that fits in one.
