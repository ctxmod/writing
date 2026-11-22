---
description: >-
  Documentation procedures for creating, validating, organizing, and
  maintaining documentation: the general procedures for every
  documentation type and the technical procedures for code
  documentation, with a selection guide.
binds_to_depth: main...
---

# Documentation Procedures

Procedures for creating, validating, organizing, and maintaining documentation artifacts. They are organized into three categories based on artifact type and required expertise; this package carries the general and technical categories, and the `specification` profile of this module carries the specification category.

## Categories

### General

Procedures for all documentation types: inventory, structure validation, organization assessment, completeness check.

- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@documentation/reference/inventory.md" />
- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@documentation/reference/structure_validation.md" />
- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@documentation/reference/organization_assessment.md" />
- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@documentation/reference/completeness_check.md" />

### Technical

Procedures for code documentation: code-coverage analysis, API documentation, runbook creation, diagram standards.

- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@documentation/reference/code_coverage_analysis.md" />
- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@documentation/reference/api_documentation.md" />
- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@documentation/reference/runbook_creation.md" />
- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@documentation/reference/diagram_standards.md" />

### Specification

Procedures for formal specifications: template compliance, SME review, version tracking, migration planning. They live in the `procedures` package of the `specification` profile (`template_compliance.md`, `sme_review.md`, `version_tracking.md`, `migration_planning.md`); select that profile for specification work.

## Selection Guide

| Goal             | Procedures                                       |
| ---------------- | ------------------------------------------------ |
| Discover state   | inventory → structure validation                 |
| Improve quality  | organization assessment → completeness check     |
| Document code    | code-coverage analysis → API documentation       |
| Operational docs | runbook creation + diagram standards             |
| Validate specs   | template compliance → SME review (specification) |
| Reorganize       | migration planning + version tracking (specification) |

## Related

- `creation` and `organization` (module `agentic`, profile `workflows`, package `reporting`, skill `writing_procedure`)
- `standards` (module `agentic`, profile `workflows`, package `validation`, skill `validation_procedure`)
