# Documentation Inventory Procedure

Catalog existing documentation files to establish scope, identify gaps, and support subsequent assessment procedures. The inventory provides a baseline for structure validation, organization assessment, and completeness checking.

## Prerequisites

- Target directory or directories identified
- File patterns defined for documentation files (e.g., `**/*.md`, `**/*.rst`, `**/*.adoc`)
- Classification scheme selected (by type, audience, or maintenance status)

## Steps

1. **Scan target directories** using recursive glob patterns against documentation file extensions. Record total file count and directory distribution.

2. **Classify by document type**. Assign each file to a primary type based on content and location:

   | Type | Indicators |
   |------|-----------|
   | Conceptual | Explains ideas, architecture, rationale |
   | Procedural | Step-by-step instructions, how-to guides |
   | Reference | API docs, configuration options, schemas |
   | Tutorial | Learning-oriented, progressive complexity |
   | Specification | Requirements, constraints, formal definitions |

3. **Identify audience** for each document. Determine whether content targets developers, operators, end users, or mixed audiences. Use directory naming, frontmatter metadata, and content sampling.

4. **Assess maintenance status**. For each file, classify currency:
   - **Current**: Content reflects present state
   - **Stale**: Content references outdated patterns, versions, or structures
   - **Unknown**: Insufficient context to determine currency

5. **Record metadata gaps**. Flag files missing frontmatter, titles, or expected metadata fields. Count gaps per category.

6. **Produce inventory report**. Structure output as categorized file list with counts, audience assignments, and maintenance status. Include summary statistics.

## Decision Points

**Mixed-type documents**: When a file serves multiple purposes (e.g., conceptual explanation with embedded procedures), classify by primary purpose. Note secondary classification in inventory.

**Large file counts** (>200 files): Sample 20% per category for audience and maintenance assessment. Extrapolate patterns to remaining files with noted confidence level.

**No established classification scheme**: Default to the five-type scheme above. Adjust categories after initial pass if project conventions suggest different groupings.

**Automated metadata extraction**: When files use consistent frontmatter, extract classifications programmatically before manual review. Reduce manual effort to gap-filling and validation.

## Success Criteria

- All documentation files cataloged with type classification
- Audience identified for each document or category
- Maintenance status assessed (current, stale, unknown)
- Metadata gaps flagged with counts
- Inventory structured for consumption by downstream procedures

## Common Issues

**Extension ambiguity**: Files without standard documentation extensions may contain documentation. Check `README`, `CHANGELOG`, and similar convention-based names.

**Symlinks and generated files**: Exclude generated documentation (build output, API docs from code) from manual inventory. Note their existence separately.

**Classification disagreement**: Multiple valid classifications for a single file. Use primary-purpose rule and document edge cases for consistency across the inventory.

**Scope creep**: Inventory expanding to include non-documentation files. Maintain strict scope by file pattern and exclude configuration, source code, and test files unless they contain embedded documentation.

## Related

- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@documentation/reference/structure_validation.md" />
- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@documentation/reference/organization_assessment.md" />
- `broad_scan` (module `agentic`, profile `workflows`, skill `discovery_procedure`)
