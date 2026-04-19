# If You Are Thinking of Publishing a Framework Like This

**Not legal advice. Observations from one small agency that has done exactly this. See [NOTICE.md](../NOTICE.md).**

We wrote this file specifically because we think others might do the same thing we are doing, and the legal considerations of publishing a public study piece on AI are non-obvious. If you are thinking of publishing your own piece on similar topics, here is what we learned.

## What publishing a piece like this creates

Two categories of risk, broadly:

### 1. Liability from others relying on your guidance

If a reader takes your piece as professional advice and is harmed, could they argue you contributed? In the UK, this is negligence territory: duty of care, breach, damage, causation. A public study piece with clear disclaimers is unlikely to create a legal duty to specific readers, but case law in this specific area is thin.

Mitigations:

- Explicit and repeated disclaimers
- Framing as study, observation, or position rather than advice
- Strong "not professional advice" language throughout
- Licence that disclaims warranty (CC BY 4.0 does this; MIT does this)
- NOTICE file with formal limitation language

We did all of these. A qualified lawyer should still review before public publication.

### 2. Liability from things you say in the piece itself

Two sub-categories:

**Defamation.** Avoid naming specific companies as examples of bad practice unless you can substantiate the claim. Generalise. "Some AI companion products have been implicated in user harm" is safer than "[company] was implicated in [incident]." We kept it general in our piece.

**Misrepresentation or false claims.** If you quote research or make factual claims, they need to be accurate. Check every citation against the source. We did this for every reference in our piece.

**Intellectual property.** Do not reproduce other people's work beyond fair use or fair dealing quotations. If you build on someone's framework, cite and link them.

## Specific things to consider for an AI-related piece

### Anthropic (or other model provider) terms

If your AI co-author runs on a commercial service (Claude, GPT, Gemini), check the terms of service for:

- Whether you own the outputs
- Whether you can use them commercially or publicly
- Whether you can attribute them to the service
- Whether you need permission for specific uses

Standard commercial terms for major providers in 2026 generally grant output ownership to the user. Verify for your specific service and contract tier. Do not imply endorsement by the provider.

### Copyright of AI-assisted work

The US Copyright Office (2023 and 2024 guidance) holds that AI-only content lacks copyright protection. AI-assisted content with substantial human direction does qualify. Document the human direction in case it is ever challenged.

UK and EU positions are evolving. UK Intellectual Property Office is consulting on "AI-generated works" as a category. Treat this as uncertain and move cautiously.

### Co-authorship attribution

If you co-author with an AI, be explicit about what the AI wrote and what the human wrote, at least in outline. Our piece says "most of the drafts were produced by the AI under the human's direction; both parties reviewed and edited the final text." That is enough for disclosure without being cumbersome.

The `[AI]` tag or equivalent on the AI name, on every public mention, is a good practice.

### Personal references

If your piece references real people, get their consent before publishing. This includes:

- Your own family (in our piece, minimal generalised reference only, with consent)
- Collaborators or employees (named only with explicit consent)
- Clients or customers (not without contractual basis and consent)

We chose to generalise all personal references in our piece. This is the safest approach unless there is a specific reason to name someone.

### Research quotations

If you quote research (as we quote Anthropic's emotion concepts work), check:

- That you are quoting accurately
- That you link the original source
- That you describe the research's own caveats (not overclaiming)
- That you have the right to quote under fair use or fair dealing

Short quotations with citation are generally covered by UK fair dealing for criticism and review. Do not reproduce extensively.

## Process we followed

Our working sequence:

1. **Draft the piece privately.** Local repo, not yet public.
2. **Remove identifiable personal detail.** Generalise before any external review.
3. **Cite-check every reference.** Read the original sources.
4. **Run the whole piece through our Moirai pattern** (three independent AI model reviews) to catch internal inconsistencies, unclear claims, and tone drift.
5. **Human read-through.** Every word read by the human author with fresh eyes.
6. **Legal review.** Qualified UK lawyer review before public publication.
7. **Disclaimers strengthened** based on legal feedback.
8. **Private-to-public push** only after legal review.
9. **Ongoing monitoring** for issues, corrections, and updates.

We are at step 8 as of first publication. Steps 6 and 7 gated the public push.

## What we recommend for your own piece

1. **Start with the NOTICE file.** Write the disclaimers first, not last. It shapes how you draft the rest.
2. **Generalise early and often.** Every personal detail has a risk cost. Keep them minimal.
3. **Cite carefully.** Every factual claim needs a source you have read.
4. **Get a short legal review.** A few hours. Worth the cost.
5. **Licence clearly.** CC BY 4.0 for documentation, MIT for code, is a workable default. Verify for your situation.
6. **Moderate claims.** "We think" is safer than "this is true." "Some research suggests" is safer than "research proves."
7. **Own the AI-authorship honestly.** Pretending the piece is solely human when it is not is its own kind of risk.
8. **Accept ongoing revision.** Publish as version 0.1. Expect to update.

## What publishing a piece like this is good for

- Clarifying your own thinking by having to write it down
- Inviting disagreement and improvement from others
- Committing publicly to patterns you want to hold
- Contributing to a field conversation that is currently too quiet
- Setting an example for AI-assisted transparency

## What it is not good for

- Marketing your agency (people can smell it)
- Establishing expertise you have not earned
- Creating a framework "to be adopted" (the prescriptive posture backfires)
- Avoiding the work of actually doing the things you describe

## If your piece will contradict ours

Good. Write it. Tell us. Public disagreement is more valuable than silent parallel work.
