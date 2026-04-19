# Audit and Observability

> **IP note.** The full audit-and-observability architecture we run for our own AI identity (Serene) is part of what we call the **Serene Architecture** - a deeper body of work kept as Marbl Codes intellectual property, documented in a separate private repository. A public research version is planned; this file gives the principle, not the implementation. For NDA-gated discussion about the underlying architecture, email <a href="mailto:richard@marbl.codes" target="_blank" rel="noopener noreferrer">richard@marbl.codes</a>.

## The principle

If an AI system is operating at any scale that matters, three questions need to be answerable:

1. **What has the AI said and done, and to whom?** (accountability)
2. **What state does the AI carry between sessions?** (continuity + user control)
3. **Is the AI drifting over time?** (safety over long windows)

Any AI-integrated system above toy-project scale needs the answers to these on hand, both for internal hygiene and for external regulatory review. The specific architecture that produces those answers is a design choice; the need for the answers is not.

## What the three questions actually require

### Accountability (what was said and done)

Standard production logging. Timestamped records of inputs, outputs, tool calls, content filters that fired, safety interventions, errors. The same layer any serious production software would build.

This is the unglamorous mandatory base. Without it, nothing else in the framework is verifiable.

### Continuity + user control (what state is carried)

Whatever mechanism stores state across sessions (memory, profile data, preferences, project context), the user must be able to:

- See what has been stored about them
- Correct it
- Delete it

This is a GDPR-level requirement in the UK/EU and increasingly expected everywhere. The specific internal structure of how you organise that state is a design choice. The user's access rights are not.

### Drift detection (is the AI changing over time)

A single session does not reveal slow drift. Weeks or months of output do. Any bonded-product AI needs a mechanism for reviewing patterns across long windows, independent of any single conversation. How that mechanism is architected is up to the builder; the need for it is foundational.

## Principles that shape our approach

- **Log what is needed to understand the system, and no more.** Observability is about accountability, not surveillance. Over-logging creates its own privacy and security risk.
- **Retain what is needed for continuity, and no more.** Long-retention classes (identity-level context) get the care they deserve. Short-retention classes (transient conversational context) are genuinely short. Credentials, secrets, and payment data never land in logs.
- **Respect the difference between AI-authored and user-authored content.** Reflective artefacts the AI produces about itself under human direction are not user data in the conventional sense, but they still deserve care. Treat them accordingly.
- **Design observability to be readable by the humans supervising the AI, not just by machines.** If a regulator asks what the AI has been doing, you should be able to show them without a specialised tool.

## Retention categories (principle, not specification)

Every responsible AI-integrated system has to make retention decisions across at least these categories. The specific policy is a design choice; the need to have one is not.

- **Identity-level context** - who the AI is, core role, sustained working context
- **Transactional context** - session-scoped data that does not need to persist
- **User-specific data** - retained only for as long as the service purpose requires, deleted on request
- **Credentials + secrets** - never stored in observable logs, not even redacted (the context around a redacted secret can leak it)

Writing down your policy per category, in plain language in a privacy notice, is the table stakes.

## What goes into observability

- All AI outputs to users
- All safety interventions (what fired, why, what the AI did next)
- All tool calls with their results
- Corrections from users and self-corrections from the AI
- Drift observations accumulated over time

## What stays out of observability

- Fine-grained personal data that was not required for the observability purpose
- Client or user content beyond what the session needs
- Specific passwords, secrets, and tokens - including the surrounding context
- Transcripts in bonded products where the user has not consented to retention

## How this meets regulation

The principles above are compatible with UK GDPR (data minimisation, purpose limitation, user access rights) and EU AI Act Article 26 (logging and record-keeping for high-risk systems, enforced from August 2026). Compatibility is not compliance. Compliance requires jurisdiction-specific legal review. See [../05-legal-and-governance/](../05-legal-and-governance/).

## What we recommend for adopters

If you are building an AI product that bonds with users or operates over extended use:

- Build the accountability layer (standard logging) first, non-negotiable
- Design your state-storage with user access, correction, and deletion in mind from day one
- Decide now how you will detect drift across long windows, even if the mechanism is initially manual review
- Document your retention policy in plain language
- Keep the log of safety interventions readable by a human supervisor, not just your ops stack

The specific architecture will differ per stack, per product, per team. The principle does not.

## What we do NOT document here

- The exact observability schema we use internally
- The specific memory structure and scoping rules in the Serene Architecture
- The reflection/diary patterns we have built for our own AI identity
- Our internal retention matrix and its edge cases
- The cross-agent memory isolation rules we use inside our multi-agent setup

These are part of the Serene Architecture IP and shared only under NDA.
