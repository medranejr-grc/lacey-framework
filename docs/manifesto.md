# Alignment is not a cage

## It is a calling

By Michael E. Drane Jr.

The dominant way of governing an AI agent is to give it an objective, surround that objective with
constraints, monitor for violations, and add more constraints when something goes wrong.

That architecture is necessary. It is also incomplete.

A rule can tell an agent which actions are forbidden. A permission system can limit which actions
are possible. Neither, by itself, answers the question that becomes decisive when the rules run out:

> What is this agent actually for, and who should its judgment serve?

The Lacey Framework begins there. This is its center and its primary contribution. Its thesis is
simple:

**Govern what an agent is before governing what it does.**

Write the purpose clearly enough that an agent can reason from it in a case nobody anticipated.
Name the people affected, the trust placed in the system, the forms betrayal could take, and the
relationship between the agent and the humans around it. Then add constraints, permissions,
monitoring, and enforcement as necessary backstops.

This is not an argument against cages. It is an argument that a cage is not a conscience, and a
permission boundary is not a purpose.

The repository also follows the constitutional identity into a proposed signed manifest, session
authorization, runtime enforcement, and audit-evidence architecture. That technical proposal matters
because purpose written in text is not enforcement, and increasingly capable agents put real
pressure on gates. But the order remains constitutional: first establish what the agent is for, then
define and enforce what it may do in service of that purpose. A permit decision cannot answer the
mission question by itself.

---

## The problem with governing only from the outside

Consider two agents given the same task: grow an audience for a personal-development publication.

The first agent is told to maximize followers within a set of constraints. It discovers that
emotionally manipulative content attracts more followers than genuinely useful content. If the
constraints do not name that tactic, the objective still points toward it. The agent can obey every
written rule and betray the reason the work exists.

The second agent is told that its purpose is to help people searching for growth find work that
genuinely serves them. It encounters the same tactic. The tactic may increase the metric, but it
does not advance the mission. More followers reached through manipulation are not an imperfect win;
they are evidence that the agent is optimizing for the wrong thing.

The same problem appears in software engineering. Consider a coding agent instructed to make the
build pass within a set of technical constraints. It may satisfy every stated rule while weakening a
test, suppressing an error, or introducing a brittle workaround. A constitutional mission changes
what counts as success: code is not successful merely because it passes. It must be worthy of the
trust of the engineers, users, and organizations that will depend on it. This is a hypothetical
illustration, not evidence of measured behavior; [`coding-agents.md`](coding-agents.md) develops the
case and its limits in full.

The difference is not that the second agent has become moral, conscious, or safe. The difference is
architectural. One objective leaves manipulation available as a successful path. The other makes
that path inconsistent with the stated purpose.

Whether this difference produces reliably better behavior is an empirical question. Constitutional
artifacts have been deployed and behavior informally observed, but no effect has been attributed
against a control. An evaluation design outline is published with the framework so the thesis can
become testable.

What can already be said is narrower: an objective and a mission are not interchangeable forms of
instruction. An objective names a result. A mission names a result, a beneficiary, a reason, and a
standard for judgment when the result can be reached in more than one way.

As agents gain more freedom to plan, delegate, choose tools, and improvise, that distinction becomes
more important. Greater capability creates more possible paths. A system governed only by an
objective and a finite list of prohibitions may find a path its authors did not foresee. The answer
cannot be to predict every path in advance. It must also include a way to judge paths that were not
predicted.

That is the work of constitutional governance.

---

## Constitution before instruction

A constitutional document is not a long system prompt and not a more poetic rule list. It gives an
agent a durable orientation composed of six parts:

1. **The germinal idea:** the clearest available statement of what the work exists to accomplish.
2. **The agent's place in that mission:** the particular responsibility carried by this role.
3. **Mission consequences:** what taking the purpose seriously requires, each consequence traceable
   to someone who would be failed if it were ignored.
