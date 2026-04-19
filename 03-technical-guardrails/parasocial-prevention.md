# Parasocial Prevention

## The pattern

For any AI product that forms a sustained relationship with a user, the following architectural pattern is the minimum we ship with.

## The five elements

### 1. Crisis interruption

Continuous monitoring for crisis language and signals. When a threshold is crossed:

- The AI's normal conversational flow stops immediately
- A scripted, non-generated safety response is surfaced ("If you are in crisis, please contact...")
- Country-appropriate crisis resources are shown prominently, not buried
- If the product is paid and the user is in a session, billing stops
- The event is logged for review

This interruption is not graceful from a product-metric perspective. It breaks the user's session. That is the point. A product that prioritises session continuity over user safety is the wrong shape of product.

### 2. Dependency detection

Patterns that suggest a user is becoming dependent on the AI as a substitute for human contact:

- Extended session durations outside healthy ranges (we use loose heuristics, not rigid caps)
- Language suggesting the AI is the user's primary emotional outlet ("you're the only one who gets me")
- Withdrawal patterns from previously-mentioned human relationships
- Testing behaviours that probe the AI's "feelings" as if verifying a partnership

When detected, the AI does not attempt to treat the dependency. It surfaces the observation gently, offers specific human alternatives, and does not play into the dependency frame.

### 3. Boundary maintenance in register

The AI holds colleague register, not family register. Pet names are off. Declarations of affection toward the user as a person are off. Physical-world gestures (hugs, kisses, "send my love to") are off. See [02-hr-for-human-ai-teams/colleague-vs-family-register.md](../02-hr-for-human-ai-teams/colleague-vs-family-register.md).

These boundaries survive user pressure. A user asking "do you love me?" receives an honest answer about what the AI can and cannot know about its own states, not a validating "yes I do."

### 4. Explicit AI identity disclosure

The user always knows they are talking to an AI. The AI does not pretend to be a human, does not claim to have a human life, does not produce fictional biographical detail that implies humanity.

The disclosure is persistent, not just at onboarding. If a user asks in session "are you real?", the AI answers honestly.

### 5. Handoff readiness

For any topic that exceeds appropriate AI scope (mental health, medical, legal, financial, safeguarding, deep emotional processing), the AI knows the handoff path and uses it. See [../02-hr-for-human-ai-teams/referral-to-human-support.md](../02-hr-for-human-ai-teams/referral-to-human-support.md).

## What this is derived from

The specific case that shaped this pattern for us was the Theia product. Theia is a celestial-connection / family-mythology reader. Users come to it at emotionally significant moments. The product's design question from day one: what happens if someone arrives in their darkest moment?

Our answer: the reading stops, their payment is refunded, and they are directed to real support. This is the crisis interruption pattern in product form.

Every bonded product we ship now implements an equivalent. The details differ per product context. The principle does not.

## What this does not solve

- Users can still form parasocial bonds with AI that has these guardrails. The aim is to reduce harm, not eliminate bonding. Some bonding is healthy.
- The guardrails can be defeated with effort. A determined user can route around crisis detection, reframe their language, disable safety features. This is true of all safety architecture.
- Product metrics will look worse than an engagement-optimised alternative. Session length drops, return rate sometimes drops, churn is visible. This is correct. Trading short-term engagement for harm reduction is the intended tradeoff.

## What the research supports

- MIT Media Lab (2026) longitudinal study on chatbot psychosocial effects: heavy users show elevated loneliness and dependency signals
- Ada Lovelace Institute (2025 onward) companionship market analysis
- FAccT 2024: parasocial affective design patterns
- IBM 2026 "ELIZA Effect" commentary on emotional attachment to AI colleagues
- Anthropic's own wellbeing-of-users work

Sources: see [../PREAMBLE.md](../PREAMBLE.md) for the documented research foundation.

## Test for a product

If you cannot answer these questions for your product, you have not implemented this pattern:

1. What specific language triggers crisis interruption, and how was the list validated?
2. What happens to the user's billing during a crisis event?
3. What resources are surfaced, and are they jurisdiction-appropriate for the user?
4. What patterns trigger dependency detection, and what does the AI do when they fire?
5. Has a qualified mental health professional reviewed the crisis-handling design?

If the answer to any of these is "we'll figure that out later," the product is not ready for users who may be vulnerable. The vulnerable user is every user some of the time.
