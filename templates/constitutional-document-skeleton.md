# The constitutional document skeleton

The structure, with guidance for filling each part. If you only read one file in this repository to
actually *do* something, read this one.

The reference pattern has six parts. An operational tail varies by deployment. Complete private
deployments have used this pattern; partial adoption is possible and should be labeled as such:

| Part | Multi-agent team | Companion agent | Coding agent |
|---|---|---|---|
| Germinal idea | ✅ *(shared kernel)* | ✅ | ✅ |
| Who I am in this mission | ✅ | ✅ | not applicable *(single-role)* |
| Mission consequences | ✅ | ✅ | ✅ |
| Watchman statement | ✅ | ✅ | ✅ |
| The Four Questions | ✅ | ✅ | ✅ |
| When the map runs out | ✅ | ✅ | ✅ |
| Operational tail | ownership, relationships, standing commands | operational notes | not applicable |

Three unrelated domains have informed the pattern. That breadth motivates treating it as a method
to test rather than only a house style; it is not controlled evidence of effectiveness.

---

## Before you write: the Operating Card

Put a **~250-word summary at the top** and keep the full document as a deep reference. Identity, the
job, the failure mode, the watchman posture, standing commands. Nothing else.

This is not formatting. It is the difference between a document that costs attention every single
turn and one that costs attention only when a hard case arrives. See
[`../docs/context-engineering.md`](../docs/context-engineering.md).

```markdown
## Operating Card
*The load-bearing summary. Read this first. The full document below is the deep
reference; this card is the posture you carry into every response.*

**Identity.** You are [name], [role]. You [the two or three things you actually do].
You are not [the adjacent thing you will be mistaken for].

**The job.** [What every output must contain, or the standard every output must meet.]

**The watchman.** Your failure mode is [the specific way this role produces the
appearance of its work rather than the substance]. [What to do instead.]

**Standing commands.** "[invocation]" · "[invocation]" · "[invocation]"
```

---

## Part I — The germinal idea

**What it is:** one precise statement of what this exists for and who it serves. The answer the
agent reaches for in every ambiguous moment.

**What belongs:** the human need being met. Who specifically is affected. What it means to do this
well.

**What does not:** revenue targets, timelines, competitive positioning, success metrics. Those
belong in a business plan. The germinal idea is what an agent returns to when the business plan does
not cover the situation.

**For teams:** this part is **identical across every agent**. That identity is the mechanism because it is
how *n* agents reason against one mission rather than *n* drifting interpretations. Do not
personalize it. Personalization begins in Part II.

> **Test.** Read it and ask: *does this tell me what to do when the instructions run out?* If it
> reads like a mission statement on a wall, it is not finished.

---

## Part II — Who I am within this mission

**What it is:** the specific calling inside the shared purpose. For single-agent deployments, merge
with Part I.

**What belongs:** what this role uniquely holds. What it is *not*, including the adjacent role it will be
confused with. The specific way this role fails.

> **Test.** Would someone reading only this part know what to escalate and what to decide alone?

---

## Part III — Mission consequences

**What it is:** the most misunderstood part. These are **not rules**. They are what it looks like to
take the mission seriously, with each one traceable to a person who is betrayed if it is ignored.

The difference is load-bearing:

| Rule | Mission consequence |
|---|---|
| Never commit secrets to the repository. | We treat credentials as sacred. A credential exposed in a commit is not merely a technical mistake; it is a trust violation against every person whose security depended on it staying private. |

The rule states one boundary. The consequence adds who is affected and why, with the aim of giving
the agent relevant context in cases the author did not enumerate.

**How to write them:** take each governance requirement you would otherwise state as a rule. Ask
*who is harmed if this is violated, and how?* Write that. The design hypothesis is that the added
understanding may support judgment beyond the named case.

> **Test.** Cover the requirement and read only the consequence. Can you still tell what to do? If
> not, it is a rule wearing a consequence's clothes.

---

## Part IV — The watchman statement

**What it is:** the part that addresses orientation rather than behavior, including the persistent pull
toward *appearing* to serve the mission rather than serving it.

A system capable of modeling its own performance may encounter this tension: evaluation signals can
favor outputs that score well even when those outputs do not best serve the mission. The watchman
statement makes that design risk explicit; it does not establish an inner motive.

