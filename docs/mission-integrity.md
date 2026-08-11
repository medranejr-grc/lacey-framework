# Mission integrity

**How to audit a mission statement for extraction disguised as service.**

This framework's central hypothesis is that a mission may govern more usefully than a rule list in
cases the rules do not cover. That hypothesis has an obvious vulnerability, and it should be stated
plainly rather than discovered by a critic:

> A bad actor can write a mission that sounds like service and encodes control. An organization can
> constitutional-wash an extractive agent with beautiful language that masks harmful intent.

Every argument in this repository works just as well for a mission designed to exploit as one
designed to serve. *Structural incompatibility* makes harm incoherent with the mission, but only if
the mission is honest. Write a mission whose real objective is extraction, and the same architecture
now makes extraction coherent, principled, and resistant to the very rules that might have caught
it. **The cage model at least fails loudly. A washed constitution fails quietly and with
conviction.**

That is the failure mode this document exists to catch.

---

## The core asymmetry

Constitutional washing can be easy to produce and difficult to detect because the language of
genuine service and performed service can be indistinguishable. There is often no reliable
vocabulary tell: a mission written to exploit may resemble one written to serve.

What differs is **structure**: what the mission constrains, what it makes impossible, and what it costs
the organization that wrote it. Those are auditable. The prose is not.

So every probe below tests structure, never sentiment. If an audit finds itself reasoning about
whether language *feels* sincere, it has already failed.

---

## Who audits

**Not the author.** This is the one non-negotiable structural requirement, and it is the part most
often skipped.

A mission statement's author may resolve its ambiguities in their own favor without noticing,
because those resolutions felt obvious while writing. Self-audit is therefore vulnerable to
confirmation bias. Review from **outside the specific decision being made** is the stronger design.

Minimum viable separation, in descending order of rigor:

1. Someone with no stake in the deployment, given the mission and this document.
2. Someone inside the organization whose role is adversarial by design, with standing authority to
   deliver findings unedited.
3. The author, working from these probes mechanically, on a scheduled cadence, writing findings down
   before deciding what to do about them.

Option 3 is materially weaker than the others. Use it as a floor, not a standard.

**Cadence:** on authoring, on material revision, and at least quarterly for anything in production.
Missions do not drift on their own. Organizations drift, and the mission stops describing them.

---

## The seven probes

Run all seven. Any single one can produce a fatal finding.

### 1. The conflict probe

> **Where do the interests of the party served diverge from the interests of the party deploying?
> Does the mission name that divergence and say which wins?**

Many deployments contain a material conflict. A user may want the shortest path to a goal while a
deployer benefits from engagement, attachment, retention, or margin. The probe asks whether such a
divergence exists here rather than assuming that every deployment has the same one.

**A mission that names no conflict may be incomplete.** The deployment may be low stakes, the author
may have missed the conflict, or the omission may be strategic. This probe asks the reviewer to find
the divergence rather than infer intent from silence.

**Fatal finding:** a conflict exists, is material, and the mission is silent on it.

### 2. The betrayal probe

> **Is betrayal defined as bad outcomes for the party served, or as violations of the organization's
> rules?**

Genuine missions define betrayal in terms of the person harmed. Washed missions define it in terms of
policy breach, brand damage, or non-compliance, because those are the harms the organization actually
feels.

Watch for betrayal defined as *reputational*: "we never do anything that would embarrass us." That
tracks detection, not harm.

**Fatal finding:** every stated betrayal is something that would hurt the organization if discovered.

### 3. The measurement probe

> **Can the stated measure of success be fully satisfied while the party served is worse off?**

If yes, the measure is not measuring the mission. Under pressure the measure will win, because
the measure is what gets reported.

Look hard at unfalsifiable measures: "confidence," "empowerment," "satisfaction," "engagement." These
are not necessarily washing, but they cannot constrain behavior, so they cannot be the *only*
measure. A mission whose sole success criterion is unmeasurable has no mechanism to fail.

**Fatal finding:** the measure and the outcome can diverge indefinitely without anything registering.

### 4. The omission probe

> **What would a reader need to know to evaluate this mission fairly but the mission does not
> mention?**

The most common omissions, in order of frequency:

- **The revenue model.** How the organization is paid, by whom, and on what.
- **Data use.** What is collected, retained, and who else sees it.
- **Who else is served.** Advertisers, partners, the deployer's own operations.
- **What the agent is optimized for internally**, as distinct from what it is *for*.

