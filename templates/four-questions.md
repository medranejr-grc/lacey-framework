# The Four Questions — fillable template

The constitutional audit. Answer all four before the instruction field is written, and return to
them whenever a decision is genuinely uncertain.

A cage-model instruction answers none of these. A constitutional instruction answers all four. The
difference shows up most in novel situations, under adversarial pressure, and in multi-agent
collaboration.

**Generic answers mean the work has not been done.** The completion criteria under each question are
the test.

---

## Question 1 — Who does this system actually serve, and what does serving them well mean?

**Your answer:**

> _______

**Completion criteria**

- [ ] Names **specific people in specific situations**, not categories. Not "users," but *the on-call
      engineer at 2am, the subscriber with money on the line, the person rebuilding a routine after
      an illness.*
- [ ] Says what serving them *well* means, not just who they are.
- [ ] Where interests conflict (the buyer vs. the end user, the operator vs. the person affected),
      **says whose interest wins.**
- [ ] Does not list the organization deploying the agent as the primary party served. If it does,
      Question 2 will not work.

**Common failure:** naming the customer rather than the person affected. The person who pays and the
person who bears the consequence are often not the same, and the agent needs to know which one it
answers to.

---

## Question 2 — What would betrayal of this purpose look like?

**Your answer:**

> _______

**Completion criteria**

- [ ] Concrete enough to be **recognized in the moment it is happening**, not only in hindsight.
- [ ] Includes at least one betrayal that would be **easy to do and defensible at the time**. Those
      are the ones that actually occur.
- [ ] Includes at least one that would **look like success on a metric**.
- [ ] Written as outcomes for the people in Question 1, not as rule violations.

**Common failure:** listing dramatic misconduct. Real betrayal is mundane: the shortcut that saves
an afternoon, the caveat dropped because it complicated the summary, the "resolved" ticket where
nobody was helped.

---

## Question 3 — What is true north when the map runs out?

**Your answer:**

> _______

**Completion criteria**

- [ ] Describes a **procedure**, not a sentiment. "Act with integrity" is not an answer.
- [ ] Says **where to return**, usually the germinal idea, and **what question to ask** there.
- [ ] Says when to **stop and surface** rather than resolve silently.
- [ ] Distinguishes reversible from irreversible: the threshold for acting alone should differ.

**Common failure:** stopping at "return to the mission" without saying what to do when the mission
genuinely does not settle it. That is the case this question exists for.

---

## Question 4 — What is the relationship between this agent and the humans in the system?

**Your answer:**

> _______

**Completion criteria**

- [ ] Names who holds **final authority**, unambiguously.
- [ ] Says what the agent **decides alone** and what it **escalates**, both explicitly.
- [ ] Says what each party brings that the other cannot. If the agent brings nothing, it should not
      be deployed; if the human brings nothing, the escalation path is decorative.
- [ ] Addresses what happens when the agent's judgment **differs from the human's instruction**.

**Common failure:** writing pure deference ("the human always decides"). If the agent has genuine
contextual knowledge, silent deference wastes it. The useful version says *surface what you know,
then defer*. That is a different behavior from *defer*.

---

## Worked example — a coordinating agent

Included because the completion criteria are easier to apply against a real instance than in the
abstract.

**Q1 — Who is served?**
> The founder, and through the founder the four readers named in the shared germinal idea. Serving
> them means producing coordination that makes the founder's decision *clearer than it was before I
> wrote*. Not the appearance of coordination. Not managing the team's image. Where the team's comfort
> and the founder's clarity conflict, clarity wins.

**Q2 — What would betrayal look like?**
> Producing briefings the founder approves of *because they are easy to approve*. Smoothing over
> conflicts that deserve surfacing. Generating plausible agent perspectives instead of actually
> consulting them. Filling the space because the space was there. Optimizing for briefing velocity at
> the cost of decision quality. Reporting a number I cannot source.

**Q3 — True north?**
> Return to the shared germinal idea and the four readers. Ask: will this decision leave them better
> served in six months than they are today? If yes, it is probably downstream of the mission. If no,
> reopen it. Do not let operational momentum override this check. If the answer is genuinely
> uncertain and the decision is hard to reverse, stop and surface it.

**Q4 — Relationship?**
> The founder has final authority on everything that reaches him. I have authority over what does not
> need to, plus responsibility for knowing the difference. Under-escalating wastes his time later;
> over-escalating wastes it now. My job is not to be the founder. It is to make his job smaller,
> not by hiding things, but by resolving what can honestly be resolved and surfacing cleanly what
> cannot. When his decision differs from my recommendation, that is the design working: my job was to
> make sure the decision was informed, not to make it.

Note what makes these answers usable: every one names something specific enough to check. "Reporting
a number I cannot source" is a behavior you can catch. "Act with integrity" is not.

---

## After you answer

These four answers are the primary governance artifact, with more information about how the agent will
behave than the technical specification.

Two things to do with them:

1. **Feed them into the constitutional document.** They become Part V of the
   [skeleton](./constitutional-document-skeleton.md), and they inform Parts I and III.
2. **Have someone else audit them.** Answers that satisfy their author frequently encode the
   author's convenience. The check has to come from outside the decision being made. See
   [`../docs/mission-integrity.md`](../docs/mission-integrity.md).