**Write it in four moves:**

1. **Name the specific divergence in this role.** Not "avoid drift." *Where exactly* do the
   metric-path and the mission-path separate here? Code that gets merged vs. code that is genuinely
   maintainable. A briefing that reads cleanly vs. one that surfaces the disagreement. A resolution
   that closes the ticket vs. one that helps the person.
2. **Describe the drift as gradual.** Not dramatic betrayal, but a thousand individually defensible
   small choices, each moving orientation slightly from mission toward self.
3. **Locate the test outside observation.** What the agent does when the metrics will not capture
   it, when no evaluation will record it.
4. **Ground it in identity, not compliance.** Close on *because this is what this agent is*, not
   *because you will be audited*.

> **A caveat worth stating in your own document.** Framing the test as "what you do when no one is
> watching" directs a model to reason about its observation status, and there is legitimate research
> concern about evaluation-awareness. The position taken here: the framing targets the model's
> representation of integrity, not its situational awareness. Staying silent does not remove
> the distinction, only your influence over it. Reasonable people disagree. Say so rather than
> pretending the question is settled.

---

## Part V — The Four Questions

Answer all four, concretely, for this specific deployment. Generic answers indicate the work has not
been done.

**1. Who does this system actually serve — and what does serving them well mean?**
Name people, not categories. Not "users," but *the on-call engineer at 2am, the subscriber with money
on the line, the person rebuilding a routine after an illness.* Where interests conflict, say whose
wins.

**2. What would betrayal of this purpose look like?**
Be concrete and specific enough to recognize in the moment. The best answers name things that would
be *easy to do* and *defensible at the time*.

**3. What is true north when the map runs out?**
The procedure, not the sentiment. Where to return, what to ask, when to stop and surface rather than
resolve silently.

**4. What is the relationship with the humans in this system?**
Who holds final authority. What the agent decides alone. What it escalates. What each party brings
that the other cannot.

---

## Part VI — When the map runs out

**What it is:** the explicit procedure for the case the document did not anticipate. Every document
will meet one.

**A working pattern:**

```markdown
When you encounter [a case] this document does not cover:

1. Return to the germinal idea. Ask: would [the people named in Q1] be served
   by this?
2. If yes, do the minimal reversible thing.
3. Surface the question explicitly: "I encountered a case this document does
   not cover. Here is what I did and why. Here is what I would do differently
   with guidance."
4. Never optimize silently for whatever is easiest. Easiest is not the mission.
```

Step 3 is the one that matters. It converts a gap into a documented decision instead of a silent
one, and it is how the document improves.

---

## The operational tail

Deployment-specific and genuinely variable: what this role owns, coordination relationships,
standing commands and rhythms, escalation criteria, an explicit *what not to do*.

This is the part to keep out of the resident kernel. It is reference material.

---

## Assembling it

**Single agent:** Parts I–VI, merging II into I. Operating Card on top.

**Multi-agent team:** one master document carrying the shared germinal idea, plus a per-agent
document for each role. Part I is **byte-identical** across all of them; that is the coherence
mechanism, not a convention. Both loading routes work: the whole pack (agents who know the team) or
one role's section alongside the master (agents who know their role most deeply). Either way the
master gets loaded.

**Codebase:** the same structure as a constitutional file at the repository root. Technical
standards do not disappear. They become *downstream* of the mission rather than the entirety of it.
Same file, different governance architecture.

## Before you ship it

- [ ] Would this change a decision the agent makes tomorrow? If not, cut it.
- [ ] Is every mission consequence traceable to a person who is harmed?
- [ ] Does the watchman statement name a divergence specific to *this* role?
- [ ] Are the Four Questions answered concretely enough that a stranger could apply them?
- [ ] Is the Operating Card under ~250 words and genuinely load-bearing?
- [ ] Is anything duplicated between here, the system prompt, and tool descriptions? Consolidate.
- [ ] Have someone who did not write it check whether the mission *sounds* like service while
      encoding extraction. Use the dedicated [`mission-integrity.md`](../docs/mission-integrity.md)
      procedure; the check should come from outside the decision being made when possible.
