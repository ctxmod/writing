# Plain style in full

The rules [prefer_plain_words.md](../rules/prefer_plain_words.md), [cut_padding.md](../rules/cut_padding.md) and [active_voice_default.md](../rules/active_voice_default.md) state their obligations and tests in brief. This file holds each rule in full, with its rationale and examples.

## Prefer Plain Words

Choose the common, concrete word over the rare or inflated one: "use",
not "utilize"; "show", not "demonstrate"; "before", not "prior to";
"end", not "conclude". Plain does not mean simple-minded — it means the
reader decodes the word instantly and spends the saved attention on
the point. A sentence that survives the plain-word test reads faster
and translates better across skill levels and machine pipes.

### Rationale

Inflated vocabulary usually signals either habit or anxiety, and both
read as padding. The plain word is almost always shorter, and shorter
sentences carry fewer places to hide a mistake. Jargon still has its
place — use it when the audience demonstrably shares the term and the
term is more precise than any plain substitute, then define it on
first use in any document that might outlive that audience.

Worked replacements: `utilize → use`, `prior to → before`,
`in order to → to`, `at this point in time → now`,
`is able to → can`.

Plain words are one part of plain language, not the whole of it: ISO
24495-1:2023 defines plain language by whether the intended readers
can find, understand, and use the information, and judges it on
readers rather than readability formulas. The standard's four
principles and how they map onto this module are in
[plain_language_standard.md](plain_language_standard.md).

### Precision and idiom

Use precise technical terms when they do real work, and leave
buzzwords unstacked; write natural idiom with neither stiffness nor
over-selling. When shortening, choose content away rather than
replacing concrete words with abstractions. When a text makes a claim
about technology, be as specific as the claim requires: name the
system, layer, or practice the claim is about, so the claim can be
checked; the umbrella term is right only when the category itself is
the subject, the term is discussed, it is part of a quotation or
official name, or professional copy introduces a familiar category and
then says what the work is. The worked pairs are in
[diction.md](diction.md).

## Cut Padding

Delete every sentence that announces, warms up, or apologizes for the
writing instead of doing it. The repeat offenders: "It is important to
note that", "As you may already know", "Please be advised that",
"I just wanted to quickly", "Needless to say". Each one delays the
point by a clause and tells the reader their time was not respected
enough to spend none of it.

### Rationale

Padding survives because it feels polite, but readers experience it as
friction: they pay attention to every word and get nothing back. The
discipline is mechanical — read a draft and mark the first seven words
of every paragraph; anything in those words that does not carry
information is a candidate. Single-word fillers go the same way:
`very`, `really`, `actually`, `basically`, `quite` almost never change
a sentence's truth, only its length. Keep the intensity only where it
is doing measurable work ("a very fast fall" where the speed is the
point).

### Restatement

A clause earns its place by adding information. Restating the
preceding clause in other words is never acceptable, however well
written: keep the more concrete formulation and cut the other. The
forms a restatement takes — colon or comma clauses that say it again,
spelled-out implications the reader already drew, paired
near-synonyms doing one job, the same claim repeated across sections,
and adjacent sentences doing one job twice — and what does not count
(a distinct fact, a tail that carries a new result, overlap that a
structured field requires) are in [redundancy.md](redundancy.md).

## Active Voice by Default

Default to the active voice: the actor acts. "The review found two
defects", not "two defects were found". Go passive only for one of
three reasons — the actor is unknown ("the package was deleted"),
irrelevant to the point ("the bridge was built in 1897"), or
deliberately de-emphasized to keep attention on the object ("the fix
was verified by three independent tests").

### Rationale

Active sentences name who did what, and named actors carry
accountability: the reader can follow up, verify, or assign credit.
Passive constructions hide that information, and hidden actors are
where vague responsibility lives. A useful audit is to search the
draft for a form of "be" followed by a past participle
(`was found`, `is considered`) and ask for each hit whether one of the
three reasons applies; if none does, name the actor and flip the
clause.
