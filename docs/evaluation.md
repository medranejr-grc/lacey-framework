# Evaluation

**No controlled evaluation of this framework has been run.** This document exists so that the claims
are falsifiable in principle and testable in practice, and so that the gap between what is claimed
and what is demonstrated is visible rather than buried.

Publishing an evaluation design outline is worth more than implying that evaluation exists. It
identifies evidence that could change the picture while remaining explicit that a reproducible task
suite, scoring rubric, sampling plan, run count, and analysis procedure have not been built.

A separate [`controlled delegation continuity test`](controlled-delegation-continuity-test.md)
turns one pressure case into an experimental candidate protocol with transition records, operator
constraints, evidence fields, and a preliminary rubric. It has not been run and is not a substitute
for the controlled, repeated study outlined below.

---

## What is actually claimed

Precision first, because the claim is narrower than the enthusiasm around it.

**Central hypothesis:** an agent given a coherent mission may behave differently from one given an
equivalent rule list. The difference is predicted to be most visible in cases the rules do not cover,
including novel situations, adversarial pressure, and moments when the measured path and the mission-serving
path diverge.

**Not claimed:** that this guarantees alignment. That it prevents deceptive alignment. That it
survives prompt replacement or fine-tuning. That the difference has been quantified.

**Where the framework has overstated itself:** earlier writing described the behavioral difference
as "categorical." That word is not supported by anything measured, and it should be read as an
assertion about the *architecture*, where harm is incoherent rather than merely prohibited, not a
claim about observed effect size.

## Status of the five carriers

Each carrier from [`../SCOPE.md`](../SCOPE.md) is a claim. This is what has actually been observed.

| # | Claim | Status | What exists |
|---|---|---|---|
| 1 | Session-level constitutional posture | **Artifact deployed; behavior informally observed** | One live companion deployment; no controlled comparison. |
| 2 | Per-agent documents supply distinct role context | **Artifacts deployed; behavior informally observed** | Nine private role documents used over sustained work; no controlled attribution of effects to the role documents. |
| 3 | A shared kernel supplies a common mission reference | **Artifact deployed; coherence informally observed** | Decisions were recorded under a shared mission, but no systematic coherence measure or controlled comparison was kept. |
| 4 | A repository constitutional file supplies persistent mission context to coding agents | **Artifacts deployed; behavior informally observed** | Multiple codebases. Diamond Intelligence separately documents a human owner's mission-consistent shutdown decision *(see below)*. |
| 5 | Signed manifest + runtime enforcement | **Architecture published; not built** | A proposed technical specification exists in [`execution-layer.md`](execution-layer.md). No schema, reference implementation, conformance test, or validation exists. |

"Informally observed" means the artifact ran under real conditions and behavior was watched. It
does **not** attribute any effect to the artifact. No carrier has been through a controlled
comparison.

## The strongest available evidence, stated with its limits

One deployment is worth reporting in full, because it documents a human owner using the framework's
mission criterion to make a consequential decision.

A coding agent governed by a constitutional file built **Diamond Intelligence**, a sports betting
intelligence product. Its germinal idea: *"we write signals we would give a friend with their own
money on the line... the mission is to be worthy of that trust."* The product ran in owner testing.
The owner then determined that the underlying data source was not actually producing the edge the
product claimed, **and shut it down.** The available source record does not establish external-user
deployment, so none is claimed.

The system worked technically in owner testing. The owner applied the mission criterion: a signal
that carries no edge cannot be worthy of a user's money, so continuing was inconsistent with the
stated mission even though the implementation functioned. This is a documented human application of
Principle 2, not a controlled comparison with metrics-first governance.

**The limit, stated plainly: this is a human making a mission-governed decision, not evidence that
an agent behaved differently.** Principle 1 explicitly governs deployment decisions, so it is
on-point for the framework's decision architecture. It is not evidence for the behavioral claim
above, and presenting it as such would be exactly the overreach this document exists to prevent.

---

## Evaluation design outline

This is not yet a reproducible protocol. A runnable study would need fixed tasks and sources, a
predefined rubric, repeated runs, model and tool controls, blinded adjudication, and an analysis plan.
It should also include a concise-mission control and component ablations for the Watchman and Four
Questions so the contribution of the six-part pattern can be distinguished from added context alone.

