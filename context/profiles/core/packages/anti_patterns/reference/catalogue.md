# Anti-pattern catalogue

Each entry below names a pattern that lowers the quality of a text, states the test that tells a legitimate use from a failure, shows a counter-example, sketches a rewrite, and gives the narrow exception where the pattern is legitimate. The entries are tests, not bans (see [tests_not_bans.md](../../basics/reference/tests_not_bans.md)): a writer facing a case the catalogue did not foresee asks whether the passage achieves what the entry protects.

Counter-examples marked "illustrative" reuse facts from the worked example in [whole_to_detail.md](../../whole_to_detail/reference/whole_to_detail.md) (a project that automates the validation and transfer of incoming orders), so they add nothing new; the others are typical of the commercial prose (offers, websites, project descriptions) where the patterns most often appear. Every rewrite is a sketch in the language of its counter-example; it shows the direction of the repair and adds no facts the original lacks.

The catalogue binds all writing, agent-facing context files included. The one standing carve-out is entry 10's exception for technical and agent reference documents.

## 1. Lists only for genuine lists

Test: the content is a set of parallel items that the reader benefits from seeing separately (steps, alternatives, criteria), and a sentence before the list says what the list is. Reasoning, relations and explanations belong in paragraphs, where the connections between the parts can be stated.

Counter-example (illustrative):

> Error handling:
>
> - retries on connection errors
> - manual handling

Rewrite (sketch):

> Temporary connection errors are handled with automatic retries. If all of them fail, the order is flagged for manual handling.

Exception: none beyond the test itself; a case that seems to need one is decided once and recorded where the rule lives.

## 2. Bulleted items with bold mini-headings

Test: the text carries its structure through sentences and real headings. A bullet that opens with a bold word or phrase acting as a mini-heading fails, because the bold label stands in for the sentence that should relate the item to the others.

Counter-example (illustrative):

> - **Validation:** the order is checked automatically.
> - **Transfer:** the order is passed to the business system.

Rewrite (sketch):

> The project automates the validation of incoming orders and their transfer to the business system.

Exception: none; a case that seems to need one is decided once and recorded where the rule lives.

## 3. Prose over choppy, salesy lines

Test: each sentence is a complete statement that the reader can check against the subject, and each paragraph break follows a turn in the content. Fragments, free-standing subordinate clauses, slogans and stacked short lines that sell a feeling fail — choppy, salesy descriptions — and so does a short paragraph whose only job is to give one phrase emphasis. The repair folds the fragment into an existing sentence and cuts the repetition it carried. It never lengthens the text, and it never expands each fragment into a full sentence of its own.

Counter-example (illustrative):

> Fast. Automatic. No manual work.

Rewrite (sketch):

> The project is to reduce the manual handling of incoming orders by automating their validation and transfer to the business system.

Counter-example, a free-standing subordinate clause set as its own paragraph after the sentence it belongs to:

> Documentation of how the website is built and run is included, so that any competent developer can take over.
>
> So that the association is never tied to a single supplier.

Rewrite (sketch):

> Documentation of how the website is built and run is included, so that any competent developer can take over and the association is never tied to a single supplier.

Exception: none; a case that seems to need one is decided once and recorded where the rule lives.

## 4. "Y, not X" contrast for effect

Test: the reader actually holds the belief X that the sentence denies. If the reader holds it, the contrast corrects a misconception and stays. If X is a position nobody in the audience holds, the contrast only manufactures drama, and the sentence should state Y directly.

Counter-example:

> "The idea behind the portal: not a showcase but a working tool for the team's everyday tasks"

Rewrite (sketch):

> The portal is built as a working tool for the team's everyday tasks.

Counter-example:

> "The form of each page follows its content, not the other way round — every page type gets a template that makes exactly that content clear"

Rewrite (sketch):

> Every page type gets a template that makes exactly that content clear.

Counter-example:

> "Try the design for real, not as pictures in a memo"

Rewrite (sketch):

> You can try the design for real.

Counter-example:

> "Accessibility is their right and not an add-on"

Rewrite (sketch):

> Accessibility is their right.

Counter-example:

> "The client should not depend on a supplier — the client should own its own tool"

Rewrite (sketch):

> The client should own its own tool.

Counter-example:

> "You pay a fixed price, not hourly rates"

Rewrite (sketch):

> You pay a fixed price.

Exception: correcting a misconception the reader actually holds. The SAGE chapter on advance organizers gives this its legitimate form, the comparative organizer, which relates new material to what the reader already believes.

## 5. Meta and internal-structure statements

Test: the sentence tells the reader something about the subject. A sentence that only describes how the text, the material or the work is organised fails; such sentences are like comments in code that narrate the code instead of explaining it.

Counter-example:

> "Each entry answers the same four questions, in the same order"

Rewrite (sketch): the sentence is removed. The entries answer their four questions, and the reader sees the shared order without being told about it.

Counter-example:

> "All 24 pages, 81 news items and blog posts, 12 events, 57 documents and the images are moved into the new website"

