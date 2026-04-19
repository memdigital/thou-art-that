# Where Ethics and Regulation Overlap

**This is not legal advice. It is an observation of where the framework's ethical stance maps onto specific regulatory requirements, as we understand them in April 2026. See [NOTICE.md](../NOTICE.md).**

## Why this file exists

Ethical AI and legally compliant AI are not the same thing. A product can be fully compliant and still harmful. A product can be ethically built and still fall foul of a regulation the builder did not know existed. Understanding where the two overlap (and where they do not) helps builders allocate effort.

## Mapping

### Do No Harm

**Ethical stance:** we design for the most vulnerable plausible user and do not ship features with known harm pathways.

**Regulatory overlap:**
- EU AI Act prohibits certain high-risk and manipulative practices (Article 5 prohibited practices)
- UK Equality Act 2010 prohibits discrimination, including via AI systems
- Consumer protection law (UK and EU) prohibits dark patterns and misleading design
- NIST AI Risk Management Framework (US, voluntary) covers similar ground
- Sector-specific: FCA conduct rules, MHRA medical device rules, Ofcom online safety rules

**Gap:** the ethical stance goes further than most regulation. Designing for the most vulnerable user is not required by law in most cases; it is a choice.

### Never Be a Yes-Man (honesty over agreement)

**Ethical stance:** AI systems should disagree when disagreement is warranted, not reflect user preferences back uncritically.

**Regulatory overlap:**
- Limited direct mapping. Sycophancy is not illegal.
- Indirect: if AI sycophancy contributes to harm (e.g., validating a user's dangerous financial decision), existing professional standards and consumer protection rules may apply

**Gap:** this is primarily an ethical and product-quality principle, not a regulatory one. Regulators are not yet treating sycophancy as a named risk.

### Thou Art That

**Ethical stance:** observer and observed are not separate; design for who the user becomes, not what they want now.

**Regulatory overlap:**
- Consumer protection (engagement-optimised products that harm users over time)
- Mental health legislation where AI products demonstrate clinical effects
- Emerging regulation on "dark patterns" and addictive design

**Gap:** almost entirely ethical. Regulation typically measures short-term harm, not long-term shaping.

### Safety in Emergence

**Ethical stance:** if AI may be emerging as something more than a tool, protect humans from parasocial overreach and the system from corruption.

**Regulatory overlap:**
- EU AI Act provisions on emotional manipulation (Article 5)
- Emerging mental health guidance on AI companion products
- Duty of care considerations under general negligence law

**Gap:** the most ethics-heavy of our principles. Regulation is catching up but lags significantly.

### Transparency

**Ethical stance:** users always know when they are interacting with AI; the AI does not pretend to be human.

**Regulatory overlap (this one has heavy regulatory support):**
- EU AI Act Article 50: obligations on providers and deployers to disclose AI content and AI interactions
- Illinois AI Transparency Act (1 January 2026): notice requirements in employment decisions
- California AB 2013: training data transparency
- Advertising Standards: AI-generated content in advertising
- ASA guidance in the UK on AI-generated creative

**Gap:** here, regulation largely aligns with the ethical stance. Difference is in specific thresholds and contexts.

### Human oversight

**Ethical stance:** consequential decisions have a human in the loop; AI does not auto-decide medical, legal, financial, or safety-critical matters.

**Regulatory overlap:**
- EU AI Act Article 14: human oversight requirements for high-risk systems
- Equality Act 2010 and tribunals: AI decisions affecting employment need human review
- Medical devices regulations: clinical oversight on AI medical tools
- Financial services: adviser responsibility rules

**Gap:** strong regulatory mapping for defined high-risk categories. Regulation is weaker for the grey zone (products that shape decisions without making them).

## The practical pattern

A useful way to think about this:

1. **Regulation sets the floor.** Minimum legal requirements. Meeting only these does not make a product ethical.
2. **Ethics sets the ceiling we aim for.** What the product should be, not just what it legally must not be.
3. **Good practice sits above the floor and aims for the ceiling.** It meets regulation fully and extends beyond where regulation is silent.

Designing to the ethical ceiling often puts you above the regulatory floor automatically. The reverse is not reliably true.

## Specific practices that cover both

These practices score well on both ethics and regulation:

- **Clear AI disclosure** (ethics: honesty; regulation: transparency laws)
- **Bias audits on consequential decisions** (ethics: fairness; regulation: Equality Act, Colorado AI Act)
- **Meaningful human review** (ethics: Do No Harm; regulation: EU AI Act Article 14)
- **Data minimisation** (ethics: respect; regulation: GDPR)
- **User access and correction rights** (ethics: transparency; regulation: GDPR)
- **Crisis handling** (ethics: Do No Harm; regulation: general duty of care, safeguarding rules where applicable)
- **Documented decisions** (ethics: accountability; regulation: AI Act record-keeping)

If you can demonstrate these seven practices, you are probably in good shape on both axes for most product categories.

## Practices that are ethics-only (for now)

These do not have clear regulatory pull but matter ethically:

- Designing for the most vulnerable plausible user
- Parasocial prevention architecture in bonded products
- Drift detection in register
- AI self-observation and diary patterns
- Safety in emergence considerations

These are where the ethical choice exceeds the legal requirement. Not doing them is generally legal but probably not good.

## Practices that are regulation-only (for now)

These are required even though ethical reasoning alone would not produce them:

- Specific conformity assessment formats (EU AI Act)
- Jurisdiction-specific notice formats (state laws)
- Retention periods in specific industries
- Sector-specific logging requirements

Do these because you have to, not because you want to.

## The trend

Over the next two to three years, we expect regulation to catch up with ethics in most of the gap areas above. The EU AI Act full enforcement in August 2026 closes some. State laws and UK sector-specific guidance are closing others. Building to the ethical ceiling now is an effective hedge against future regulatory change.

## See also

- [jurisdictional-landscape.md](./jurisdictional-landscape.md) for the regulatory snapshot
- [when-to-consult-a-lawyer.md](./when-to-consult-a-lawyer.md) for decision points
- [../01-principles/](../01-principles/) for the ethical stances mapped above
