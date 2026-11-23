# Pre-send checks in full

The [pre_send_checks.md](../rules/pre_send_checks.md) rule states the hard stops and the final control question, and requires this checklist and the three tests before a message leaves. This file holds all of them in full.

A message that reads well is checked before it leaves, because a fault that survives into the send is the recipient's to discover. The checks below are the general core of a sales send routine, scaled to the message. Where the consuming repository keeps its own compliance controls — marketing-law and personal-data checks, send approval — those run separately and this file replaces none of them.

## Hard stops

The message does not leave while any of these holds, and a well-formulated text is never excused by an otherwise high average:

- An unverified fact that the message's point rests on.
- An invented relationship or an invented shared history.
- A result claim the sender cannot stand behind.
- A material limitation omitted where its absence misleads (§3 of [message_doctrine.md](message_doctrine.md)).
- A commitment the sender cannot keep.
- A recipient who has declined contact.

## The checklist

An unchecked point leads to a concrete change or a reasoned decision, never routine clicking:

- There is a clear reason to communicate exactly this to exactly this recipient.
- The message builds on the actual relationship and answers the latest relevant question (§5 of [message_doctrine.md](message_doctrine.md)).
- Claims, conclusions, limitations and commitments have the right grounds (§6).
- The information is needed for the recipient's assessment; the rest is removed or placed correctly (§3).
- The next step, where there is one, is intelligible, motivated, and possible for the recipient (§7).
- The tone implies neither nonexistent insight, nor superiority, nor social obligation.
- The message survives forwarding and matches what the sender has said elsewhere and can actually deliver (§8).
- The sender would say every sentence to the recipient in person and stands behind it, the message carries nothing a template would contain, and a message whose job is the relationship (thanks, apology, condolence, congratulation) is the sender's own writing ([relational_messages.md](relational_messages.md); the core `integrity` and `machine_tells` packages).
- Sender, recipient, links, attachments, dates and any promised reply time are checked.
- The subject line and the close pass the per-sentence control question of the claims doctrine ([claims_and_evidence.md](../../../../core/packages/claims/reference/claims_and_evidence.md) §6), and the subject line states the message's intent and the role it concerns ([messages.md](../../replies/reference/messages.md)).
- Prose written in English or Swedish to someone outside the sender's circle is checked for idiom written from the facts (English: the `write_from_facts` rule of the `translation` profile; Swedish: `svenska_fran_sakunderlaget` in the writing_sv module's `core` profile).

## The three tests

- The interchangeability test: if names and companies are swapped, is the message unchanged? For a personal message this is a warning sign of generic content. Standardized delivery information is exempt.
- The forwarding test: is the content still correct and defensible when someone other than the intended recipient reads it?
- The answer-cost test: what must the recipient actually do to reply? When the effort is larger than the message implies, the request is changed or the effort is described honestly.

## The final control question

The last question before sending is whether the recipient has been given sufficient, correct and relevant reasons for exactly the step the message asks for. Whether the message sounds convincing is beside it.

