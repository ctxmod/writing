# Structure Validation Procedure

Verify that documentation follows structural conventions: heading hierarchy, section ordering, depth limits, and navigation patterns. Structure validation precedes content validation and identifies organizational defects that affect findability and comprehension.

## Prerequisites

- Target documents identified (individual files or directory scope)
- Structural standards defined (heading depth, section ordering, length guidelines)
- Inventory available when validating across a documentation set

## Steps

1. **Parse document structure** by extracting headings with their levels. Build a heading tree for each document. Record heading count, maximum depth, and level distribution.

2. **Validate heading hierarchy**. Check for:
   - Skipped levels (H1 to H3 without H2)
   - Multiple H1 headings per document
   - Heading depth exceeding defined maximum (typically 3-4 levels)
   - Empty sections (heading followed immediately by another heading)

3. **Check section ordering** against applicable conventions. Verify that required sections appear in expected positions:
   - Title as first element after frontmatter
   - Overview or introduction before detail sections
   - Examples, references, or related sections at the end

4. **Measure section lengths**. Calculate word counts per section. Flag sections outside target ranges:
   - Below minimum (under-developed, consider merging)
   - Above maximum (consider splitting)
   - Uniform length across all sections (signals mechanical generation)

5. **Assess navigation structures**. Verify presence and correctness of:
   - Table of contents for long documents (800+ words)
   - Cross-references to related documents
   - Breadcrumb indicators when applicable (directory-based hierarchy)

6. **Validate formatting consistency**. Check that parallel structures use consistent formatting:
   - List items follow uniform pattern (verb-first, noun-first)
   - Table columns maintain consistent types
   - Code blocks specify language identifiers

7. **Document violations** by severity. Classify each finding:
   - **Error**: Broken hierarchy, missing required sections
   - **Warning**: Sections outside length targets, formatting inconsistencies
   - **Info**: Style preferences, optimization opportunities

## Decision Points

**No defined structural standard**: Use general documentation conventions (single H1, sequential heading levels, 100-800 word sections) as baseline. Document assumed standards in validation report.

**Generated documentation**: Apply relaxed structural validation to auto-generated content (API docs, changelog). Focus on readability rather than authoring conventions.

**Multi-format projects**: When documentation uses multiple formats (Markdown, reStructuredText, AsciiDoc), validate each format against its own heading syntax. Report findings in format-neutral terms.

## Success Criteria

- All documents parsed without structural errors
- Heading hierarchy follows sequential levels
- Required sections present in expected positions
- Section lengths within acceptable ranges
- Navigation structures present where needed
- Findings documented with severity classifications

## Common Issues

**Frontmatter misidentified as content**: YAML frontmatter delimiters may interfere with heading detection. Strip frontmatter before structural parsing.

**Markdown heading ambiguity**: Both ATX (`#`) and Setext (underline) heading styles may coexist. Normalize to one style for consistent parsing.

**Deeply nested content**: Documents with 5+ heading levels often signal scope problems. Recommend splitting into multiple documents rather than adding structural validation exceptions.

**Table-heavy documents**: Documents primarily composed of tables may have few prose sections. Adjust section length validation to account for tabular content density.

## Related

- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@documentation/reference/completeness_check.md" />
- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@documentation/reference/inventory.md" />
- `standards` (module `agentic`, profile `workflows`, package `validation`)
