# Genre principles for web copy

A page of web copy has one reader task to serve: deciding, from a quick read, whether the work the page describes is relevant. The base model in [whole_to_detail.md](../../../../core/packages/whole_to_detail/reference/whole_to_detail.md) therefore applies with the page as the document. Its opening gives the frame by naming the work, each section adds something the page has not yet said, and every sentence states what the reader can check. The tests below apply that model to a page; the anti-pattern catalogue in [catalogue.md](../../../../core/packages/anti_patterns/reference/catalogue.md) applies to every sentence as well.

## The opening names the work

The test for a page's opening: does it say what the work actually is? A reader who stops after the opening holds a correct, coarse picture of what is done and for whom, in the terms of the work itself.

A familiar category, such as "AI" or "compliance", may introduce the work only when the same sentence or the next one names the concrete substance behind it, such as the engineering work actually done. An opening that stays at the category is a buzzword lead and fails, because the reader learns which field is meant and nothing about the work. The precision rule behind the test is in [prefer_plain_words.md](../../../../core/packages/basics/rules/prefer_plain_words.md), section "Be as specific as the claim requires", which also gives the cases where the umbrella term is the right word.

## Each claim once per page

The base rule that every clause adds information, in [cut_padding.md](../../../../core/packages/basics/rules/cut_padding.md), names repetition between sections of one document as the hardest kind to see. Web copy is where it occurs most, because each section of a page is written to stand alone. The test: read the page's sections in order and list the claims each one makes; a claim that appears in a second section with nothing new resting on it is cut from that section. A site that says four times that it weighs technology against business value says it three times too many.

A short functional reminder still passes, per entry 7 of the catalogue: a phrase that ties a section's detail back to the page's frame does work, and a restated claim does not.

## The stating register

Every sentence of web copy states a fact the reader can check; a sentence that tries to move the reader fails the stating-register test in [tone_and_register.md](../../../../core/packages/basics/reference/tone_and_register.md), whatever its language. Rhetorical questions, framing that presumes the reader's problem, and intensifiers meant to persuade are the usual failures there, and on a web page they are the default temptation, since a page is written to be acted on. A house style may sharpen the test for its own language, such as a sales-register test for Swedish outward text; the Swedish terminology rules for web copy are `facktermer` (module `writing_sv`, profile `webb`, package `principer`).

## Shown qualities and defensible claims

A quality the work has is shown through what was built, delivered or decided, and every claim on a page can be defended if a reader asks. Both rules, with their tests, are in [show_qualities.md](../../../../core/packages/claims/rules/show_qualities.md); the claims doctrine in [claims_and_evidence.md](../../../../core/packages/claims/reference/claims_and_evidence.md) sets how firmly each claim may be stated.

## Terminology that follows an external text

A text whose terminology deliberately follows an external text, such as an advertisement it answers or a client's own wording, keeps that text's terms and says so in its own header. The header note is what grants the exception: without it, the house terminology applies, and with it, only the terms the external text actually uses are kept. An editing pass that meets such a note leaves those terms as they are. The Swedish form of the rule, with its reason and limits, is the exception for externally anchored terminology in `facktermer` (module `writing_sv`, profile `webb`, package `principer`).

