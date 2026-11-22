# Technical Specification File Structure

Technical specifications define implementation requirements for protocols, data formats, algorithms, and system interfaces. They extend the base specification schema with conformance classes, testable requirements, implementation guidance, and machine-readable schema references. Every normative statement in a technical specification targets a specific conformance class and carries objective pass/fail verification criteria.

See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::structure@specification/reference/specification_structure.md" />.
See `reference_over_copy` (module `engineering`, profile `principles`, package `design`).

## Technical Specification Frontmatter

Technical specifications add fields beyond the base specification frontmatter:

```yaml
---
name: spec-identifier
version: 1.0.0
status: draft | proposed | standard | deprecated
spec-type: technical
conformance-classes:
  - parser
  - validator
  - generator
schema-format: json-schema | yaml | protobuf | xml-schema
normative-references:
  - path/to/dependency-spec.md
---
```

| Field | Required | Description |
|-------|----------|-------------|
| spec-type | Yes | Always `technical` for this schema |
| conformance-classes | Yes | List of implementation categories |
| schema-format | Conditional | Format when machine-readable schemas exist |
| normative-references | Conditional | Specifications this document depends on |

See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::metadata@documentation/reference/document_versioning.md" />.

## Conformance Structure

Conformance classes categorize implementations by their role in the specification's ecosystem. Each class receives a definition followed by requirements organized in MUST, SHOULD, MAY progression.

### Class Definition Pattern

```markdown
### {Class Name}

A **{Class Name}** {one-sentence role definition}.

A conforming {Class Name}:
- MUST {absolute requirement with verifiable criteria}
- MUST {second absolute requirement}
- SHOULD {strong recommendation with justification context}
- MAY {optional capability}
```

Define classes before requirements sections. Subsequent requirement sections reference these classes by name, ensuring every normative statement has an unambiguous target.

### Class Examples Across Specification Types

| Spec Type | Typical Conformance Classes |
|-----------|----------------------------|
| Protocol spec | Sender, Receiver, Intermediary |
| Data format spec | Writer, Reader, Validator |
| API spec | Client, Server, Proxy |
| System architecture spec | Producer, Consumer, Coordinator |

Specifications with multiple conformance classes define requirements per class. A single implementation may conform to multiple classes simultaneously.

See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::structure@specification/reference/normative_language.md" />.

## Requirement Organization

Group requirements by technical area rather than by keyword level alone. Grouping by area keeps related constraints together, making the specification easier to navigate for implementers working on specific components. Within each area, order requirements from MUST through SHOULD to MAY.

### Identification Pattern

Assign each requirement a stable identifier combining section and sequence:

```markdown
- **[PARSE-01]**: A conforming Reader MUST accept all encodings listed in Section 3.2
- **[PARSE-02]**: A conforming Reader SHOULD report the detected encoding in diagnostic output
- **[VAL-01]**: A conforming Validator MUST reject input exceeding the size constraint defined in Section 4.1
```

Identifiers enable cross-referencing in test assertions, conformance reports, and variance documentation. Use descriptive prefixes (`PARSE`, `VAL`, `AUTH`, `SERIAL`) derived from the technical area.

### Testability

Every MUST and SHOULD statement requires an objective verification method. Define measurable criteria rather than subjective qualities.

| Testable | Untestable |
|----------|------------|
| "MUST reject messages exceeding 64 KB" | "MUST handle large messages appropriately" |
| "SHOULD respond within 500 ms" | "SHOULD be responsive" |
| "MUST produce output matching the schema in Annex A" | "MUST produce correct output" |

## Implementation Guidance

Implementation sections provide non-normative technical direction. Mark them explicitly as informative to prevent confusion with requirements.

### Section Format

```markdown
## Implementation (Informative)

This section provides guidance for implementers. It contains no normative requirements.

### Algorithm Overview

{Description of recommended approach}

### Data Structures

{Suggested internal representations}

### Pseudocode

{Language-agnostic algorithm description}
```

Include implementation guidance when the specification defines behavior complex enough that requirements alone leave significant ambiguity. Omit it when requirements are self-explanatory.

See `imrad_structure` (module `writing_academic`, profile `scholarly_prose`, package `composition`).

## Test Assertions

Test assertions map requirements to verification procedures. Group assertions by conformance class and link each to its source requirement. Each requirement appears once in the normative sections; test assertions reference them by identifier rather than restating content.

See `ssot` (module `engineering`, profile `principles`, package `design`).

```markdown
## Test Assertions

### Reader Conformance

| ID | Requirement | Input | Expected Result |
|----|-------------|-------|-----------------|
| T-PARSE-01 | [PARSE-01] | Valid input in each listed encoding | Successful processing |
| T-PARSE-02 | [PARSE-01] | Invalid encoding | Rejection with diagnostic |
| T-VAL-01 | [VAL-01] | Input exceeding size constraint | Rejection with error code |
```

Each assertion includes the input conditions and expected observable result. Test assertions are informative unless the specification explicitly states that passing a test suite constitutes conformance. Distinguish between normative test requirements and informative test suggestions.

## Machine-Readable Schemas

When a specification defines structured data, provide machine-readable schemas alongside prose requirements.

### Reference Pattern

```markdown
## Schema Definition

The normative schema is maintained at `schemas/{spec-name}.{format}`.

This schema version MUST match the specification version per the
versioning conventions.
```

### Embedding vs External Reference

| Approach | When to Use |
|----------|-------------|
| External file | Schema exceeds 50 lines; consumers need programmatic access |
| Embedded in spec | Schema under 50 lines; tightly coupled to prose requirements |

Align schema versions with specification versions. A schema change that alters validation behavior requires a corresponding specification version increment.

## Technical Annexes

Technical specifications include domain-specific annexes. Mark each as normative or informative.

| Annex Type | Content | Typically |
|------------|---------|-----------|
| Security Considerations | Threat model, required mitigations | Normative |
| Performance Considerations | Benchmarks, complexity constraints | Informative |
| Testing Requirements | Test suite structure, coverage expectations | Varies |
| Migration Guide | Version transition procedures | Informative |
| Variance Reporting | Extension and deviation documentation format | Normative |

### Variance and Extension

Define how implementations document deviations from SHOULD requirements and specification extensions:

```markdown
## Annex: Variance Reporting (Normative)

Implementations that deviate from SHOULD requirements MUST document
each deviation with:
- Requirement identifier
- Description of deviation
- Justification for the deviation
```

See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::audience@documentation/reference/expertise.md" />.
See `density_by_frequency` (module `writing_context`, profile `core`, package `density`).

## Validation Checklist

See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::maintenance@documentation/reference/documentation_review.md" />.

- [ ] Frontmatter includes all required technical specification fields
- [ ] Every conformance class has a definition and categorized requirements
- [ ] All MUST and SHOULD statements include verifiable criteria
- [ ] Requirements use stable identifiers with descriptive prefixes
- [ ] Implementation sections marked as informative
- [ ] Test assertions link to source requirements
- [ ] Machine-readable schemas version-aligned with specification
- [ ] Technical annexes marked normative or informative
- [ ] Variance reporting format defined for SHOULD deviations
