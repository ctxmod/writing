# Naming Conventions Schema

Naming conventions enable consistent identification and discovery of documents and other artifacts. Predictable patterns allow both humans and automated systems to locate, reference, and organize content efficiently.

Choose one word separator per collection and hold it everywhere: in directory names, file names, and identifiers. Where the tooling prescribes one, it decides; ctxmod modules, for instance, require snake_case (`[a-z][a-z0-9_]{0,63}`) for profiles, packages, and content file names, and draw a warning on anything else. The patterns below use snake_case; a collection whose convention is hyphenated substitutes `-` for `_` throughout and keeps every other constraint.

## File Naming

### Directory Structure

Organize files in hierarchical directories reflecting conceptual relationships:

```
{category}/
├── {subcategory}/
│   ├── {topic}/
│   │   └── {artifact}.md
│   └── {artifact}.md
└── {artifact}.md
```

**Constraints**:
- Directory names: lowercase, words separated by the collection's separator (snake_case here)
- Maximum nesting depth: 4 levels
- Related artifacts in adjacent directories

### File Names

File names describe content purpose and scope.

**Format**: `{descriptor}.{extension}` or `{descriptor}_{qualifier}.{extension}`

**Constraints**:
- Pattern: `^[a-z][a-z0-9_]*\.(md|yaml|json)$`
- Length: 3-50 characters (excluding extension)
- No hyphens (in a snake_case collection), spaces, or uppercase characters
- Underscores separate words within descriptors

**Examples**:
- `frontmatter.md`
- `severity_classification.md`
- `report_creation.md`

### Temporal File Names

Files with temporal significance include date and time components.

**Format**: `{date}/{time}_{type}_{descriptor}.{extension}`

**Components**:
- Date directory: `YYYY-MM-DD`
- Time prefix: `HH-mm`
- Type: artifact classification
- Descriptor: content identifier

**Examples**:
- `{date}/{time}_discovery_configuration.md`
- `{date}/10_15_validation_naming.md`

## Identifier Patterns

### Frontmatter Name Construction

Build frontmatter `name` fields (where the collection's tooling reads frontmatter; see the frontmatter schema in this package) systematically from artifact characteristics.

**Pattern**: `{category}_{subcategory}_{topic}`

| Component | Source | Example |
|-----------|--------|---------|
| category | Primary artifact type | `schema`, `objective`, `procedure` |
| subcategory | Domain or area | `metadata`, `writing`, `validation` |
| topic | Specific subject | `frontmatter`, `discovery`, `structural` |

**Examples**:
- `schema_metadata_frontmatter`
- `objective_writing_report_discovery`
- `procedure_validation_structural`

### Key Construction

Build abbreviated `key` fields from name components.

**Pattern**: `{cat_abbrev}_{sub_abbrev}_{topic_abbrev}`

| Full Term | Abbreviation |
|-----------|--------------|
| schema | schema |
| objective | obj |
| procedure | proc |
| orchestration | orch |
| reference | ref |
| discovery | disc |
| validation | val |
| implementation | impl |
| analysis | anly |
| metadata | meta |
| writing | wri |
| report | rep |
| structure | struct |
| frontmatter | fm |
| naming | name |
| versioning | ver |

**Examples**:
- `schema_meta_fm` (from schema_metadata_frontmatter)
- `obj_wri_rep_disc` (from objective_writing_report_discovery)
- `proc_val_struct` (from procedure_validation_structural)

### Uniqueness Requirements

Identifiers must be unique within their scope:

| Scope | Uniqueness Requirement |
|-------|------------------------|
| name | Globally unique across all artifacts |
| key | Unique within artifact category |
| file path | Unique within repository |

## Standard Abbreviations

### Category Abbreviations

| Category | Abbreviation | Use In |
|----------|--------------|--------|
| objective | obj | name, key |
| procedure | proc | name, key |
| schema | schema | name, key |
| orchestration | orch | name, key |
| reference | ref | name, key |
| principle | princ | name, key |

### Domain Abbreviations

| Domain | Abbreviation | Use In |
|--------|--------------|--------|
| discovery | disc | name, key |
| validation | val | name, key |
| implementation | impl | name, key |
| remediation | rem | name, key |
| analysis | anly | name, key |
| synthesis | synth | name, key |
| summary | sum | name, key |
| writing | wri | name, key |
| reading | read | name, key |
| maintenance | maint | name, key |
| metadata | meta | name, key |

### Artifact Type Abbreviations

| Type | Abbreviation | Use In |
|------|--------------|--------|
| report | rep | name, key |
| configuration | config | name, key |
| structure | struct | name, key |
| frontmatter | fm | key only |
| naming | name | key only |
| versioning | ver | key only |

## Pattern Application

### Reference Files

```
reference/{domain}/{topic}.md
```

Name: `{domain}_{topic}` or `{topic}` when unique

**Example**:
- Path: `reference/principles/writing/clarity.md` (a nested reference tree)
- Name: `writing_style_clarity` or `clarity`

### Schema Files

```
reference/writing/schemas/{category}/{type}.md
```

Name: `schema_{category}_{type}`
Key: `schema_{cat_abbrev}_{type_abbrev}`

**Example**:
- Path: `reference/principles/writing/docs/metadata/frontmatter.md`
- Name: `schema_metadata_frontmatter`
- Key: `schema_meta_fm`

### Objective Files

```
reference/objectives/{domain}/{topic}.md
```

Name: `objective_{domain}_{topic}`
Key: `obj_{domain_abbrev}_{topic_abbrev}`

**Example**:
- Path: `skills/writing/objective/reference/reports/discovery.md`
- Name: `objective_writing_report_discovery`
- Key: `obj_wri_rep_disc`

### Procedure Files

```
reference/procedures/{domain}/{topic}.md
```

Name: `procedure_{domain}_{topic}`
Key: `proc_{domain_abbrev}_{topic_abbrev}`

**Example**:
- Path: `skills/validation/procedure/reference/structural.md`
- Name: `procedure_validation_structural`
- Key: `proc_val_struct`

## Resolution Rules

When referencing artifacts by name:

1. **Exact match**: Name matches frontmatter `name` field exactly
2. **Key match**: Reference matches frontmatter `key` field
3. **Alias match**: Reference matches entry in frontmatter `aliases` array
4. **Partial match**: Reference matches unique suffix of name (use with caution)

**Resolution priority**: exact name > key > alias > partial

## Anti-Patterns

| Avoid | Why | Instead |
|-------|-----|---------|
| Inconsistent abbreviations | Discovery fails | Use standard abbreviation table |
| Redundant path components | Verbose names | Derive uniqueness from hierarchy |
| Generic names | Collision risk | Add distinguishing qualifier |
| Deep nesting in names | Verbose identifiers | Limit to 3-4 components |
| Uppercase in identifiers | Pattern matching complexity | Lowercase only |

## Validation Checklist

- [ ] File names follow the collection's pattern (`[a-z][a-z0-9_]*` for snake_case)
- [ ] Frontmatter name globally unique
- [ ] Key uses standard abbreviations
- [ ] Temporal files include date directory and time prefix
- [ ] Directory depth within 4 levels
- [ ] No redundant components in name construction
- [ ] Abbreviations consistent with standard table