Rewrite (sketch), main text, with the counts moved to an appendix sub-section:

> The pages, news items and blog posts, events, documents and images are moved into the new website.

Counter-example:

> "Hours not used in one month do not carry over to the next month. This keeps the price low and predictable."

Rewrite (sketch): both sentences leave the main text. The first sentence moves unchanged into the appendix sub-section that holds the terms; the second is omitted.

Exception: a navigational pointer that tells the reader where deferred detail lives, such as a short reference to the appendix sub-section that entry 6 sends detail to. In a long text, brief reading guidance ("in the next section", "finally") also passes when used sparingly: it orients the reader within the subject.

## 6. Detail that belongs in an appendix or nowhere

Test: the reader needs this detail at this point to understand, decide or act. Detail that passes stays where it is. Detail that some readers want but the main line does not depend on moves to a specific sub-section of an appendix, which can be read when needed or out of particular interest. Detail that no reader needs is omitted. [reader_order.md](../../whole_to_detail/rules/reader_order.md) gives the four placement tiers in full.

Counter-example: the migration inventory and the hour-rollover rule quoted under entry 5 are also examples of this pattern: a lot of detail that either need not be mentioned at all, or should be mentioned in a specific sub-section of an appendix.

Rewrite (sketch): see the rewrites under entry 5.

Exception: none is needed. Detail the reader needs at that point to decide or act stays, and that outcome comes from the test itself.

## 7. Repetition

Test: a sentence that returns to earlier material does new work. A short functional reminder passes: it re-orients the reader, or refreshes a term just before the term carries new weight. A sentence that restates a claim the text has already established, with nothing new resting on it, fails.

Counter-example (illustrative), late in the section on error handling:

> As mentioned above, the project is to reduce the manual handling of incoming orders.

Rewrite (sketch): the sentence is removed, or, where the reader needs the tie-back, replaced by a reminder that connects the detail to its frame:

> The retries serve the same goal: the order is either processed automatically or becomes visible for manual action.

Exception: short functional reminders, as described in the test. The reconciliation with Heiser's strategic redundancy is set out in [whole_to_detail.md](../../whole_to_detail/reference/whole_to_detail.md).

## 8. Order of emphasis

Test: the text moves as a funnel from frame to detail. Each passage opens with what the reader needs to interpret the rest, and each detail follows the point it serves. Detail that arrives before its principle fails, as does a central point placed after its own particulars.

Counter-example (illustrative):

> The system makes at most three attempts with increasing wait times. Temporary connection errors are handled with automatic retries.

Rewrite (sketch):

> Temporary connection errors are handled with automatic retries. The system makes at most three attempts with increasing wait times.

Exception: a conclusion may come first when the intended reader can understand it without preparation, as §5 of the model allows. When it rests on unfamiliar categories or assumptions, those come first or are explained right beside it.

## 9. Question headings

Test: the description sits where it is relevant in the text, under a heading that carries its message. A heading phrased as a question, followed by its answer, fails when it forces a question onto material that would read naturally without one.

Counter-example (illustrative):

> What happens if an order cannot be processed?

Rewrite (sketch), as a heading that carries the answer:

> Orders that cannot be processed become visible for manual action

Exception: rare, and natural in genres built around the reader's own questions, such as an FAQ or a "frequently asked questions" page.

## 10. Content-declaration openings

Test: the opening of a section gives the reader a frame, in the sense of question 5 of [review_test.md](../../whole_to_detail/rules/review_test.md). An opening that only announces the topic ("This section is about …") fails in reader-facing writing.

Counter-example (illustrative):

> This section is about error handling.

Rewrite (sketch), from the model's own example:

> Error handling is to ensure that an order is either processed automatically or becomes visible for manual action.

Exception: technical and agent reference documents, where a scope statement helps a reader or agent decide whether to read on. In reader-facing writing the pattern is not allowed.

## 11. Hand-holding: obvious implications

Test: the sentence tells the reader something they could not draw from what the text has already stated. A sentence or clause that only spells out a consequence every reader of the document draws unaided fails: it holds the reader's hand more than the reader needs. Where the plain statement leaves room for a wrong reading, the repair sharpens the statement itself instead of adding a sentence that explains it.

Counter-example, an offer's price section, where a fixed price has already been stated:

> You pay a fixed price. If the work takes longer than estimated, that is our risk.

Rewrite (sketch): the paragraph is removed, because a fixed price already places the risk of overrun with the contractor. The sentence that states how the price was reached carries the one fact the paragraph pointed at, that the time is an estimate:

> The price is calculated from the time each part is estimated to take, …

Exception: an implication the reader would plausibly miss or misread, such as a legal or commercial consequence that does not follow from common understanding, is stated, as a term where it binds. This entry refines the restatement test of [cut_padding.md](../../basics/rules/cut_padding.md) for consequences rather than repeated claims; entry 7 covers material the text has already said, this entry material the text never needed to say.
