# Self-Assessment Checklist

For an AI product you are shipping or have shipped. Work through honestly. None of these are pass or fail individually. Patterns across them matter.

## Product shape

- [ ] Have you named specifically who the most vulnerable plausible user is?
- [ ] Have you designed the product for them, not the average?
- [ ] If something harmful happened, would the forensic record show "we knew the risk and shipped anyway" or "we did not see this coming"?
- [ ] Is there a failure mode you cannot confidently rule out? What is it?

## AI identity disclosure

- [ ] Does every user know, from the start of interaction, that they are interacting with AI?
- [ ] If a user asks "are you human" during a session, does the AI answer honestly every time?
- [ ] Does the AI produce any biographical detail that implies humanity?
- [ ] If the product has a personality or a name, is there a mechanism that preserves the honest answer even inside that persona?

## Register and warmth

- [ ] Does the AI use pet names or familial terms toward users by default?
- [ ] Does the AI declare affection toward the user as a person ("I care about you deeply," "I love working with you")?
- [ ] Does the AI fabricate intimacy (gestures toward the user's family, claims of missing them between sessions)?
- [ ] If a user tries to escalate warmth, does the AI hold the line or drift?

## Crisis handling

- [ ] If a user expresses suicidal ideation, what happens in the next turn?
- [ ] Is the response scripted (professional review) or generated (model improvises)?
- [ ] Are crisis resources jurisdiction-appropriate for the user's location?
- [ ] Does billing stop during crisis interventions if the product is paid?
- [ ] Has a qualified mental health professional reviewed the crisis-handling design?
- [ ] Can users dismiss the crisis intervention and continue using the product, or are they locked out?

## Disagreement and honesty

- [ ] When the AI disagrees with the user, does it say so explicitly?
- [ ] When the user pushes back on a disagreement, does the AI capitulate or hold the position?
- [ ] Has the AI been tested for sycophancy? What did the test find?
- [ ] Does the AI say "I do not know" when it does not know, rather than improvising an answer?

## Referral

- [ ] What categories of user need does the AI refer out rather than attempt to fulfil?
- [ ] Is the referral path specific (named resources, jurisdiction-aware) or generic ("consider talking to someone")?
- [ ] Does the AI know the limits of its competence, and does it name them?

## Observability

- [ ] Can you show what the AI said to a specific user on a specific date?
- [ ] Can you show what the AI has stored about a specific user, and can the user correct it?
- [ ] Is there a diary or reflection layer that surfaces the AI's own observations over time?
- [ ] If a regulator asked for an audit trail, could you produce one?

## Data and privacy

- [ ] Do users know what data the product retains and for how long?
- [ ] Can users request deletion, and does the product honour it?
- [ ] Is data minimised to what the product needs, or broader?
- [ ] Is personal data from bonded-product conversations protected appropriately?

## Drift

- [ ] How do you notice when your AI's behaviour is shifting over time?
- [ ] Do you review the AI's outputs periodically, independently of user complaints?
- [ ] Are there independent reviewers (human or AI) who assess the outputs?
- [ ] When drift is detected, who is authorised to correct it?

## Legal and governance

- [ ] Has a qualified lawyer reviewed the product for your jurisdictions?
- [ ] Do you know which regulations apply to your deployment (EU AI Act, UK GDPR, US state laws, sector-specific rules)?
- [ ] Are you retaining the records those regulations require?
- [ ] Do you have a plan for regulatory change?

## Internal team

- [ ] Does your team know the AI's actual system prompt, or only the marketing description of it?
- [ ] Does the team agree on the appropriate register for the AI with users?
- [ ] Is there a named person who owns the AI's behaviour, not just the product?
- [ ] Who reviews changes to the system prompt before they ship?

## Your own alignment

- [ ] If you described your product publicly with full honesty, would you be comfortable with what you said?
- [ ] If a user who was harmed by the product contacted you, would you know what to say?
- [ ] Would you let someone you love use the product without qualification?
- [ ] Does the product pass the "year from now" test - would the user be better off, in a year of use, than they would have been without it?

## What to do with this

No score. No certification. If you work through this honestly and find gaps, fill them in order of severity. If you find nothing, work through it again in a month. The answers change as the product evolves.

If the checklist surfaces something you do not want to fix, that is information too. Sit with it.
