# Define Before Use

A term is defined at first use, and after that it is used — one name
per thing, throughout. Literals that the reader must reproduce
exactly — commands, flags, file names, UI strings — go in code
spans: run `ctxmod vet --root ./context`, click **Export**, open
`settings.toml`. Prose paraphrase of a literal ("the settings file")
is for flowing sentences; the literal itself appears wherever the
reader must act on it.

## Rationale

Undefined terms and shifting names are the two fastest ways a
document loses a reader's trust. The definition at first use can be
as light as a parenthetical expansion ("the indexer (the component
that walks the source tree)") — the point is that the reader never
has to guess whether two words name one thing. Synonym variation,
natural in essays, is a defect in documentation: "the dashboard",
"the console", and "the control panel" for one surface sends the
reader hunting for a distinction that does not exist. The code-span
rule is the reproducibility contract — anything in a code span can
be copied and pasted and will work; anything the reader must type
exactly but that sits in plain prose will eventually be retyped
wrong.
