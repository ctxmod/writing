# Whole-to-detail structure

Every writing profile in this module rests on one model of how a text is ordered: each part first gives the reader the frame that the following detail presupposes, and the detail then refines that frame step by step. The model is set out below in six sections; the sections after it add refinements from the sources, correct one attribution, and list the sources.

## The hierarchical whole-to-detail structure

A hierarchical whole-to-detail structure organizes text so that each part first gives the reader the **frame of interpretation** needed to understand what follows. The content then develops through successive refinement: from main idea to sub-ideas, from sub-ideas to explanations, and from explanations to concrete details.

The central rule:

> Give the reader the frame that a piece of information presupposes before you present the information.

The model is close to the pedagogical principle of _advance organizers_: first introduce superordinate, relevant concepts that help the reader understand and place the information that follows. Technical writing states a corresponding rule: never presuppose more knowledge than the reader's prior knowledge together with what the text has already established (see the attribution note below). [Springer](https://link.springer.com/rwe/10.1007/978-1-4419-1428-6_157)

"Hierarchical whole-to-detail structure" is used here as a descriptive model, not as the name of a single standardized theory of writing.

## 1. The whole makes the details understandable

An opening overview should not only say which topic is coming. It should explain how the reader is to understand it.

Depending on the content, the frame may need to answer:

- What is this about?
- Which question, task or problem is being treated?
- What is the main point or the intended result?
- How does this part connect to the larger context?
- Which concepts, delimitations or preconditions are needed?

