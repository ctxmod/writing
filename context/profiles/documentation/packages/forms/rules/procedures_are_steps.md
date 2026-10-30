# Procedures Are Steps

A procedure is a numbered list of imperative steps: one action per
step, each step starting with the verb ("Open", "Run", "Confirm"),
and the expected result stated where a step can succeed or fail —
"The terminal prints the version; if it prints an error, the binary
is not on the path". Background, caveats, and alternatives stay out
of the step bodies.

## Rationale

Procedures are executed, not read, and an executing reader holds a
single question: what do I do next? Numbering earns its keep when
steps can be referenced ("re-run step 3 after the restart"), when
order is load-bearing, and when a reader resumes mid-procedure after
an interruption — all normal conditions for real procedures. One
action per step is the error-recovery discipline: when step 4 fails,
the reader knows step 4 is where things stand, which an
"and-then-also" step destroys. The expected-result clause is what
turns a list into a procedure — it lets the reader detect failure
themselves, at the step where it happened, instead of three steps
later.
