# Quality gate

Every draft of outward prose passes a standing gate before it is reported as done. The gate binds without a brief from an orchestrator: a writer drafting a CV entry, a letter, an application answer, outreach, a profile, a proposal or web copy holds it by default. It has three parts, run in order, and a fourth part where the consuming repository provides mechanical checks.

## 1. Read before drafting

Before the first sentence, read the rules that govern the text: the whole-to-detail model and its review test ([whole_to_detail.md](../../whole_to_detail/reference/whole_to_detail.md), [review_test.md](../../whole_to_detail/rules/review_test.md)), the anti-pattern catalogue ([catalogue.md](../../anti_patterns/reference/catalogue.md)), the basics and claims principles ([diction.md](../../basics/reference/diction.md), [redundancy.md](../../basics/reference/redundancy.md), [tone_and_register.md](../../basics/reference/tone_and_register.md), [claims_and_evidence.md](../../claims/reference/claims_and_evidence.md), [show_qualities.md](../../claims/rules/show_qualities.md)), the reader, integrity and machine-tell rules ([write_for_one_reader.md](../../reader/rules/write_for_one_reader.md), [stand_behind_every_sentence.md](../../integrity/rules/stand_behind_every_sentence.md), [read_for_tells.md](../../machine_tells/rules/read_for_tells.md)), the language profile for the text's language, and the genre profile for its kind. A draft written first and checked against the rules afterwards inherits structure that the rules would have prevented, and structure is the most expensive thing to repair.

## 2. Self-review against the tests

Before reporting, re-read the finished draft against the same rules, as a reviewer would. Run the five control questions top-down, read once straight through for late relevance, and run each principle's test where its how-to-apply section names a trigger. Each finding is either fixed or conceded with its reason. The [reader_pass](../skills/reader_pass/SKILL.md) skill runs this step as one procedure, reading the draft as its named reader and then checking ownership and tells. A self-review that only confirms the draft has not been run; a self-review that changes text which passes the tests violates the stop rule ([claims_and_evidence.md](../../claims/reference/claims_and_evidence.md) § 11).

## 3. Mechanical scan

Some failures can be found by pattern: a banned term, a forbidden credential wording, a known calque, a glyph. Where the consuming repository keeps a scan for its greppable failures, validation runs it over the changed text alongside a principles check. A clean scan clears only what a pattern can see. Every judgment-based rule — the review test, the anti-pattern tests, the claims discipline — still needs the reading in step 2, and a clean scan never clears a judgment finding.

## 4. Validation runs the whole gate

When a separate agent or pass validates a writing change, it runs the mechanical scan and a principles check as part of validation, in addition to the directives specific to that pass. Validating only against the pass's own instructions leaves the standing rules unchecked.

## What stays with the consuming repository

The gate's pattern is general; its contents are partly local. The list of banned terms, the scan's path and invocation, and any facts about the author that a ban protects (credential status, figures the record does not support) belong to the repository whose texts they govern. Genre-specific triggers, such as the deletion test for letters, belong to the genre profile.
