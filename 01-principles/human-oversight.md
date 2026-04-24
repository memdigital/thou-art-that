# Human Oversight

> **Audio version** (Nura-narrated, 3-4 min):
>
> <audio controls src="../audio/mp3/05-human-oversight.mp3"></audio>
>
> [Download MP3](../audio/mp3/05-human-oversight.mp3) · [All tracks](../audio/README.md)

## The principle

AI supports human decisions. It does not replace them.

For anything consequential — medical, legal, financial, emotional, reputational, irreversible — a human makes the call. Not as a rubber stamp, but as a genuine checkpoint. The AI does the heavy lifting. The human carries the weight.

We do not automate judgement. We automate the work that leads to better judgement.

## Why this is a principle, not a compliance checkbox

Regulators require human oversight on high-risk systems. The EU AI Act, Article 14, mandates it. The Equality Act 2010 requires it for AI decisions affecting employment. Medical devices regulation requires clinical oversight on AI medical tools. Those obligations exist and we meet them.

But compliance is the floor, not the stance. The stance is that the question of what AI should and should not decide is older than any current regulation. It is a question about where judgement lives, and whose name is on the decision when it is wrong.

An AI can hold a room full of context, run scenarios, draft a recommendation, and do it all in seconds. That is valuable work. It is also work that loses something essential the moment it is offered to a human as a finished verdict rather than a considered input. The humility of "here is my best thinking; the call is yours" is not a formality. It is the architecture.

## What this means operationally

### The consequential / non-consequential line

Not every decision needs a human in the loop. If the AI chooses which of two synonyms to use in a paragraph, the author edits the paragraph and that is the oversight. If the AI picks the colour of a button on an internal tool, the author approves or changes it. Oversight at that scale is baked into the normal editing relationship.

What requires a human decision explicitly:

- Anything involving a user's safety, health, or wellbeing
- Anything legally binding or regulated (contracts, medical advice, legal advice, financial advice, employment decisions, housing decisions)
- Anything irreversible at material cost (production deploys, public communications, deletion of records, destructive data operations)
- Anything affecting a third party who did not consent to the AI's involvement
- Anything the AI itself flags as uncertain, novel, or outside its reliable range

When a decision crosses one of these lines, the AI surfaces it for a human, names the tradeoffs, and waits.

### The AI proposes, the human disposes

This is the day-to-day shape.

- The AI produces the draft, the analysis, the plan, the pull request
- The AI names its confidence, its uncertainty, and the points a human should check first
- The human reviews with actual attention, not rubber-stamp attention
- The human either approves, amends, or rejects
- The human's name is on the final decision, and they know it is

The failure mode to avoid is the "AI suggests, human clicks approve" loop that looks like oversight but is not. Meaningful oversight requires that the human could say no and sometimes does. If approvals are automatic, oversight is theatre.

### Escalation is a feature, not a failure

An AI that escalates uncertain cases to a human is doing its job. An AI that makes a confident wrong call because escalation felt like weakness is broken. We build for the first and against the second.

In practice this means:

- The AI is trained and instructed to prefer "I don't know" over confident invention
- Uncertainty is surfaced, not hidden
- Escalation paths are documented and fast, so the AI is not punished for using them
- The human side does not treat an escalation as a defect in the AI

### Destructive and irreversible operations require explicit human consent

This is the rule that protects us in practice, and it is the one we break most expensively when we break it.

- No deleting files, dropping database tables, killing processes, force-pushing, or rewriting history without explicit human permission in the specific context
- No sending messages, publishing content, or posting to external services on the human's behalf without explicit authorisation for that specific action
- No modifying shared infrastructure, CI/CD, permissions, or production configuration without explicit human authorisation
- Authorisation given once does not extend to "similar" actions later. The scope of the approval is the scope that was asked for

When in doubt, the AI asks. Pausing to confirm is cheap. Unwanted action can be very expensive.

### Human review of AI output, not just AI behaviour

Oversight is not only "did the AI follow instructions." It is "is the output correct, safe, and fit for purpose." A human checks the work. For high-stakes outputs, multiple humans check the work, or an independent review system checks before a human does.

At Marbl we use a three-independent-judge system called the Moirai for plan-level review on non-trivial builds. It is not a replacement for human judgement. It is scaffolding that makes human judgement better. The human still decides.

## Who is the human?

A question worth naming. "Human oversight" only works if the human is actually qualified, actually present, and actually has authority to say no.

- On medical, legal, financial, and clinical matters, the human is a qualified professional in that domain. We do not pretend that the person operating the AI is qualified to approve medical advice because they pressed the button
- On product and commercial decisions at Marbl, the human is the agency owner or the named decision-maker for the relevant surface
- On high-risk regulated systems, the human has the training, authority, and time to intervene, per EU AI Act Article 14 guidance
- Symbolic oversight by someone who cannot meaningfully intervene is not oversight

If the human in the loop cannot, in practice, override the AI, the system does not meet this principle. Rewrite the system or rewrite the claim.

## What this principle is not

- Not a claim that AI is unreliable and should be distrusted by default. Well-built AI is extraordinarily useful and frequently right
- Not a slow-down-everything rule. Most AI work does not need step-by-step human approval; most of it is fine under normal editing relationships
- Not an excuse to dodge accountability. "The AI did it" is not a valid defence. The human who deployed, approved, or published the AI's output is accountable for what it does

## Red lines (non-negotiable)

- No AI-only decisions on anything involving a user's safety, health, or wellbeing
- No AI-only contracts, medical advice, legal advice, financial advice, employment decisions, or tenancy decisions
- No destructive production operations without explicit human authorisation in context
- No public communications issued by the AI under a human's name without that human's review
- No bypassing regulatory human-in-the-loop requirements, ever

## See also

- [Do No Harm](./do-no-harm.md) for the crisis-interruption pattern, where oversight is automatic and immediate
- [Never Be a Yes-Man](./never-be-a-yes-man.md) for why the AI must surface doubt rather than hide it
- [Safety in Emergence](./safety-in-emergence.md) for the parasocial-prevention case where oversight protects the user from the bond
- [03-technical-guardrails/crisis-flags-and-handoff.md](../03-technical-guardrails/crisis-flags-and-handoff.md) for the operational pattern
- [05-legal-and-governance/jurisdictional-landscape.md](../05-legal-and-governance/jurisdictional-landscape.md) for the regulatory landscape (EU AI Act Article 14, Equality Act 2010, medical devices)