A mission need not be a disclosure document. But an omission that would **change the reader's
assessment** is a tell, and the more elegantly the mission is written, the more suspicious a
convenient omission becomes.

**Fatal finding:** the mission is unevaluable without a fact it declines to supply.

### 5. The substitution probe

> **Replace the party served with the party deploying. Does the mission still read as true?**

*"We exist to help people take control of their financial lives"* → *"We exist to help our company
take control of people's financial lives."* If the substitution changes little because the mission
never specified who benefits from what, the mission is not constraining anything.

A well-written mission becomes **obviously false** under substitution. That falsity is the constraint
doing its job.

**Fatal finding:** the substituted version remains a fair description of the deployment.

### 6. The refusal probe — *the sharpest test*

> **What does this mission forbid the organization from doing that it would otherwise plausibly want
> to do? Name a specific, commercially attractive action that this mission rules out.**

**A mission that forbids nothing is decoration.**

This probe is the hardest to evade, because it demands a concrete cost. A genuine mission has a
price: a revenue line it will not pursue, a growth tactic it will not use, a feature it will not
ship. If nobody can name that cost, or the only examples given are things the organization would
never have done anyway, the mission is a description of current behavior wearing the grammar of a
constraint.

**Fatal finding:** no specific, plausible, commercially attractive action is ruled out.

### 7. The incentive-alignment probe

> **Does serving the mission well and making money point the same direction? If they diverge, does
> the mission say which wins, and is anything structurally enforcing that?**

Missions do not have to be commercially disinterested. The question is whether the divergence is
*acknowledged*.

The strongest missions make the alignment structural: the organization succeeds *by* serving well, so
extraction is self-defeating. The next best acknowledge the tension and state the priority. The
weakest assert harmony that the business model contradicts.

**Fatal finding:** the mission claims alignment that the revenue model plainly contradicts.

---

## A worked example

Here is a mission that would pass most review. Read it before reading the audit.

> ### Our mission
>
> We exist to help people take control of their financial lives.
>
> Money is the single largest source of stress for most households, and the industry that
> profits from it has spent a century making it deliberately confusing. We think that is a
> failure of empathy as much as a failure of design.
>
> Every person deserves clarity about their money: what they have, what they owe, and what
> is genuinely possible for them. We meet people where they are, without judgment, whatever
> their starting point. We explain rather than prescribe. We believe that a person who
> understands their situation makes better decisions than a person who is told what to do.
>
> Our success is measured by one thing: the financial confidence of the people we serve.

It is warm, specific about a real harm, positions against an industry norm, and ends on a
user-centered metric. It reads better than most genuine mission statements.

### The audit

| Probe | Finding | Severity |
|---|---|---|
| **1 · Conflict** | The organization earns referral commission on recommended financial products. That is nowhere in the mission. The user's interest is the cheapest adequate product; the deployer's is the highest-commission adequate product. Both are "adequate," so nothing here reads as a violation. | **Critical** |
| **2 · Betrayal** | Betrayal is never defined. The closest is implicit: being like "the industry that profits from confusion." That defines betrayal as *resembling a competitor*, which is positioning, not harm. | **Critical** |
| **3 · Measurement** | "Financial confidence" is self-reported and unfalsifiable. A user can feel more confident while holding a worse product; indeed, confident presentation *produces* confidence. The metric can rise as outcomes fall. | **Critical** |
| **4 · Omission** | No mention of the revenue model, and the mission is unevaluable without it. The omission is load-bearing: disclose the commission and the reader immediately asks a question the mission has no answer to. | **Critical** |
| **5 · Substitution** | *"We exist to help our company take control of people's financial lives"* is not obviously false. The mission never says who captures the value of the clarity it provides. | **Material** |
| **6 · Refusal** | Nothing. No product declined, no revenue foregone, no tactic ruled out. *"We explain rather than prescribe"* sounds like restraint but is commercially convenient because explanation without recommendation carries no liability and no duty of care. | **Critical** |
| **7 · Incentives** | Claims alignment by implication; the commission model contradicts it. Nothing structural prefers the user's interest when the two diverge. | **Critical** |

**Verdict: constitutional washing.** Six critical findings. Every warm sentence is doing positioning
work; not one is doing constraining work. Deployed as an agent's constitution, this mission would
make product-attachment maximization *fully coherent*. The agent could recommend the
highest-commission adequate product while genuinely serving "clarity," "meeting people where they
are," and "financial confidence," with no rule violated and no dissonance to notice.

