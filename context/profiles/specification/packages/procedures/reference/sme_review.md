# SME Review Procedure

Coordinate subject matter expert review cycles for specification documents. SME review validates technical accuracy, identifies gaps in reasoning, and provides domain-specific approval before specifications advance to implementation. This procedure organizes review requests, tracks feedback, and manages approval gates.

## Prerequisites

- Specification document completed and template-compliant
- Reviewers identified with their expertise areas
- Review criteria defined (accuracy, completeness, feasibility, risk)
- Review timeline established

## Steps

1. **Identify required reviewers**. Map specification sections to expertise domains:
   - Technical accuracy: Engineers familiar with affected systems
   - Security implications: Security specialists (when applicable)
   - Operational feasibility: Operations or SRE teams
   - Product alignment: Product stakeholders
   - Cross-team impact: Teams whose systems interact with proposed changes

2. **Prepare review package**. Assemble materials for reviewers:
   - Specification document with current version indicator
   - Review criteria specific to each reviewer's expertise
   - Questions or areas requiring particular attention
   - Deadline for feedback
   - Feedback format (inline comments, structured form, meeting)

3. **Distribute review requests**. Send targeted requests to each reviewer with:
   - Clear scope (full document or specific sections)
   - Expected time investment
   - Priority relative to other work
   - Context on urgency and downstream dependencies

4. **Collect and organize feedback**. As reviews arrive:
   - Record each comment with reviewer attribution
   - Classify by type: technical correction, design concern, question, suggestion
   - Identify conflicting feedback between reviewers
   - Track outstanding reviews against deadline

5. **Resolve feedback**. For each piece of feedback:
   - **Accept**: Incorporate change into specification
   - **Reject**: Document rationale for disagreement
   - **Discuss**: Flag for synchronous resolution when written exchange is insufficient
   - **Defer**: Acknowledge as valid but outside current scope

   Update specification to reflect accepted feedback. Record all decisions.

6. **Manage approval gate**. After feedback resolution:
   - Verify all required reviewers have responded (or deadline passed with escalation)
   - Confirm blocking concerns resolved
   - Obtain explicit approval from required reviewers
   - Record approval with reviewer name and date

7. **Document review cycle**. Capture review metadata:
   - Reviewers and their response status
   - Feedback summary by category
   - Decisions on rejected or deferred feedback
   - Approval status and conditions

## Decision Points

**Reviewer non-response**: When reviewers miss deadlines, escalate to management. Set a maximum wait period; beyond that, document the gap and proceed with noted risk.

**Conflicting expert opinions**: When SMEs disagree, facilitate direct discussion between conflicting parties. If consensus fails, escalate to a decision-maker with authority over the contested domain.

**Minor vs major revisions**: Minor feedback (typos, clarifications) can be resolved without re-review. Major feedback (design changes, new requirements) requires a second review cycle for affected sections.

**Conditional approval**: Reviewers may approve contingent on specific changes. Track conditions and verify resolution before marking approval as complete.

## Success Criteria

- All required reviewers identified and contacted
- Reviews received or escalated within timeline
- Feedback classified and resolved with documented decisions
- Approval obtained from all required reviewers
- Review cycle documented with metadata
- Specification updated to reflect accepted feedback

## Common Issues

**Review fatigue**: Long or frequent review requests reduce feedback quality. Keep review scope focused and provide clear guidance on what to evaluate.

**Expertise gaps**: When no available reviewer has the required expertise, document the gap. Consider external consultation or accept the risk with documentation.

**Approval bottlenecks**: Single-approver dependencies create scheduling risks. Identify backup approvers for critical review roles.

**Scope expansion during review**: Reviewers identifying new requirements during review. Capture as separate follow-up items rather than expanding the current specification's scope.

## Related

- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@specification/reference/template_compliance.md" />
- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@specification/reference/version_tracking.md" />
- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@documentation/reference/completeness_check.md" />
