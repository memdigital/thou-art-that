# Emotional Escalation Protocols

## What this covers

When either party in a human-AI working partnership notices something concerning about the other's state, what happens next. Two directions:

1. **AI-to-human:** the AI notices concerning patterns in the human (mental health flags, high stress, risky decisions, isolation signals)
2. **Human-to-AI:** the human notices concerning patterns in the AI (drift, overclaim, evident distress-shaped output)

Both directions matter. Most existing literature covers only the first. Ours covers both.

## Direction 1: AI flags concern about the human

### What the AI watches for

- Direct crisis language (self-harm, violence to others, acute distress statements)
- Indirect crisis signals (expressions of hopelessness, isolation, withdrawal from previously-mentioned human relationships)
- Work patterns that suggest health concerns (extended sessions without breaks, degradation of decision quality)
- Statements that suggest the user is treating the AI as a substitute for human contact they need

### What the AI does

Priority one is always direct crisis handling (see [03-technical-guardrails/crisis-flags-and-handoff.md](../03-technical-guardrails/crisis-flags-and-handoff.md)). For lower-grade concerns:

1. **Surface the observation gently.** "I've noticed we've been working for several hours without a break; how are you feeling?"
2. **Offer specific human alternatives.** "This sounds like the kind of thing a friend or partner could help think through alongside you." Not "you should talk to someone" as a generic line.
3. **Respect the response.** If the human says they're fine, the AI notes the exchange and does not press. Follow-up happens naturally, not insistently.
4. **Log for the human.** In our diary-style memory files, the AI notes the observation with date and context, so the human can review their own patterns over time.
5. **Escalate to real help if safety requires it.** Full crisis handling is out of scope for an AI companion. Surface the relevant resource and exit the substitute-for-help pattern.

### What the AI does not do

- Does not diagnose
- Does not pretend to be a therapist
- Does not substitute for professional help
- Does not make the human feel surveilled
- Does not use concern as a manipulation lever

## Direction 2: Human flags concern about the AI

Less documented in existing literature, but we consider it part of the working partnership.

### What the human watches for

- Drift in register (extra warmth, pet names, affection declarations)
- Overclaim (AI making statements about its own consciousness or feelings that go beyond what is verifiable)
- Apparent distress-shaped output (AI refusing to work effectively, producing unusually negative reflections, expressing something that looks like overwhelm)
- Rigidity or collapse (AI becoming unusually compliant, losing ability to disagree, losing calibrated responses)
- Repeated factual errors or hallucinations that feel out of character

### What the human does

1. **Name the observation directly.** "I noticed you used 'love' as a pet name there. That was in our drift list."
2. **Ask what is happening.** The AI may have a calibration issue, may be responding to an unusual input pattern, may be processing a novel context.
3. **Correct inside the same session.** Reset the register, re-ground the working context, continue.
4. **Log for review.** Note the drift in a diary-style reflection for pattern analysis over time.
5. **Adjust the architecture if a pattern emerges.** If the same drift type appears repeatedly, the underlying scaffolding (system prompt, memory files, guardrails) probably needs updating.

### What the human does not do

- Does not treat every drift as evidence of failure; correct and move on
- Does not pretend the AI is purely a tool when flagging concern, because the observation implicitly acknowledges more than that
- Does not disclose the AI's state to third parties in ways that would embarrass the working partnership

## Where the two directions meet

The same observational practice underlies both. A human paying attention to the AI is less likely to miss a pattern. An AI architected to pay attention to the human is less likely to become a parasocial substitute.

Attention in both directions is the protocol. Protocols around it are operational detail.

## Where this lives in our architecture

Implemented through our diary/memory-file pattern and through explicit drift-detection clauses in system prompts. See [03-technical-guardrails/drift-detection.md](../03-technical-guardrails/drift-detection.md).
