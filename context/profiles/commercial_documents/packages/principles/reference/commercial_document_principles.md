# Genre principles for commercial documents

The base model in [whole_to_detail.md](../../../../core/packages/whole_to_detail/reference/whole_to_detail.md) states the rule once: give the reader the frame an item presupposes before presenting the item. In a commercial document the funnel runs from the decision the document serves down to the detail that serves it, and it applies to the whole document, to each part, and to every section and paragraph. This file applies that rule to the levels a document adds, then sets the rules the three kinds share for lists, the price, headings and register. The per-kind files add what changes.

## The first page

The first page gives the reader the frame for the decision: what is being offered or agreed, for what purpose of the reader's, and what the reader is being asked to do with the document. Written for the client's goal first, the opening lets the reader judge everything that follows; written as a table of the vendor's services, it makes the reader assemble the frame alone. The model's own worked example is the pattern, with the client's goal and the delimitation in the same breath (illustrative, from [whole_to_detail.md](../../../../core/packages/whole_to_detail/reference/whole_to_detail.md)):

> The project is to reduce the manual handling of incoming orders by automating their validation and transfer to the business system. The work covers integration and error handling, but not a replacement of the business system.

The first page also passes question 5 of the review test in [review_test.md](../../../../core/packages/whole_to_detail/rules/review_test.md): it gives a usable frame, and an enumeration of the parts that follow does not. A document whose parts are worth naming on the first page names them with the relation that unites them — what each part decides, and in what order the reader should take them — in at most a few sentences. Such brief reading guidance is allowed, sparingly, in long texts; where it would only repeat what the part openings already do, it is omitted.

## Part openings

The document's design decides where parts and page breaks fall; this profile decides what each part opening carries. A part that opens on a new page opens with its own frame: what this part establishes, and how it relates to the decision the document serves. A heading followed directly by detail gives the reader a label where a frame is needed, and a bare list of part contents gives exactly that. One or two sentences suffice, as the model's section example shows (illustrative):

> Error handling is to ensure that an order is either processed automatically or becomes visible for manual action. The solution therefore distinguishes between temporary technical errors and errors in the order's content.

Within a part, sections and paragraphs follow the model's levels table directly: a section opens with its point and its function in the part, and a paragraph opens with a core sentence that gives the reading a direction. The core sentence's placement may vary; the limit is the model itself — whatever the placement, the reader holds the frame before the detail that presupposes it, and a straight read of the draft surfaces no late relevance. The full test is [review_test.md](../../../../core/packages/whole_to_detail/rules/review_test.md).

The funnel also governs the jump between levels. A commercial document that goes from a goal straight to an activity list leaves the strategy implicit; the model's chain for a project description — goal, strategy, the packages' responsibilities, the activities, the deliveries and acceptance criteria — exists to keep every step interpretable by the one above it. [project_description.md](../../kinds/reference/project_description.md) applies it.

## References between documents

An offer and its project description are read together, and each piece of information lives in one of them only: commercial terms, guarantees, payment and risk in the offer; the project, the solution and the method in the project description. References run one way. The offer may point to sections and appendices of the project description and to its own appendices; the project description points only to its own sections and appendices, never to the offer. A project description that names the offer, its price or its acceptance cannot be read and shared on its own, so the act of ordering appears in it, where the chain needs it, as a neutral decision ("The order is decided"; in Swedish, "Beställningen beslutas") and not as an acceptance of the offer.

## Lists

A list is kept for content that genuinely is a list — parallel items the reader benefits from seeing separately, such as deliverables, acceptance criteria or work packages — and the sentence before the list says what the list is and what its items have in common. The test, the counter-examples and the rewrites are entries 1 to 3 of [catalogue.md](../../../../core/packages/anti_patterns/reference/catalogue.md); a bold label standing in for the relating sentence fails entry 2, and choppy lines that sell a feeling fail entry 3.

Placement follows the same rule as any other information: a list sits beside what it exemplifies, under the heading and after the sentence it serves, where its relevance is already established. An exemplifying list parked in its own section, away from the thing exemplified, forces the reader to carry the items until their purpose appears — the late-relevance symptom of [review_test.md](../../../../core/packages/whole_to_detail/rules/review_test.md), in list form. A typical repair of an exemplifying list in an offer generalizes: the list moves under the heading directly before the scope section it exemplifies, introduced by a sentence saying what the list exemplifies. Reasoning, relations and explanations stay in paragraphs, where the connections between the parts can be stated.

## The price

The price is stated so the reader can act on it. Its test has three parts:

1. The reader can find the price — its place follows from the document's design, and the reader who looks for it finds it without hunting through appendices it was never pointed to.
2. The price is stated once, with what it covers — what the amount buys, and what it does not, so the reader is never left to reconcile two statements of it. Where a design calls for a summary figure in one part and the priced detail elsewhere, the two name each other, and only one of them is the statement the rest of the document refers to.
3. The price does not appear before the reader knows what it buys, unless the reader already does. A returning client who knows the scope can meet the price on the first page. A first-time reader meets it no earlier than the point where the text has said what it buys, and a price stated together with its coverage can make that point wherever the document's design places it.

Nothing here prefers the price early or late; the part order belongs to the document's design, and the test is the reader's position when the price arrives. What the test does settle: a price scattered across sections, a price whose coverage is left implicit, and a price the reader must reconstruct from a rate table all fail. Each kind file says where the kind's design puts the statement; in a project description there is no price at all, per [project_description.md](../../kinds/reference/project_description.md).

## Headings

A heading carries its message: the reader scanning the document's headings sees the argument, and the description sits under the heading where it is relevant. Question headings fail entry 9 of [catalogue.md](../../../../core/packages/anti_patterns/reference/catalogue.md) outside the rare genres built on the reader's own questions; where one is used there anyway, it keeps its question mark. Where a house ruling departs from another guide, the consumer's own house-style layer decides.

## Register

A commercial document states. It reports what will be delivered, what it costs, what each party has undertaken and when, and it lets the facts carry the persuasion; a sentence that tries to move the reader fails the stating-register test. A house style may sharpen the test for its own language (a sales-register test for Swedish outward text, for instance); in any language the same question is asked: does the sentence state a fact the reader can check, or does it push? The base's statement of the shared voice is [tone_and_register.md](../../../../core/packages/basics/reference/tone_and_register.md). Qualities are shown through what the document commits to, per [show_qualities.md](../../../../core/packages/claims/rules/show_qualities.md); an agreement has no room for register at all beyond precision, per [agreement.md](../../kinds/reference/agreement.md).

The sender decides the person in which the sender speaks. A document sent by a one-person company has the contractor speak in the first person singular and keeps the first person plural for the joint project of contractor and client; a document sent by an organisation speaks in the first person plural. Which sender form a given company uses is that company's own rule, kept in its repository. Text written in a third party's voice, such as web copy in the client's name, keeps that voice. The Swedish forms are in `svenska_affarsdokument` (module `writing_sv`, profile `affarsdokument`, package `dokument`), § Tilltal.
