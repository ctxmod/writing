# Reader empathy

A text succeeds when the person it was written for can find what they need, understand it, act on it, and come away sure that the writer had them in mind. Empathy in writing is the working discipline behind that outcome. The writer builds a model of one reader (what they already hold, what they came for, how much attention they will give) and writes to the model instead of to their own head. The sections below set out that model and the tests that keep a draft faithful to it. They apply in every genre; the genre profiles say where the reader differs.

## 1. Name the reader

A text written for "the audience" drifts toward the average sentence, which fits no one in particular. Before drafting, name the reader and four facts about them. They are who the reader is in relation to the writer, what they already know about the subject, what they will do, decide or feel after reading, and how much time they will give the text. For a message the reader is the recipient. For a page it is the person who arrives with a task. For a document with several readers it is the primary one, and the others are served by placement (the "make available" and appendix tiers of [reader_order.md](../../whole_to_detail/rules/reader_order.md)) instead of by a text pitched between them.

The test: can the writer state the four facts before the first sentence? When they cannot, the draft waits. An agent or assistant drafting on someone's behalf asks for what it cannot know, as the personal-contacts rule in the `correspondence` profile already requires for shared history.

This is the first step of plain language as ISO 24495-1 defines it. Its "relevant" principle starts from identifying the readers and their purpose ([plain_language_standard.md](../../basics/reference/plain_language_standard.md)).

## 2. The curse of knowledge

Better-informed people cannot set aside what they know when they predict how a less-informed person will judge something. Camerer, Loewenstein and Weber named the effect in 1989, from experiments in which informed traders failed to ignore private information even when ignoring it would have paid. Pinker treats it as the main cause of opaque prose. A writer who has used a term, an abbreviation or a shortcut for years stops seeing it, and the step the writer finds too obvious to state is often the one the reader lacks.

The test is a marking pass. Read the draft as the named reader and mark every term, abbreviation, reference to an earlier event, unstated step and in-group name. For each mark, ask whether this reader holds it. The repair is local. Define the term where it first carries weight (the `define_before_use` rule of the `documentation` profile states the docs form), give the example that makes it concrete, or state the step that was skipped. The whole-to-detail rule that prerequisites come before what depends on them is the structural form of the same repair ([whole_to_detail.md](../../whole_to_detail/reference/whole_to_detail.md) §3).

The repair cuts both ways. Explaining what the reader already holds is the same failure of modeling, seen from the other side, and catalogue entry 11 covers it ([catalogue.md](../../anti_patterns/reference/catalogue.md)). The reader is intelligent and outside the writer's head. A text that treats the reader as slow, or as a colleague who shares every assumption, has modeled someone else.

Pinker's remedy is the reliable one. When the stakes justify it, show the draft to someone who resembles the reader and watch where they stall. A reviewer who reads as the reader does the same work, which is why ISO 24495-1 judges plain language on readers and not on readability formulas.

## 3. What the reader came for

Readers arrive with a question, a task or a decision, and the text that answers it first respects them most ([answer_first.md](../../structure/rules/answer_first.md)). The question is the reader's, in the reader's terms. A writer who answers the question they would have liked to be asked has written for themselves.

Some texts exist mainly for a relationship. A thank-you, an apology, a condolence, a congratulation or a reply to someone in difficulty carries little information, and what the reader needs from it is to be acknowledged accurately. Such a text names the specific thing (what the person did, what happened to them, what will change) and stops. Narrating the writer's own feelings at length moves the text's center from the reader to the writer. The `correspondence` profile carries the genre form in `relational_messages`.

## 4. The reader's time

Most readers skim. Nielsen's 1997 study found that 79 percent of test users scanned any new web page and 16 percent read word by word. Nielsen Norman Group's eyetracking work since 2006 shows the scanning patterns. In the F-pattern the eye fixates on the first lines of a text and on the first words of each line. In the layer-cake pattern it reads headings and skips the body. Only in the uncommon commitment pattern does it read nearly everything. Scanning is strongest when text is unformatted, when the reader wants to finish quickly, and when they are not interested enough to read every word.

Three consequences follow for any genre. The point belongs in the first sentences, where every reader looks. Headings, first sentences of paragraphs and first words of lines carry the content a scanner takes away, so they state it and do not gesture at it ([headings_that_predict.md](../../structure/rules/headings_that_predict.md)). And every sentence costs the reader something. Padding transfers effort from the writer, who saved the work of choosing, to the reader, who pays for the choice not made ([cut_padding.md](../../basics/rules/cut_padding.md)).

Respect for time is not brevity at any price. A text cut until the reader cannot act costs more time than it saved, because the reader must ask, wait and read again; the message doctrine's "short without becoming skimpy" states the balance for messages (`message_doctrine` in the `correspondence` profile, §9).

## 5. Expectations inside the sentence

