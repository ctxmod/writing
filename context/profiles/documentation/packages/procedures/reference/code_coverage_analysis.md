# Code Coverage Analysis Procedure

Identify code units that lack corresponding documentation by comparing source code inventory against existing documentation. Produces a prioritized gap list that guides subsequent documentation creation efforts.

## Prerequisites

- Source code directory accessible for scanning
- Documentation inventory completed or documentation directory identified
- Code unit granularity defined (package, module, class, function, endpoint)

## Steps

1. **Scan source code units**. Extract documentable entities at the chosen granularity:
   - Packages or modules with public interfaces
   - Exported types, functions, and constants
   - API endpoints and routes
   - Configuration schemas and options
   Record each unit with its location, visibility (public/private), and approximate complexity.

2. **Scan existing documentation**. Catalog documentation files that describe code behavior. Map each documentation file to the code units it covers, using:
   - Explicit references (file paths, import statements, type names)
   - Directory structure alignment (docs mirroring source layout)
   - Content analysis (matching code identifiers in prose)

3. **Compute coverage matrix**. For each code unit, determine documentation status:

   | Status | Definition |
   |--------|-----------|
   | Documented | Dedicated documentation exists with substantive content |
   | Partially documented | Mentioned in documentation but lacks detail |
   | Undocumented | No corresponding documentation found |
   | Self-documenting | Inline comments or doc-comments provide sufficient coverage |

4. **Calculate coverage metrics**. Produce aggregate statistics:
   - Overall coverage percentage
   - Coverage by category (packages, types, functions)
   - Coverage by visibility (public vs private)

5. **Prioritize gaps**. Rank undocumented units by impact:
   - Public API surface (highest priority)
   - Cross-module dependencies
   - Complex logic (cyclomatic complexity, line count)
   - Usage frequency (import count, call frequency)

6. **Produce gap report**. List undocumented and partially documented units with priority ranking, suggested documentation type, and estimated effort.

## Decision Points

**Granularity selection**: Finer granularity (function-level) produces comprehensive coverage data but increases analysis time. Start at module level; drill into specific modules only when coverage questions arise.

**Inline documentation sufficiency**: Some code uses doc-comments extensively. Decide whether inline documentation satisfies coverage requirements or whether separate documentation is also needed.

**Generated code**: Auto-generated code may not need hand-written documentation. Exclude generated files from coverage analysis or mark them separately.

**Test documentation**: Test files often contain implicit documentation through test names and setup. Decide whether test coverage substitutes for separate documentation.

## Success Criteria

- All source code units cataloged at chosen granularity
- Documentation mapped to corresponding code units
- Coverage matrix produced with status per unit
- Aggregate metrics calculated
- Gaps prioritized by impact
- Report ready for documentation planning

## Common Issues

**Name mismatches**: Documentation uses different naming than source code (abbreviations, aliases). Use fuzzy matching and content analysis alongside exact name matching.

**Scattered documentation**: A single documentation file may cover multiple code units, or multiple files may partially cover one unit. Track many-to-many relationships in the coverage matrix.

**Monorepo complexity**: Large codebases with multiple independently documented packages. Scope analysis per package to maintain manageable analysis size.

**Stale documentation**: Documentation exists but describes an outdated version of the code. Coverage analysis identifies presence, not accuracy. Accuracy verification requires separate content validation.

## Related

- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@documentation/reference/inventory.md" />
- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@documentation/reference/api_documentation.md" />
- `broad_scan` (module `agentic`, profile `workflows`, skill `discovery_procedure`)
