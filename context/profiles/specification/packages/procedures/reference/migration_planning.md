# Migration Planning Procedure

Plan documentation restructuring with dependency mapping, phased execution, rollback procedures, and consumer notification. Translates organization assessment findings into executable plans that minimize disruption.

## Prerequisites

- Organization assessment completed with restructuring recommendations
- Documentation inventory current (files, classifications, cross-references)
- Consumer dependencies mapped (who references which documents, automated tools)
- Target structure defined (desired directory organization, naming conventions)

## Steps

1. **Map current dependencies**. For each documentation file in the migration scope:
   - Identify inbound references (files linking to this document)
   - Identify outbound references (files this document links to)
   - Identify external references (URLs, bookmarks, CI/CD configurations, scripts)
   - Identify automated consumers (documentation generators, search indexes, link checkers)

2. **Define target state and redirects**. Describe the desired outcome:
   - Target directory structure with file placement
   - New naming conventions applied
   - Cross-reference updates required
   - Redirect strategy: create redirects from old paths, schedule removal timeline

3. **Identify migration units**. Group files into independently migratable units:
   - Files with shared dependencies that must move together
   - Files with no external dependencies (migrate first as low-risk)
   - Files with many consumers (migrate last with maximum preparation)

4. **Sequence migration phases**. Order migration units by dependency and risk:

   | Phase | Target | Criteria |
   |-------|--------|----------|
   | Phase 1 | Low-dependency files | Few inbound references, no automation dependencies |
   | Phase 2 | Internal documentation | Files referenced only by other documentation |
   | Phase 3 | Cross-referenced files | Files referenced by code, configuration, or automation |
   | Phase 4 | High-traffic files | Entry points, frequently accessed references |

5. **Create execution checklist**. Per phase:
   - [ ] Pre-migration backup completed
   - [ ] Files moved to target locations
   - [ ] Redirects established
   - [ ] Inbound references updated
   - [ ] Outbound references verified
   - [ ] Automated consumers updated
   - [ ] Consumers notified
   - [ ] Verification tests passed
   Rollback triggers: broken references, consumer complaints
   Rollback steps: restore backup, verify success

6. **Estimate effort and timeline**. For each phase:
   - File count and complexity
   - Reference update count
   - Consumer notification requirements
   - Testing and verification effort
   - Buffer for unexpected issues

## Decision Points

**Big-bang vs phased migration**: Small documentation sets (<30 files) may benefit from single-phase migration. Large sets require phased approach to manage risk.

**Redirect duration**: Internal documentation may use short redirect periods (2-4 weeks). External-facing documentation may require longer periods (3-6 months) or permanent redirects.

**Automated reference updates**: Batch reference updates reduce manual effort when tools can update programmatically. Verify automated updates with spot checks.

**Migration scope expansion**: Capture additional restructuring opportunities as future phases rather than expanding current scope.

## Success Criteria

- All file dependencies mapped (inbound, outbound, external, automated)
- Target state defined with directory structure and naming
- Migration phases sequenced by risk and dependency
- Redirect strategy defined per moved file
- Rollback procedures documented per phase
- Execution checklist prepared per phase
- Effort estimates produced for scheduling

## Common Issues

**Hidden dependencies**: References in scripts, CI/CD configurations, or external tools may not appear in documentation-only searches. Extend dependency scanning to code and configuration.

**Redirect accumulation**: Successive migrations create redirect chains. Audit and collapse chains during each migration.

**Consumer resistance**: Consumers accustomed to existing organization may resist changes. Communicate benefits and provide clear mapping.

**Incomplete reference updates**: Missing updates creates broken links. Use automated link checking after each phase.

## Related

- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@documentation/reference/inventory.md" />
- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@documentation/reference/organization_assessment.md" />
- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@specification/reference/version_tracking.md" />
- `ssot` (module `engineering`, profile `principles`, package `design`)