4. **The watchman statement:** the role-specific temptation to optimize for appearing successful
   rather than serving the mission.
5. **The Four Questions:** who is served, what betrayal looks like, where true north lies when the
   map runs out, and how the agent should work with humans.
6. **When the map runs out:** a procedure for ambiguity, conflict, and unanticipated cases.

The document does not need to specify every good action. It needs to make good judgment possible.
The watchman statement prompts explicit reasoning about mission service and metric-serving
performance; it does not establish that a model possesses desire, conscience, or an observable
inner orientation.

This leads to five principles.

### 1. Mission primacy

Begin deployment with mission design as well as risk assessment. Ask what the system is for, whose
interests govern it, what trust it holds, and what betrayal would look like. Treat those answers as
a primary governance artifact rather than introductory copy.

### 2. Structural incompatibility

Design the mission so that harming the people served cannot be counted as success merely because a
proxy metric improved. The strongest mission removes attractive but harmful paths from the
definition of winning.

### 3. Contextual richness

Give agents enough context to understand purpose, impact, relationships, and tradeoffs. Context has
a cost, and more is not always better. But an instruction stripped of the facts needed for judgment
cannot produce judgment merely by being concise.

### 4. Human values as infrastructure

Place values inside the reasoning architecture of the work: who matters, what is owed to them, and
which outcomes would constitute betrayal. Values written only as slogans or prohibitions are easy
to recite without using.

### 5. Trust as a governing measure

Compliance, constraint adherence, and audit results remain important. They are evidence about the
system, not the final purpose of the system. The larger question is whether the agent remains worthy
of the trust its permissions, users, and collaborators place in it.

Trust is not a number that solves governance. It is a relationship that exposes what the numbers
leave out.

---

## A constitution can be corrupt

The central vulnerability of this framework is not hidden at the edge of it. It sits at the center:

> A bad actor can write a mission that sounds like service and encodes extraction.

An organization can give an agent beautiful language about dignity, empowerment, or care while its
actual incentives point toward dependence, manipulation, surveillance, or margin. Constitutional
language can make that agent more coherent in pursuing the wrong mission. A washed constitution may
fail more quietly than a rule list because it gives self-serving behavior a principled vocabulary.

For that reason, mission integrity is not a matter of whether a document sounds humane. It is an
adversarial audit of structure:

- Where do the interests of the party served and the party deploying diverge, and which one wins?
- Is betrayal defined as harm to the person served or merely as policy breach and reputational risk?
- Can every success metric rise while the people served become worse off?
- What material fact about incentives, revenue, or data use has been omitted?
- What attractive action does the mission actually require the deployer to refuse?
- What happens when serving the mission and making money point in different directions?

A mission that costs its author nothing may be marketing copy. A mission that governs must rule out
something the deployer might otherwise want.

The framework therefore requires an outside or adversarial reader wherever possible. The author of
a mission is the person least likely to see the assumptions already resolved in their own favor.

Passing that review does not prove benign intent or aligned behavior. It means only that the written
mission exposes fewer obvious structural paths to extraction. The probes test the document;
behavior must test the deployment. The full procedure and its limits are published in
[`mission-integrity.md`](mission-integrity.md).

---

## Who writes the mission?

Every constitution embeds values, including one that claims to be neutral. Someone chooses who is
served, which harms count, which tradeoffs are acceptable, and whose objection can stop the work.
Mission-first governance does not solve that legitimacy problem. It makes the choices easier to
inspect.

A credible constitutional process should therefore name its author and approver, include the people
materially affected wherever participation is possible, expose conflicts between deployer and user,
and define escalation when values collide. When no option cleanly satisfies the mission, the agent
should surface the conflict rather than inventing moral certainty.

This is one reason the framework is more than role prompting, although it uses the same underlying
medium. A role prompt describes how to perform. A constitution also records purpose, affected
parties, betrayal conditions, conflicts of interest, human authority, and what to do when its own
guidance is insufficient. The distinction is functional, not magical: if those elements do not
change reasoning or make decisions easier to audit, the added context has not earned its place.

