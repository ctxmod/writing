# Tell catalogue

Each entry names a pattern that readers associate with machine-generated text. It states the test that separates a legitimate use from a failure, shows a counter-example and a rewrite, and gives the narrow exception. The entries are tests, not bans ([tests_not_bans.md](../../basics/reference/tests_not_bans.md)). A pattern that lowers a text's quality whoever wrote it is held in the anti-pattern catalogue ([catalogue.md](../../anti_patterns/reference/catalogue.md)), and this file points to that entry instead of repeating it. Why the tells matter, and why none of them proves anything about who wrote a text, is in [why_machine_text_fails.md](why_machine_text_fails.md).

Every repair here puts something specific where the tell stood, or cuts the sentence. Disguise (an added contraction, a typo, a folksy aside) repairs nothing. Counter-examples marked "illustrative" reuse the order-handling example of [whole_to_detail.md](../../whole_to_detail/reference/whole_to_detail.md); the others are typical of messages, letters and web pages. Rewrites are sketches and add no facts the original lacks.

## Words

### 1. Stock vocabulary

Test: each word is the one the author would use aloud for this exact claim, and it names something the reader can identify. Words that corpus studies and editors find overused in generated text fail when they decorate instead of naming. Examples are "delve", "underscore", "showcase", "pivotal", "crucial", "intricate", "tapestry", "landscape", "realm", "testament", "foster", "leverage", "robust", "seamless", "elevate", "navigate (the complexities of)" and "notably". A cluster of them in one paragraph is the stronger signal. The repair is the plain or the specific word ([prefer_plain_words.md](../../basics/rules/prefer_plain_words.md), [diction.md](../../basics/reference/diction.md)), and where none exists, the sentence had nothing to say.

Counter-example (illustrative):

> The project delves into the intricate landscape of order handling, showcasing a robust and seamless solution.

Rewrite (sketch):

> The project automates the validation and transfer of incoming orders.

Exception: the literal or technical sense ("a robust estimator", "the regulatory landscape" in a text about land use, "underscore" for the character). The list is a prompt to check and never a ban; its members change with each model generation, and the current editors' list is kept in Wikipedia's "Signs of AI writing".

### 2. Inflated significance

The pattern is entry 13 of the anti-pattern catalogue. Its machine forms are "stands as a testament to", "plays a pivotal role in", "marks a significant milestone", "underscores the importance of", "has shaped the conversation around", and the scene-setting opener "In today's fast-paced world". Each passes only with evidence, where the significance is itself the point.

### 3. Commentary tails

The pattern is entry 14 of the anti-pattern catalogue. Its machine forms are trailing participles that evaluate the clause before them ("…, highlighting the need for", "…, ensuring a seamless experience", "…, reflecting a deep commitment to"). A tail passes only when it carries a further fact.

### 4. Abstraction in place of the thing

Test: the reader could point at what each noun phrase refers to. "Various stakeholders", "a range of solutions", "key aspects", "in many ways", "valuable insights" and "the overall experience" fail when the text knows the specific people, solutions or aspects and does not name them. [diction.md](../../basics/reference/diction.md) ("Be as specific as the claim requires") holds the precision rule.

Counter-example:

> We discussed various aspects of the proposal and gained valuable insights from key stakeholders.

Rewrite (sketch):

> Finance accepted the price; operations asked for a later start, which moves delivery to May.

Exception: a real category used as the subject, or a summary whose particulars follow at once.

## Sentences

### 5. Manufactured contrast

The pattern, with its variants "not just X, but Y", "Y rather than X", "no X, no Y, just Z" and "It's not about X. It's about Y.", is entry 4 of the anti-pattern catalogue. Its test decides here as well. The contrast stays only when the reader holds the denied position.

### 6. Triads by habit

The pattern is entry 12 of the anti-pattern catalogue. Generated text reaches for three adjectives, three parallel phrases and three benefits because the rhythm sounds complete, so a series of three is checked member by member.

### 7. Hedge fog and false balance

