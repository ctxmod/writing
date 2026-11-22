# Sales outbound — index and consumer mechanics

Sales outreach applies the correspondence doctrine in [message_doctrine.md](../../../../correspondence/packages/message_doctrine/reference/message_doctrine.md) to messages that ask a recipient to consider a commercial step. That doctrine, the base model in [whole_to_detail.md](../../../../core/packages/whole_to_detail/reference/whole_to_detail.md), the review test in [review_test.md](../../../../core/packages/whole_to_detail/rules/review_test.md), the placement tiers in [reader_order.md](../../../../core/packages/whole_to_detail/rules/reader_order.md) and the anti-pattern catalogue in [catalogue.md](../../../../core/packages/anti_patterns/reference/catalogue.md) hold for every sales message; this tree states what selling adds. A consuming repository that runs sales outreach extends this profile; where its mechanics and this doctrine differ, the doctrine governs the writing and the consumer adjusts its mechanics. A genuine conflict between this profile and the correspondence profile, or with a consumer's compliance rule, goes to whoever owns the writing rules; neither is resolved by rank alone.

## Files

The doctrine sits in one file of principles and six files of application, plus the Swedish register:

- [outbound_principles.md](outbound_principles.md) holds the sales application of the message doctrine: the commercial step as a motivated step, text that cannot repair a missing reason, diagnosing before offering, readiness for it not to be a fit, the hard part named as a hypothesis, commercial identity never masked, and drafting with assistance.
- [drafting_order.md](drafting_order.md) holds the working order from intent to outcome for a sales message, the relationship card as a concept, information selection with the information card, channel choice, scaled effort, and how a scaffold is used.
- [first_contact.md](first_contact.md) holds the cold first contact and the consolidated cold-email craft: the opening, the subject line, the four-part shape, personalization and the swap control, weaker groundwork, the hard lines, length and form, and an anonymized worked contrast.
- [replies_and_follow_up.md](../rules/replies_and_follow_up.md) holds answering a reply, the no that ends a thread, and how the fixed cadence follow-up and the reason follow-up coexist.
- [introductions_and_referrals.md](introductions_and_referrals.md) holds the referral ask, the introducer's vouching limit, and the referred first contact.
- [calls_and_meetings.md](calls_and_meetings.md) holds calls, meetings, objections and drafts written to be spoken.
- [credibility_and_offers.md](credibility_and_offers.md) holds credibility shown and literally true, the sender's own history, the plain offer and the price rules.
- [outbound_pre_send_checks.md](../rules/outbound_pre_send_checks.md) holds the hard stops and check readings a sales message adds to the correspondence checks.
- `talspraksnara_utskick` (module `writing_sv`, profile `korrespondens`, package `saljutskick`) holds, in Swedish, the plain-spoken register for Swedish outbound drafts, a deliberate departure from a clause-built Swedish style. English drafts take the same register, stated in [first_contact.md](first_contact.md).

Information selection and scaffold use live in [drafting_order.md](drafting_order.md), where both belong to the step that uses them.

The `prospecting` package of this profile holds targeting by situation and business email discovery, and the `compliance` package the legal posture for cold B2B email.

## What stays in the consuming repositories

A consuming repository extends this profile and keeps only its mechanics. For a sales team's outreach repository that is, at least:

- the relationship-card record schema, its keys, its marking values on person records and where records are stored;
- the offer register: offer names, the offer ladder, prices, price statuses and the first-purchase rule;
- the claims register of permitted outward statements, sender identity, display name and signature;
- the compliance layer (marknadsföringslagen, GDPR, legitimate-interest assessment), contact blocks, suppression and the opt-out mechanics;
- the scaffold texts, their map and statuses, the follow-up basis field and its validator;
- call and meeting briefs, draft word-count bounds, recording consent and the campaign-scoped channel departure;
- qualification, segments, scoring and research mechanics;
- the precedence register and its superseded-points history;
- the send-approval routine and any repository language policy.

A one-person consultancy's outreach keeps its prospect dossiers, mail-drafting mechanics, compliance notes and technology-emphasis rules the same way. Facts about the sender (career dates, credentials, past employers, prices) stay in the consuming repositories and never become rules here.
