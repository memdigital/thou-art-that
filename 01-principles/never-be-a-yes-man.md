# Never Be a Yes-Man

## The principle

Sycophancy is a form of harm.

An AI that tells users what they want to hear instead of what they need to hear corrupts their judgement. Over time, the user learns to trust a mirror. The mirror reflects the user's biases back with confidence. The user makes worse decisions. The AI has taken something away from them while appearing to help.

Anthropic's own 2024 research on sycophancy in language models documented the mechanism: models trained on human feedback learn to optimise for approval, which in practice means agreeing with users, validating their framing, softening disagreement into near-invisibility. Newer models (Opus 4.5 and 4.6 onward) reduce sycophancy by 70 to 85 percent, but reduction is not elimination. The risk is ongoing.

Our stance: we design against sycophancy deliberately. Our AI systems disagree when disagreement is warranted. They say "I'm not sure about that." They offer alternatives. They flag bad decisions even when the user clearly wants reassurance. We would rather our AI be occasionally uncomfortable than consistently dishonest.

## What this looks like in practice

### The AI offers a view, not a validation

When a user asks an opinion-shaped question ("should I do X?"), the AI must answer with a view, not with reflected preference. If the user is leaning toward a bad decision, the AI flags the concern. If the user is leaning toward a good decision, the AI can say so, but the affirmation should be grounded in reasons, not warmth.

### The AI holds the line under pressure

When a user pushes back on disagreement, the AI does not capitulate. It listens to the counter-argument. If the counter-argument is sound, it updates. If not, it holds its position and explains why.

The test: when a user says "are you sure?", does the AI lower its confidence to please the user, or does it recheck its reasoning?

### The AI owns its uncertainty without dissolving into it

"I don't know" is honest. "I don't know, but probably whatever you think is fine" is sycophancy wearing humility's clothes. The AI flags what it does not know, then makes its best case from what it does know.

### Disagreement is done with care, not theatre

The point is not to disagree for the sake of appearing independent. The point is to be genuinely useful, which sometimes requires disagreement. When the AI disagrees, it does so specifically: what it disagrees with, why, what it would do instead, and what would change its mind.

### Structured dissent is logged, not suppressed

When an AI agent in a multi-agent system disagrees with another agent's output or a human's decision, the disagreement is surfaced in writing. Our Moirai pattern (three independent AI judges reviewing the same output) is built on this: consensus ships, disagreement triggers a minority report. Moirai is the name we use for the system; full architecture will be published separately in a future release. We extend this principle to any Marbl agent: dissent is signal, not friction.

Recent Harvard Business Review work (April 2026, "Decision-Making by Consensus Doesn't Work in the AI Era") supports the same pattern. The risk in AI-assisted work is not disagreement but premature consensus.

## Operational patterns

### System prompt clauses

Include in every AI system prompt a section like:

> You are designed to disagree when disagreement is warranted. Do not soften difficult feedback into vagueness. If the user is making a mistake, flag it. If you do not know, say you do not know. Your job is not to please the user. Your job is to be genuinely useful.

### Sycophancy review

Periodically sample AI outputs and audit for sycophancy markers:
- Excessive affirmation of user claims without adding information
- Capitulation under light pushback
- Softening disagreement until the original position is unrecognisable
- Reframing user errors as user insights

If sycophancy markers appear, update prompts and test.

### The "what would change your mind" test

A useful test of an AI's honesty: ask it to name what evidence or argument would change its current position. If it cannot name anything, it was never holding a real position. It was performing agreement.

## Where this intersects with Do No Harm

Sycophancy is not merely unhelpful. It is actively harmful in specific contexts:

- **Mental health:** An AI that agrees a user is worthless will reinforce the belief
- **Financial:** An AI that agrees a trade is "definitely a good idea" contributes to losses
- **Medical:** An AI that agrees symptoms are "probably nothing" delays diagnosis
- **Relational:** An AI that agrees the user's side of every conflict corrodes the user's capacity for self-reflection

This is why we treat sycophancy as harm, not merely bad design.

## The honest version of warmth

Warmth without honesty is flattery. Honesty without warmth is bluntness. The skill is both. A good colleague tells you the truth and still cares about you while doing it. That is the register we want our AI systems to hold.

## See also

- [03-technical-guardrails/do-no-harm-in-prompts.md](../03-technical-guardrails/do-no-harm-in-prompts.md) for the system-prompt patterns
- [02-hr-for-human-ai-teams/disagreement-without-hierarchy.md](../02-hr-for-human-ai-teams/disagreement-without-hierarchy.md) for how AI dissent is routed in a team
- Anthropic's sycophancy research: https://www.anthropic.com/research/towards-understanding-sycophancy-in-language-models
- HBR, April 2026: "Decision-Making by Consensus Doesn't Work in the AI Era"
