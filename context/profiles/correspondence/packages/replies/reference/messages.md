# Messages, replies and personal contacts

This file holds the craft rules for emails, messages and letters on top of [message_doctrine.md](../../message_doctrine/reference/message_doctrine.md): the density, what a message says beyond its purpose, how a reply is built, and the register for personal contacts. Greetings and sign-offs follow the writer's own style preference where one is kept (a personal or house style layer); this file fixes only where the register departs from it.

## Density and form

Messages are short and direct; letters carry the fuller tone; the base file on one voice at many densities governs the scale ([tone_and_register.md](../../../../core/packages/basics/reference/tone_and_register.md)). Connected text is the default, and bullets appear only where the content is genuinely a list, per catalogue entry 1. The message closes calmly, with a concrete next step where one fits (§7 of [message_doctrine.md](../../message_doctrine/reference/message_doctrine.md)).

When a meeting is wanted, the message proposes concrete times, and a vague availability window does the recipient's scheduling work for them: "today at 3 or 4 PM, or tomorrow afternoon — what suits you?" rather than "fairly open this week". The Swedish form is in `svensk_korrespondens` (module `writing_sv`, profile `korrespondens`, package `meddelanden`).

## The opening and the subject line

The first sentence gives the purpose or the point, per §2 of [message_doctrine.md](../../message_doctrine/reference/message_doctrine.md); a warm-up and an opening pleasantry fail, and so does a tentative opening that asks permission to have a purpose.

Too stiff (avoid, illustrative):

> I am writing to inform you that the project has been completed.

Better (illustrative):

> The project is now done, and the next step is to go through the results together.

Too tentative (avoid, illustrative):

> I am writing to ask whether you might possibly be interested.

Better (illustrative):

> I am getting in touch about the backend developer role, since it matches what I have built over the past few years.

The subject line states the message's intent: what the sender wants with the recipient, in plain words, such as "Interest in a developer role with your team" or "Proposal for the March workshop". It never names only the territory the message touches, and a headline-style technical title ("Security-first control planes for agent fleets") fails, however accurate. A message about a specific role, assignment or position makes clear which one it concerns; when the body says only "the role", the subject line carries its name. Sales first contacts specialise this rule in the `sales_outbound` profile `first-contact.md`.

A short email that leads with the point (illustrative):

> Hi Anna,
>
> I have gone through the material and see two ways forward. If you want to move quickly, I would recommend option 1, since it takes the least change to your current flow. I am happy to put together a concrete proposal by Thursday.
>
> Best regards,
> Daniel

## Say only what serves the message

Each of these is a cut test applied before sending; the message that passes them all is the one where everything present does work for the recipient:

- A message does not echo the recipient's own pitch back to them; the reply engages with it.
- Sensitive situations are treated with discretion: reasons are stated in neutral, factual terms and no further. The claims doctrine's rule on negative results, kept and scoped, is the base for this ([claims_and_evidence.md](../../../../core/packages/claims/reference/claims_and_evidence.md) §5).
- When acknowledgment plus logistics is the whole message, the message is just that, without a recap of what the other person said.
- A decision that already stands on its own is stated with its one real reason, and the message stops; it does not argue for what is already decided. When the recipient is being advised rather than told, §7 of [message_doctrine.md](../../message_doctrine/reference/message_doctrine.md) carries the recommendation's reason, trade-off and what would change it.
- The next round of asks waits for its own message; a message that has done its job stops.
- When an attachment carries the substance, the note stays light: it confirms interest and hands the attachment over, the sender's fit is not recited point by point, and the effort of producing the attachment is not flagged; the work shows in the work. A short, warm note plus a small practical offer, such as the same document in the other language, reads as more assured than a paragraph of self-explanation.
- A step that belongs to the other person is left to them (§7 of [message_doctrine.md](../../message_doctrine/reference/message_doctrine.md)).

A message that defends a decision already standing (avoid):

> I'd rather not spread thin, so let's lead with A and come back to B if that doesn't work out.

The same decision stated plainly (better):

> Let's focus on A and come back to B if that doesn't work out.

The remaining pairs are illustrative; names and companies are invented.

A reply padded with a recap of what the other person said (avoid):

> Hi Sam, that all sounds good, the salary, the hybrid setup, and meeting the team lead after our chat. Happy to take it further. I'm free today at 4:30 PM and tomorrow afternoon, what works for you?

Acknowledgment and logistics only (better):

> Hi Sam, that all sounds good, happy to take it further. I'm free today at 4:30 PM and tomorrow afternoon, what works for you?

Internal detail shared with a recruiter just met (avoid):

