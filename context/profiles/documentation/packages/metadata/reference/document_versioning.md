# Versioning Schema

Version metadata tracks artifact evolution and communicates compatibility expectations. Versioning enables consumers to understand change impact, maintain compatibility, and plan upgrades.

## When to Version

Version artifacts when changes affect consumers:

| Change Type | Version Impact | Rationale |
|-------------|----------------|-----------|
| Breaking structure change | Major increment | Consumers must adapt |
| Significant content addition | Minor increment | New capability available |
| Clarification or correction | Patch increment | Existing behavior refined |
| Formatting or typo fix | No increment | No semantic change |

**Threshold rule**: Version when consumers would benefit from knowing the artifact changed. Routine maintenance does not require versioning.

## Version Format

### Semantic Versioning

Use semantic versioning for artifacts with external consumers.

**Format**: `{major}.{minor}.{patch}`

| Component | Increment When | Example |
|-----------|----------------|---------|
| major | Breaking changes | 2.0.0 |
| minor | Backward-compatible additions | 1.3.0 |
| patch | Backward-compatible corrections | 1.2.4 |

**Constraints**:
- Pattern: `^(0|[1-9]\\d*)\\.(0|[1-9]\\d*)\\.(0|[1-9]\\d*)$`
- Initial release: `1.0.0`
- Pre-release: `0.x.x` (no compatibility guarantees)

### Date-Based Versioning

Use date-based versioning for artifacts without backward compatibility requirements.

**Format**: `YYYY.MM.DD` or `YYYY.MM`

| Granularity | Use Case |
|-------------|----------|
| Daily | Frequently updated artifacts |
| Monthly | Periodically revised artifacts |

**Constraints**:
- Pattern: `^\\d{4}\\.(0[1-9]|1[0-2])(\\.([0-2]\\d|3[01]))?$`

## Frontmatter Version Fields

### Version Field

Current artifact version:

```yaml
---
version: 1.2.0
---
```

### Minimum Compatible Version

Earliest version consumers can migrate from:

```yaml
---
version: 2.0.0
min-compatible: 1.5.0
---
```

### Deprecation Notice

Signals pending removal:

```yaml
---
version: 1.8.0
deprecated: true
deprecated-in: 1.8.0
removal-in: 2.0.0
successor: path/to/replacement.md
---
```

| Field | Required | Description |
|-------|----------|-------------|
| deprecated | Conditional | Boolean indicating deprecation status |
| deprecated-in | Conditional | Version when deprecation began |
| removal-in | Conditional | Version when artifact will be removed |
| successor | Conditional | Path to replacement artifact |

## Changelog Integration

### Changelog Location

Changelogs accompany versioned artifacts:

| Artifact Scope | Changelog Location |
|----------------|-------------------|
| Single artifact | Adjacent `CHANGELOG.md` |
| Directory | `{directory}/CHANGELOG.md` |
| Repository | Root `CHANGELOG.md` |

### Changelog Entry Format

```markdown
## [{version}] - {YYYY-MM-DD}

### Added
- New feature or capability

### Changed
- Modification to existing behavior

### Deprecated
- Feature marked for future removal

### Removed
- Feature removed from artifact

### Fixed
- Correction to existing behavior
```

### Changelog Categories

| Category | Content |
|----------|---------|
| Added | New features, sections, or capabilities |
| Changed | Modifications to existing content |
| Deprecated | Features marked for future removal |
| Removed | Content deleted from artifact |
| Fixed | Corrections to errors or inaccuracies |

## Breaking Change Criteria

Breaking changes require major version increment:

| Domain | Breaking Change Examples |
|--------|-------------------------|
| Structure | Required section removed, field renamed |
| Schema | Field type changed, constraint tightened |
| Behavior | Process step order changed, output format altered |
| Reference | Target path changed, resolution rules modified |

### Breaking Change Documentation

Document breaking changes explicitly:

```markdown
## [2.0.0] - 2026-06-01

### Changed
- BREAKING: Renamed `scope` field to `focus` in analysis frontmatter
  - Migration: Update all analysis artifacts to use `focus` instead of `scope`
```

## Migration Documentation

### Migration Section

Include migration guidance for breaking changes:

```markdown
### Migration from 1.x to 2.0

1. Rename `scope` field to `focus` in frontmatter
2. Update references from old field name to new
3. Verify validation passes with new schema
```

### Compatibility Period

| Version Relationship | Support Duration |
|---------------------|------------------|
| Current major (N.x.x) | Full support |
| Previous major ((N-1).x.x) | Limited support |
| Older majors | No support |

## Version Lifecycle

### Pre-Release Phase

Artifacts under development:

```yaml
---
version: 0.3.0
status: draft
---
```

- Major version 0 indicates pre-release
- No backward compatibility guarantees
- Frequent breaking changes expected

### Stable Phase

Artifacts ready for consumption:

```yaml
---
version: 1.0.0
status: stable
---
```

- Semantic versioning applies
- Breaking changes require major increment
- Deprecation before removal

### Deprecation Phase

Artifacts being phased out:

```yaml
---
version: 1.8.0
status: deprecated
deprecated: true
successor: path/to/replacement.md
---
```

- New consumers should use successor
- Existing consumers should plan migration
- Functionality maintained until removal version

### Removal

Artifact no longer available:

- Remove artifact file
- Update changelog with removal entry
- Update references to point to successor

## Examples

### Semantic Version

```yaml
---
name: schema-report-discovery
version: 1.2.0
min-compatible: 1.0.0
---
```

### Date-Based Version

```yaml
---
name: monthly-guidelines
version: 2026.05
---
```

### Deprecated Artifact

```yaml
---
name: legacy-validation
version: 1.5.0
deprecated: true
deprecated-in: 1.5.0
removal-in: 2.0.0
successor: skills/validation/objective/reference/structural.md
---
```

## Validation Checklist

- [ ] Version format matches chosen scheme
- [ ] Breaking changes increment major version
- [ ] Changelog exists for versioned artifacts
- [ ] Changelog entries categorized correctly
- [ ] Deprecation includes successor path
- [ ] Migration documentation accompanies breaking changes
- [ ] min-compatible field present when applicable
