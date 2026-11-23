# Reader pass

The pass takes a draft and returns it revised, with a short record of what changed and why. It applies three core packages in order (`reader`, `integrity`, `machine_tells`) and then the genre profile's checks. It is part of the self-review step of the standing [quality gate](../rules/quality_gate.md), and it replaces none of the gate's other steps. Each step names the file that holds its tests, and the pass applies those tests without restating them.

## Inputs

- The draft.
- The named reader. For a message this is the recipient; for a page or a document, the primary reader and their task.
- The purpose, meaning what the reader should be able to do, decide or feel after reading.
- The genre and language, which decide the profiles that apply.
- The facts the text rests on, and who owns them.

When the reader, the purpose or a fact the draft depends on is unknown, ask the author before revising. Do not fill the gap with a plausible guess; [author_integrity.md](../../integrity/reference/author_integrity.md) § 2 treats a supplied detail as an invented one.

## 1. Name the reader

Write down, for the pass's own use, who the reader is to the author, what they already know, what they will do with the text, and how much attention they will give it ([write_for_one_reader.md](../../reader/rules/write_for_one_reader.md)). Every later step reads the draft against this note.

## 2. Read once as the reader

Read the whole draft straight through as that person, without editing. Mark five things:

- where the reader would stall on a term, a reference or a skipped step (the curse of knowledge, [reader_empathy.md](../../reader/reference/reader_empathy.md) § 2);
- where they would think "I know" (hand-holding, catalogue entry 11);
- where they would ask "so what?" or skim on;
- where an earlier fact only now makes sense (the late-relevance symptom, [review_test.md](../../whole_to_detail/rules/review_test.md));
- where they would notice that the text could have gone to anyone ([reader_empathy.md](../../reader/reference/reader_empathy.md) § 6).

Then check the opening. A reader who stops after the first two sentences should hold the point and know what is asked of them ([answer_first.md](../../structure/rules/answer_first.md)).

## 3. Cut what tells the reader nothing

For each sentence, ask the per-sentence control question ([claims_and_evidence.md](../../claims/reference/claims_and_evidence.md) § 6), the restatement test ([redundancy.md](../../basics/reference/redundancy.md)) and the placement test ([reader_order.md](../../whole_to_detail/rules/reader_order.md)). Cut, move or merge what fails. After cutting, check that every fact the reader needs to act is still present and that no remaining sentence leaves a false impression (§ 7 of the claims doctrine). Repair the stalls marked in step 2 with a definition, an example or the missing step.

## 4. Check ownership

Read each sentence as the author, asking whether they would say it to this reader in person and could defend it ([stand_behind_every_sentence.md](../../integrity/rules/stand_behind_every_sentence.md)). Check every anecdote, example, figure and first-person claim against the facts, every hedge and every unqualified claim against the evidence, and every reported feeling for truth and size ([author_integrity.md](../../integrity/reference/author_integrity.md)). Where a policy governs the text, confirm that its disclosure requirement is met and that nothing misstates how the text was produced ([disclosing_assistance.md](../../integrity/reference/disclosing_assistance.md)).

## 5. Read for tells

Run [tell_catalogue.md](../../machine_tells/reference/tell_catalogue.md), the whole-text entries (formatting, rhythm, interchangeability) on one more straight read and the rest sentence by sentence. Repair each hit with the specific fact, decision or reason it stood in for, or cut the sentence. Leave the features the catalogue lists as non-tells alone, and never roughen a text to make it look human.

## 6. Apply the genre's checks

Run the checks the genre profile adds. For messages these are the correspondence pre-send checks and, for selling, the sales_outbound ones; for applications, the deletion test and review passes of the job_application profile; for web copy, the page tests; for documentation and essays, their review procedures. Run the language profile's checks for the text's language.

## 7. Stop

Stop when the tests pass. A sentence that is factual, relevant and sayable stands even if it could be phrased differently ([claims_and_evidence.md](../../claims/reference/claims_and_evidence.md) § 11). A pass that keeps rewriting passing text has stopped serving the reader.

## Output

Return the revised draft, followed by a short list of findings. Each finding is either fixed (what changed and which test it failed) or conceded (why the text stays). List any open question for the author separately, such as a missing fact, an unconfirmed experience or a disclosure decision. The list is for the author and never goes to the reader.
