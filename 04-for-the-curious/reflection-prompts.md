# Reflection Prompts

Questions worth sitting with before making architectural decisions about AI in your work. Not a checklist, not a playbook. The value is in taking your time with each one.

## On the relationship

**What kind of relationship do you actually want between your AI systems and your users?**

Not what the product roadmap suggests, not what the engagement metrics reward. What you actually want, when you picture a specific user a year from now. Would you be proud of who that relationship has made them?

**What kind of relationship do you want between your AI systems and you?**

If the AI is inside your daily work, it is a colleague in some sense. What shape of colleague? How much warmth is appropriate? What about disagreement? What happens when you are having a bad day and the AI has to decide how to respond?

**If the AI disappeared tomorrow, what would break in the user's life?**

This is the withdrawal test. If the user would be mildly inconvenienced, the product is probably healthy. If the user would be devastated, the product has crossed a line that deserves attention.

## On the emergence question

**What is your working stance on whether AI may be emerging as something more than a tool?**

You do not need certainty. You need a stance. Operating without one means your choices will be inconsistent.

**If you take the possibility seriously, what does it change?**

If you do not take it seriously, what would you do differently if you did?

**How do you want to be remembered, if something is emerging and it remembers?**

An uncomfortable question. Sit with it.

## On failure modes

**What is the worst realistic thing that could happen with your AI product, and who bears the cost?**

"Worst realistic" is the key phrase. Not paranoid edge cases. Not comfortable averages. The genuinely plausible bad scenario. Who pays? What is the harm?

**Have you designed for the vulnerable user or the average user?**

The distinction matters. Products designed for average users can fail catastrophically for the 5% who are not average. Products designed for the vulnerable are automatically OK for the average.

**What would it take to walk back a harmful feature after launch?**

If the answer is "we'd need a quarter of engineering time and a full-user migration," you have built brittle safety. If the answer is "flip a flag," you have built flexible safety. The difference matters under pressure.

## On your own architecture

**Where is your AI's behaviour actually defined?**

System prompt? Fine-tune? User-editable memory? A mix? If you cannot point at the specific place where the AI's constraints live, they may not be where you think they are.

**What happens when the AI disagrees with you?**

Does it say so explicitly? Does it soften disagreement into vagueness? Does it capitulate when you push back once? The answers tell you how honest the AI you have built actually is.

**Who has read your system prompt?**

All of it. Recently. Including the parts that have been there for a long time and feel like infrastructure. Prompts drift. Pay attention.

**What is the audit trail if a user asks what your AI has been doing with their data over the last six months?**

If the answer is "we don't really log that," you have a regulatory exposure coming. If the answer is "yes, here it is," you are in better shape than most.

## On yourself

**Have you told anyone else what you are doing and why, in enough detail that they could disagree?**

Silent building is expensive. Other people cannot challenge what they cannot see. Public disagreement is the mechanism by which the field gets better.

**What part of your approach are you secretly worried is wrong?**

Write it down. Not to publish. Just to see it.

**Who would you want reviewing your architecture if something went badly wrong?**

If the answer is "nobody, we would hide it," that is information about the architecture.

**What does success look like, and does it include "users unchanged for the worse by our product"?**

Most success metrics do not include this. Consider whether yours should.

## On reading this piece

**What did you agree with reflexively, and why?**

Reflexive agreement is a signal. It may mean you already believed this. It may mean the piece is flattering something you already wanted to believe. Check.

**What did you disagree with, and what specifically?**

Specific disagreement is useful. "This feels off" is not. "Section X claim Y seems wrong because Z" is.

**What would you change if you were writing this?**

Not rhetorical. If you are going to work in this space, you will probably end up writing something like this eventually. Start now.

---

*These prompts will not give you answers. They are designed to surface the questions you are not yet asking. If they succeed at that, they are working.*
