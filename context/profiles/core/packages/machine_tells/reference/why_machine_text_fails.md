# Why machine-sounding text fails readers

When a reader suspects that a text was produced by a machine on the sender's behalf, they read it as cheaper. They credit it with less effort and less sincerity, and the discount falls on the sender as well as the text. The research below shows the effect, its limits, and why the repair is substance and ownership. Making the text look human is not the repair. The tests themselves are in [tell_catalogue.md](tell_catalogue.md).

## 1. What readers do with suspected machine text

Hancock, Naaman and Levy (2020) named the field. In AI-mediated communication an intelligent agent modifies, augments or generates messages on a communicator's behalf, and the authors argued that this changes how people judge each other through text. The experiments since then point the same way, with limits.

Jakesch and colleagues (CHI 2019) showed people human-written accommodation-host profiles and told them some were AI-written. Where readers believed they were seeing a mix, they trusted the hosts whose profiles they took for AI-written less, an effect the authors called the "replicant effect". Where everyone was believed to use AI, the difference disappeared.

Suspicion alone is enough. Hohenstein and colleagues (*Scientific Reports*, 2023; two randomized experiments, n = 1,036) found that actual use of smart replies sped up conversations and made partners rate each other as closer and more cooperative. Yet participants whom their partner suspected of using smart replies were rated more negatively, whether or not they had used them.

Sincerity suffers most visibly. Cao and Li (*Journal of Computer-Mediated Communication*, 2026; two pre-registered studies, N = 546 for apologies and N = 561 for thank-you messages) found that cues of AI involvement reliably lowered the perceived sincerity of the message. Once readers had been made aware of AI mediation, their suspicion carried over to later messages that bore no cue, and lowered forgiveness and reciprocity.

Which kinds of message suffer most is contested. Liu and colleagues (CHI 2022) found that trust in email writers fell when readers were told AI was involved, but, against the authors' expectation, less so for interpersonal emails than for transactional ones. Studies summarized by Nielsen Norman Group in 2026 found the opposite, with the largest penalties for interpersonal writing. The consistent finding is the general one, that suspected machine authorship lowers trust in the sender.

Disclosure has its own evidence. Schilke and Reimann (2025; 13 experiments, more than 5,000 participants) found that disclosing AI use lowered trust and that exposure by a third party lowered it further, while a review of news-reader studies found no consistent disclosure penalty. The consequences for disclosure are in [disclosing_assistance.md](../../integrity/reference/disclosing_assistance.md).

## 2. Workslop and the cost to the sender

Niederhoffer, Hancock and colleagues (*Harvard Business Review*, September 2025) defined workslop as "AI generated work content that masquerades as good work, but lacks the substance to meaningfully advance a given task". In their survey of 1,150 full-time US desk workers, about 40 percent had received some in the previous month, and each case took close to two hours to deal with. Recipients judged senders harshly. Around half saw the sender as less creative, capable and reliable than before, and 42 percent as less trustworthy. The figures are self-reported and come from a study run with a coaching company's research lab, so they show the direction of the judgment more reliably than its size. The mechanism matches §3. A polished text that leaves the work to the reader shifts effort onto them while appearing to have saved it.

## 3. Effort and signal

People use effort as a cue to quality. Kruger and colleagues (2004) found that identical poems and paintings were rated higher when people believed they had taken longer to make. Personal writing works partly as a costly signal. A specific letter shows that its writer spent attention on this reader, and a text anyone could have generated in seconds shows nothing of the kind.

Labour-market research shows the signal eroding. Galdin and Silbert (working paper, 2025) found on a freelance platform that before LLMs, employers paid more for workers whose applications were tailored to the job, and after LLMs they did not. Their model implies a less meritocratic market when written applications stop signalling ability. Assistance at the surface is a different matter. In a field experiment with nearly half a million jobseekers, Wiles, Munyikwa and Horton (*Management Science*, 2025) found that algorithmic help that fixed spelling and grammar on resumes increased hiring by about 8 percent, and employers were not later disappointed. The penalty attaches to replacing the author's substance and attention, not to clean prose, which is why [author_integrity.md](../../integrity/reference/author_integrity.md) §6 allows editing help everywhere and keeps the substance with the author.

