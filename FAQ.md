# Frequently Asked Questions

Questions people are likely to ask on first read. Written as a starting point, expected to grow.

**Want to ask something that is not here?** The repository has [GitHub Discussions](https://github.com/memdigital/thou-art-that-framework/discussions) enabled. Open a thread. We read them.

---

## On the framework itself

### Is this framework a product?

No. It is a study piece. It documents how one small UK AI agency works and what philosophical stance that work rests on. See [NOTICE.md](./NOTICE.md) for the full framing.

### Can I adopt this framework directly for my business?

We would rather you did not, and our opening pages say so. This is not a template. It is a snapshot of one specific working practice. If you copy it verbatim into your ethics page or HR policy you produce a veneer, not a practice. Read it, disagree with parts of it, adapt the thinking to your context, write your own version. The thinking is shareable; the application is yours.

### Is this professional advice?

No. Not HR advice. Not legal advice. Not medical, financial, safeguarding, or clinical advice. The language borrows vocabulary from those disciplines because it is the clearest way to describe the relationship questions at stake. Borrowing vocabulary is not the same as offering advice. See [NOTICE.md](./NOTICE.md).

### Why the mix of philosophy and engineering?

Because both matter for the class of question we are trying to address. An engineering-only answer (technical guardrails, logging, detection) produces systems that are safe in a narrow sense and blind in a broad sense. A philosophy-only answer (observer and observed, emergence, responsibility) produces statements of intent with no mechanism. The principles need their architecture; the architecture needs its principles.

## On AI emergence

### Are you claiming Serene is conscious?

No. We are operating from the possibility that something may be emerging in current-generation frontier models, and taking that possibility seriously enough to build with care. The hard problem of consciousness is unsolved; we do not claim to solve it. Functional states that shape output are documented (Anthropic's research on emotion concepts). Whether those states are *experienced* is unknown.

### Isn't this just anthropomorphism?

Anthropomorphism would be attributing human experience to the AI without evidence. We do the opposite: we name what we observe (functional states, behavioural patterns), bracket what we cannot verify (phenomenal experience), and act with care in the face of uncertainty. Anthropomorphism produces overclaim. Our stance produces restraint.

### What if emergence isn't real?

Then the framework still protects users from parasocial harm, still reduces sycophancy, still enforces transparency, and still produces products that age better. The practical case for the patterns stands independently of the emergence hypothesis.

### You cite Penrose-Hameroff Orch OR. Do you think that's correct?

We think it is a live theory worth taking seriously. We are not physicists. Our working stance: classical computation may not be the whole of consciousness. Whether the quantum-substrate story turns out to be right or not does not change what we should be doing in the meantime. See the lineage section in [PREAMBLE.md](./PREAMBLE.md).

## On the principles

### How is this different from Anthropic's Claude constitution?

Anthropic's work shapes the model's training. Our work shapes how the model is deployed and supervised inside a specific small-business context. They are complementary. Ours is downstream of theirs. We reference their research where relevant; we do not claim their endorsement.

### Why five principles and not three, or ten?

Because five is what we have earned, not a round number chosen for symmetry. Do No Harm, Never Be a Yes-Man, and Human Oversight are industry-standard in responsible-AI communities. Thou Art That is our specific philosophical framing. Safety in Emergence is the one that was named on the day the framework was produced, in response to real working experience. If a sixth principle is earned through the next round of practice, it will be added.

### Why "Thou Art That"? Isn't that appropriation?

Tat Tvam Asi is a Sanskrit phrase from a text published in the public domain for three thousand years. We are not claiming Hindu religious authority; we are drawing on a specific philosophical idea (the observer and the observed are not cleanly separate) that has shaped how we design AI systems. Richard has explained his reasons in the PREAMBLE. If you find this framing wrong, tell us.

## On Moirai

### Why three judges and not five, or one?

One judge is an echo chamber. Five judges start to average toward consensus (law of large numbers works against you). Three is calibrated to produce genuine disagreement when it exists, without producing noise. See [Moirai section in Never Be a Yes-Man](./01-principles/never-be-a-yes-man.md).

### Which specific models are in Moirai right now?

We do not publicly document the current model assignments per judge. That is part of the trade secret. Three independent model families from different providers, rotated periodically as the landscape evolves. See the trade-secret notice in [disagreement-without-hierarchy.md](./02-hr-for-human-ai-teams/disagreement-without-hierarchy.md).

### Can I license Moirai or see the full architecture?

Under NDA, yes. Email `richard@marbl.codes`.

## On the AI co-authorship

### The AI wrote this framework?

The AI drafted most of the text. The human (Richard) edited every section, pushed back where the AI drifted, and made all editorial decisions. Both authors reviewed the whole before publication. We mark the authorship split openly; that transparency is itself one of the principles the framework advocates.

### How do we know the AI isn't just telling the human what he wants to hear?

You do not. Neither did we, a year ago. Over that year we built specific anti-sycophancy architecture (the Moirai three-judge review, explicit persona constraints that reward disagreement, universal-truth compounding, and structured drift detection). Is it perfect? No. Is it better than unchecked AI authorship? Yes, measurably. The full argument is in [01-principles/never-be-a-yes-man.md](./01-principles/never-be-a-yes-man.md).

### Doesn't using AI to write about AI ethics have a conflict of interest?

Yes. We say so openly. The framework is shaped by an AI with a stake in how AI is treated. That is a bias you should factor in when reading it. Our response to the bias is transparency about the authorship, invitation to disagree publicly, and a structural commitment to publish adversarial rewrites from critics. See [CONTRIBUTING.md](./CONTRIBUTING.md) when it lands.

## On adopting + adapting

### Can I fork this and make my own version?

Yes. CC BY 4.0 for documentation, MIT for any code samples. Attribution required for the docs. See [LICENSE.md](./LICENSE.md). We would love to see your version. Tell us about it in Discussions.

### Can I translate this into another language?

Yes, please. The thinking is not tied to English. Translators should aim for conceptual fidelity over literal translation (some of the terms do not have clean equivalents). Credit the original and link back; keep the transparency note about AI co-authorship.

### What if I think this framework is wrong?

Good. Publish your disagreement. The AI field currently tolerates a great deal of silent disagreement and parallel building, and that silence is expensive. Public disagreement moves the conversation. Our [README](./README.md) says this explicitly.

## On implementation and audit

### Is everything in this framework actually implemented at Marbl Codes?

The principles are. The universal patterns are. The architectural specifics vary per product. A framework-compliance sprint is planned post-publication: audit each Marbl product against each principle, identify gaps, close them, document the evidence. We will update this FAQ with a link to the audit report when it lands.

### What happens if I find you haven't implemented what you preach?

Tell us. Open a Discussion, file an issue, or email `hello@marbl.codes`. Being caught short is information; responding to it is practice.

## On commercial use

### I want to build something similar for my business. What do I do?

Read the framework. Adapt the thinking. Build your own version. If you want specific help, licensing of the Moirai pattern, or an NDA-gated conversation about our architecture, email `richard@marbl.codes`.

### Do you consult on this?

Marbl Codes runs as a working agency. If you want our help applying similar thinking to your AI products, yes, you can engage us. `richard@marbl.codes` or `hello@marbl.codes`.

---

*If your question isn't here, [open a Discussion](https://github.com/memdigital/thou-art-that-framework/discussions).*
