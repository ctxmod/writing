# Frontmatter Schema

Frontmatter provides machine-readable metadata at the beginning of a document. A YAML frontmatter block enables consistent identification, classification, and cross-referencing across a documentation collection, when the tooling that reads the collection interprets it.

Frontmatter is only worth writing where something reads it. Check what the collection's tooling interprets before adding fields: a static-site generator may read `title` and `date`; a context manager may read a few keys and treat the rest as body text. In a ctxmod module, for example, rule files interpret exactly one property, `paths:`, and reference files do not interpret frontmatter at all — a leading `---` block there renders as body, so the description belongs in the opening sentence instead. Fields nothing reads are noise that drifts out of date.

The schema below is a reference design for a collection whose tooling does interpret frontmatter. Adapt the field names and patterns to that tooling; keep the discipline (one identifier convention, short summaries, resolvable cross-references, category fields only where they carry information).

## Universal Fields

Fields applicable to all documents regardless of type or domain:

```yaml
---
name: unique_identifier
key: short_alias
summary: One-line description of the document's purpose
aliases:
  - alternate_name
related:
  - path/to/related/document.md
---
```

| Field   | Required    | Type   | Description                                                          |
| ------- | ----------- | ------ | -------------------------------------------------------------------- |
| name    | Yes         | string | Unique identifier for pattern matching and reference resolution      |
| key     | Conditional | string | Abbreviated reference (required for frequently-referenced documents) |
| summary | Conditional | string | One-line description (required for documents that may be inlined)    |
| aliases | No          | array  | Additional names for pattern resolution                              |
| related | No          | array  | Paths to related documents for cross-referencing                     |

## Field Specifications

### name

Primary identifier for the document. Used by pattern-matching systems to locate documents by logical name rather than by file path.

**Format**: Lowercase words joined by one separator, chosen once per collection. Use the separator the collection's file names use (see the naming guidance in this package): snake_case where the tooling requires it, as ctxmod does for profiles, packages, and file names; hyphens where the collection's convention is hyphenated.

**Constraints**:

- Pattern (snake_case collections): `^[a-z][a-z0-9_]*$`; hyphenated collections use `^[a-z][a-z0-9-]*$`
- Length: 3-50 characters
- Must be unique within the collection

**Examples**:

- `schema_metadata_frontmatter`
- `procedure_report_creation`
- `objective_writing_discovery`

### key

Abbreviated reference for concise citations and quick lookup. Useful when full names are verbose.

**Format**: Abbreviated segments joined by the collection's separator

**Constraints**:

- Pattern: `^[a-z]{2,6}(_[a-z]{2,6})*$` (or the hyphenated equivalent)
- Length: 2-20 characters
- Should convey document type and primary topic

**Examples**:

- `schema_meta_fm` (from schema_metadata_frontmatter)
- `proc_rep_cre` (from procedure_report_creation)
- `obj_wri_disc` (from objective_writing_discovery)

### summary

Brief description used when documents are referenced or inlined at low verbosity. Must convey purpose without requiring the full document.

**Format**: Single sentence, no terminal period

**Constraints**:

- Length: 10-100 characters
- Must describe what the document provides or defines
- Avoid generic descriptions

**Examples**:

- `YAML frontmatter field definitions for document identification`
- `Create structured reports documenting findings with attribution`
- `Patterns for building coherent self-contained sections`

Where the tooling does not read a summary field, the same sentence opens the document body instead.

### aliases

Additional names that resolve to this document during pattern matching. Useful for common abbreviations or alternative terminology.

**Format**: Array of strings following the name pattern

**Use cases**:

- Common abbreviations (`fm` for `frontmatter`)
- Domain synonyms (`config` for `configuration`)
- Legacy references during migration

### related

Cross-references to documents that provide context, extend concepts, or share a topic area. Related links appear in navigation and enable discovery of connected content.

**Format**: Array of relative paths from the repository root

**Constraints**:

- Pattern: `^[a-z0-9./_\-]+\.(md|yaml|json)$`
- Paths must resolve to existing documents
- Bidirectional relationships preferred (both documents list each other)

