# Genre principles for essays

An essay's frame is its claim. The opening tells the reader what the text will defend and on what kind of evidence, each section advances that defence, and the ending, the title and the standfirst claim what the body has earned. This is the base model of [whole_to_detail.md](../../../../core/packages/whole_to_detail/reference/whole_to_detail.md) with the argument as the main idea, and the review test in [review_test.md](../../../../core/packages/whole_to_detail/rules/review_test.md) is the acceptance check for a draft. The tests below are the ones an essay fails most easily; each points to the base file that holds it in full.

## The argument is the through-line

The test for every section: does it advance the argument, or does it only cover more of the topic? A section that surveys the field without moving the claim forward fails, and is cut or rewritten so that it does work for the claim. Every sentence passes the per-sentence control question in [claims_and_evidence.md](../../../../core/packages/claims/reference/claims_and_evidence.md), section 6.

Claims about the world follow the same file. They are delimited where a broad claim cannot be defended, each keeps its statement type explicit (observation, assessment, possibility or interpretation), the investigated case comes before the generalization drawn from it, and negative findings are kept and scoped. A mechanism the reader can picture outweighs a named quality: the essay shows the work, the passage or the case, and leaves the judgment to the reader where the text has earned it (section 8). Redundancy, diction and register follow the base principles ([redundancy.md](../../../../core/packages/basics/reference/redundancy.md), [diction.md](../../../../core/packages/basics/reference/diction.md), [tone_and_register.md](../../../../core/packages/basics/reference/tone_and_register.md)).

## Arguing with another author

Most essays, analyses and critiques answer someone, and [argumentation.md](argumentation.md) carries the tests. The ones an essay fails most easily are these:

1. The text contests what the author actually claims, and places the disagreement where conceding the essay's evidence would cost that author something (sections 1 and 2).
2. A proposed criterion can fail, uses conditions the opponent would accept, and asks about reliability in degrees (section 4).
3. The case that resists the thesis stays in the text (section 5).
4. The ending, the title and the standfirst claim what the body defends, and keep the distinctions the body drew. A title may carry the stronger reading only when the standfirst narrows it explicitly (sections 8 and 9).

Historical and documentary cases follow [working_with_sources.md](working_with_sources.md): the essay counts origins where it might count publications, prefers the narrower causal claim, and keeps each source's degrees of confidence in its own prose.

## Criticism: evaluative claims need evaluative reasons

An evaluation of a work, such as a ranking, a judgment that it is better or worse, or a verdict on a performance, is supported by attention to the work: a described passage, a comparison, or a property the opposing judgment misses. Reception history, sales, attendance and later restoration are evidence that something happened to the work. They count toward its quality only as far as the text justifies why the process behind them bears on the particular quality being judged. The rule, with its worked repairs, is section 6 of [argumentation.md](argumentation.md).

The genre adds one boundary that the base does not state. Historical evidence constrains claims about past practice, such as how a work was performed or received in its time. It does not decide whether a present performance or reading succeeds artistically, which is an evaluative claim and needs an evaluative reason. The same distinction applies to performance: fidelity to a historical practice is a claim historical evidence can test, while whether a performance succeeds now is an evaluative claim.

## Voice and ownership

An essay is signed, and its reader reads it as one person's thinking. The thesis, the cases, the judgments and the reasons for them are the author's own, and every sentence passes the core ownership test, that the author would say it and defend it ([author_integrity.md](../../../../core/packages/integrity/reference/author_integrity.md)). Assistance with sources, structure and wording is the author's to choose, and assessed or published work follows the declaration rules of the institution or publisher ([disclosing_assistance.md](../../../../core/packages/integrity/reference/disclosing_assistance.md) § 1).

The machine tells an essay shows most often fail tests this file already holds. A survey of positions that never commits to one fails "The argument is the through-line" above. A topic declared "complex and multifaceted" with considerations listed on every side and no verdict is the hedge fog and false balance of the tell catalogue (entry 7). "In conclusion" followed by the body again is the summary close (entry 10), and the ending rule in [argumentation.md](argumentation.md), section 8, says what an ending owes instead. Claims that a work or an event "shaped the conversation" or "left a lasting legacy" are inflated significance unless the essay argues them (anti-pattern catalogue entry 13), and "critics argue" with no critic named is vague attribution (tell catalogue entry 8; [working_with_sources.md](working_with_sources.md), section 2). The catalogue is [tell_catalogue.md](../../../../core/packages/machine_tells/reference/tell_catalogue.md).

## Length

Length follows the argument. A length target is a guide and never itself a reason to cut: a long draft loses its repetition first and keeps the qualifications that make its claims correct, per [claims_and_evidence.md](../../../../core/packages/claims/reference/claims_and_evidence.md), section 7. When a draft is criticized, the usual remedy is clearer limits on the claim, and adding another case is a separate decision that is usually the wrong one, per [argumentation.md](argumentation.md), section 5.

## Academic craft

The `scholarly_prose` profile of the writing_academic module holds the general academic craft this genre draws on: composition, revision, voice, rhythm, limitations and citations. Where it conflicts with a house ruling, the consumer's own house-style layer decides.


## Language

The genre has no language delta of its own. A Swedish essay follows the Swedish language rules (the `writing_sv` module's `core` profile), and where an essay exists in two languages, the order in which the original and its version are written, and how the version is written from the original's facts, is in the `translation` profile of this module and, for Swedish, in its `writing_sv` application (profile `webb`, package `genrer`, "Originalet först").

## Status

This genre doctrine was seeded as a placeholder, with research into essay craft still pending; until that research lands, the general principles of the `core` profile carry everything the genre has not ruled. What this file holds is the doctrine ruled so far, mostly in editorial feedback rounds on early essay drafts. New rulings from essay feedback enter here, or in the `core` profile when they hold for every genre, through the feedback-to-rules method (the `writing_context` module's `derivation` profile).
