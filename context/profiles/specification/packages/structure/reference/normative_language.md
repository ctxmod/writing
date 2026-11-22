# Normative Language

Technical specifications use RFC 2119 and RFC 8174 keywords to indicate requirement levels with precise conformance semantics.

## RFC 2119 Keywords

RFC 2119 defines keywords that express requirement strength in technical standards. These keywords enable precise communication about what implementations must, should, or may do. RFC 8174 (published in 2017) clarifies that only ALL CAPS variants carry normative weight—a distinction that resolves significant ambiguity in earlier interpretations.

| Keyword | Meaning | Use When |
|---------|---------|----------|
| **MUST** | Absolute requirement | Violation breaks interoperability |
| **MUST NOT** | Absolute prohibition | Action would cause harm or failure |
| **REQUIRED** | Synonym for MUST | Emphasizing requirement nature |
| **SHALL** | Synonym for MUST | Legal or formal contexts |
| **SHOULD** | Strong recommendation | Deviation requires justification |
| **SHOULD NOT** | Strong negative recommendation | Usage requires justification |
| **RECOMMENDED** | Synonym for SHOULD | Best practice emphasis |
| **MAY** | Truly optional | No interoperability impact |
| **OPTIONAL** | Synonym for MAY | Feature flagging |

### Capitalization Rule

Only UPPERCASE keywords carry normative weight. Lowercase variants are ordinary prose with no binding effect. This distinction is the most significant clarification since RFC 2119's original publication.

**Normative (binding)**:
> Implementations MUST validate input before processing.

**Informative (non-binding)**:
> Implementations must be careful with user input.

The lowercase "must" creates no conformance requirement. Readers encountering the first example understand they face a formal obligation. The second example provides guidance without binding force. This distinction enables specifications to discuss concepts using everyday language while reserving UPPERCASE keywords for actual requirements.

### Keyword Frequency Guidelines

| Document Type | MUST | SHOULD | MAY |
|---------------|------|--------|-----|
| Core protocol | High | Medium | Low |
| API specification | Medium | High | Medium |
| Best practices | Low | High | High |
| Informative annex | None | Low | Medium |

Use MUST sparingly. Every MUST creates a hard conformance requirement that implementations cannot deviate from. When a specification contains too many MUST requirements, implementations become brittle—any legitimate variation fails conformance testing. SHOULD provides flexibility for best practices where deviation may be justified in specific contexts.

### Relationship to Validation Severity

A validation framework that grades its findings maps RFC 2119 keywords to severity levels, typically as follows:

| RFC 2119 Keyword | Severity | Meaning |
|------------------|--------------|---------|
| MUST / MUST NOT | Error | Absolute requirement, must fix |
| SHOULD / SHOULD NOT | Warning | Strong recommendation, should fix |
| MAY / OPTIONAL | Info | Truly optional, may fix |

See the `validation_objective` skill (module `agentic`, profile `workflows`).

## Normative vs Imperative

Normative language and imperative language serve different purposes. Understanding this distinction prevents misapplication of RFC 2119 keywords in contexts where they create unnecessary rigidity.

Normative language (RFC 2119 keywords) defines conformance requirements with binary pass/fail outcomes. Each normative statement becomes a test case: either an implementation satisfies the requirement or it fails conformance. Imperative language provides behavioral directives without formal compliance semantics. Imperative statements guide action without creating formal verification obligations.

| Aspect | Normative | Imperative |
|--------|-----------|------------|
| Purpose | Conformance requirements | Action directives |
| Scope | Formal specifications | General guidance |
| RFC 2119 | Yes (MUST/SHOULD/MAY) | No |
| Testability | Binary pass/fail | Context-dependent |
| Typical usage | Schemas, validation procedures | Rules, commands, commits |

**Pattern examples from an agent-context repository**:

- **Rule (imperative)**: "Main agents pass report paths; they never read intermediate reports"
- **Git commit (imperative)**: "Add normative language style guide"
- **Schema (normative)**: "Implementations MUST provide a `name` field matching pattern `^[a-z][a-z0-9-]*$`"

Most agent-context files (rules, skills, prompts) use imperative language. Reserve normative language for formal conformance requirements.

## Conformance Classes

Define explicit classes of implementations with their requirements. Conformance classes answer the question "who must comply?" by identifying distinct implementation categories. Each class receives a definition followed by MUST, SHOULD, and MAY statements that apply specifically to that class.

**Example conformance class structure**:

> **Note**: The following examples illustrate conformance class structure. Formal specifications using normative language appear primarily in schema definitions and validation procedures.

```markdown
### Parser

A **Parser** converts input text into in-memory structure.

A conforming Parser:
- MUST accept all valid input as defined in Section 3
- MUST reject invalid input with a diagnostic message
- SHOULD provide line/column information in error messages
- MAY offer auto-correction suggestions

### Validator

A **Validator** verifies structure against schemas.

A conforming Validator:
- MUST detect all constraint violations defined in Section 4
- MUST report violations with the constraint identifier
- MAY provide auto-correction suggestions
```

### Conformance Statement Pattern

Each conformance class contains:

1. **Definition**: What kind of component or system
2. **MUST requirements**: Absolute necessities
3. **SHOULD requirements**: Strong recommendations
4. **MAY requirements**: Optional features

This progression from mandatory to optional creates a clear hierarchy. Readers immediately understand which requirements are absolute and which allow flexibility. Without explicit conformance classes, requirements like "MUST validate input" become ambiguous—every component type might interpret the requirement differently.

## Writing Normative Requirements

