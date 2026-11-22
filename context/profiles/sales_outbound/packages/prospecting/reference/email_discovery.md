# Business email discovery

How to find and verify a prospect's work email address from public information for B2B outreach: manual search, pattern inference (including learning the pattern from a known coworker's address), confidence levels, and when to queue a human verification. It resolves a real, deliverable address for a recipient already chosen by situation targeting ([situation_targeting.md](situation_targeting.md)), and operates under the legal posture in the `compliance` package of this profile.

## Principle: public sources and honest inference only

Find addresses the way a diligent person would by hand, from public information, and be honest about confidence. Do **not** buy lists, run mass scrapers, or use breach data. A guessed address that bounces wastes the one shot at a first impression and can hurt deliverability, so every address carries a confidence level and low-confidence ones get verified before send.

## Methods, in order of preference

### 1. Published address (high confidence)

The address is stated publicly: on the company site, a personal site, a GitHub profile or commit, a conference page, a public PDF, a blog byline, an open-source `AUTHORS`/`package.json`/`Cargo.toml`, a public CV. If a person has published their work email, use it. This is the cleanest case and needs no verification.

### 2. Pattern inference from a known address (medium–high confidence)

Most companies use **one consistent email format**. If any one real address at the domain can be found, the recipient's can be inferred:

- Find a known address at the company, from any public source: a press contact, a support or sales address that reveals the local-part format, a developer's public commit email, a team member's published address, a job ad's application address.
- **Learning the pattern from a coworker's address is explicitly fine.** If a colleague of the target publishes `anna.svensson@example.se`, the company pattern is almost certainly `first.last@example.se`, so the target Erik Lund is `erik.lund@example.se`. The coworker's address is used **only to learn the format**, never to contact the coworker or trade on any relationship; that distinction is the rule.
- Apply the inferred pattern to the recipient's real, correctly spelled name. Mind national characters: in Swedish names most corporate schemes map `å/ä→a` and `ö→o`, but verify, because some keep them.

Common Swedish and Nordic patterns: `first.last@`, `first@`, `flast@`, `firstl@`, `first.last@` on a separate mail domain. Note which pattern the evidence supports and why.

### 3. Reasoned guess (low confidence — must be verified)

No known address, but the domain and the person's name are known. Construct the most likely address from common patterns. **This is never sent without verification**; queue it (below).

### 4. Catch-all or role address (last resort)

Only when no individual address can be found and the company is small enough that a founder reads `hello@` or a first-name address. Note it as low confidence and prefer queuing a manual lookup for the real person first.

## Verification

For anything below high confidence, verify before the draft is sent:

- **What an agent can do:** corroborate across sources (does the inferred pattern match two independent known addresses?), check that the domain has working mail (MX records exist), sanity-check the name spelling.
- **What is queued for the sender (manual work):** running a real email verifier (a free or paid SMTP-level checker), or any tool behind a login or paywall. Where the agent has no verification tool, **low- and medium-confidence addresses are queued in the outreach work queue with the inferred address, the evidence, and the confidence level**, and the draft is held (or marked "verify before send") until the sender confirms.

Record the outcome and the confidence with the prospect's record (for example `email` and `email_confidence` fields in the prospect dossier).

## Tools and their boundaries

- **Allowed, agent-driven:** web search, reading public pages, inspecting public git history, reading public documents, DNS/MX sanity checks (through a queued manual step if needed).
- **Queued for the sender:** paid finders (Hunter.io, Apollo, RocketReach, Clearbit), LinkedIn Sales Navigator, anything requiring an account or payment. The agent names the tool and the exact lookup to run; the sender runs it and pastes back the result.
- **Never:** scraping at scale, breach or leak databases, buying contact lists.

## The confidence-to-action map

| Confidence | Source | Action |
|---|---|---|
| High | Published, or pattern matching ≥2 known addresses | Draft and send (after normal review) |
| Medium | Pattern from one known address | Queue a quick verification; draft, mark "verify before send" |
| Low | Reasoned guess, no known address | Queue verification or a manual lookup; do not send until confirmed |
| Unknown | Nothing found | Queue a manual lookup for the address (or the right person) |

## Why this rigor matters

An outreach effort that bounces, misspells a name, or emails the wrong person contradicts any claim of care and correctness the sender makes. Getting the address right, and being honest when unsure, is part of being the professional the outreach claims to be. When in doubt, queue it: a one-day delay for verification costs nothing next to a bad first impression.
