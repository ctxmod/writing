# Reader Expertise

Documentation serves readers with different knowledge levels. Expertise calibration adjusts technical density, assumed context, and jargon usage to match the reader's background. Miscalibration—writing for experts when beginners will read, or over-explaining for experts—wastes reader attention and damages trust.

This principle applies to human readers. For agent context optimization, see `context_efficiency` (module `writing_context`, profile `core`, package `density`). Agents process density differently than humans—they benefit from high signal-to-noise ratios without progressive disclosure.

## Expertise Levels

Three expertise levels define distinct calibration targets:

| Level | Characteristic | Goal | Context Assumption |
|-------|----------------|------|-------------------|
| Beginner | Learning fundamentals | Understand what and why | Minimal domain knowledge |
| Intermediate | Building competence | Apply concepts to tasks | Core terminology known |
| Expert | Seeking precision | Reference specifics, edge cases | Full domain fluency |

### Beginner

Beginners encounter concepts for the first time. They need context that experts take for granted. Documentation for beginners explains what something is before explaining how to use it. Analogies to familiar concepts reduce cognitive load.

Effective patterns: Start with outcomes, provide complete examples, explain terminology inline, use consistent vocabulary throughout.

### Intermediate

Intermediates understand fundamentals and seek application. They know core concepts but need guidance connecting them to tasks. Documentation for intermediates assumes familiarity with basics and focuses on procedural clarity.

Effective patterns: State goals immediately, list prerequisites concisely, provide step-by-step procedures, note common variations.

### Expert

Experts seek precision and completeness. They resent time spent on explanations they already understand. Documentation for experts maximizes information density—specifications, edge cases, implementation details.

Effective patterns: Dense reference tables, precise specifications, minimal prose, comprehensive coverage.

## Jargon Calibration

Technical terminology serves precision when readers share understanding. It creates barriers when they do not.

| Level | Jargon Threshold | Definition Strategy |
|-------|------------------|---------------------|
| Beginner | Define all domain terms | Inline definitions on first use |
| Intermediate | Core terms assumed | Define specialized or novel terms |
| Expert | Full vocabulary assumed | Define only when introducing new concepts |

The threshold determines which terms require explanation. Beginners need explicit definitions for "API," "latency," and "configuration." Intermediates know these but may need "idempotent" or "eventually consistent" explained. Experts require definitions only for terms you invented.

For general guidance on technical term usage, see reference/principles/writing/clarity.md:76-87.

## Technical Density

Density measures information per unit of text. Higher density serves experts efficiently. Lower density gives beginners time to absorb concepts.

**Density indicators**:
- Concepts per paragraph (1-2 for beginners, 3-4 for experts)
- Assumption frequency (few assumptions for beginners, many for experts)
- Example-to-explanation ratio (more examples for beginners)

**Calibration strategies**:

For high density (experts): Replace explanatory prose with tables. Use precise specifications. Omit rationale for established patterns. Trust reader competence.

For low density (beginners): One concept per section. Explain rationale before mechanics. Provide working examples before variations. Use consistent terminology without synonyms.

## Progressive Disclosure

Mixed audiences benefit from layered information. Progressive disclosure reveals complexity incrementally—basic information visible immediately, advanced details available on demand.

**Implementation patterns**:

*Summary-then-detail*: Open with what readers need to know, follow with how it works internally. Beginners stop at the summary; experts continue to implementation details.

*Graduated examples*: Start with minimal working examples, then show variations and edge cases. Beginners use the basic example; experts reference the variations.

*Explicit audience markers*: Label sections by intended audience when a single document must serve multiple levels. "For advanced usage" signals beginners to skip; "Basic overview" signals experts to skim.

## Single-Audience Preference

When possible, write separate documents for different expertise levels rather than forcing mixed-audience compromise. A dedicated beginner guide serves beginners better than a mixed document that experts find tedious and beginners find incomplete.

Separate when:
- Expertise levels differ substantially
- Content length warrants multiple documents
- Different intents (learning vs reference) apply

Combine when:
- Audience expertise is uniform
- Content is short enough for progressive disclosure
- Separating would fragment closely related information

## Audience Assessment

Determine reader expertise by context:

| Context | Typical Audience |
|---------|-----------------|
| Getting started guides | Beginners |
| How-to procedures | Intermediates |
| API references | Experts |
| Troubleshooting guides | Intermediates to experts |
| Architecture documents | Experts |

When uncertain, err toward lower expertise. Over-explaining briefly annoys experts. Under-explaining loses beginners entirely.

## Integration

Expertise calibration intersects with other principles:

- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::audience@documentation/reference/reader_intent.md" /> - Expertise and intent together determine structure. A beginner with learning intent needs tutorials; an expert with information intent needs reference docs.
- `kiss` (module `engineering`, profile `principles`, package `design`) - Match complexity to reader knowledge. Simple interfaces for beginners; complete interfaces for experts.
- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::basics@core/reference/clarity_principles.md" /> - Beginners have higher intrinsic load from unfamiliarity. Reduce extraneous load through clear structure and consistent terminology.
