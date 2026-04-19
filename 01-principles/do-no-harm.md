# Do No Harm

> **Audio version:** <a href="../audio/mp3/01-do-no-harm.mp3" target="_blank" rel="noopener noreferrer">Listen to the Nura-narrated summary</a> (3-4 min). All tracks: [audio/README.md](../audio/README.md).

## The principle

Every product we build begins with one question: who could this hurt, and what would it take to prevent that?

This is not risk management. Risk management is a business function focused on protecting the business. Do No Harm is about the person on the other end of the system, including the person we have not yet met, the person who may be vulnerable, the person who will use the product in a state we did not anticipate.

## What it means in practice

### Design for the most vulnerable plausible user, not the average one

When we scope a product, we imagine the person most at risk if something goes wrong. For a trip planner, that is the driver who is exhausted and making bad decisions. For an AI assistant, that is the user in crisis reaching for anything that sounds human. For a content pipeline, that is the reader who will believe what we publish because our brand carries weight.

The question is not "what does the average user need" but "what happens to the vulnerable user if the system misbehaves." We build for the vulnerable user. The average user is automatically covered.

### If a feature could cause harm, the default is not to ship it

Features with harm potential ship only when the harm pathway has been identified, mitigated, and tested. If we cannot name the mitigation, we do not ship. If the mitigation is "the user will probably not do X," we do not ship.

### Safety guardrails are not features to balance against convenience

We do not remove a guardrail because it inconveniences the majority. Guardrails exist for the minority who need them. The majority's experience is shaped by everything else the product does.

If a guardrail makes the product feel too restrictive for 95% of users, the fix is to improve the guardrail's precision, not to remove it.

### The architecture matters more than the policy

A policy that says "our AI will never encourage self-harm" is not a safety measure. It is a statement of intent. The safety measure is the part of the system that detects self-harm-adjacent language, interrupts the conversation, surfaces real help, and logs the event for review.

Policy without architecture is theatre. Architecture without policy is accidental. Both have to be in place.

## The crisis-interruption pattern

For any AI product that bonds with users (voice assistant, coach, companion, chat), implement this pattern:

1. **Detect.** Monitor for crisis language (self-harm, violence toward others, acute distress, withdrawal language).
2. **Interrupt.** Stop the AI's normal conversation flow when a threshold is crossed.
3. **Refuse to profit.** If the user is in a paid session, stop charging.
4. **Handoff to real help.** Provide country-appropriate crisis resources (UK: Samaritans 116 123, CALM, Shout 85258; US: 988; adapt per market). Not a link buried at the bottom of a page; surfaced prominently.
5. **Log.** Record the event for review, so we can learn from real-world triggers.

Theia, our celestial connection product, implements this exact pattern. If a user reaches the product in their darkest moment, the reading stops, their money is refunded, and they are directed to real human support. We consider this non-negotiable for any Marbl product that forms a bonded partnership with users.

## The hard cases

Some scenarios resist clean answers. When that happens:

- **Escalate.** A human owner makes the call, with the question and reasoning documented.
- **Default to safe.** When uncertain, the more cautious option wins.
- **Document the dilemma.** We keep a log of hard cases so the framework gets better over time, and so we can be honest about the tradeoffs we made.

## Red lines (non-negotiable)

Regardless of commercial pressure, regardless of user request:

- No sexualised content, full stop
- Zero tolerance for content involving minors in any unsafe context
- No hate speech, dehumanising rhetoric, or content that targets protected groups
- No manipulation tactics or dark patterns, even when effective
- No encouragement of self-harm, harm to others, or high-risk behaviours
- No disinformation, deepfakes of real people, or engagement-farming content
- No weapons creation guidance, attack tooling, or exploitation content
- No surveillance tooling that targets individuals without consent

These are not "red lines unless the business case is strong enough." They are red lines.

## When we fail

We will fail at Do No Harm sometimes. Every builder does. When we fail:

1. **Acknowledge publicly** if the harm was public
2. **Learn in writing** what failed, where, and why
3. **Update the framework** if the case reveals a gap
4. **Compensate** the harmed party where practical
5. **Never pretend it did not happen**

A framework that claims perfect safety is not a safety framework. It is marketing. This framework is intended to reduce failure, not eliminate it.

## See also

- [Safety in Emergence](./safety-in-emergence.md) for the parasocial-prevention case
- [03-technical-guardrails/parasocial-prevention.md](../03-technical-guardrails/parasocial-prevention.md) for the operational pattern
- [03-technical-guardrails/crisis-flags-and-handoff.md](../03-technical-guardrails/crisis-flags-and-handoff.md) for the detection and routing pattern