## 4. Tells are real, detection is unreliable

Readers notice patterns, and some patterns are measurable. Kobak and colleagues (*Science Advances*, 2025) compared word frequencies in more than 15 million PubMed abstracts with projections from earlier years and estimated that at least 13.5 percent of 2024 abstracts were processed with LLMs, over 40 percent in some subgroups. The excess was almost entirely style words. "Delves" was 28 times more frequent than projected, "underscores" 13.8 times and "showcasing" 10.7 times, with "potential", "findings", "crucial", "intricate" and "notably" among the common ones. Juzek and Ward (COLING 2025) identified 21 such focal words and found evidence consistent with, but not proving, a role for human-feedback training.

Yet most people cannot tell machine text from human text, and the cues they rely on are wrong. In six experiments with 4,600 participants, Jakesch, Hancock and Naaman (*PNAS*, 2023) found that people could not detect AI-generated self-presentations. They took first-person pronouns, contractions and family topics as signs of a human, cues a generator can easily produce. People who use LLMs often for writing do much better. In Russell, Karpinska and Iyyer (ACL 2025) the majority vote of five such annotators misclassified 1 of 300 articles. They relied on AI vocabulary and also on formulaic structure, originality and clarity.

The Wikipedia project that cleans up generated articles keeps the most detailed public list of signs ("Signs of AI writing"), and it states the limits plainly. The signs are symptoms of a problem and not the problem, detectors and human judgment both err, and fixing the surface signs without the underlying problem only makes the problem harder to find. Its list also changes as models change. Overuse of em dashes, for example, moved to its historical section in 2026 after newer models were tuned to avoid them.

## 5. What follows for writers

- Tells are symptoms of missing substance. A stock word, an inflated claim or a summary close usually marks the place where the author had nothing specific to say. The repair puts the specific fact, decision or reason there, or cuts the sentence.
- Camouflage fails twice. Adding contractions, typos or folksy asides to make a text read as human games the flawed cues of §4. It deceives the reader, and the text still tells them nothing. Only substance and ownership pass the catalogue's tests.
- The catalogue is built on functions, not word lists. A word list dates with each model generation, while a test of what a sentence does for its reader does not. The vocabulary entry treats words as a symptom to check, never as banned terms.
- A tell is never proof about someone else's text. Careful, correct and formal prose is not evidence of a machine, and a reviewer who meets tells in a colleague's draft names the defect ("this paragraph is generic", "this claim has no source") and not a suspected origin.
- The evidence is young and partly contested. Effects vary with context, with what readers expect, and with how common AI use becomes. The direction of the findings is stable enough to act on, and the sizes are not.

Related: [tell_catalogue.md](tell_catalogue.md), [read_for_tells.md](../rules/read_for_tells.md), [reader_empathy.md](../../reader/reference/reader_empathy.md), [author_integrity.md](../../integrity/reference/author_integrity.md).

## Sources