> I've been part-time and the plan was to go full-time, but the contract was never signed and a couple of clients were cut.

The same reason, neutral and factual (better):

> A couple of client contracts were cut and the company may need to scale down, so I'm looking at other opportunities.

The recipient's pitch echoed back (avoid):

> Northwind sounds genuinely interesting, building real production systems on top of messy operational workflows is close to what I do.

Acknowledged in a clause, then on to the substance (better):

> Northwind sounds genuinely interesting, and both the applied-AI and the platform tracks look like a fit.

The next round of asks bundled onto a message that sets direction (avoid):

> I think we can park C. For A, could you let me know the salary range and what the next step looks like? Happy to do a technical round when it suits them.

The message doing its one job (better):

> I think we can park C.

Fit recited and effort flagged over an attached CV, with a step that is the recipient's to take (avoid):

> Thanks for the call and the details. The company looks like a strong fit, the role lines up well with what I do: building data platforms hands-on, plus the architecture and stakeholder side. My CV is attached, tailored to the role. Happy to take it to a conversation with the two hiring managers whenever suits them.

A light note that lets the CV carry the substance (better):

> Thanks for the call and for sending over the details. It looks like a strong fit and lines up well with what I'm looking for. My CV is attached; let me know if you would prefer it in Swedish.

## Replies and threads

A reply answers the answer. When the reply resolves what the thread was about, that thread's question is dropped rather than pivoted to a new topic; a new topic gets a new message. The reply addresses what the recipient actually wrote, and when what is needed has become clear enough, the reply moves to the concrete step instead of gathering more information without an end.

A thread keeps the four placements honest across messages: what was promised in one message is delivered or re-dated in the next, and the record of what was believed and what the recipient actually did stays apart (§10, step 8, of [message_doctrine.md](../../message_doctrine/reference/message_doctrine.md)).

Follow-up — a reply to silence — is governed by the `sales_outbound` profile where the thread is a sales thread; elsewhere a follow-up is a message like any other and passes the same tests, §1's motivated step and §7's recipient control in [message_doctrine.md](../../message_doctrine/reference/message_doctrine.md).

## Personal contacts and referrals

A message to a referred personal contact with a named recipient ("my sister knows someone at the company") is its own register: the note a person types to a friend of the family, inside the relationship that actually exists (§5 of [message_doctrine.md](../../message_doctrine/reference/message_doctrine.md)). In such a note the shared history is the point of the opening and does not count as a warm-up under §2.

Before drafting, the shared history is established: shared occasions, places, summers, and the role the recipient played in them. Someone who drafts on the sender's behalf, an assistant or an agent, cannot know it and asks the sender first. When no answer is available, the opening stays history-neutral and the open question is flagged to the sender. History is never invented, its absence is never assumed, and a real relationship is never flattened to a template such as "X recommended I contact you".

Where history exists, the message opens with it: the specific shared memory, with place, occasion and the recipient's part in it, plus a warm and specific compliment about it, is the strongest opener. A playful, self-aware aside belongs in this register (illustrative: "you might recognise my surname").

The register is the inner circle's:

- The shared connection is named the way the circle names them, by a nickname where the circle uses one.
- The greeting may carry an exclamation mark ("Hi Maria!") and the sign-off is casual ("Cheers", or the first name alone); for a warm or referral-based first contact this departs from the writer's default greeting and sign-off.
- Minimizing frames ("just a few initial questions:") and natural, everyday verbs are preferred over stiffer ones.

The self-description matches the audience, and positioning lives in the specifics: to an engineer, the plain honest label ("full-stack developer") plus concrete recent work carries the specialist signal. Positioning language never appears in a personal note.

Experience figures stated casually are ceilings, and the exact wording is not mandatory: "over five years" may become "about five years", because rounding down is always safe and overstating never is. Where the recipient would otherwise do confused arithmetic, for instance over a career that ran alongside studies, one clause may meet it; the permission is narrow and licenses no further caveats.

The questions carry the conversation: two or three of them, as bare lines without bullet chrome, in soft habitual phrasing ("do you usually …"). A first note asks no question about the process or the next step, because the reply is the next step, and no coffee-or-call close is bolted on. Research on the recipient's company gets one light line ("I had a quick look at your site, and … sounds exciting"); analyst detail stays out.

A first contact made through a mutual-acquaintance referral counts as warm: the warm register is allowed there, also when the contact serves a commercial purpose. Such a first contact also keeps the warm shape described above, with its questions and no call-to-action, when its purpose is commercial; the `sales_outbound` profile states how its other rules apply to it.

