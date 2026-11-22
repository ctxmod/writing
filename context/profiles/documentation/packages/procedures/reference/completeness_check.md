# Completeness Check Procedure

Validate that documentation files contain all required elements for their document type: sections, frontmatter fields, cross-references, and expected content blocks. Completeness checking differs from structure validation by focusing on presence of required content rather than its organization.

## Prerequisites

- Target documents identified with their document types
- Requirements defined per document type (required sections, metadata fields, content blocks)
- Inventory available for cross-reference validation

## Steps

1. **Load type requirements**. For each document type, identify mandatory elements:
   - Required frontmatter fields (name, summary, related)
   - Required sections (varies by type)
   - Required content blocks (examples, decision points, success criteria)
   - Required cross-references (related documents, principle references)

2. **Validate frontmatter**. Check each file against frontmatter requirements:
   - All required fields present
   - Field values non-empty and properly formatted
   - Name field follows naming conventions
   - Related paths reference existing files

3. **Check required sections**. Parse document headings and verify presence of each required section for the document type. Record missing sections with their expected position.

4. **Verify cross-references**. Extract all internal references (file paths, section links, tag references) and validate:
   - Referenced files exist at specified paths
   - Referenced sections exist within target files
   - No circular reference chains that prevent resolution
   - Bidirectional references where conventions require them

5. **Assess content blocks**. For each required content block, verify:
   - Block is present and non-empty
   - Content matches expected format (table, list, prose)
   - Minimum content threshold met (avoid stub sections)

6. **Produce completeness report**. List each document with its compliance status:
   - **Complete**: All requirements met
   - **Partial**: Some requirements missing, documented gaps
   - **Incomplete**: Critical requirements missing

## Decision Points

**Unknown document type**: When a file lacks type classification, infer type from directory location, content patterns, or filename conventions. Apply the most likely type's requirements with reduced confidence.

**Optional vs required sections**: Some document types define optional sections that enhance quality but are not mandatory. Report missing optional sections as informational, not errors.

**Broken cross-references**: Distinguish between references to files that never existed (likely errors) and references to files that were moved or renamed (likely maintenance debt). Check version history when accessible.

**Stub content**: Sections containing placeholder text ("TODO", "TBD", single-sentence stubs) satisfy presence requirements but not substance. Flag stubs separately from missing sections.

## Success Criteria

- All files checked against type-specific requirements
- Frontmatter validated for required fields and format
- Required sections verified present
- Cross-references validated for target existence
- Completeness status assigned per document
- Report distinguishes critical gaps from minor omissions

## Common Issues

**Evolving requirements**: Document type requirements change over time. Older documents may lack sections added to requirements after creation. Track requirement versions to distinguish non-compliance from pre-existing content.

**False positives on cross-references**: Parameterized references (template variables, dynamic paths) fail static validation. Identify and exclude parameterized references from validation.

**Overly strict requirements**: Applying all requirements uniformly may flag legitimate variations. Allow type-specific exceptions documented in the requirements definition.

**Large-scale incompleteness**: When most documents fail completeness checks, the requirements may be aspirational rather than enforced. Prioritize critical fields (name, summary) over comprehensive compliance.

## Related

- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@documentation/reference/structure_validation.md" />
- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@documentation/reference/inventory.md" />
- `completeness` (module `agentic`, profile `workflows`, package `validation`)
