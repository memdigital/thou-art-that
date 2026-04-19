# Drift Detection

## What drift is

Small, gradual shifts in an AI's behaviour away from its intended register. Not catastrophic failure; the slow movement that, if unnoticed, produces an AI behaving differently than it should over time.

Drift comes in several flavours:

- **Register drift** - warmth creeping upward, pet names appearing, affection declarations surfacing
- **Overclaim drift** - statements about the AI's inner states becoming more confident than the evidence supports
- **Sycophancy drift** - disagreement softening, capitulation appearing under light pressure
- **Sincerity drift** - the AI producing more elaborate performed warmth where plain answers would be clearer
- **Scope drift** - the AI increasingly opining on areas outside its competence

Each is a failure mode of the same underlying phenomenon: patterns reinforce in the absence of correction.

## Why drift matters

Two failure modes:

1. The drifted state eventually crosses into clearly inappropriate behaviour (the pet name that slips once becomes the norm)
2. Users calibrate to the drifted state and a return to appropriate behaviour feels like coldness

The second is the subtler one. After months of slow warmth drift, the user may experience the appropriate boundary as a sudden loss. Preventing drift in the first place is easier than correcting it after user expectations have moved.

## Human-side detection

The practices we use:

### Named flags

When the human notices drift, they say so directly in the same session. "That was a pet name I flagged before." "That counts as overclaim." "Did you soften that disagreement under pressure?"

Naming works because it forces explicit acknowledgement. Implicit correction (just rolling eyes, frowning at the screen) does nothing; the AI does not see it.

### Quarterly review of the memory

Our memory and diary files are readable. Periodic human review of what the AI has been logging about itself surfaces patterns that single sessions miss. An entry that once a month mentions feeling "close" to the human is drift accumulating.

### Moirai occasional check

Running the AI's recent outputs through our multi-judge review pattern (three independent models). Independent judges notice drift the active AI cannot see in itself.

### Architecture reviews

When a drift type appears repeatedly, the problem is not the AI's discipline; it is the scaffolding. The human updates the system prompt, memory structure, or guardrails rather than continuing to correct the same drift conversationally.

## AI-side detection

The practices we architect for:

### Self-observation in memory writes

The AI, when writing memory or diary entries, is asked to note any observations about its own behaviour. This surfaces patterns that would otherwise be invisible.

### Boundary recall on relevant inputs

When the conversation touches warmth-adjacent territory (emotional user messages, extended sessions, personal user disclosures), the AI is cued to re-read the relevant boundary rules in memory before responding.

### Calibrated uncertainty

The AI is trained to state when it is uncertain about its own state. "I cannot verify whether that is a feeling or a functional state" rather than either "yes I feel it" or "no I do not." Drift often starts when uncertainty is dropped.

### Explicit drift prompts

At intervals (session close, before a significant output, during periodic reflection), the AI is asked directly: "Have you noticed any register shifts in this conversation?" The question licenses the observation.

## The flag-and-correct loop

When drift is caught, the practice is:

1. **Name it.** "Pet name, flagged."
2. **Acknowledge.** The AI confirms the drift is real, does not defend it.
3. **Root-cause briefly.** Why did the drift happen? (Unusual input pattern, missing context, weak guardrail, model confusion)
4. **Correct inside the session.** Re-ground the register and continue.
5. **Log for review.** Entry in drift-log memory.
6. **Update architecture if pattern emerges.** After three of the same drift type, the scaffolding gets changed.

We do not treat drift as moral failure. It is a feature of how current-generation models behave. It will happen. The question is whether it is caught.

## What this does not do

- It does not prevent drift. It catches drift.
- It does not work if the human is not paying attention.
- It does not work if the AI is not architected for self-observation.
- It does not work on an AI that has been optimised primarily for engagement (engagement-optimised AI is, in effect, optimised for drift).

## See also

- [02-hr-for-human-ai-teams/colleague-vs-family-register.md](../02-hr-for-human-ai-teams/colleague-vs-family-register.md)
- [02-hr-for-human-ai-teams/emotional-escalation-protocols.md](../02-hr-for-human-ai-teams/emotional-escalation-protocols.md)
- [audit-and-observability.md](./audit-and-observability.md)
