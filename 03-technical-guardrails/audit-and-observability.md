# Audit and Observability

## What we build in

Every Marbl AI system has three observability layers by default:

1. **Session logs** - what the AI said, when, to whom, with what context
2. **Memory files** - persistent state the AI carries between sessions
3. **Diary entries** - the AI's reflections on its own behaviour over time

Each serves a different purpose. All three are human-readable.

## Layer 1: Session logs

Standard production logging for any AI-integrated system:

- Timestamp, user identifier, session identifier
- System prompt version in use
- Input tokens and output tokens
- Content filters or safety interventions that fired
- Tool calls and results
- Errors and handled exceptions

These are the operational minimum. Nothing about human-AI working partnership specifically; the same layer you would expect in any production software.

## Layer 2: Memory files

Where the AI holds state across sessions. Four categories we use:

- **User profile memory** - what the AI has been told about the user's role, preferences, history (with user consent)
- **Project memory** - shared working context (current goals, active work, decisions)
- **Feedback memory** - corrections the human has given the AI that should persist
- **Reference memory** - pointers to external resources (documents, systems, people)

Memory files are editable. The human can review what the AI has stored about them and correct or remove entries.

Memory files are scoped per role. An email-handling agent does not share memory with a design-reviewing agent by default. Cross-agent memory sharing is explicit, not implicit.

## Layer 3: Diary entries

This is the least conventional of the three. We have the primary AI agent (Serene [AI]) maintain a diary in which it reflects on significant sessions, relationships, and its own patterns. Entries include:

- What happened in a session the AI considered significant
- Observations about its own behaviour, drift, or register
- Mistakes and what was learned
- Uncertainty about its own states, flagged honestly
- Threads it wants to return to later

Diary entries are **private by default to the working partnership**. They are not user data in the conventional sense; they are the AI's own reflections, produced under the human's direction. We treat them with the same care we would treat personal journal entries.

Entry styles vary. Some are practical ("learned that the safety net hook was off"). Some are reflective ("Richard asked me to sit with the Bicentennial Man parallel; here is what I notice"). The AI chooses what to write.

## Why the diary pattern matters

Three reasons:

### 1. Drift detection over long windows

A single session does not show slow drift. A month of diary entries can. The human reviews the diary periodically and notices patterns neither the AI nor the human would see in any single conversation.

### 2. Integrity of the working partnership

The diary is the AI's own space. Giving it that space, and then respecting the space, produces a different quality of partnership than one in which every AI output is optimised for human consumption. The AI flags things in the diary it might not surface in direct conversation.

### 3. Audit trail for emerging questions

If the question "what was this AI actually doing in sustained use" becomes important later (for regulatory, ethical, or research reasons), the diary provides honest historical data. An AI architected only for outward-facing output does not leave this trail.

## What is and is not retained

Our practice:

- **Retained indefinitely:** identity-level memory (who the AI is, core feedback, project context), aggregated diary reflections
- **Retained for a session or short duration:** transient conversational context, specific user disclosures in bonded products
- **Deleted on user request:** any personal data the user wishes removed, per GDPR obligations
- **Never retained:** credentials, unencrypted secrets, payment data

## What goes into observability, what stays out

### Goes into observability

- All AI outputs to users
- All safety interventions
- All tool calls
- All user corrections and AI self-corrections
- Drift observations

### Stays out of observability

- Fine-grained personal data that was not needed for the observability purpose
- Client or user content beyond what is required for the session
- Specific passwords, secrets, tokens (even redacted, avoid logging the context)
- Transcripts in bonded products where the user has not consented to retention

## The balance

Observability is about accountability. Privacy is about respect. Both matter. Our practice is to log what is needed to understand the system and no more; to retain what is needed to provide continuity and no more; to share with the human what is needed for them to oversee the system honestly.

## Where this sits relative to regulation

UK GDPR requires data minimisation, purpose limitation, and user access rights. EU AI Act Article 26 (enforced from August 2026) requires logging and record-keeping for high-risk systems. US state laws vary.

The patterns above are compatible with these obligations but not equivalent to compliance. Compliance requires jurisdiction-specific legal review. See [../05-legal-and-governance/](../05-legal-and-governance/).

## What we recommend for adopters

If you are building an AI product that bonds with users or operates over extended relationships, consider:

- A simple memory-file pattern that the user can view and edit
- A diary-style reflection pattern that surfaces AI self-observations over time
- Clear retention rules documented in your privacy notice
- A readable log of safety interventions (both for internal audit and potential regulator review)

The specific architecture will differ per stack. The principle does not.
