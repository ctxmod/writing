# Content Evolution

Documentation follows a lifecycle from creation through maintenance to eventual removal. Managing this lifecycle prevents information rot and keeps content aligned with the systems it describes.

## Content Lifecycle

Documentation progresses through four stages: creation, maintenance, deprecation, and deletion. Each stage requires different actions.

Creation occurs when new concepts emerge. Maintenance ensures content remains accurate as systems change. Deprecation marks content as outdated while providing transition paths. Deletion removes content that no longer serves readers.

The lifecycle applies to individual files and sections within files. A section may become deprecated while its parent file remains active.

## Creation Triggers

Create new documentation when concepts require dedicated treatment. Three signals indicate the need:

**Scope expansion**: An existing file would exceed reasonable length if expanded.

**Multiple consumers**: Several files reference the same information, suggesting extraction to a shared source.

**Distinct audience**: The content serves readers with different needs than existing documentation.

Before creating, verify no existing file covers the topic.

## Maintenance Signals

Content requires attention when accuracy degrades.

| Signal | Response |
|--------|----------|
| Implementation differs from documentation | Update documentation to match current behavior |
| Multiple files describe the same concept | Extract to single source, update references |
| Readers report confusion | Clarify language or restructure content |
| Pattern superseded by better approach | Update guidance, document migration path |

Regular review catches problems before they compound.

## Versioning Strategies

Version documentation when significant changes affect readers. Minor corrections do not require versioning. Breaking changes and major restructuring do.

**Semantic approach**: Major versions indicate breaking changes. Minor versions cover additions and non-breaking updates. Patch versions address corrections.

Version identifiers belong in changelogs, not scattered across individual files.

## Changelog Integration

Changelogs record what changed, when, and why.

```markdown
## [2.0.0] - 2026-06-15

### Added
- Authentication flow documentation

### Changed
- API endpoint paths for v2 migration

### Deprecated
- Legacy authentication (see migration guide)
```

Categories clarify intent: Added introduces new content, Changed modifies existing content, Deprecated signals future removal, Removed confirms deletion.

## Migration Documentation

Migration guides help readers transition between versions.

| Component | Purpose |
|-----------|---------|
| Summary | What changed and why |
| Impact | Who needs to act |
| Steps | Specific actions to take |
| Examples | Before and after comparisons |

Keep migration guides concise. Link to detailed explanations rather than embedding them.

## Deprecation Process

Deprecation provides transition time before removal.

**Deprecation notice template**:

```markdown
> **Deprecated**: This approach is no longer recommended.
>
> **Reason**: [Brief explanation of why]
> **Alternative**: See [current approach](link)
> **Removal**: Scheduled for [version or date]
```

Place deprecation notices at the section or file start. Deprecation duration should match user impact.

## Deletion Criteria

Delete documentation when it no longer serves readers.

**Ready for deletion when**:

- [ ] Content describes functionality that no longer exists
- [ ] No internal or external references remain
- [ ] Deprecation period has elapsed
- [ ] Replacement documentation covers the topic adequately

Archive selectively. Keep archives for content with historical significance.

## Related

Single source of truth prevents version conflicts by centralizing information.
See `ssot` (module `engineering`, profile `principles`, package `design`).

Reference mechanisms maintain currency as sources change.
See `reference_over_duplication` (module `writing_context`, profile `core`, package `density`).

Clear communication supports effective migration guides.
See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::basics@core/reference/clarity_principles.md" />.
