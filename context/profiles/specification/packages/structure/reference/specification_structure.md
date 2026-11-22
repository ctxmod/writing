# Specification Document Schema

Specifications define normative requirements that implementations follow. Unlike reference files (which explain concepts) or procedures (which describe workflows), specifications establish binding obligations using RFC 2119 keywords. This schema covers cross-specification document organization applicable to any specification type.

See `convention_over_configuration` (module `engineering`, profile `principles`, package `design`).
See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::structure@specification/reference/normative_language.md" />.

## Document Organization

Specification sections follow a standard ordering that moves from orientation through normative content to supplementary material. The sequence below applies regardless of specification domain.

| Order | Section | Purpose | Required |
|-------|---------|---------|----------|
| 1 | Overview | Scope, purpose, and intended audience | Yes |
| 2 | Terminology | Domain-specific term definitions | Conditional |
| 3 | Conformance | Implementation classes and their obligations | Yes |
| 4 | Requirements | Normative statements organized by level | Yes |
| 5 | Implementation | Non-normative technical guidance | No |
| 6 | Annexes | Informative supplementary material | No |

Include Terminology when the specification introduces specialized vocabulary or redefines common terms with precise meanings. Omit it when all terms carry their standard interpretation.

See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::structure@documentation/reference/section_hierarchy.md" />.

## Section Purposes

**Overview** establishes what the specification covers and what falls outside its scope. State the problem domain, the artifact types governed, and any prerequisite knowledge. Readers who finish the overview should know whether this specification applies to their work.

**Terminology** provides precise definitions referenced throughout the document. Each term appears in bold, followed by its definition. Defined terms carry their specification meaning in all subsequent sections.

**Conformance** identifies distinct implementation classes and maps requirements to each class. A data format specification might define Producer and Consumer classes. An interface specification might define Client and Server classes. Each class receives specific MUST, SHOULD, and MAY obligations.

**Requirements** contains the normative core. Group requirements by functional area, with each requirement identifiable by section number or descriptive label. Every requirement uses RFC 2119 keywords and meets testability criteria: a verifiable pass/fail outcome must exist.

See `research_first` (module `engineering`, profile `principles`, package `practice`).

**Implementation** provides non-normative guidance for implementers. Algorithms, pseudocode, and worked examples appear here. Mark this section explicitly as informative to prevent readers from treating guidance as requirements.

**Annexes** contain supplementary material: extended examples, security considerations, performance analysis, or migration guidance. Label each annex as normative or informative.

See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::structure@documentation/reference/section_construction.md" />.

## Cross-Specification Patterns

### Property Tables

Specifications frequently define properties, fields, or parameters. Use a standard five-column format for consistency:

| Property | Type | Required | Default | Description |
|----------|------|----------|---------|-------------|
| `identifier` | string | Yes | — | Unique name matching `^[a-z][a-z0-9-]*$` |
| `version` | string | No | `"1.0"` | Semantic version of the artifact |
| `encoding` | enum | No | `"utf-8"` | Character encoding for text content |

This format applies to API parameter definitions, data format field descriptions, protocol message attributes, and configuration option catalogs.

### Algorithm Pseudocode

When specifications describe algorithms, use language-agnostic pseudocode with clear step numbering:

```
Algorithm: Validate({input})
  1. IF {input} is empty THEN return Error("empty input")
  2. FOR each {element} in {input}:
     2.1 IF {element} violates constraint C THEN record violation
  3. IF violations exist THEN return Error(violations)
  4. RETURN Success
```

Mark algorithm sections as informative unless the specification mandates a specific algorithm.

### Normative vs Informative Marking

Every section carries either normative or informative status. Sections without explicit marking default to normative. Mark informative content using one of these patterns:

- Section-level: append "(Informative)" to the heading
- Block-level: prefix with `> **Note**:` or `> **Example**:`
- Inline: use "for example" or "such as" to signal illustrative content

See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::basics@core/reference/clarity_principles.md" />.
See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::structure@documentation/reference/navigation.md" />.

## Specification Categories

Different specification types emphasize different sections from the standard ordering.

| Category | Emphasis | Section Characteristics |
|----------|----------|------------------------|
| Protocol specifications | Conformance, Requirements | Message formats, state machines, error handling |
| Data format specifications | Terminology, Requirements | Schema definitions, encoding rules, validation |
| Interface specifications | Conformance, Implementation | Endpoint definitions, request/response schemas |
| Requirements specifications | Requirements | Functional and non-functional obligations |
| Process specifications | Implementation, Annexes | Workflow definitions, decision criteria |

Each category shares the base document organization. Category-specific extensions add sections appropriate to their domain—a Wire Format section for protocols, an Authentication section for interfaces. The base ordering remains stable; extensions insert at logical positions.

See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::metadata@documentation/reference/frontmatter.md" />.

## Validation Checklist

Specification document compliance verification:

- [ ] All six standard sections present in correct order
- [ ] Overview states scope, intended audience, and prerequisites
- [ ] Conformance section defines implementation classes
- [ ] Requirements use RFC 2119 keywords correctly
- [ ] Every requirement has verifiable pass/fail criteria
- [ ] Property tables use five-column format
- [ ] Informative sections explicitly marked as such
- [ ] Cross-references to related specifications resolve
- [ ] Terminology section included when specialized vocabulary used
- [ ] Annexes labeled as normative or informative

See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::structure@specification/reference/normative_language.md" />.

## Related

See `convention_over_configuration` (module `engineering`, profile `principles`, package `design`).
See `research_first` (module `engineering`, profile `principles`, package `practice`).
See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::structure@specification/reference/normative_language.md" />.
See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::basics@core/reference/clarity_principles.md" />.
See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::structure@documentation/reference/section_construction.md" />.
See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::structure@documentation/reference/section_hierarchy.md" />.
See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::structure@documentation/reference/navigation.md" />.
See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::metadata@documentation/reference/frontmatter.md" />.
See `academic_language` (module `writing_academic`, profile `scholarly_prose`, package `language`).
See `kiss` (module `engineering`, profile `principles`, package `design`).
See `dry` (module `engineering`, profile `principles`, package `design`).
