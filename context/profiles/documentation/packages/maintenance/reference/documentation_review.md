# Documentation Review

Reviews prevent documentation decay by catching errors, enforcing standards, and identifying drift from implementation. Systematic review processes maintain documentation quality over time.

## Review Triggers

Reviews occur in response to specific events rather than arbitrary schedules.

| Trigger | Scope | Timing |
|---------|-------|--------|
| Pre-merge | All documentation changes | Before integration |
| Scheduled | High-traffic files, entry points | Quarterly |
| Signal-based | Files with reader reports or implementation drift | As signals emerge |
| Pattern update | Files using superseded approaches | After pattern changes |

Pre-merge reviews catch issues early. Scheduled reviews detect gradual decay in stable content. Signal-based reviews respond to specific quality indicators.

## Reviewer Roles

Different review aspects require different expertise.

| Role | Focus | Qualifications |
|------|-------|----------------|
| Technical reviewer | Accuracy, completeness, correctness | Domain expertise |
| Writing reviewer | Style standards, anti-patterns, clarity | Writing guidelines familiarity |

Rotate roles across team members to prevent bottlenecks and spread knowledge. A single reviewer can fill both roles when qualified, though separation improves thoroughness.

## Quality Gates

Reviews proceed in two phases: automated checks followed by human evaluation.

### Phase 1: Automated

Automated checks run before human review begins:

- **Link integrity**: All references resolve to existing files
- **Style linting**: Flagged words and phrases from anti-patterns
- **Metadata validity**: Required fields present and correctly formatted
- **Structure compliance**: Heading hierarchy, section length limits

Failed automated checks block human review. Fix issues and resubmit.

### Phase 2: Human

Human reviewers evaluate aspects automation cannot assess.

**Technical accuracy**:
- Claims match current implementation
- Examples execute correctly
- Version-specific content reflects correct versions

**Cognitive load**:
- Information disclosed progressively
- No walls of text without structure
- Appropriate use of tables, lists, and prose

**Writing standards**:
- Anti-patterns eliminated
- Clarity principles followed
- Voice and tone consistent

See `anti_patterns` (module `writing_context`, profile `core`, package `basics`).
See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::basics@core/reference/clarity_principles.md" />.

## Review Process

Reviews follow a structured sequence to ensure consistency.

1. **Scope check**: Limit reviews to 400 lines per session. Larger changes require multiple review cycles.
2. **Author annotation**: Authors explain significant changes to guide reviewer attention.
3. **Parallel evaluation**: Technical and writing reviews proceed simultaneously when reviewers differ.
4. **Gate resolution**: Failed gates require fixes and complete re-review of affected sections.
5. **Approval**: Both technical and writing approval required before merge.

Document review decisions for future reference. Patterns in review feedback inform style guide updates.

## Related

Content evolution describes the lifecycle that reviews support.
See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::maintenance@documentation/reference/content_evolution.md" />.