Test: each hedge marks a real uncertainty in the sentence it concerns, and where the reader asked for a judgment, the text gives one. A text that qualifies every sentence ("may potentially", "it could be argued", "generally", "in some cases"), or that lists considerations on every side and stops without a verdict, has protected itself at the reader's expense. The calibration rule is [claims_and_evidence.md](../../claims/reference/claims_and_evidence.md) § 3, and the integrity form is [author_integrity.md](../../integrity/reference/author_integrity.md) § 3.

Counter-example:

> There are several factors to consider, and the best approach may depend on your specific needs and circumstances.

Rewrite (sketch), from the correspondence profile's worked email:

> I would recommend option 1, since it takes the least change to your current flow.

Exception: a genuine open question, stated once with what would settle it.

### 8. Vague attribution

Test: a claim attributed to others names who, so the reader can check it. "Experts agree", "studies show", "many believe", "industry reports suggest" and "critics argue" fail. The repair names the source, or states the claim as the author's own and answers for it ([author_integrity.md](../../integrity/reference/author_integrity.md) § 2); the source rules are in `working_with_sources` of the `prose` profile.

Counter-example:

> Studies show that automation reduces errors in order processing.

Rewrite (sketch), stating only what the author knows:

> In the pilot, automated validation caught every malformed order before it reached the business system.

Exception: an attribution the genre does not expect to source, such as a commonplace in casual speech, where nothing rests on it.

### 9. Service frames

Test: the opening and the close carry information for this reader. Assistant-style frames fail. Openers such as "Great question!", "Certainly!", "I hope this email finds you well" and "I wanted to reach out to" fail, and so do closers such as "I hope this helps", "Let me know if you have any other questions" and "Feel free to reach out". They are the padding of [cut_padding.md](../../basics/rules/cut_padding.md) in the form readers now link to generated text, and they tell the reader the text was not written with them in mind.

Counter-example:

> Great question! The deadline is Friday. I hope this helps, and let me know if you have any other questions.

Rewrite (sketch):

> The deadline is Friday.

Exception: a concrete offer tied to a real next step ("I can send the March figures before the review if they would help"), which is content.

### 10. Summary close

Test: the last paragraph does new work, by opening the next step, stating the decision, or answering what the reader will do now. A close that restates the body ("In summary", "Overall", "Ultimately", "In conclusion") fails. It is the repetition of catalogue entry 7 at the end of a text, and the claims doctrine's rule that the close opens the next step ([claims_and_evidence.md](../../claims/reference/claims_and_evidence.md) § 6) holds the repair.

Exception: a summary placed first in a long document, which is the answer-first rule ([answer_first.md](../../structure/rules/answer_first.md)), or a conclusion section a genre requires.

## Shape

### 11. Formatting by default

Test: the form matches the genre and the content. A message reads as a letter; headings appear where a reader navigates; a list holds genuinely parallel items; bold marks the one thing that must not be missed. Headings on a five-line email, bullets carrying reasoning, bold labels opening every item, emoji as bullet markers, and title case on every heading fail. Catalogue entries 1 and 2 hold the general tests; the correspondence profile's "Scannable by Default" rule holds the message form.

Exception: a document whose readers navigate it, where headings and lists do the reader's work.

### 12. Uniform rhythm

Test: sentence and paragraph length follow the content. Paragraphs of identical length, sentences of identical shape, and paragraphs that each end on a short emphatic line read as produced to a template. The evidence for this tell is weaker than for vocabulary; it is a reading test, and a text should never be roughened at random to pass it. The positive rule is in [tone_and_register.md](../../basics/reference/tone_and_register.md) ("Flow"). Sentences vary in length for emphasis, not at random. Catalogue entry 3 covers the emphatic one-liner.

Exception: a form whose units are parallel by design, such as steps of a procedure or entries of a reference table.

### 13. Interchangeable text

Test: swap the reader, the subject or the sender for another plausible one, and parts of the text must change. A text that survives the swap unchanged was written to no one, and readers sense it whether or not they think of machines. This is the master test that the others serve. It generalizes the interchangeability test of the correspondence pre-send checks and the swap control of the `sales_outbound` first-contact rules, and [reader_empathy.md](../../reader/reference/reader_empathy.md) § 6 sets out the repair.

