# Version Tracking Procedure

Maintain specification version history by recording changes, tracking approvals, and managing deprecation with migration paths. Version tracking ensures specification evolution remains auditable and consumers can identify the current authoritative version.

## Prerequisites

- Specification document exists with initial version
- Version numbering convention established
- Change tracking mechanism available (version control, changelog section, metadata)
- Approval requirements defined per change category

## Steps

1. **Establish version scheme**. Select a versioning convention appropriate to the specification type:
   - **Semantic**: `major.minor.patch` for specifications with backward-compatibility contracts
   - **Sequential**: `v1`, `v2`, `v3` for specifications without compatibility guarantees
   - **Date-based**: `YYYY-MM-DD` for specifications tied to temporal releases
   Document the chosen scheme in specification metadata.

2. **Record version history**. Maintain a history section or separate changelog:
   - Version identifier
   - Date of change
   - Author or approver
   - Summary of changes (added, modified, removed sections)
   - Rationale for significant changes

3. **Classify changes by impact**. Each modification falls into a category:

   | Category | Impact | Approval Required |
   |----------|--------|------------------|
   | Cosmetic | No behavioral change (typos, formatting) | Author only |
   | Clarification | Existing meaning preserved, wording improved | Author + one reviewer |
   | Addition | New requirements or sections added | SME review required |
   | Modification | Existing requirements changed | Full review cycle |
   | Removal | Requirements deleted or deprecated | Full review + migration plan |

4. **Apply change approval**. For each modification:
   - Determine change category
   - Obtain required approvals based on category
   - Record approval in version history
   - Update version number according to scheme

5. **Manage deprecation**. When retiring specification content:
   - Mark deprecated sections with deprecation notice and effective date
   - Provide migration guidance (replacement specification, alternative approach)
   - Set removal timeline (deprecation period)
   - Notify consumers of deprecation

6. **Maintain version accessibility**. Ensure consumers can:
   - Identify current version unambiguously
   - Access previous versions for reference
   - Compare versions to understand changes
   - Determine migration requirements between versions

## Decision Points

**Breaking changes**: When modifications invalidate implementations built against previous versions, treat as major version increment. Provide migration guidance and deprecation period proportional to consumer count.

**Parallel versions**: When multiple specification versions must coexist (phased migration), maintain clear status indicators (current, deprecated, draft) and cross-reference between versions.

**Change batching**: Individual small changes may not warrant version increments. Batch related changes into a single version update with combined changelog entry.

**Retroactive corrections**: Errors discovered in released versions may require corrective updates. Apply corrections to the current version and note the correction in version history referencing the affected previous version.

## Success Criteria

- Version scheme documented and applied consistently
- Version history captures all changes with dates and authors
- Changes classified by impact and approved accordingly
- Deprecated content marked with migration guidance
- Current version identifiable without ambiguity
- Previous versions accessible for reference

## Common Issues

**Version history gaps**: Changes applied without version history updates. Integrate version tracking into the change workflow so history updates happen as part of the change, not after.

**Unclear current version**: Multiple copies or branches create ambiguity about which version is authoritative. Designate a single canonical location; all other copies reference it.

**Deprecation without migration**: Removing content without providing alternatives strands consumers. Require migration guidance as a precondition for deprecation.

**Over-versioning**: Incrementing versions for every minor edit creates noise. Batch cosmetic changes and reserve version increments for substantive modifications.

## Related

- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@specification/reference/sme_review.md" />
- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@specification/reference/migration_planning.md" />
- `ssot` (module `engineering`, profile `principles`, package `design`)
