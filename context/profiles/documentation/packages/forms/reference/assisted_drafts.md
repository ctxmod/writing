# Documentation drafted with assistance

A documentation reader arrives with a task and trusts the page to describe the product as it is. Drafting help (a generator, a template, a colleague's notes) is welcome on that page under the core ownership rule ([author_integrity.md](../../../../core/packages/integrity/reference/author_integrity.md) § 6). The author answers for every statement about the product, and two failures matter more in docs than anywhere else.

## Every statement about the product is verified

A generated draft states plausible behavior with the same confidence as real behavior. It may invent a flag, a default value, a configuration key or an error message, or describe how a similar product works. The test: every command, option, value, output and limit on the page has been checked against the product or its source, at the version the page documents. Output shown to the reader is real output, as the code-style rule of [docs_style_basics.md](docs_style_basics.md) already requires. Where behavior could not be verified, the page says so or leaves it out ([author_integrity.md](../../../../core/packages/integrity/reference/author_integrity.md) § 3). A page that is wrong with confidence costs the reader more than a gap.

## Filler that reads as generated

Docs readers scan for the step or the fact they came for, and generated filler stands in their way ([reader_empathy.md](../../../../core/packages/reader/reference/reader_empathy.md) § 4). These forms fail in documentation:

- An opening that restates the heading ("This section provides an overview of authentication"). Catalogue entry 10 allows a short scope statement in reference documents only when it helps the reader decide whether to read on.
- Generic advice that would fit any product ("follow best practices", "ensure proper configuration", "it is important to monitor performance"). It fails the interchangeability test of the tell catalogue (entry 13); the repair states the specific setting or check, or cuts the sentence.
- "Simply", "just" and "easily" in a step, which tell a reader who is stuck that the fault is theirs.
- A summary at the end of every page that repeats the page (tell catalogue entry 10).
- Hedges on documented behavior ("should typically return") where the behavior is known. Present tense states it ([docs_style_basics.md](docs_style_basics.md)).
- Bulleted reasoning and bold-labeled bullets where a procedure needs numbered steps or a concept needs a paragraph (anti-pattern catalogue entries 1 and 2; [procedures_are_steps.md](../rules/procedures_are_steps.md)).

The tests are in [tell_catalogue.md](../../../../core/packages/machine_tells/reference/tell_catalogue.md); this list names their documentation forms.
