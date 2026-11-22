# Tone and Register

Register is the formality level a document holds: the vocabulary,
sentence shape, and directness a reader expects from this kind of
text in this setting. A changelog entry, a resignation letter, and a
group chat message can state the same fact in three registers, and
each is correct in its place.

## Match register to audience and medium

Calibrate against two axes. Audience: how well do the readers know
the domain, and what relationship do they have with the writer?
Medium: what does the channel itself signal — a pull-request comment
sits more casual than a signed letter; a status report sits more
formal than a chat thread. When the two axes disagree, the audience's
expectation wins; medium sets the floor, not the ceiling. Between two
defensible registers, take the plainer one: a document slightly too
casual reads as friendly, one too stiff reads as evasive.

## Hold one register per document

Readers experience a register shift as a false note — the "Hey folks!"
opening followed by "pursuant to the aforementioned agreement" breaks
the trust the warmer opening built, because one of the two voices was
not sincere. Decide the register before drafting the first sentence,
and let it govern vocabulary, contractions, forms of address, and how
much explanation each term gets.

## Avoid register whiplash inside a sentence

The sharpest failures are local: a formal noun riding a casual clause
("the deliverable is gonna ship Friday"), slang in a legal sentence,
marketing adjectives in an incident report. When a revision must
preserve a phrase from another register — a quoted requirement, a
product name — keep the quotation exact and let the surrounding
sentence carry the document's own register.

## Signposts and effort

Formality is not length. Formal writing is often shorter — it strips
small talk, hedges, and self-reference — while casual writing earns
warmth with specific, concrete detail. If a draft feels stiff, cut
nominations and stock phrases before adding exclamation marks; if it
feels cold, add one specific acknowledgment of the reader's situation
rather than a paragraph of pleasantries.

## One voice, many densities

Keep the voice the same in its values across genres and adjust its
density to the medium: short and direct in email and chat, fuller and
more flowing in documents, letters, essays, and applications, and
tightest in the structured parts of a CV.

## The stating register

Outward prose states facts. The test for every sentence: does it state
a fact, or does it try to move the reader? Say what was done or what is
the case, concretely, and stop. Rhetorical questions to the reader,
problem framing that presumes the reader's problem, intensifiers meant
to persuade ("truly", "world-class"), and implied promises ("I help you
…") are the typical ways a sentence fails the test. The rule applies to
all writing in every language; a language or house style may develop
it further for sales-adjacent outward text.

## Self-labels

The voice of a text is what the text notices. A self-label ("curious",
"passionate", "structured") pinned beside a factual conclusion adds
nothing the reader can check, and reads as template whatever its
content. The test: strike the label and ask whether the sentence lost
any information a reader could verify; where it did not, the label
goes, and what the text chose to notice carries the voice.

## Flow

How flow is built (mainly subordinate clauses and conjunctions, or
dashes, or short sentences) is a personal-style decision that a
writer's own style layer may fix. The general ideal is only that
sentences carry connected thought as connected syntax, and vary in
length for emphasis rather than at random. Varying length never
licenses a sentence fragment or a one-line paragraph set apart for
emphasis; both fail entry 3 of the anti-pattern catalogue
([catalogue.md](../../anti_patterns/reference/catalogue.md)).

## Against the template voice

Start from the real requirement, a real case, a real decision, and an
honest reason, and keep the technical or subject texture.

Announce-then-colon. A setup that only announces what follows ("What
makes X interesting is Y: Z", "Here is the thing: …") fails, because
the sentence could have said Y directly. When the setup frames what
attracts, state it as a personal perception ("I find it especially
attractive that …"), never as the single exhaustive reason.

## No colon joins clauses in running prose

No colon joins or introduces clauses in running prose, in any
language. A colon that binds one statement to the next, or that
introduces an explanation, an example or an elaboration inside a
running sentence, reads as a template tell, even where a style guide
would allow it (Isof's _Snabba skrivregler_ §1.8 does, for Swedish).
The fix is a full stop and a new sentence, or a conjunction that names
the relation ("because", "so"). Both of these fail (illustrative):

> The setup is simple: one service, one database.

> I want responsibility that lasts over time: a platform that is maintained for years.

Rewritten (illustrative):

> The setup is one service and one database.

> I want responsibility that lasts over time. A platform should be maintained for years, not deployed once and left.

The colon stays where it is not joining prose. That covers headings and
labels ("Format:", "**Length:**"), a lead-in to a list set out as a list,
clock times and ratios, the Swedish inflection colon (EU:s), and the
colon before a quotation. The test is whether the colon sits between
two pieces of running sentence, and if it does, the sentence is
rewritten. The Swedish form
of the rule is `skiljetecken` in the writing_sv module's core profile.

AI output is an editor's input (repetition, unclear wording, grammar),
never a generic draft to accept: the final text keeps only wording the
author would say aloud.

Related: [diction.md](diction.md), and the register entries of the
anti-pattern catalogue ([catalogue.md](../../anti_patterns/reference/catalogue.md)).
