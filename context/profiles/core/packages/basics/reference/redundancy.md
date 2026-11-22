# Redundancy

A clause earns its place by adding information. Restating the preceding clause in other words is never acceptable, however well the restatement is written: keep the more concrete of the two formulations and cut the other.

## What counts as restatement

The forms a restatement takes:

- Colon or comma clauses that say again what was just said.
- Spelled-out implications: tails introduced by "which …", "so …", or "that is …", and whole sentences, that only draw the conclusion the reader has already drawn from what precedes them. A consequence that any reader of the document draws unaided from a stated fact is already held; stating it holds the reader's hand. Entry 11 of the anti-pattern catalogue ([catalogue.md](../../anti_patterns/reference/catalogue.md)) gives an example.
- Paired near-synonyms doing one job ("mentor and support", "the rollout and the operationalization").
- The same claim repeated across sections of one document. Each sentence can be correct on its own and the document still says it three times too many.

Adjacent sentences fail the same way when they do one job twice. Two sentences that follow each other do two different jobs: one carries the fact, and the other carries a connection, a motivation or a consequence that the first does not hold. A consequence the reader draws unaided from the first sentence is held by it. Where the second sentence merely re-presents what the first established, it is a restatement with a longer reach.

## What does not count

What is cut is the restatement; the facts stay. Two adjacent sentences that each carry a fact of their own are not redundant, however alike they sound. A tail that carries a result the main clause does not ("…, which cut load times by over 60%") is not redundant either. A figure of this kind appears only when it is true and substantiated.

Restated (avoid):

> Leading the support team taught me to handle customers directly, gather
> and clarify their problems, and take a case the whole way myself.
> (…after a paragraph that already said exactly this)

Merged, keeping only the facts the second version added (better):

> I owned each customer case directly, gathering and clarifying
> the problem and taking it from there through to resolution.

## Why

A restatement reads as filler, slows an otherwise dense text, competes for limited space, and signals uncertainty: someone who says a thing twice does not trust that the first time was enough.

## How to apply

Read every clause and ask what it adds that is not already in the text; where the answer is "nothing", cut it. Repeat the check at document level, since repetition between sections is harder to see than within a sentence. Structured fields (tags, scales, stand-alone form answers) may overlap where the field type requires it; running text may not.

A sentence earns its place by adding information: cut restatements ruthlessly, including the same claim repeated across sections of one document, but never cut a distinct fact just because it sits near a similar one.

Related: [diction.md](diction.md), the per-sentence control question in [claims_and_evidence.md](../../claims/reference/claims_and_evidence.md), the repetition entry in [catalogue.md](../../anti_patterns/reference/catalogue.md), and the short rule [cut_padding.md](../rules/cut_padding.md).
