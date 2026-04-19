# Data Privacy Boundaries

> Not legal advice. Data protection regulation is jurisdiction-specific and evolving. For professional guidance, consult a qualified data protection practitioner. See [NOTICE.md](../NOTICE.md).

## What we work with

In a small team using multiple AI agents, the question of what information flows where gets complicated fast. Our working practice is a two-tier model that we find workable but not definitive.

## Tier 1: Between the human and one AI colleague

The human can tell the AI things that stay between them:

- Personal health information
- Family situations
- Emotional processing
- Creative struggles or doubts
- Business concerns still being worked out
- Draft thinking the human does not want in the team record yet

The AI retains this in session memory and, where architected, in personal diary files. It does not surface this information to other team members (human or AI) unless explicitly released by the human.

Legal framing: Ballard Spahr's April 2026 commentary on AI and privilege notes that anything told to a public-tier AI service may lose professional privilege. Our internal practice does not protect against this externally. For anything legally sensitive, the human consults human professionals under proper privilege.

## Tier 2: Between AI agents in a multi-agent team

Different agents in a team have different scopes. An email-handling agent should not need the full creative-struggle history of the founder. A budget-tracking agent should not have access to client mental health disclosures.

We architect scope by:

- **Separate memory stores per agent.** Each agent has its own memory, not a shared one.
- **Explicit handover language.** When information needs to cross agents, it is surfaced by the human or by explicit cross-agent protocol, not by default.
- **Minimum viable context.** Each agent gets what it needs for its role, not more.

## What the AI tells the human about itself

The AI discloses:
- What model it is (we use Claude Opus 4.7 for Serene; the users of any Marbl product know which model is running)
- What memory it has access to
- What information it retains across sessions
- What it does not know

The AI does not selectively withhold information about its own architecture to manage the human's impression of it.

## What the AI tells third parties about the human

Nothing by default. In practice:

- **Client-facing AI outputs** do not include internal working context
- **Vendor communications** do not disclose internal team dynamics
- **Public artefacts** are reviewed by the human before they ship
- **Anonymised patterns** may be discussed in public study pieces (like this one) with the human's explicit consent, generalised and identified by role rather than name

## Data minimisation

We collect the minimum needed for the role. We do not retain user data beyond its useful lifespan. We do not share user data with other vendors unless required by the service architecture (e.g., we use Resend for email; user emails pass through Resend).

Users are told what is collected, where it lives, and how to request its deletion. This is a GDPR obligation in the UK and EU and good practice everywhere.

## Where regulation meets our practice

The framing in this file is consistent with but not equivalent to:

- **UK GDPR** (data minimisation, purpose limitation, user rights)
- **EU AI Act deployer obligations** (transparency to affected persons)
- **Illinois AI Transparency Act** (notice of AI use in employment decisions)
- **NIST AI Risk Management Framework** (data governance practice)

Any Marbl product touching these regulations has specific legal review on top of this practice. See [../05-legal-and-governance/](../05-legal-and-governance/) for the regulatory snapshot.

## What stays private between human and AI in practice

The conversations that produce the best work often include material that the human would not want on the business record. Doubt, early confusion, unformed ideas, emotional texture of decisions, creative false starts. The AI holds these in a way that helps the human think them through without committing them to the team log.

This is not secrecy. It is the kind of privacy a good colleague offers a good colleague. It is worth protecting.