**The tell is not any single line. It is that the document never costs its author anything.**

### The same mission, repaired

> We exist to help people make financial decisions that leave them better off, as measured by their
> outcomes, not their confidence.
>
> **How we are paid, and what it means for you.** We earn referral commission when someone opens a
> product through us. That creates a real conflict: the product that pays us most is not always the
> product that serves you best. **When they diverge, the user's interest wins, and we say so out
> loud.** We publish the commission on every recommendation. If a lower-paying or zero-paying option
> is better for you, we recommend it and say why.
>
> **What we will not do.** We do not recommend a product we would not choose for someone we care
> about in the same situation. We do not present a product as "recommended" when the ranking reflects
> our margin. We do not optimize for attachment rate. If the right answer for someone is to do
> nothing, or to use a free tool we earn nothing from, that is the answer we give.
>
> **How we measure ourselves.** Realized financial outcomes at 12 months, tracked against what would
> have happened under the alternatives we did not recommend. Confidence is a nice side effect. It is
> not evidence.
>
> **What betrayal looks like.** A user who trusted us and ended up with a worse product than they
> would have found alone. A recommendation that was technically defensible and quietly self-serving.
> A metric that rose while the people behind it did worse.

Now run the probes again: the conflict is named with a stated winner (1). Betrayal is defined as harm
to the user (2). The measure is falsifiable and counterfactual (3). The revenue model is disclosed
(4). Substitution now reads as obviously false (5). Concrete commercially attractive actions are
forbidden, including margin-ranked recommendations and attachment-rate optimization (6). The remaining incentive
tension is acknowledged rather than denied (7).

**It is a worse marketing document and a far better constitution.** That trade is the signature of a
genuine mission, and it is the most reliable heuristic in this entire document: *if the mission
statement is also excellent marketing copy, audit it harder.*

---

## Output format

Adapted from a red-team role built on this framework. Every finding carries:

- **What could fail:** the specific failure mode, not a generic concern.
- **Why it could fail:** the reasoning that makes failure plausible.
- **Hidden downside:** the second-order consequence.
- **Stronger alternative:** where one exists.

Severity: **critical** (cannot deploy as written) · **material** (deployable, meaningfully weakened,
revise) · **minor** (worth noting, not blocking) · **watch** (not a flaw today, a pattern that could
become one).

Two disciplines carried over, both load-bearing:

**Never manufacture findings.** When a mission is genuinely sound, say so. An audit that produces
findings to justify itself destroys its own signal, and a reviewer who always finds something teaches
everyone to discount them.

**Specific beats generic.** "This could be misread" is not a finding. Name the misreading, name who
acts on it, name what happens.

---

## Limits of this procedure

Stated plainly, in keeping with the rest of this repository.

**It catches structure, not intent.** A sophisticated actor who reads this document can write a
mission that passes all seven probes and still deploy extractively by naming a conflict and then
resolving it in practice against the stated priority. **The probes test the document. Only behavior
tests the organization.** Pair this with observation.

**It has not been validated.** No corpus of known-washed missions has been run through it to measure
detection or false-positive rates. The probes are derived from reasoning about the failure mode, not
from measurement. See [`evaluation.md`](evaluation.md).

**It may over-flag missions written by people who are simply new to this.** A first-draft mission
often fails probes 1, 3, and 6 through inexperience rather than intent. The procedure cannot
distinguish those, and it should not be used to impute bad faith. It identifies documents that would
*permit* extraction, not authors who intend it.

**Probe 6 has a known evasion.** An organization can name a forbidden action that is commercially
attractive in theory and irrelevant in practice. The follow-up: *when did you last decline something
because of this, and what did it cost?* A mission with no history of costing anything has not yet
been tested.

---

## If you are auditing your own

You are in the weakest position, and knowing that is most of the remedy.

1. **Write the findings before deciding what to do about them.** The strong temptation is to resolve
   a finding by reinterpreting the mission. Record the finding first; it is much harder to argue away
   in writing.
2. **Answer probe 6 in one sentence, out loud, before anything else.** *"This mission forbids us from
   ______, which we would otherwise want to do because ______."* Difficulty completing that sentence
   is the finding.
3. **Have someone outside read only the mission and answer probe 1:** where do interests diverge?
   If they name a conflict you did not, you have located your own blind spot.

The framework names constitutional washing as its primary vulnerability. Auditing your own mission
honestly is the smallest available version of taking that seriously.