Exception: standardized information that is meant to be identical for every reader, such as delivery terms or a policy notice.

## Relationship

### 14. Performed feeling

Test: a feeling the text reports is true, is the size the author would show face to face, and is carried by a specific detail. "I'm truly thrilled", "deeply passionate", "I completely understand how frustrating this must be" and "I was so moved" fail when they stand in for a reason or presume the reader's state. The integrity rule is [author_integrity.md](../../integrity/reference/author_integrity.md) § 5, and the presumed-feelings rule is [reader_empathy.md](../../reader/reference/reader_empathy.md) § 7.

Counter-example:

> I'm truly thrilled and deeply passionate about the opportunity to contribute to your amazing team!

Rewrite (sketch), giving the reason instead of the feeling:

> Your clinical-decision product is where I want to apply what I have learned about regulated data.

Exception: a feeling that is the message, stated once and plainly, such as congratulations or condolence.

### 15. Drafting residue

Test: nothing in the text is addressed to the writer instead of the reader. Placeholders ("[Name]", "[Company]"), a tool's framing ("Here is a revised version:", "Certainly! Below is"), notes about the model's knowledge, Markdown asterisks in a plain-text message, and a subject line repeated as the body's first line are errors and have no exception, as genuine errors have none under [tests_not_bans.md](../../basics/reference/tests_not_bans.md). The general rule against drafting residue is [claims_and_evidence.md](../../claims/reference/claims_and_evidence.md) § 7.

## What is not a tell

Some features are widely taken as signs of machine text and are not reliable signs, and a revision that strips them from sound prose makes the text worse. The editors behind Wikipedia's list name several as ineffective indicators, among them correct grammar, a formal or mixed register, a "robotic" tone, and a transition word such as "Additionally" on its own. The em dash is contested. Generated text used it heavily until about 2026, the editors moved it to their historical indicators once newer models were tuned to avoid it, and professional writers use it routinely. A dash fails only where it serves a pattern above, such as the dramatic pivot of entry 5. This module's own prose uses dashes and keeps them.

A single list of three real items, a well-made sentence and a confident claim with its evidence are not tells. The stop rule holds ([claims_and_evidence.md](../../claims/reference/claims_and_evidence.md) § 11). A formulation that is factual, relevant and sayable stands, and a tell test that finds nothing changes nothing.

## How to apply

Run the catalogue on a finished draft, after the reader and integrity checks, as part of [read_for_tells.md](../rules/read_for_tells.md). Read once straight through for entries 11–13, which show only at the level of the whole text, then sentence by sentence for the rest. For each hit, find what the sentence was meant to say. Write that specific thing, or cut the sentence.

## Sources

- https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing — WikiProject AI Cleanup, "Signs of AI writing": undue emphasis on significance and legacy, superficial "-ing" analyses, vague attributions, outline-like conclusions, AI vocabulary by era, negative parallelisms, rule of three, style and markup signs, collaborative communication, ineffective indicators, historical indicators (em dashes, section summaries); accessed 2026-11-23.
- https://arxiv.org/html/2406.07016v5 — Kobak et al., *Science Advances* 11(27), 2025: excess style words in 2024 PubMed abstracts ("delves", "underscores", "showcasing", "potential", "findings", "crucial", "intricate", "notably"); accessed 2026-11-23.
- https://aclanthology.org/2025.coling-main.426 — Juzek and Ward, COLING 2025: 21 focal words overrepresented in LLM-generated abstracts; accessed 2026-11-23.
- https://aclanthology.org/2025.acl-long.267 — Russell, Karpinska and Iyyer, ACL 2025: expert detectors' cues (vocabulary, formulaic structure, originality, clarity); accessed 2026-11-23.
- https://pmc.ncbi.nlm.nih.gov/articles/PMC10089155 — Jakesch, Hancock and Naaman, *PNAS* 2023: the flawed human cues (pronouns, contractions, family topics) that camouflage would exploit; accessed 2026-11-23.