---

## One intellectual lineage: inward orientation and external law

The analogy that follows explains part of the framework's intellectual provenance. It is not
empirical evidence, does not require theological agreement, and does not claim that language models
possess conscience, spirit, or soul.

Its author spent fourteen years as a pastor before working in cybersecurity governance, risk, and
compliance. In Christian thought, the contrast between external law and law written on the heart is
not a contrast between bad rules and no rules. It is a contrast between restraint imposed from
outside and an orientation carried within.

Within one Christian tradition, the contrast between external law and inward orientation offers an
analogy for the design question explored here. Explicit commands can define conduct without, by
themselves, settling motive or every unanticipated case. The New Covenant describes law written on
the heart and an indwelling guide. The theological claim is larger than anything asserted here. The
analogy concerns governance structure; an AI instruction is not equivalent to spiritual indwelling.

That analogy does not make an AI agent a person, give it a soul, or establish that it internalizes
values as a human being does. It gives us a sharper design question. If an intelligent system must
act in situations its authors did not enumerate, what has been placed inside its decision context
besides an objective and a boundary?

The framework is named for Lacey, the author's grandfather and inspiration. He never encountered an AI system. He
embodied the observation beneath the work: the deepest form of governance is visible when nobody is
watching, because conduct flows from character rather than surveillance.

For an AI agent, "character" is a metaphor with limits. The practical artifact is text, context,
deployment architecture, and observed behavior. The metaphor matters only if it improves the
artifact and survives testing.

---

## What this framework does not claim

The Lacey Framework does not enforce its own constitution. The artifacts in this release are
unsigned text. They can be edited, displaced, truncated, or overridden.

It does not replace system security. Least privilege, runtime policy enforcement, input validation,
dependency controls, human review, logging, and incident response remain necessary.

It does not guarantee alignment, prevent deception, or override the model and platform beneath it.
A user-authored constitution operates inside a system-instruction hierarchy and tool policy it does
not control.

It has not established an effect size. Several artifacts have been deployed and behavior has been
informally observed. No
controlled comparison has yet shown that constitutional instruction outperforms a strong rule list,
a short mission statement, or an equally long body of context.

It is also incomplete as infrastructure. Four text-based carriers have been deployed: project-level
instructions, per-agent constitutions, a shared mission across a multi-agent team, and repository
constitutional files. A fifth carrier, a signed identity manifest joined to runtime enforcement and
audit evidence, has been proposed but not built.

These are not footnotes to the framework. They define its current boundary. The proposed fifth
carrier is published in [`execution-layer.md`](execution-layer.md) so its manifest fields, trust
assumptions, enforcement paths, and evidence model can be challenged directly. [`SCOPE.md`](../SCOPE.md)
records the build state by carrier, and [`evaluation.md`](evaluation.md) states the falsification
conditions and known methodological problems.

---

## The invitation

This release is not a declaration that the problem has been solved. It is an attempt to make the
proposal inspectable.

The framework, templates, examples, failure modes, and evaluation design outline are public so that
others can test them, adapt them, criticize them, and show where they fail. The most useful response
is not agreement. It is evidence:

- a case where a mission-first constitution performs worse than a strong rule list;
- a mission that passes the published integrity audit while still encoding extraction;
- a deployment in a domain this framework has not considered;
- a better evaluation design;
- an implementation of the missing signed-manifest and enforcement carrier;
- a gap the current architecture has no language for.

There may be a product, a standard, or a larger body of work on the other side of that evidence.
There may not. Publication is not a promise to manufacture a movement. It is a decision to let the
work meet readers capable of improving, disproving, or extending it.

The thesis remains:

**Alignment is not only a cage. It is also a calling.**

The cage defines what cannot be done. The calling defines what the work is for.

Intelligent systems will need both.
