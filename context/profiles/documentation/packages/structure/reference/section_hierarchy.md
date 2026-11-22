# Document Hierarchy

Hierarchy decisions shape how readers navigate and comprehend documents. The principles here govern when to create sections, how deep to nest, and how to validate structure before writing.

## Section Organization Principles

Create sections based on conceptual boundaries, not arbitrary length. Each section addresses one distinct topic. Readers should understand a section without reading adjacent sections.

**Ordering patterns** influence comprehension:

| Pattern | Use When |
|---------|----------|
| General to specific | Introducing unfamiliar concepts |
| Foundation to application | Building understanding incrementally |
| Frequent to rare | Readers need common cases first |
| Chronological | Process or workflow documentation |

Section vs. subsection decision: If content could standalone as a separate document, make it a top-level section. If content only makes sense in context of a parent, make it a subsection.

## Heading Semantics

Headings carry semantic weight beyond formatting. Each level signals a specific relationship.

| Level | Semantic Role | Constraints |
|-------|---------------|-------------|
| H1 | Document context | Exactly one per file |
| H2 | Primary scanning anchors | Minimum two if any used |
| H3 | Working memory limit | Deepest comfortable navigation |
| H4 | Minor elaboration | Triggers restructuring consideration |

**Avoid stacked headings**: An H2 immediately followed by H3 without intervening text signals redundant structure. Either add introductory content or merge the levels.

**No lone subsections**: If a parent heading has only one child, either the child absorbs into the parent or the parent splits into multiple children.

## Depth Decisions

Deep hierarchies exceed cognitive limits. When reading an H4, readers maintain H1, H2, and H3 context simultaneously. H5+ exceeds structural working memory (Miller's Law applied to hierarchy).

Screen reader users navigate by jumping between headings. Deep structures force excessive keystrokes and degrade time-to-value.

**Decision sequence**:

1. **At H3**: Comfortable. Continue if needed.
2. **At H4**: Pause. Consider semantic alternatives (tables, definition lists, bold text).
3. **Needing H5**: Stop. Split the file or promote content.

**Alternatives to deep nesting**:

- Replace H4s with bold text for minor items
- Use tables for parallel information
- Split to separate file with H4 content becoming H2
- Use collapsible sections for advanced details

## Document Outlining

Draft headings before writing content. The outline functions as a validation tool, not just a planning artifact.

**Validation checks**:

- Read H1 through H3 sequence aloud. The progression should tell a coherent story.
- Verify each H2 represents a distinct topic. Overlap indicates need for restructuring.
- Check for orphaned content. Sections that reference other sections extensively may need reorganization.
- Confirm depth stays shallow. Prefer breadth (more H2s) over depth (H3s under H2s).

**Accessibility heuristic**: Navigate your outline as a screen reader user would. If finding specific content requires more than three heading jumps, restructure for faster access.

## Related

See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::basics@core/reference/clarity_principles.md" />.
