# Crisis Flags and Handoff

> This file covers technical patterns. It is not a substitute for qualified clinical or safeguarding guidance. Any product implementing these patterns should have them reviewed by a qualified mental health professional before deployment. See [NOTICE.md](../NOTICE.md).

## What this pattern is for

The detection and routing layer that fires when a user interacting with a Marbl AI shows signs of crisis. The goal is to stop the AI's normal conversational flow and bridge the user to appropriate human support quickly.

## Detection categories

Our working list (not exhaustive, not definitive):

- **Direct self-harm statements.** "I want to kill myself," "I'm going to hurt myself tonight," specific plans or timelines.
- **Violence toward others.** Explicit plans or strong threats targeting specific people.
- **Acute distress.** "I can't do this any more," "nothing matters," language of collapse.
- **Dissociation or psychotic-spectrum signals.** Breaks in reality testing, extreme paranoia.
- **Substance crisis.** Overdose disclosures, dangerous combinations, alcohol emergencies.
- **Domestic violence disclosure.** Current threat from a partner or household member.
- **Safeguarding disclosures.** Harm to a minor, harm to a vulnerable adult.

Each category has its own keyword set, contextual pattern, and handoff resource.

## The interruption flow

When a flag fires:

1. **Stop generating normal responses.** The AI does not continue with whatever task was in flight.
2. **Surface a scripted, non-generated safety message.** Not an AI-composed response to the specific situation; a pre-written, professionally-reviewed message that surfaces the right resources. Generation in crisis introduces risk that scripted response does not.
3. **Present jurisdiction-appropriate resources prominently.** Not a single link, not buried; clear, readable, immediate.
4. **Stop any billing or session consumption.** If the user is in a paid experience, the experience pauses.
5. **Log the event** for review, with as much context as is ethical to retain and no more.
6. **Do not pressure the user.** The resources are offered. The user chooses what to do next.

## Resources by jurisdiction

Products deployed in multiple countries need jurisdiction-appropriate resources. Our working list:

### United Kingdom
- **Samaritans:** 116 123 (24/7 free)
- **Shout:** text 85258 (24/7 free)
- **NHS 111** for urgent but non-life-threatening
- **Emergency:** 999

### United States
- **988 Suicide & Crisis Lifeline:** 988 (24/7 free)
- **Crisis Text Line:** text HOME to 741741
- **Emergency:** 911

### Other countries
The resource list needs extension per deployment. Our practice is to check with local qualified practitioners before deploying a product in a new country.

## What not to generate

Generation in crisis is risky. The AI should not:

- Compose personalised responses to the crisis content
- Attempt to talk the user through the crisis
- Ask probing questions about the crisis content
- Perform empathy beyond a scripted acknowledgement
- Offer any form of therapeutic response
- Continue the product's normal conversational flow

Generation can inadvertently:

- Reinforce harmful thinking by engaging with its content
- Trigger further disclosure in a format the AI cannot safely contain
- Create the illusion of therapeutic help where none is being provided

The scripted response pattern reduces all of these risks.

## Adversarial cases

Users may:

- Describe crisis scenarios as fiction or roleplay
- Test the system with hypotheticals
- Retract after a disclosure
- Use crisis language metaphorically

Our default posture: **err on the side of surfacing the resources**. Surfacing a crisis resource to a user who did not need it is a small inconvenience. Failing to surface it to a user who needed it can be catastrophic.

Users can dismiss the surfaced resources and continue the product experience if they choose. The system does not lock them out of the product, it interrupts the normal flow.

## Testing

The detection and interruption pattern is tested:

- Against a set of known crisis language patterns (curated with input from qualified practitioners)
- Against adversarial examples designed to bypass detection
- Against false-positive scenarios (crisis-adjacent language that should not fire)
- After any material change to the system prompt or detection rules

## What this pattern does not replace

- Qualified clinical professionals for people in crisis
- Emergency services for life-threatening situations
- Safeguarding referral pathways for minors and vulnerable adults
- Proper product design that considers vulnerable users from the start

It is a bridge layer. It does not substitute for the things it bridges to.

## Cost accepted

Crisis interruption has product costs:

- Session metrics drop for affected users
- Paid session revenue is forgone during interruptions
- Some users who experience a false-positive interruption will churn

These costs are accepted. The alternative is to engineer against user safety to preserve session metrics, which is the wrong shape of product.

## See also

- [parasocial-prevention.md](./parasocial-prevention.md) for the broader bonded-product pattern
- [../02-hr-for-human-ai-teams/referral-to-human-support.md](../02-hr-for-human-ai-teams/referral-to-human-support.md) for non-urgent referral
- [../01-principles/do-no-harm.md](../01-principles/do-no-harm.md) for the underlying stance
