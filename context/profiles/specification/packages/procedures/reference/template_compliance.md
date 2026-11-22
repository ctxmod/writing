# Template Compliance Procedure

Verify that specification documents conform to their required template structure. Template compliance ensures specifications contain all expected sections in the correct order with appropriate content depth, enabling consistent review and comparison across specifications.

## Prerequisites

- Specification document identified for validation
- Applicable template defined (section names, ordering, required content)
- Understanding of which template sections are mandatory vs optional

## Steps

1. **Identify applicable template**. Determine which template governs the specification based on:
   - Document type (design doc, RFC, technical spec, requirements doc)
   - Project conventions (standard template location, naming)
   - Explicit template reference in document metadata

2. **Extract template requirements**. List required elements:
   - Mandatory sections with expected ordering
   - Required metadata fields
   - Content format requirements per section (prose, table, diagram)
   - Minimum content depth per section

3. **Parse specification structure**. Extract headings and section content from the target document. Build a section inventory with heading levels, word counts, and content type.

4. **Compare against template**. For each template requirement, check:
   - **Present**: Section exists with expected heading
   - **Ordered**: Section appears in correct position relative to other sections
   - **Formatted**: Content uses required format (prose, list, table)
   - **Substantive**: Content exceeds minimum depth threshold (not a stub)

5. **Identify deviations**. Classify each deviation:

   | Deviation | Severity | Example |
   |-----------|----------|---------|
   | Missing mandatory section | Error | No "Alternatives Considered" section |
   | Wrong section order | Warning | "Risks" before "Proposed Solution" |
   | Wrong content format | Warning | Prose where table expected |
   | Stub content | Warning | Section contains "TBD" only |
   | Missing optional section | Info | No "Open Questions" section |
   | Extra sections | Info | Sections not in template |

6. **Produce compliance report**. List deviations by severity with:
   - Template requirement violated
   - Current state in document
   - Suggested correction
   - Section location (heading and approximate line)

## Decision Points

**No explicit template**: When no template is defined, infer requirements from other specifications in the same project. If no precedent exists, apply a general specification template: summary, problem statement, proposed solution, alternatives, risks, implementation plan, success metrics.

**Template evolution**: Templates change over time. Validate against the template version current when the specification was written, or against the latest version if the specification is being updated.

**Partial compliance**: Specifications in draft status may intentionally omit sections. Check document status metadata before reporting missing sections as errors.

**Custom sections**: Specifications may include sections beyond the template. Additional sections are acceptable unless the template explicitly prohibits them.

## Success Criteria

- Applicable template identified and requirements extracted
- All mandatory sections verified present
- Section ordering validated
- Content format checked per section
- Deviations classified by severity
- Compliance report produced with corrections

## Common Issues

**Template ambiguity**: Templates with vague section descriptions ("relevant context") produce inconsistent compliance judgments. Clarify template definitions before validation.

**Section naming variations**: Authors may use different heading text for the same conceptual section ("Related Work" vs "Prior Art"). Match sections by content purpose when heading text differs.

**Nested template requirements**: Templates requiring sub-sections within sections increase validation complexity. Validate top-level sections first, then drill into sub-section requirements.

**Multiple applicable templates**: When a document could match multiple templates, select the most specific template. Document the selection rationale in the compliance report.

## Related

- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@specification/reference/sme_review.md" />
- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@documentation/reference/structure_validation.md" />
- `standards` (module `agentic`, profile `workflows`, skill `validation_procedure`)
