# Reader Intent

Documentation serves different cognitive modes. Readers approach technical content with specific goals: learning new concepts, solving immediate problems, retrieving known facts, or building deeper understanding. The reader's intent determines optimal structure, not the author's preferences.

This principle applies to human readers. For agent context optimization, see `context_efficiency` (module `writing_context`, profile `core`, package `density`). Human cognition differs from token budgets—humans benefit from structured navigation and progressive disclosure, while agents benefit from density and reference minimization.

## Intent Framework

Four distinct reader intents require four distinct structural approaches:

| Intent | Reader Goal | Cognitive Mode | Primary Value |
|--------|-------------|----------------|---------------|
| Learning | Acquire new skills | Guided exploration | Safe environment to practice |
| Problem-solving | Complete a task | Focused execution | Direct path to solution |
| Information | Retrieve specific facts | Quick lookup | Immediate answers |
| Understanding | Build mental models | Deep contemplation | Conceptual connections |

### Learning Intent

Readers with learning intent need guided progression through unfamiliar territory. They benefit from sequenced steps, concrete examples, and meaningful exercises. The structure should prevent failure—learners gain confidence through successful completion.

Effective learning documentation: starts with achievable goals, provides complete working examples, progresses from simple to complex, and explains each step's purpose.

### Problem-Solving Intent

Readers solving problems already possess background knowledge. They need direct routes to solutions without conceptual preambles. The structure should assume competence and provide actionable steps.

Effective problem-solving documentation: states the goal immediately, lists prerequisites concisely, provides step-by-step instructions, and addresses common variations.

### Information Intent

Readers seeking information want facts, not narrative. They know what they need and want to find it quickly. The structure should optimize for scanning and random access.

Effective information documentation: uses consistent formatting, provides complete coverage, enables quick navigation, and states facts without elaboration.

### Understanding Intent

Readers building understanding want to know why, not just how. They seek conceptual frameworks and design rationale. The structure should connect ideas and explore alternatives.

Effective understanding documentation: explains context and history, discusses trade-offs and alternatives, connects to broader principles, and addresses edge cases.

## Structural Signatures

Each intent produces observable patterns:

| Intent | Typical Length | Structure Pattern | Navigation Style |
|--------|----------------|-------------------|------------------|
| Learning | 1000-3000 words | Sequential chapters | Linear progression |
| Problem-solving | 300-800 words | Numbered steps | Goal-oriented |
| Information | Variable | Tables, lists | Random access |
| Understanding | 800-2000 words | Topical sections | Conceptual threads |

## Example: Authentication

The same topic structures differently by intent:

| Intent | Title | Opening |
|--------|-------|---------|
| Learning | "Build Your First Auth System" | "In this tutorial, you'll implement password-based authentication..." |
| Problem-solving | "Add OAuth to Existing App" | "Prerequisites: running app with user model. Steps: 1. Install provider..." |
| Information | "Auth API Reference" | "POST /auth/login - Parameters: email (string), password (string)..." |
| Understanding | "Authentication Architecture" | "Authentication balances security against user friction. This document examines..." |

## Integration

Reader intent intersects with other principles:

- `kiss` (module `engineering`, profile `principles`, package `design`): Match complexity to reader's current knowledge level
- **Cognitive load**: Learning intent requires lower density than information intent
- `context_efficiency` (module `writing_context`, profile `core`, package `density`): Different intents tolerate different levels of detail

Structure documents around reader goals. A single document rarely serves multiple intents well—separate them or clearly delineate sections by intent.

## Related

This framework derives from Daniele Procida's Diátaxis system, which maps documentation types across two axes: theory versus practice, and acquisition versus application.

See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::audience@documentation/reference/expertise.md" />.
See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::basics@core/reference/clarity_principles.md" />.