Readers also hold expectations about where information sits in a sentence, and prose that meets them is read faster. Gopen and Swan set out the reader-expectation account in 1990. Readers expect the start of a sentence (the topic position) to link back to what they know and the end (the stress position) to carry what is new and important. They expect the subject close to its verb, and the action in the verb. Williams's *Style* teaches the same through characters as subjects, actions as verbs, and old information before new. This module holds these as craft rules already, in [clarity_principles.md](../../basics/reference/clarity_principles.md) (concrete subjects, strong verbs, visible actors) and [flow_and_transitions.md](../../structure/reference/flow_and_transitions.md) (old-before-new and linking by echo); they are the sentence-level form of reader empathy.

## 6. Specificity is the evidence of attention

A reader can tell whether a text was written to them or could have been sent to anyone, and the generic text tells them they were not worth the effort. Specificity is how attention shows on the page. It means the fact from the reader's last message, the constraint they named, the part of their work the writer actually read, or the decision that is theirs to make, used where it changes what the text says.

The test generalizes the interchangeability test of the correspondence pre-send checks. Swap the reader for another plausible one and ask what must change. When nothing must, the text has not seen its reader, and the repair is to find what is true of this reader and let it steer the content. Adding their name to the same sentences does not count. A detail placed only to prove that research happened fails the same test, which is the swap control of the `sales_outbound` profile's first-contact rules.

Specificity has a limit. Private detail the reader did not share with the writer, or a show of research, reads as surveillance or as performance. The detail used is the one the reader would expect the writer to know and that changes what the text says.

## 7. Seen without flattery

Readers want to feel seen, which means their situation is reflected accurately and taken seriously. Flattery is something else. It asserts a quality of the reader the writer cannot know ("your impressive work", "a leader like you"), reads as a sales move, and fails the stating register in [tone_and_register.md](../../basics/reference/tone_and_register.md). Presumed feelings fail for the same reason ("I know how busy you are", "I understand how frustrating this must be"). They read the reader's mind without grounds, which the message doctrine rules out (`message_doctrine` in the `correspondence` profile, §5).

The test: every sentence about the reader states something they told the writer, something the writer observed, or something checkable. An acknowledgment is one specific sentence about their actual situation ("the March numbers arrived after your deadline, so the review runs on the February set"), never a paragraph of pleasantries. A text that sees the reader also trusts them. It does not over-explain, moralize, or tell them what to feel about what it says.

## How to apply

Run §1 before drafting anything outward, and §2 as a marking pass on every draft for a reader outside the writer's own working context. Check §3 against the opening, §4 against the first sentences and headings, and §5 sentence by sentence where the prose reads slowly. Use §6 as the swap test on any text addressed to a person, and §7 on every sentence whose subject is the reader. The [reader_pass](../../process/skills/reader_pass/SKILL.md) skill runs these checks together with the integrity and machine-tell checks.

Related: [write_for_one_reader.md](../rules/write_for_one_reader.md), [author_integrity.md](../../integrity/reference/author_integrity.md), [why_machine_text_fails.md](../../machine_tells/reference/why_machine_text_fails.md), and `reader_intent` and `expertise` (module `writing`, profile `documentation`, package `audience`).

## Sources

- https://www.cmu.edu/dietrich/sds/docs/loewenstein/CurseknowledgeEconSet.pdf — Camerer, Loewenstein and Weber, "The Curse of Knowledge in Economic Settings: An Experimental Analysis", *Journal of Political Economy* 97(5), 1989, pp. 1232–1254, doi:10.1086/261651; the origin of the term and the finding that informed agents cannot ignore private information; accessed 2026-11-23.
- https://news.harvard.edu/gazette/story/2012/11/exorcising-the-curse-of-knowledge — report of Pinker's account of the curse of knowledge (chunking, the remedy of testing a draft on a representative reader), developed in his *The Sense of Style* (Viking, 2014), chapter 3; accessed 2026-11-23.
- https://www.nngroup.com/alertbox/9710a.html — Nielsen, "How Users Read on the Web", 1 October 1997 (79 percent scan, 16 percent read word by word); accessed 2026-11-23.
- https://www.nngroup.com/articles/f-shaped-pattern-reading-web-content/ — Pernice, "F-Shaped Pattern of Reading on the Web: Misunderstood, But Still Relevant", 12 November 2017, reviewed 19 August 2026 (F-pattern since 2006, layer-cake, spotted, commitment and other patterns, and when scanning is strongest); accessed 2026-11-23.
- https://www.americanscientist.org/blog/the-long-view/the-science-of-scientific-writing — Gopen and Swan, "The Science of Scientific Writing", *American Scientist* 78(6), 1990, pp. 550–558 (topic and stress positions, subject–verb proximity, action in the verb); accessed 2026-11-23.
- https://en.wikipedia.org/wiki/Style:_Lessons_in_Clarity_and_Grace — Williams (later with Bizup), *Style: Lessons in Clarity and Grace*, 12th edition, Pearson (characters as subjects, actions as verbs, cohesion through old-before-new); accessed 2026-11-23.
- https://www.iso.org/standard/78907.html — ISO 24495-1:2023, the "relevant" principle and readers over formulas; detail in this package's sibling reference `plain_language_standard.md`; accessed 2026-11-23.