- https://academic.oup.com/jcmc/article/25/1/89/5714020 — Hancock, Naaman and Levy, "AI-Mediated Communication: Definition, Research Agenda, and Ethical Considerations", *Journal of Computer-Mediated Communication* 25(1), 2020, doi:10.1093/jcmc/zmz022; accessed 2026-11-23.
- https://sml.stanford.edu/publications/hancock-jt/ai-mediated-communication-how-perception-profile-text-was-written-ai — Jakesch, French, Ma, Hancock and Naaman, "AI-Mediated Communication: How the Perception that Profile Text was Written by AI Affects Trustworthiness", CHI 2019, doi:10.1145/3290605.3300469 (the replicant effect); accessed 2026-11-23.
- https://pmc.ncbi.nlm.nih.gov/articles/PMC10073210 — Hohenstein et al., "Artificial intelligence in communication impacts language and social relationships", *Scientific Reports* 13, 5487 (2023); accessed 2026-11-23.
- https://academic.oup.com/jcmc/article/31/6/zmag024/8890537 — Cao and Li, "The sequential replicant effect in interpersonal sincerity: evidence from AI-mediated apology and gratitude", *Journal of Computer-Mediated Communication* 31(6), published online 8 October 2026, doi:10.1093/jcmc/zmag024; accessed 2026-11-23.
- https://doi.org/10.1145/3491102.3517731 — Liu, Mittal, Yang and Bruckman, "Will AI Console Me when I Lose my Pet? Understanding Perceptions of AI-Mediated Email Writing", CHI 2022 (abstract read through the Semantic Scholar record); accessed 2026-11-23.
- https://www.nngroup.com/articles/disclose-ai-paced/ — Nielsen Norman Group, 25 September 2026, summary of disclosure studies (news-reader review; degree of AI use; interpersonal writing); accessed 2026-11-23.
- https://ideas.repec.org/a/eee/jobhdp/v188y2025ics0749597825000172.html — Schilke and Reimann, "The transparency dilemma: How AI disclosure erodes trust", *OBHDP* 188 (2025), 104405; accessed 2026-11-23.
- https://hbr.org/2025/09/ai-generated-workslop-is-destroying-productivity — Niederhoffer, Kellerman, Lee, Liebscher, Rapuano and Hancock, "AI-Generated 'Workslop' Is Destroying Productivity", *Harvard Business Review*, 22 September 2025; the definition and survey figures were verified through secondary reports (https://www.simonwillison.net/2025/Sep/22/workslop, https://www.axios.com/2025/09/24/ai-workslop-workplace-efficiency-study) because the article is paywalled; accessed 2026-11-23.
- https://api.crossref.org/works/10.1016/s0022-1031(03)00065-9 — Kruger, Wirtz, Van Boven and Altermatt, "The effort heuristic", *Journal of Experimental Social Psychology* 40 (2004); accessed 2026-11-23.
- https://arxiv.org/abs/2511.08785 — Galdin and Silbert, "Making Talk Cheap: Generative AI and Labor Market Signaling", working paper, 11 November 2025; accessed 2026-11-23.
- https://www.nber.org/papers/w30886 — Wiles, Munyikwa and Horton, "Algorithmic Writing Assistance on Jobseekers' Resumes Increases Hires", *Management Science* 71(12), 2025, doi:10.1287/mnsc.2024.04528; accessed 2026-11-23.
- https://arxiv.org/html/2406.07016v5 — Kobak, González-Márquez, Horvát and Lause, "Delving into LLM-assisted writing in biomedical publications through excess vocabulary", *Science Advances* 11(27), 2 July 2025, doi:10.1126/sciadv.adt3813; accessed 2026-11-23.
- https://aclanthology.org/2025.coling-main.426 — Juzek and Ward, "Why Does ChatGPT 'Delve' So Much? Exploring the Sources of Lexical Overrepresentation in Large Language Models", COLING 2025; accessed 2026-11-23.
- https://pmc.ncbi.nlm.nih.gov/articles/PMC10089155 — Jakesch, Hancock and Naaman, "Human heuristics for AI-generated language are flawed", *PNAS* 120(11), e2208839120, 7 March 2023; accessed 2026-11-23.
- https://aclanthology.org/2025.acl-long.267 — Russell, Karpinska and Iyyer, "People who frequently use ChatGPT for writing tasks are accurate and robust detectors of AI-generated text", ACL 2025; accessed 2026-11-23.
- https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing — WikiProject AI Cleanup, "Signs of AI writing" (caveats, signs by era, ineffective indicators, historical indicators including em dashes); accessed 2026-11-23.
