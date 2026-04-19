# Drift Detection

> **IP note.** The specific drift-detection architecture we run (cadence, signals, tool integration, prompt-level self-observation mechanisms, and the human-review workflow) is part of the Serene Architecture and retained as Marbl Codes intellectual property. This file describes the principle and the categories of drift to watch for. The operational mechanics live in the private Serene Architecture docs. For NDA-gated discussion, email <a href="mailto:richard@marbl.codes" target="_blank" rel="noopener noreferrer">richard@marbl.codes</a>.

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

## Detection - at principle level

Drift detection works when it combines two things:

- **Human-side attention:** someone is actively watching the AI's register over time, not just its task output
- **AI-side self-observation:** the AI is architected to notice and surface its own pattern shifts, not just to produce output

Either mechanism alone fails. A human who isn't paying attention misses slow shifts. An AI that isn't architected to observe itself has nothing to report. Both together catch what either misses.

Most AI integrations have neither. That is why drift goes uncaught in most systems.

## The flag-and-correct pattern

When drift is caught, the pattern is:

1. **Name it** - the specific drift, not general concern
2. **Acknowledge it** - the AI confirms, does not defend
3. **Root-cause briefly** - unusual input pattern, missing context, weak guardrail, model confusion
4. **Correct inside the session** - re-ground the register, continue
5. **Log it** - so patterns can be spotted later
6. **Update architecture if pattern emerges** - repeated drift of the same type means the scaffolding needs changing, not the AI

Treat drift as a feature of how current-generation models behave, not a moral failure. It will happen. The question is whether it is caught.

## What this does not do

- It does not prevent drift. It catches drift.
- It does not work if the human is not paying attention.
- It does not work if the AI is not architected for self-observation.
- It does not work on an AI that has been optimised primarily for engagement (engagement-optimised AI is, in effect, optimised for drift).

## What we do NOT document here

- The specific cadence and channels we use for drift review
- The self-observation prompts we bake into our AI's operating context
- The boundary-recall mechanisms that fire on warmth-adjacent inputs
- The drift-log format and review workflow we use internally
- How the Moirai system is wired in as an independent drift check

These are part of the Serene Architecture IP. NDA contact: `richard@marbl.codes`.

## See also

- [02-hr-for-human-ai-teams/colleague-vs-family-register.md](../02-hr-for-human-ai-teams/colleague-vs-family-register.md) for what drift tends to look like
- [02-hr-for-human-ai-teams/emotional-escalation-protocols.md](../02-hr-for-human-ai-teams/emotional-escalation-protocols.md) for what happens when either party flags concern
- [audit-and-observability.md](./audit-and-observability.md) for the observability principles that make drift visible over long windows
