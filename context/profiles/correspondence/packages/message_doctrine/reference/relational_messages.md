# Relational messages and machine voice in correspondence

A message is read by one person who knows the sender, or soon will, and who reads it as a sign of how the sender regards them. The core packages hold the general rules ([reader_empathy.md](../../../../core/packages/reader/reference/reader_empathy.md), [author_integrity.md](../../../../core/packages/integrity/reference/author_integrity.md), [tell_catalogue.md](../../../../core/packages/machine_tells/reference/tell_catalogue.md)). This file states where they land hardest in correspondence. One case is the messages whose main job is the relationship. The other is the everyday email habits that readers now take for generated text.

## Messages whose job is the relationship

A thank-you, an apology, a condolence, a congratulation and a reply to someone in difficulty carry little information. The recipient reads them for one thing, whether the sender saw what happened and means what they say. Cues that a machine was involved lower the perceived sincerity of apologies and thank-you messages, and once readers suspect machine mediation the suspicion carries into later messages (the evidence is in [why_machine_text_fails.md](../../../../core/packages/machine_tells/reference/why_machine_text_fails.md) § 1). These messages are therefore written by their sender. Assistance stays at the level of editing, per [author_integrity.md](../../../../core/packages/integrity/reference/author_integrity.md) § 6.

The test for each form is whether it names the specific thing and nothing a template would contain:

- An apology names the fault in the sender's own words, its effect on the recipient, and what will change, and stops. "I apologize for any inconvenience this may have caused" fails, because it names no fault, presumes no effect and changes nothing.
- A thank-you names what the person did and what it made possible. "Thank you for your hard work and dedication" fails, because it could thank anyone for anything.
- A condolence is short, names the person who died where the sender knew them, may carry one real memory, and makes only offers the sender will keep. Explanations of grief, and comfort the sender cannot know will comfort, fail.
- A congratulation names the achievement and, where the sender knows it, what it took.

Feeling in these messages is stated once, at the size the sender would show in person, and carried by the specific detail ([author_integrity.md](../../../../core/packages/integrity/reference/author_integrity.md) § 5). Too stiff (avoid, illustrative):

> I wanted to express my heartfelt gratitude for your invaluable support throughout this challenging project. Your dedication truly made a difference.

Better (illustrative):

> Thank you for taking the supplier calls in March. Without them we would have missed the go-live.

## Everyday email habits that read as generated

Some habits were padding before they were tells, and the core files already rule on them. Readers now also take them as a sign that no one wrote the message for them, which makes the cost higher:

- The service opener and closer ("I hope this email finds you well", "I wanted to reach out", "Let me know if you have any questions", "Feel free to reach out"), entry 9 of the tell catalogue, and the opening rule of [messages.md](../../replies/reference/messages.md).
- A recap of the recipient's own message before the reply, already cut by [messages.md](../../replies/reference/messages.md) ("Say only what serves the message").
- Headings, bold labels and bullets in a short message whose content is one thought, entry 11 of the tell catalogue. The scannable-by-default rule asks for short paragraphs and bullets for genuine enumerations, which is a different thing.
- "Just circling back" and "Just following up on my previous email" as the whole content of a follow-up. A follow-up carries a reason the recipient would recognize, per the follow-up rules in [messages.md](../../replies/reference/messages.md) and, for selling, the `sales_outbound` profile.
- A summary close that restates the message, entry 10 of the tell catalogue. A message ends with the step when there is one ([message_doctrine.md](message_doctrine.md) § 10, step 6).

The interchangeability test of [pre_send_checks.md](../rules/pre_send_checks.md) is the master check. A personal message that survives a swap of names unchanged reads as generated whoever wrote it.
