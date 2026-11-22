# Organization Assessment Procedure

Evaluate how documentation files organize within their directory hierarchy. Identify redundancies, assess findability from reader perspective, and recommend consolidation or restructuring when patterns degrade navigation efficiency.

## Prerequisites

- Documentation inventory completed (file listing with classifications)
- Directory structure accessible for traversal
- Understanding of target audience navigation patterns

## Steps

1. **Map directory hierarchy**. Record the full directory tree. Note depth levels, naming conventions, and grouping strategy.

2. **Identify organizational pattern**. Classify the dominant pattern:

   | Pattern | Description | Suited For |
   |---------|-------------|-----------|
   | Topic-based | Files grouped by subject area | Reference documentation |
   | Task-based | Files grouped by workflow or action | Procedural documentation |
   | Audience-based | Files grouped by reader role | Mixed-purpose documentation |
   | Lifecycle-based | Files grouped by development phase | Process documentation |
   | Hybrid | Combined strategies at different levels | Large documentation sets |

3. **Detect redundancies**. Compare file titles, headings, and content summaries across the inventory. Flag:
   - Duplicate content in separate files
   - Overlapping scope between adjacent files
   - Identical procedures in multiple locations

4. **Assess findability**. For each major documentation category, trace the path a reader would follow to locate information:
   - Count navigation steps from entry point to target content
   - Identify dead ends (directories with no cross-references)
   - Note orphaned files (no inbound references from other documents)

5. **Evaluate naming consistency**. Check whether file and directory names follow predictable conventions:
   - Consistent delimiter usage (hyphens, underscores, camelCase)
   - Descriptive names that indicate content
   - Parallel naming across similar categories

6. **Identify consolidation opportunities**. Flag cases where:
   - Multiple small files could merge into one structured document
   - Single large files could split into focused documents
   - Cross-cutting content could extract into a shared reference

7. **Produce assessment report**. Document organizational pattern, redundancies found, findability scores, naming issues, and recommended restructuring actions.

## Decision Points

**Organizational pattern conflicts**: Hybrid organization with clear entry points per audience may be appropriate when documentation serves diverse audiences. Distinguish deliberate repetition (quick-start guides) from accidental duplication by checking whether both locations reference the same source. Assess against current reader needs rather than original intent.

**Small documentation sets** (<20 files): Flat organization often outperforms complex hierarchies. Recommend depth only when file count warrants it. Legacy organization may reflect historical decisions--assess against current reader needs.

## Success Criteria

- Organizational pattern identified and documented
- Redundancies cataloged with locations and overlap descriptions
- Findability assessed with navigation step counts
- Naming consistency evaluated
- Consolidation opportunities listed with rationale
- Assessment structured for consumption by migration planning procedures

## Common Issues

**Organizational bias**: Assessors familiar with the documentation navigate efficiently regardless of organization quality. Use fresh-reader perspective or time-to-find metrics.

**Hidden relationships**: Documents may relate through content without explicit cross-references. Content analysis supplements directory structure analysis.

**Tool-generated structure**: Documentation generators impose directory conventions that may conflict with optimal organization. Distinguish tool constraints from design choices.

## Related

- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@documentation/reference/inventory.md" />
- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@specification/reference/migration_planning.md" />
- `ssot` (module `engineering`, profile `principles`, package `design`)
