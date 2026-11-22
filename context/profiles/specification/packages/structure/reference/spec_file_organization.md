# Specification File Organization

Multi-file specifications require consistent file organization to remain navigable as they grow. This file defines directory structure, naming, depth management, and index patterns for specification documents. It covers physical file layout; for section content and document structure within specification files, see the specification schema files.

## Directory Structure

Specifications use numbered directories to establish reading order. Each top-level section occupies a two-digit-prefixed directory or file under the specification root.

```
{spec-root}/
├── README.md
├── 00-foundations/
│   ├── README.md
│   ├── 01-terminology.md
│   └── 02-principles.md
├── 01-requirements/
│   ├── README.md
│   ├── 01-functional.md
│   └── 02-constraints.md
└── 02-conformance/
    ├── README.md
    └── 01-classes.md
```

The `XX-` prefix enforces a deterministic sequence. Readers and tools process sections in numerical order without relying on alphabetical sorting of descriptive names.

See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::structure@documentation/reference/section_hierarchy.md" />.

## File Naming Conventions

Specification files follow the pattern `XX-kebab-case.md`, where `XX` is a two-digit number and the descriptor identifies the section content. A collection whose convention is snake_case (ctxmod content, for instance, requires it) uses `XX_snake_case.md` and holds that separator throughout; the numbering rules are the same.

**Rules**:
- Directories: `XX-{descriptor}/` (e.g., `00-foundations/`, `01-requirements/`)
- Files within directories: `XX-{descriptor}.md` (e.g., `01-terminology.md`)
- Root index: always `README.md`
- Number gaps allow future insertion (use increments of 5 or 10 for initial sections)

The `XX-` prefix handles ordering; the kebab-case descriptor handles identification. Together they produce paths that sort correctly and read naturally.

See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::metadata@documentation/reference/file_naming.md" />.

## Depth Management

Specifications enforce a maximum of two levels from the specification root.

| Level | Contains | Example Path |
|-------|----------|-------------|
| 0 | Root index and overview files | `{spec-root}/README.md` |
| 1 | Numbered section directories or files | `{spec-root}/01-requirements/` |
| 2 | Files within section directories | `{spec-root}/01-requirements/02-constraints.md` |

No further nesting beyond level 2. When a level-2 file grows beyond manageable size, split its content across sibling files in the same directory rather than introducing a subdirectory. This limit preserves discoverability and keeps breadcrumb paths short.

### File vs Directory Decision

Line count determines whether a section warrants its own directory:

| Line Count | Organization |
|------------|-------------|
| < 150 lines | Single file at parent level |
| 150-300 lines | Single file with internal table of contents |
| > 300 lines | Subdirectory with multiple files |

Complexity also factors in. A 120-line file covering three independent topics may benefit from a directory split, while a 200-line file on a single cohesive topic may remain a single file with a table of contents.

## Index Files

Each directory in a specification contains a `README.md` serving as its entry point. The root README provides the full specification index; section READMEs introduce their subsection.

**Root README structure**:

```markdown
# {Specification Title}

Brief description of the specification's purpose and scope.

## Contents

| Section | Description |
| ------- | ----------- |
| [00 Foundations](./00-foundations/) | Terminology and foundational principles |
| [01 Requirements](./01-requirements/) | Functional and constraint requirements |
| [02 Conformance](./02-conformance/) | Conformance classes and testing criteria |
```

**Section README structure**:

```markdown
# {Section Title}

Brief description of this section's scope.

## Contents

| File | Description |
| ---- | ----------- |
| [01 Terminology](./01-terminology.md) | Key terms and definitions |
| [02 Principles](./02-principles.md) | Governing principles for this section |
```

Contents tables use a two-column format: linked file name and brief description. This pattern provides scannable navigation without duplicating file content.

## Navigation Patterns

Every specification file includes breadcrumb navigation at both top and bottom, connecting it to its parent and siblings.

**Top breadcrumb** (placed after frontmatter, before title):

```markdown
[{Spec Title}](../README.md) > [{Section}](./README.md) > {Current File}
```

**Bottom navigation** (placed at file end):

```markdown
---
← [Previous: 01 Terminology](./01-terminology.md) | [Next: 03 Constraints](./03-constraints.md) →
```

Previous/next links follow the numerical ordering. The first file in a section links back to the section README; the last file links forward to the next section's README.

See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::structure@documentation/reference/navigation.md" />.

## Cross-References

Specifications reference other sections by relative path. Use descriptive link text that identifies the target section's content rather than its number.

**Preferred**: `See [conformance class definitions](../02-conformance/01-classes.md) for implementation requirements.`

**Avoid**: "See section 02-01 for details."

Descriptive references remain stable when section numbers change during reorganization. Cross-references prevent duplication across specification files—each concept appears in one location with other files referencing it.

See `reference_over_duplication` (module `writing_context`, profile `core`, package `density`).
See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::metadata@documentation/reference/frontmatter.md" />.
See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::metadata@documentation/reference/document_versioning.md" />.

## Validation Checklist

Specification file organization compliance verification:

- [ ] All files use XX-kebab-case naming convention
- [ ] Directory depth does not exceed 2 levels from spec root
- [ ] README.md present in every directory
- [ ] File vs directory decision follows line count guidelines
- [ ] Breadcrumb navigation present at top and bottom of files
- [ ] Contents tables use two-column format (file, description)
- [ ] Cross-references use descriptive link text, not numbers
- [ ] Section numbering allows gaps for future insertions
- [ ] No broken relative paths after restructuring
- [ ] Previous/next navigation follows numerical order
