# Runbook Creation Procedure

Author operational procedures for system maintenance, incident response, deployment workflows, and recurring tasks. Runbooks prioritize step-by-step clarity, explicit prerequisites, and verifiable outcomes. Each step must be executable by an operator following the document without prior familiarity with the system.

## Prerequisites

- Operational workflow identified and understood
- System access requirements documented
- Success and failure states defined
- Subject matter expert available for accuracy verification

## Steps

1. **Define scope and trigger**. State what the runbook covers and when to use it:
   - Triggering condition (alert, scheduled task, manual request)
   - Expected duration
   - Required expertise level
   - Systems and components involved

2. **Document prerequisites**. List everything an operator needs before starting:
   - System access and credentials (reference locations, not values)
   - Required tools and their versions
   - Expected system state before execution
   - Dependent runbooks that must complete first

3. **Write sequential steps**. Each step follows a consistent format:
   - **Action**: What to do (verb-first, imperative)
   - **Command**: Exact command or interface action (when applicable)
   - **Expected result**: What the operator should observe
   - **Verification**: How to confirm the step succeeded

   Number steps sequentially. Use sub-steps for actions that share context but require multiple commands.

4. **Add decision points**. At branching points, provide explicit criteria:
   - State the condition to evaluate
   - Describe each branch with its own steps
   - Include the default action when conditions are ambiguous

5. **Document rollback procedures**. For each step that modifies system state, provide:
   - Rollback command or action
   - Verification of successful rollback
   - Point of no return (if applicable)

6. **Include troubleshooting section**. List anticipated failure modes:
   - Symptom description
   - Diagnostic steps
   - Resolution or escalation path
   - Contact information for escalation

7. **Add completion checklist**. Provide a final verification list:
   - System state after successful execution
   - Notifications to send (stakeholders, monitoring systems)
   - Cleanup actions (temporary files, debug flags)
   - Documentation updates (incident log, change record)

## Decision Points

**Simple vs complex workflows**: Workflows under 10 steps may not need rollback sections or troubleshooting. Scale runbook formality to workflow risk and complexity.

**Automation candidates**: Workflows executed frequently with no decision points are automation candidates. Note automation potential in the runbook and reference any existing automation.

**Multi-operator workflows**: When a procedure requires handoffs between teams, clearly mark handoff points with responsible parties and communication channels.

**Environment differences**: When steps vary by environment (staging vs production), use parallel columns or conditional sections rather than separate runbooks. Maintain a single source.

## Success Criteria

- Scope and trigger conditions stated clearly
- Prerequisites complete and verifiable
- Steps executable without additional context
- Each step includes expected result and verification
- Rollback documented for state-changing steps
- Troubleshooting covers common failure modes
- Completion checklist enables verification of success

## Common Issues

**Assumed knowledge**: Steps that skip "obvious" actions fail when executed by unfamiliar operators. Include every action, even ones that seem self-evident.

**Command copy-paste failures**: Commands containing environment-specific values (hostnames, IDs) fail when copied verbatim. Use clearly marked placeholders and document where to find actual values.

**Stale runbooks**: System changes invalidate steps. Attach review dates and schedule periodic validation against current system state.

**Missing failure paths**: Runbooks that cover only the success path leave operators stranded on failure. Invest equal effort in failure documentation.

## Related

- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@documentation/reference/diagram_standards.md" />
- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::procedures@documentation/reference/structure_validation.md" />
- <ctxmod_path path="ctx:github.com/ctxmod/writing/context::shared::basics@core/reference/clarity_principles.md" />
