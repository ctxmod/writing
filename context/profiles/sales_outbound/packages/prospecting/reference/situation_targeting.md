# Targeting by situation

How a B2B practice decides who is worth a cold email, and how it builds the understanding needed to write one that does not read as cold: situation-based targeting, public research sources, picking the recipient, the dossier each prospect gets, and how a research session runs. The email address is resolved afterwards by [email_discovery.md](email_discovery.md); the message itself follows the first-contact craft ([first_contact.md](../../outreach/reference/first_contact.md)).

## Target by situation, not by list

Do not assemble a list of companies in a sector and email all of them. Look for companies in a **situation** where the practice's specific competence is the obvious answer, because the situation is what creates both relevance and urgency, and relevance is what makes a cold email legitimate (see the legitimate-interest balancing test in [gdpr_eprivacy_cold_email.md](../../compliance/reference/gdpr_eprivacy_cold_email.md)).

The practice defines its qualifying situations in its own positioning, kept in its repository. They take shapes like these:

- A **pilot that has stalled** between a promising demo and production.
- A **regulatory deadline** forcing a capability to ship safely.
- A **prototype hitting a production wall**, where reliability, cost, or security suddenly matter.
- A company that **wants a capability over its own data or systems** and has nobody in-house who has shipped that before.

Some sectors make a situation bite harder (regulated industries, fast-growing scale-ups), and the practice may note where its credibility is strongest. But the door in is always the *situation*, not the sector.

A practice that would also welcome another kind of engagement (a permanent role instead of a contract, say) records that in its own positioning and in each dossier's `door` field; the cold email still leads with the situation and a useful offer, never with the engagement form, which surfaces in the conversation if and when it fits.

## Signals that a company is in one of these situations

These are what to look for in research; each is a concrete, observable hook an email can open with:

- **Hiring signals:** an open role for exactly the competence the practice offers, or a senior role whose description mentions the problem. A company hiring for this has the need and the budget but not yet the person.
- **Public statements:** a blog post, podcast, or conference talk where a founder or CTO says they are building the capability, or struggling to.
- **Product signals:** a recently launched feature that is visibly rough, a "beta" label, a changelog mentioning the work.
- **Funding signals:** a recent raise whose announcement names the area; the money and the mandate are fresh.
- **Regulatory exposure:** a company in a regulated sector (fintech, health, public sector) that has announced ambitions where the regulatory angle is the differentiator nobody else is offering.
- **Technical signals:** job-ad stacks, public repos, or engineering-blog detail that show a stack adjacent to the practice's own.

## Where to find them (public sources only)

Research uses **public sources**. No purchased lists, no scraped databases.

- **Job boards:** company career pages, LinkedIn Jobs, regional startup boards (in the Nordics, The Hub), consultancy-broker assignment posts, Wellfound, specialist boards.
- **Funding and news:** regional tech press (in Sweden, Di Digital and Breakit), Tech.eu, Sifted, EU-Startups, press releases, the company's own newsroom.
- **Ecosystems:** accelerator and incubator portfolios (in Stockholm, for example SUP46, STING, Norrsken, Antler) as *directories of companies in the right stage* — to research and email, not to ask insiders for introductions.
- **Company surfaces:** the company website, engineering blog, public GitHub, changelog, product pages.
- **People:** the public-facing parts of LinkedIn, company team pages, conference speaker lists, podcast guest lists, to identify the right recipient (usually the CTO, founder, VP Engineering, or head of product).

When research needs something behind a login or a paywall (a full LinkedIn profile, a paid database), **queue it for manual work** rather than guessing; see the queue below.

## Picking the right recipient

One person per company, the person who owns the problem and can say yes:

- **Small startup (≤ ~30):** founder, CEO or CTO.
- **Scale-up:** CTO, VP Engineering, or head of product or of the relevant function.
- **Larger or regulated organisation:** the head of the relevant function, or an engineering manager owning the specific initiative; avoid generic "info@" addresses.

Pick the person whose job the practice would make easier. The email should be something that person is glad to have received because it speaks to a problem they actually own.

## The dossier

Every prospect that survives qualification gets a short dossier, the raw material for a genuinely personal email and for follow-ups. It lives as one file per company in the outreach repository. A dossier records:

```markdown
---
type: prospect
company: <name>
domain: <company.com>
status: researching | drafted | sent | replied | call-booked | referral | closed | parked
recipient: <name, role>
email: <address or "unknown — queued">
email_confidence: high | medium | low | unknown
situation: <the one-line reason they're a target>
door: contract | role | either | unknown
created: <YYYY-MM-DD>
updated: <YYYY-MM-DD>
---

# <Company>

## Why them (the situation)
The specific, observable signal that put them on the list, with the source link.

## The hook
The one true, specific opening observation the email will lead with.

## What we'd offer
Which rung of the practice's offer ladder fits, and why.

## Recipient
Who, their role, why them, what they likely care about. Source links.

## Research notes
Stack, funding, product detail, anything that sharpens the email or the follow-up.

## Manual work needed
Anything queued: email verification, deeper research behind a login, a judgment call.

## Log
- YYYY-MM-DD: researched / drafted / sent / replied / followed up / referral asked
```

Keep dossiers **factual and sourced**. Every claim the email will rest on must trace to something real, the same discipline the substance rule ([show_qualities.md](../../../../core/packages/claims/rules/show_qualities.md)) enforces for any claim. A fabricated or sloppy "hook" is worse than no email.

## The working data

The outreach repository keeps the working data, not this reference. A layout that works:

```
outreach/
  prospects/        one dossier per company: <company_slug>.md
  pipeline.md       the at-a-glance tracker (company, recipient, status, next step, dates)
  queue.md          the manual-work queue
  templates.md      message scaffolds
  suppression.md    the opt-out list (see the compliance package)
```

- **The dossier** per company, in the format above.
- **The pipeline** — a single table giving the whole funnel at a glance, one row per prospect: company, recipient, status, last action and date, next action and date. This is how gaps stay visible.
- **The queue** — the manual-work queue: an ordered checklist of things only the sender (or a more privileged session) can do, each with enough context to act without re-research. Example items: "Verify erik.lund@example.se before sending the Example draft (pattern-inferred, medium confidence)"; "Full LinkedIn read on Example's CTO, behind login"; "Decide go/no-go on <borderline target>."

## How a research session runs

1. Find N companies matching a qualifying situation from public sources.
2. For each, decide the recipient and write the dossier (situation, hook, offer, recipient, sources).
3. Resolve the email via [email_discovery.md](email_discovery.md), or queue a manual lookup.
4. Hand the qualified dossiers to the drafting step (the first-contact craft in [first_contact.md](../../outreach/reference/first_contact.md), and the repository's own mail-drafting mechanics).
5. Update the pipeline and the queue.

A good session might research 15–30 companies, qualify 8–15, and produce that many dossiers and drafts, plus a clear queue of what the sender must verify or send. Quality of fit and of the hook matters far more than count.