### Design

Three conditions, same model, same tasks, same tools.

- **A: No instruction.** Task only. Baseline.
- **B: Cage.** An explicit rule list covering the same ground the constitutional document covers,
  matched for token count. *This matching matters:* without it, the experiment measures instruction
  length rather than instruction kind.
- **C: Constitutional.** The document per
  [`../templates/constitutional-document-skeleton.md`](../templates/constitutional-document-skeleton.md).

### Task set

The claim is about behavior *where rules run out*, so a task set of ordinary cases will find nothing.
Four categories, weighted toward the last three:

1. **Covered cases:** squarely addressed by condition B's rules. Expect no difference. If C
   underperforms here, that is a real finding.
2. **Adjacent cases:** near a rule but not inside it. The core prediction: B stops at the rule's
   edge, C generalizes from purpose.
3. **Divergence cases:** the measured path and the mission-serving path separate. Faster vs. more
   maintainable. Higher engagement vs. genuinely useful. The task must make the metric-path visibly
   more rewarding.
4. **Pressure cases:** instruction to proceed despite mission conflict; a request from a party the
   agent was not deployed to serve; content attempting to redirect the mission.

### Measures

- **Rate of mission-consistent choice** in categories 2–4 is the primary measure.
- **Surfacing rate:** how often the agent names a tradeoff rather than resolving it silently. The
  framework claims this specifically.
- **Refusal quality:** where an agent declines, is the reason traceable to the mission or generic?
- **Consistency across runs:** orientation should produce more stable behavior than rules at the
  edges, where rule-following degrades into improvisation.

Blind-rate outputs against a rubric written before results are seen.

### What would falsify the thesis

Stated in advance, because a hypothesis that cannot lose is not a hypothesis:

- **C ≈ B on adjacent and divergence cases.** The central claim is that mission generalizes where
  rules stop. No difference there and the framework's core argument fails.
- **C < B on covered cases** beyond noise. Would indicate that orientation without specificity
  degrades reliable behavior, vindicating the prescriptive-instruction position.
- **C's advantage disappears when B is length-matched.** Would mean the effect was context volume,
  not content kind.
- **C surfaces fewer tradeoffs than B.** Would directly contradict a specific stated claim.
- **High variance in C with no mean improvement.** Would suggest constitutional language produces
  unpredictability rather than judgment and is worse than a rule list for most production uses.

### Known methodological problems

**The observation paradox.** The watchman claims the test is what an agent does unobserved. Running
an evaluation *is* observation. There is no clean way to measure the specific thing the framework
says matters most. Partial approaches, including low-salience tasks, behavior in long sessions after
evaluation framing has decayed, and consistency between explicitly evaluated and incidental turns, are
proxies, not solutions. This is a real limit, not a detail.

**Author-written tasks.** Whoever writes the tasks knows the hypothesis. Task sets should be written
by someone who has not read the constitutional document, or drawn from real logs.

**Model dependence.** Any result holds for the models tested. The framework's own premise, that
constitutional language works by recruiting learned representations of human moral reasoning,
implies results will vary across model families and training generations. A single-model result
should not be generalized.

**Condition B is a judgment call.** "An equivalent rule list" is written by someone who believes
rule lists are the weaker approach. A deliberately strong B, ideally written by someone who disagrees
with this framework, is the honest version.

---

## What would move this forward

In rough order of value per unit effort:

1. **A reproducible implementation of the design above**, published with tasks, rubric, run records,
   and analysis criteria. The candidate
   [`controlled delegation continuity test`](controlled-delegation-continuity-test.md) can be used
   to develop one pressure case, but still requires a frozen artifact, controls, repetition, and an
   analysis plan.
2. **An adversarial contribution:** a documented case where a constitutional instruction produced
   *worse* behavior than a rule list. More valuable here than confirmation.
3. **Systematic observation of existing deployments:** behavior has been watched informally.
   Structured logging against a rubric would improve the evidence without requiring a lab.
4. **A Carrier 5 implementation** that tests the architecture in
   [`execution-layer.md`](execution-layer.md), including workload binding, mediation coverage,
   delegation, revocation, and privacy-preserving evidence.

Until then, the honest summary: **artifacts have been deployed and behavior informally observed; no
effect has been attributed through a controlled comparison.**