Where the tooling offers resolvable link components (ctxmod's `ctxmod_path` and `ctxmod_link`, for instance), prefer them in the body over a `related` list: the tool then checks that each target exists.

## Category-Specific Fields

Different document categories extend the universal fields with specialized metadata.

### Report Documents

```yaml
---
type: discovery | analysis | validation | summary | implementation | remediation
date: YYYY-MM-DD
time: HH-mm
source: "{work context or 'general'}"
objective: "{producing task or objective name}"
status: "{status value when applicable}"
---
```

| Field     | Required    | Description                     |
| --------- | ----------- | ------------------------------- |
| type      | Yes         | Report classification           |
| date      | Yes         | Creation date                   |
| time      | Yes         | Creation time                   |
| source    | Yes         | Work context or "general"       |
| objective | Yes         | Producing task or objective     |
| status    | Conditional | Completion or compliance status |

### Objective Documents

```yaml
---
name: objective_identifier
base_behavior: "{parent objective path}"
---
```

| Field         | Required    | Description                                |
| ------------- | ----------- | ------------------------------------------ |
| base_behavior | Conditional | Link to parent objective for inheritance   |

### Work Item Documents

```yaml
---
id: "{work item identifier}"
status: pending | in_progress | completed | blocked
priority: critical | high | medium | low
assigned: "{assignee identifier}"
---
```

| Field    | Required | Description                 |
| -------- | -------- | --------------------------- |
| id       | Yes      | Unique work item identifier |
| status   | Yes      | Current state               |
| priority | Yes      | Relative importance         |
| assigned | No       | Current assignee            |

A work-tracking tool usually owns these fields itself (ctxmod's work store keeps work records and their status in its own store, for instance); write them by hand only where no tool does.

### Orchestration Documents

```yaml
---
phase: "{orchestration phase}"
pattern: sequential | parallel | conditional
---
```

| Field   | Required    | Description                      |
| ------- | ----------- | -------------------------------- |
| phase   | Conditional | Orchestration phase identifier   |
| pattern | No          | Execution pattern classification |

## Validation Rules

### Format Validation

```yaml
# Name format (snake_case collection)
name: "^[a-z][a-z0-9_]{2,49}$"

# Key format
key: "^[a-z]{2,6}(_[a-z]{2,6}){0,3}$"

# Date format
date: "^\\d{4}-(0[1-9]|1[0-2])-(0[1-9]|[12]\\d|3[01])$"

# Time format
time: "^([01]\\d|2[0-3])-[0-5]\\d$"

# Path format
related: "^[a-z0-9./_\\-]+\\.(md|yaml|json)$"
```

### Required Field Validation

| Condition             | Required Fields                     |
| --------------------- | ----------------------------------- |
| All documents         | name                                |
| Frequently referenced | name, key                           |
| Inline-eligible       | name, summary                       |
| Report documents      | type, date, time, source, objective |
| Work items            | id, status, priority                |

### Cross-Reference Validation

- Related paths must resolve to existing documents
- Referenced objectives must exist in the objectives hierarchy
- Base-behavior links must point to valid parent objectives

## Examples

### Reference Document

```yaml
---
name: context_efficiency
key: ctx_eff
summary: Maximize information value per token in agent interactions
aliases:
  - token_efficiency
related:
  - reference/kiss.md
  - reference/clarity.md
---
```

### Report Document

```yaml
---
name: discovery_report_{date}
type: discovery
date: {date}
time: {time}
source: general
objective: discovery
scope: Configuration file inventory
---
```

### Objective Document

```yaml
---
name: objective_writing_report_validation
key: obj_wri_rep_val
summary: Create validation reports documenting compliance status
base_behavior: reference/reports.md
related:
  - reference/validation_report_structure.md
---
```

## Validation Checklist

- [ ] The collection's tooling actually reads every field present
- [ ] name field present and matches the collection's pattern
- [ ] key field present if the document is frequently referenced
- [ ] summary field present if the document may be inlined (or the summary opens the body where no tool reads it)
- [ ] All related paths resolve to existing documents
- [ ] Category-specific required fields present
- [ ] Date and time formats correct (YYYY-MM-DD, HH-mm)
- [ ] Status values from the allowed enumeration
