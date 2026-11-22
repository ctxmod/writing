# Genre principles for translation

A translation succeeds when its reader cannot tell it is one. The target text is written from the facts of the original, as a fluent writer of the target language who knew only those facts would write it; the original's sentence structure, idiom and conventions stay behind. The base model in [whole_to_detail.md](../../../../core/packages/whole_to_detail/reference/whole_to_detail.md) applies to the target text in full, so the target text's order serves its own reader, and a frame the original left implicit is made explicit where that reader needs it.

## Both directions are written from the fact base

The rule holds for Swedish into English and English into Swedish alike. The test: would a fluent writer of the target language, knowing only the facts, have produced this phrasing? Where the answer is no, the sentence is rewritten from the facts. Every word of a sentence can be correct and the sentence still fail, because a structure carried over from the source and patched in the target language keeps the source's shape and reads as a translation.

The language profiles hold the test's worked repairs in each direction, and they are not repeated here. Swedish into English is the rule [write_from_facts.md](../rules/write_from_facts.md) of this package: the established English term over a literal rendering, phrases that comment on a resemblance cut, unsupported universals replaced by the actual problem, and natural idiom that can carry a Swedish sensibility of clarity, modesty and an absence of hype. English into Swedish is the rule "Svenska skriven från sakunderlaget" (`svenska_fran_sakunderlaget` in the writing_sv module, profile `core`, package `regler`), applied to translation in `oversattning_och_terminologi` (module `writing_sv`, profile `webb`, package `genrer`).

## The target language's conventions

The target text follows the target language's conventions for compounds, capitals, quotation marks, apostrophes, numbers and abbreviations. A convention carried over from the source text is a mechanical error in the target text, whatever the source did. The conventions that differ between Swedish and English are tabulated, with their sources, in `terminologi_och_parallellsprak` (module `writing_sv`, profile `parallellsprak`, package `sprakbruk`); each language profile holds its own conventions in full.

## One term per concept

A concept keeps one name throughout the target text. A translator who alternates between a target-language term and the source-language term for the same concept makes the reader wonder whether two things are meant. The general rules are in [prefer_plain_words.md](../../../../core/packages/basics/rules/prefer_plain_words.md) and [cut_padding.md](../../../../core/packages/basics/rules/cut_padding.md); the Swedish practice, with the first-occurrence form for a term the reader may meet in English, is in `terminologi_och_parallellsprak` (module `writing_sv`, profile `parallellsprak`, package `sprakbruk`).

## The original comes first

Where a text has an original and a translated version, the original is written and settled first, and the version is written from the original's facts afterwards. A change of substance is made in the original and carried into the version; the version does not drift into a second text with claims of its own. Which language is the original is decided per publication and recorded with it; a Swedish publication with an English version keeps Swedish as the original.

## Machine and agent drafts

A draft from machine translation, a chatbot or an agent is input to the translator, reviewed critically like any other source; the agent's own draft is reviewed with the same scepticism. The base's ruling that AI output is an editor's input is in [tone_and_register.md](../../../../core/packages/basics/reference/tone_and_register.md), and the Swedish source for the review rule is _Snabba skrivregler_ chapter 56, cited in `terminologi_och_parallellsprak` (module `writing_sv`, profile `parallellsprak`, package `sprakbruk`).