Not every question needs an answer every time. What matters is that the overview gives a useful context for the details, and does not merely list what is coming. That is the difference between real conceptual preparation and a plain table of contents. [Springer](https://link.springer.com/rwe/10.1007/978-1-4419-1428-6_157)

Compare two imagined openings to an architecture section:

> "The system uses PostgreSQL, a message queue and three background processes."

Here the reader gets the components, but not the principle that unites them.

> "The system separates receiving an order from processing it, so that slow external services do not block the user's request. The order is stored first and then processed asynchronously."

Now there is a frame for understanding why the database, the queue and the background processes are needed. The technical details can come after.

## 2. The same pattern recurs at several levels

The structure is hierarchical because the document's parts contain subordinate parts in turn. It is recurrent because the same principle applies within each level: introduce the whole, develop the parts, and make their relation clear. Technical writing advice applies this both to section overviews and to paragraphs with one coherent main thought. [Heiser](https://gernot-heiser.org/style-guide.html)

| Level      | What the frame establishes                                  | What is developed next                                |
| ---------- | ----------------------------------------------------------- | ----------------------------------------------------- |
| Document   | Purpose, main message, scope and overall structure.         | The document's larger questions and parts.            |
| Section    | The section's main point and its function in the document.  | Sub-questions, reasoning, comparisons or steps.       |
| Subsection | A delimited sub-idea and its relation to the section.       | Explanations, evidence and concrete solutions.        |
| Paragraph  | One main thought, often through a core sentence.            | Refinements, arguments, examples and consequences.    |

The table is a practical application of the model, not a mandatory outline. A short section may need a single orienting sentence; a complex document may need a summary and a separate overview of concepts.

An overarching introduction does not replace all local orientation either. When a section changes perspective or introduces a new problem, the reader needs to learn how the new part fits in. [Heiser](https://gernot-heiser.org/style-guide.html)

## 3. The principles that govern the order

### Prerequisites before dependents

If understanding B requires A, A must be known when B is presented. It may be known already or have been established in the text; it need not be explained again needlessly. This is the model's most important ordering rule. [Heiser](https://gernot-heiser.org/style-guide.html)

In practice this means, for example:

- Define an unfamiliar concept before using it in reasoning.
- Establish an assessment criterion before using it to compare alternatives.
- Explain which problem a solution addresses before going into its mechanics, unless the problem is already known.

### Main thought before development

The reader should normally learn what a section or paragraph is to convey before the text develops arguments, evidence or details. A core sentence thus gives not just a topic but a direction for the reading. [Pressbooks](https://pressbooks.pub/hayleyinhighered/chapter/intro-to-structure-and-editing/)

The difference, for example:

> Topic statement: "There are several aspects to the deployment."

> Main thought: "The deployment proceeds in stages to limit the consequences of any errors."

The second makes it clearer how the details that follow are to be read.

### Relations before enumeration

A list of parts is not automatically an explanation of a whole. The frame needs to show what unites the parts: are they alternative solutions, steps in a process, causes of the same problem, or components with different responsibilities? Making the superordinate relation visible is a central function of a conceptual preparation. [SAGE](https://in.sagepub.com/sites/default/files/upm-binaries/14256_Chapter13.pdf)

A practical rule therefore follows:

> Before you enumerate the parts, say what they are parts of and how they relate to one another.

### Refine step by step

Do not go directly from a very abstract goal to an isolated implementation detail. Put in the intermediate steps needed for the relation to become understandable. The movement is close to _progressive differentiation_: starting from general concepts and successively developing more specific ones. [HKU](https://kb.edu.hku.hk/approaches_advance_organizers/)

In a project description the chain may be, for example:

> The project's goal → the chosen strategy → the work packages' responsibilities → concrete activities → deliveries and acceptance criteria.

Each level then explains the role of the next.

### Give only the frame that is needed

Whole-to-detail does not mean that every text should open with a long history or a very broad perspective on its subject. The frame starts from what the intended reader already knows and what the reader needs to understand next. Relevant preparation ties new information to existing knowledge; it does not retell everything from the beginning. [Springer](https://link.springer.com/rwe/10.1007/978-1-4419-1428-6_157)

## 4. Example: a project description

The following illustrates the model at three levels.

### The document's opening

> The project is to reduce the manual handling of incoming orders by automating their validation and transfer to the business system. The work covers integration and error handling, but not a replacement of the business system.

This establishes goal, approach and delimitation. The reader gets a frame for judging the rest of the project description.

### The opening of the section "Error handling"

> Error handling is to ensure that an order is either processed automatically or becomes visible for manual action. The solution therefore distinguishes between temporary technical errors and errors in the order's content.

The section introduces its goal and the division that the following parts build on.

### A paragraph in the section

> Temporary connection errors are handled with automatic retries. The system makes at most three attempts with increasing wait times. If all of them fail, the order is flagged for manual handling.

The paragraph opens with the principle, refines the behaviour, and finally describes the outcome.

Note that "three attempts" becomes meaningful only once the reader knows which kind of error is handled and what function the retries serve.

## 5. The model governs the order of understanding, not a single outline

Whole-to-detail does not mean that every text must follow the order "background → problem → solution". What matters is that the reader has the right prerequisites at the right moment. Sections can then be organized by, for example, process, comparison or argument, while still introducing their subject before developing it. [Heiser](https://gernot-heiser.org/style-guide.html)

A concrete conclusion may therefore come first if the intended audience can understand it. If the conclusion rests on unfamiliar categories or assumptions, those must be established first, or explained right beside the conclusion.

## 6. A practical review test

The model translates into five control questions for every document, section and paragraph, and one symptom that most reliably exposes a fault in the order. They are set out, with how to apply them, in [review_test.md](../rules/review_test.md).

## Refinements from the sources

Three refinements sharpen the model without changing it, and a fourth settles how it reads at paragraph level.

A forward reference is allowed when an approximate understanding is enough at that point. Gernot Heiser's style guide allows a forward reference when an approximate understanding of the concept suffices at that point in the text. The rule "prerequisites before dependents" still holds; the forward reference passes only when the dependency at that point is shallow.

Details visibly tie back to the frame. The SAGE chapter on advance organizers names a phase called integrative reconciliation: new material is related back to the organizer that introduced it. Applied here, a detail does more than follow its frame in sequence. The text shows which part of the frame the detail serves, so the reader never has to reconstruct the connection.

Functional refreshes stay and restated claims go. Heiser recommends "strategic redundancy" (a short preview and summary around a section) and refreshers for terms that have not been used for many pages. That partly collides with the rule against repetition ([redundancy.md](../../basics/reference/redundancy.md)). The reconciliation: a sentence that re-orients the reader, or reminds them what a term means before it carries new weight, does work and stays. A sentence that says again what the text has already established, with nothing new resting on it, is repetition and goes.

The core sentence of a paragraph may sit in different positions, as guidance on section construction commonly advises. What does not vary is the dependency order: by the time a detail arrives, the reader holds the frame the detail needs, either from the core sentence or from what the text has already established. A paragraph that opens with a concrete case and states its point afterwards passes when the case is readable on its own; it fails when the case only makes sense once the point is known. The model's "main thought before development" says "normally", and this is how that word is read.

## Attribution note

The model's opening rule — never presuppose more knowledge than the reader's prior knowledge together with what the text has already established — is often linked to the Springer encyclopedia entry on advance organizers. The wording comes from Heiser ("don't expect more knowledge … than the union of the initial state and what you've told them so far"); the Springer entry does not contain it. The Springer entry still supports the surrounding claims: it defines advance organizers as material at a higher level of abstraction, generality and inclusiveness, which is why a frame differs from a table of contents.

## Sources

- Gurlitt, J. (2012). "Advance organizer." In N. M. Seel (ed.), _Encyclopedia of the Sciences of Learning_. Springer. <https://link.springer.com/rwe/10.1007/978-1-4419-1428-6_157>
- Heiser, G. _Style guide_. <https://gernot-heiser.org/style-guide.html>
- SAGE, chapter 13, "Advance organizers" (models of teaching). <https://in.sagepub.com/sites/default/files/upm-binaries/14256_Chapter13.pdf>
- Språkrådet (2014). _Myndigheternas skrivregler_. §1.5.3 "Sammanfatta det viktigaste" supports putting the most important first, in a summary that can be read on its own; §3.5 supports informative headings that carry the message.
- The HKU knowledge-base page and the Pressbooks chapter cited inside the model could not be retrieved when the model was checked; their claims agree with the sources above but are unverified at source.
