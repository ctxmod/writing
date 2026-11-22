# Diagram Standards Procedure

Define standards for visual documentation: architecture, sequence, flowchart, and state machine diagrams. Covers notation, tooling, labeling, and prose integration.

## Prerequisites

- Diagram purpose identified (architecture overview, interaction flow, state transitions, data flow)
- Target audience defined (determines detail level)
- Rendering environment known (Markdown-embedded, standalone image, interactive)
- Tooling availability confirmed

## Steps

1. **Select diagram type**:

   | Information | Diagram | Notation |
   |-------------|---------|----------|
   | Component relationships | Architecture | Boxes/arrows, C4 |
   | Temporal interactions | Sequence | UML, Mermaid |
   | Decision logic | Flowchart | Standard symbols |
   | State transitions | State machine | UML statechart |
   | Data movement | Data flow | DFD |
   | Hierarchical structure | Tree | Nested boxes |

2. **Apply notation conventions**. Use consistent visual elements:
   - **Components**: Labeled rectangles with type indicators
   - **Connections**: Directed arrows with relationship labels
   - **Boundaries**: Dashed rectangles for system or trust boundaries
   - **Annotations**: Brief notes attached to elements requiring explanation
   - **Color**: Functional grouping only, not decorative. Ensure readability without color (accessibility).

3. **Set detail level** appropriate to audience and purpose:
   - **Overview**: 5-10 elements maximum. Shows major components and primary relationships.
   - **Detailed**: 10-25 elements. Shows subcomponents and secondary relationships.
   - **Implementation**: 25+ elements. Shows specific interfaces, protocols, and data formats.

   When a diagram exceeds its target detail level, split into multiple diagrams at different abstraction levels.

4. **Write labels**. Every element requires:
   - Descriptive name (noun for components, verb for actions)
   - Type indicator when not obvious from context
   - Technology/protocol label on connections when relevant

5. **Integrate with prose**. Each diagram must:
   - Appear near the prose section it illustrates
   - Include a caption describing what the diagram shows
   - Reference specific elements in surrounding text
   - Avoid conveying information available only in the diagram (prose must stand alone)

6. **Choose rendering format**:
   - **Text-based** (Mermaid, PlantUML): Version-controllable, diff-friendly
   - **Structured data** (D2, Graphviz DOT): Programmatic generation
   - **Visual tools** (draw.io, Excalidraw): Flexible layout
   Store source files alongside rendered output.

7. **Validate and maintain diagrams**. Verify that:
   - All referenced components exist in the system
   - Connections represent actual relationships
   - Labels match terminology used in prose documentation
   - Diagram reflects current state, not historical or planned state
   - Creation or review dates marked; source included in review scope

## Decision Points

**Format selection**: Text-based diagrams (Mermaid, PlantUML) integrate with version control and render in documentation pipelines. Visual tools produce better layouts for complex diagrams. When a system requires both overview and detail, create separate diagrams at each abstraction level linked through consistent component naming.

## Success Criteria

- Diagram type matches information being conveyed
- Notation follows defined conventions consistently
- Detail level appropriate for audience
- All elements labeled with descriptive names
- Diagram integrated with surrounding prose
- Source files stored alongside rendered output
- Diagram verified against current system state

## Common Issues

**Over-detailed diagrams**: Diagrams attempting to show everything become unreadable. Apply detail level guidelines and split when necessary.

**Orphaned diagrams**: Diagrams without surrounding prose context lack interpretive framework. Always embed diagrams within explanatory sections.

**Inconsistent notation**: Different diagrams using different conventions. Establish project-level notation standards.

**Accessibility gaps**: Diagrams conveying information exclusively through color exclude color-blind readers. Use shape, pattern, and label differences alongside color.

## Related

- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@documentation/reference/api_documentation.md" />
- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@documentation/reference/runbook_creation.md" />
- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::basics@core/reference/clarity_principles.md" />
