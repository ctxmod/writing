# Navigation Structures

Navigation structures guide readers through documents. Where hierarchy defines logical organization and sections build coherent units, navigation provides explicit pathways for movement and orientation. These patterns help readers locate content, track their position, and connect related ideas.

## Navigation by Intent

Reader intent determines navigation strategy. The framework in `reference/principles/writing/docs/audience/intent.md` identifies four distinct modes, each requiring different navigation support.

| Intent | Navigation Style | Primary Pattern |
|--------|------------------|-----------------|
| Learning | Linear progression | Next/previous links, sequential TOC |
| Problem-solving | Goal-oriented | Step numbering, prerequisites |
| Information | Random access | Alphabetical index, search, anchors |
| Understanding | Conceptual threads | Cross-references, related topics |

Learning readers follow guided paths and benefit from sequential navigation. Information seekers need immediate access to specific sections without reading surrounding content. Match navigation investment to document complexity—simple documents need minimal navigation aids, while comprehensive references require robust indexing.

## Table of Contents

Place tables of contents at the document top, immediately after any introductory paragraph. Use clear labels: "Contents" or "On This Page."

**Formatting principles**:

- Use vertical layouts for readability
- Match entries exactly to heading text
- Include H2 and H3 levels at minimum
- Add back-to-top links after major sections in long documents
- Maintain consistent TOC structure across related documents

Readers build mental models of document organization from TOC structure. Inconsistent formatting or omitted headings disrupt these expectations.

## Cross-References

Cross-references connect ideas without interrupting flow. They provide depth for interested readers while allowing others to continue.

**Effective link patterns**:

- Use descriptive phrases: "for authentication details" outperforms "See Authentication"
- Preview subject matter so readers can decide whether to follow
- Prefer stable anchors (section headings) over fragile references (line numbers)
- Distinguish internal from external links when the distinction matters

Link text should set expectations. Readers evaluate whether a link serves their current goal based on the description. Vague references like "click here" or "see more" force unnecessary navigation.

## Signposting

Signposting orients readers within sections. It complements hierarchy by making structure explicit through prose.

**Key patterns**:

- **Section previews**: "This section covers three authentication methods: passwords, tokens, and OAuth."
- **Order phrases**: "First, configure the server. Then, register clients. Finally, test the flow."
- **Bold subheads**: Create scannable landmarks within longer sections
- **Section conclusions**: Synthesize main points or bridge to subsequent content

Signposting reduces cognitive load by setting expectations. Readers who know what comes next process information more efficiently than those navigating blind.

## Breadcrumbs

Breadcrumbs display hierarchical location within a document set: Home > Docs > Writing > Structure.

**Implementation guidelines**:

- Show the path from root to current location
- Make ancestor pages clickable; keep current page as plain text
- Use semantic markup (nav element, aria-label) for accessibility
- Apply to documentation hierarchies where readers navigate between related pages

Breadcrumbs answer "Where am I?" and provide shortcuts to parent contexts. They benefit large documentation systems more than standalone documents.

## Related

See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::structure@documentation/reference/section_hierarchy.md" />.
See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::structure@documentation/reference/section_construction.md" />.
See <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::audience@documentation/reference/reader_intent.md" />.