Every normative requirement must be testable with objective pass/fail criteria. Testability is the primary quality metric for normative statements. A requirement that cannot be verified provides no value as a conformance criterion.

### Structure Pattern

```markdown
### X.Y Requirement Name

[Context explaining why this matters]

A [conformance class] **MUST** [specific action]:

1. [Sub-requirement 1]
2. [Sub-requirement 2]

**Rationale**: [Why this requirement exists]

**Example**: [Concrete illustration]
```

### Good vs Poor Requirements

| Quality | Requirement | Analysis |
|---------|-------------|----------|
| Poor | "Implementations should handle errors properly" | Vague, untestable |
| Good | "When validation fails, implementations MUST return an error object containing `code`, `message`, and `location`" | Specific, verifiable |

### Testability Criterion

| Requirement | Testable | Why |
|-------------|----------|-----|
| "MUST validate JSON" | Yes | Feed invalid JSON, check rejection |
| "MUST be efficient" | No | No measurable threshold |
| "MUST reject resources > 100MB" | Yes | Specific threshold |
| "SHOULD be user-friendly" | No | Subjective |

Every MUST and SHOULD statement requires a verification method. Define measurable criteria, not subjective qualities. When writing a requirement, ask: "How would someone test this?" If the answer involves subjective judgment, reframe the requirement with specific, observable criteria.

SHOULD requirements also need testability. The difference is that SHOULD violations require documented justification rather than automatic failure. An implementation that deviates from SHOULD requirements remains conformant if it explains why the deviation is acceptable for its context.

See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::basics@core/reference/clarity_principles.md" />.

## Informative Content

Mark non-normative content explicitly to prevent confusion. Specifications contain both normative requirements and supporting material (examples, rationale, implementation tips). Without clear marking, readers may treat examples as requirements or dismiss actual requirements as mere suggestions.

### Notes

```markdown
> **Note**: This algorithm is one possible approach. Implementations
> MAY use alternative algorithms that produce equivalent results.
```

### Examples

```markdown
> **Example**: The following shows typical usage. This is
> informative and not required for conformance.
```

### Rationale

```markdown
> **Rationale**: This requirement exists because early implementations
> encountered interoperability issues when [specific scenario].
```

### Informative Annexes

```markdown
## Annex A: Implementation Tips (Informative)

This annex provides non-normative guidance for implementers.
```

Clear separation between normative and informative content prevents readers from treating examples or explanations as requirements.

## Common Mistakes

Avoid these pitfalls when writing normative requirements. Each mistake reduces specification clarity and makes conformance testing unreliable.

### Overusing MUST

**Problem**: Every requirement is MUST, making specifications brittle.

**Fix**: Reserve MUST for true interoperability requirements. Use SHOULD for best practices.

### Ambiguous Scope

**Problem**: "MUST validate the input" (who? how?)

**Fix**: "A conforming Parser MUST reject input containing invalid UTF-8 sequences, returning error code `E001`"

### Mixing Normative and Informative

**Problem**: "Implementations MUST be careful, and should consider sandboxing"

The lowercase "should" appears normative but carries no binding weight. Readers cannot determine whether "sandboxing" is a strong recommendation or casual advice.

**Fix**: Separate into distinct statements with consistent capitalization:

```markdown
Implementations MUST validate untrusted input before processing.
Implementations SHOULD use sandboxing for additional security.
```

### Undefined Terms

**Problem**: Using technical terms without definitions.

**Fix**: Create a Terminology section defining all domain-specific terms:

```markdown
## 1. Terminology

**Document**
: A complete artifact consisting of metadata and content nodes.

**Valid**
: Conforming to all MUST requirements in this specification.
```

Terms defined in the Terminology section have precise meanings throughout the specification. This prevents interpretation disputes.

### Self-Referential Requirements

**Problem**: "Documents MUST be valid" (circular—what defines validity?)

**Fix**: Define validity in terms of specific, checkable properties.

See `anti_patterns` (module `writing_context`, profile `core`, package `basics`).

## When to Use Normative Language

Normative language is powerful but easily overused. Apply it selectively. Every RFC 2119 keyword creates a formal obligation requiring systematic verification. Documents that overuse normative keywords become difficult to implement and test.

**Use normative language when**:

- Writing schema definitions with field requirements
- Defining validation procedures with conformance criteria
- Creating formal specifications (in spec-scoped paths)
- Documenting API or protocol contracts
- Writing acceptance criteria with pass/fail outcomes

**Do NOT use normative language when**:

- Writing general reference files (explaining concepts)
- Authoring rules (behavioral guidance, not conformance)
- Creating commands (orchestration templates)
- Defining agents (context setup)
- Writing reports or work items (narrative documentation)

### Context File Category Guidance

| Category | Use Normative? | Example |
|----------|----------------|---------|
| Schema definitions | Yes | "Implementations MUST provide `name` field" |
| Validation procedures | Yes | "Conforming artifacts MUST include required sections" |
| General reference | No | "Agents read files to understand context" |
| Rules | No | "Main agents pass report paths" (imperative) |
| Commands | No | "Launch discovery agent" |
| Agents | No | "This agent analyzes code structure" |
| Reports | No | "Analysis revealed three issues" |

When in doubt, use imperative language. Normative language creates formal obligations that require systematic verification. The scope a file lives in determines what assumptions it can make. A file scoped to specification work (a specification profile or package, selected only for that work) can assume specification context and use normative language freely. A file in a general scope (core writing guidance, selected for every task) must remain applicable to all artifact types.

## Related

See `standards` (module `agentic`, profile `workflows`, skills `validation_procedure` and `validation_objective`).
