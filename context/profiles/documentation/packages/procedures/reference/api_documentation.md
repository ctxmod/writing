# API Documentation Procedure

Create reference documentation for APIs by extracting information from source code annotations, type definitions, and usage patterns. Produces structured API references with endpoint descriptions, parameter schemas, response formats, and usage examples.

## Prerequisites

- API source code accessible (endpoints, handlers, type definitions)
- API conventions identified (REST, GraphQL, RPC, library API)
- Output format defined (Markdown, OpenAPI, generated HTML)
- Code coverage analysis completed (identifies undocumented endpoints)

## Steps

1. **Inventory API surface**. Catalog all public interfaces:
   - Endpoints with HTTP methods and paths (REST APIs)
   - Query and mutation definitions (GraphQL APIs)
   - Exported functions and types (library APIs)
   - RPC service definitions and methods (gRPC/RPC APIs)
   Record each entry with its source location.

2. **Extract type information**. For each interface, document:
   - Input parameters with types, constraints, and defaults
   - Return types with field descriptions
   - Error types and conditions
   - Authentication and authorization requirements

3. **Document request/response contracts**. For each endpoint or function:
   - Describe purpose in one sentence
   - List parameters with type, required/optional status, and validation rules
   - Describe response structure with field meanings
   - Note side effects and state changes

4. **Create usage examples**. For each documented interface:
   - Provide a minimal working example showing correct invocation
   - Include expected response or return value
   - Add error case examples for common failure modes
   - Use realistic but simplified data values

5. **Organize by domain**. Group related endpoints or functions under domain headings rather than alphabetical listing. Within each group, order by typical usage flow (create before read, list before detail).

6. **Add navigation aids**. Include:
   - Table of contents for documents exceeding 20 entries
   - Quick-reference table listing all endpoints with method, path, and summary
   - Cross-references between related endpoints

7. **Validate completeness**. Verify every public interface has documentation covering purpose, parameters, responses, and at least one example. Flag gaps.

## Decision Points

**Auto-generated vs hand-written**: When source code uses structured annotations (OpenAPI decorators, JSDoc, Go doc-comments), auto-generate base documentation and supplement with hand-written context. When annotations are sparse, write documentation manually from source analysis.

**Versioned APIs**: Document the current version. For breaking changes, note migration paths from previous versions. Maintain version indicators in headings or metadata.

**Internal vs external APIs**: Internal APIs may require less formal documentation. Apply full procedure to external-facing APIs; use abbreviated documentation for internal interfaces.

**Unstable interfaces**: Mark experimental or unstable APIs clearly. Include stability indicators and expected timeline for stabilization.

## Success Criteria

- All public API endpoints or functions documented
- Parameter types, constraints, and defaults specified
- Response structures documented with field descriptions
- Usage examples provided per endpoint
- Documentation organized by domain with navigation aids
- No undocumented public interfaces in final output

## Common Issues

**Schema drift**: API implementation evolves faster than documentation. Integrate documentation updates into development workflow through review checklists.

**Over-documentation of internals**: Documenting private implementation details creates maintenance burden. Focus on public contracts; reference source code for implementation details.

**Example staleness**: Examples that no longer work erode trust in documentation. Validate examples against current implementation when feasible.

**Complex nested types**: Deeply nested request or response types resist flat documentation. Use hierarchical formatting or reference shared type definitions to avoid repetition.

## Related

- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@documentation/reference/code_coverage_analysis.md" />
- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@documentation/reference/diagram_standards.md" />
- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::basics@core/reference/clarity_principles.md" />
