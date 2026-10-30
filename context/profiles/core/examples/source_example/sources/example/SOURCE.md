# Example Source

A small synthetic source stored under the `sources/example/` directory
of the `source_example` example package
(`profiles/core/examples/source_example/`). It demonstrates the
sources structure — chunks with declared locators, a summary citing
chunks through implicit path specifiers — and is the target of the
live citations carried by the example package's own content domains.

The package around it is the worked demonstration of a well-formed
package: a `package.yaml` entrypoint, content domains (`rules/`,
`reference/`) carrying the module's only live citations, and this
directory-form source those citations would resolve against.

This source covers no external material: every chunk is synthetic
teaching prose written for this module, so `source.yaml` declares no
`coverage:`. Its citation key is the derived qualified name
`writing_core_source_example_example` — module name, profile segment,
package segment, and source name underscore-joined, with the
structural directory names excluded from the chain. Shared committed
content outside this package carries no live citations: citation
syntax is taught inside code spans there, so this package is the only
place a live citation of this source stands.

## Locators

- `chunks/01_memo_draft.md` declares the locator `memo draft`.
- `chunks/02_edit_notes.md` declares the locator `edit notes`.
- Every file also carries its implicit path locator
  (`chunks/01_memo_draft.md`, `chunks/02_edit_notes.md`,
  `summary/overview.md`, `SOURCE.md`), so
  `[@writing_core_source_example_example#chunks/01_memo_draft.md]`
  addresses the memo draft without any declared locator.
