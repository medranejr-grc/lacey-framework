# Scope — what this release is, and what it is not

This repository publishes the **whole current conceptual stack of the Lacey Framework**, but not as
a flat stack of equal contributions or a complete implementation. Its center is constitutional
governance: the mission, people served, betrayals, judgment, and human relationships that define
what an agent is for. The framework then follows that identity downward through authorization,
runtime enforcement, and audit evidence.

The order matters. Technical gates can decide whether an action is permitted without deciding
whether the action serves the mission. Constitutional language cannot make those gates unnecessary.
The framework therefore says: begin with purpose, then carry that purpose into enforceable scope and
inspectable evidence.

The parts are also not at the same stage. Constitutional artifacts have been written and used. The
execution layer is a proposed technical specification that has not been implemented or validated.

Two maps below. They measure different things and are easy to confuse: the **layer map** says
*where* governance sits in the stack. The **carrier model** says *how* a constitutional instruction
travels from a written document to a running agent.

---

## 1. The layer map — where governance sits

| Layer | Governs | Who controls it |
|---|---|---|
| **sub zero** | The model and platform substrate: system instruction hierarchy, refusal behavior, vendor tool policy, and hidden runtime constraints. | The model provider. Not you. |
| **layer zero** | Mission, constitutional identity, and the approved fixed identity manifest. *What the agent is and is authorized to be.* | The deploying organization and accountable humans. Constitutional artifacts are developed here; the signed manifest is proposed. |
| **layer one** | Session identity, tools, permissions, workflows, credential brokering, and runtime policy enforcement. | The deploying organization through infrastructure. Proposed here, not built. |
| **layer two** | Integrity-protected evidence, artifacts, logs, outputs, deployments, and human assessment of outcomes. | The deploying organization through instrumentation and review. Proposed here, not built. |

**Sub zero is a hard ceiling and this framework does not pretend otherwise.** A user-authored
constitutional document cannot override a model's system instructions, a platform's safety
hierarchy, or a vendor's tool policy. Everything here operates *inside* limits set by someone else.
Naming that dependency is not a weakness in the framework; a framework that failed to name it would
be the weaker one.

## 2. The carrier model — how instruction propagates

Five carriers, each a **testable claim** about how constitutional governance reaches an agent's
runtime. Stated as claims on purpose: a claim can be shown false, and the status column says which
ones have been exposed to real conditions.

| # | Carrier | The claim | Status |
|---|---|---|---|
| **1** | **Project / system instructions** | A master constitutional document loaded at the session level supplies persistent mission context across conversations in that project. | **Artifact deployed; behavior informally observed.** One live companion deployment; no controlled comparison. |
| **2** | **Per-agent constitutional document** | A role-specific document loaded alongside the master supplies specialized context with its own calling, mission consequences, and watchman statement. | **Artifacts deployed; behavior informally observed.** Nine private role documents used over sustained work; no controlled comparison. |
| **3** | **Shared germinal idea** | An identical kernel propagated across per-agent documents gives the team a common mission reference while local responsibilities differ. | **Artifact deployed; coherence informally observed.** No systematic record or controlled comparison. |
| **4** | **Repository constitutional file** | A constitutional file at a repository root supplies persistent mission context to coding agents working in that codebase. | **Artifacts deployed; behavior informally observed.** Multiple codebases. Diamond Intelligence separately documents a human owner's mission-consistent shutdown decision. |
| **5** | **Signed manifest + runtime enforcement** | A cryptographically signed identity manifest, correctly bound to a mediated workload and evidence path, could make approved identity and observed actions mechanically inspectable. | **Published as a proposed architecture; not built or validated.** See [`docs/execution-layer.md`](docs/execution-layer.md). |

### This release provides working structural guidance for Carriers 1–4 and a public proposal for Carrier 5.

Complete public worked examples cover Carriers 2–4. The public Carrier 1 example is intentionally
partial; a complete companion deployment remains private.

Carriers 1–4 are **text artifacts**: documents you write, place, and load. Carrier 5 is
**infrastructure**: signing, workload and session identity, policy enforcement, credential
mediation, and evidence. Its current design is published in
[`docs/execution-layer.md`](docs/execution-layer.md), along with the assumptions and gaps that keep
it from being called an implementation or standard.

### A carrier is not the constitution

The authoritative user-authored artifact should remain vendor-neutral. A filename such as
`AGENTS.md`, `CLAUDE.md`, or a platform's Project Instructions is an **entry point** that carries the
approved constitution into that environment. A per-agent document is a **role extension**. A task
brief is bounded direction for one run. Neither the entry point, role, nor task should silently
become a competing source of mission.

The practical hierarchy, platform-specific entry points, copyable adapters, and loading checks are
in [`docs/implementation-guide.md`](docs/implementation-guide.md).

> **A revision to the original model, stated openly.** The source architecture grouped Carriers 1–3
> as "constitutional" and 4–5 as "technical." That split tracked *what had been built or deployed*
> in early 2026, not what kind of thing each carrier is. Carrier 4 has since been deployed, and it is a text
> artifact like 1–3, not infrastructure like 5. The meaningful line is **text versus
> infrastructure**, and it falls between 4 and 5.

---

## What this framework does not do

Read this before adopting anything here.

- **It does not enforce anything.** Every artifact in this repository is unsigned text. It can be
  edited, overridden, truncated, or ignored. It does not survive a system-prompt replacement, a
  fine-tune, or a successful injection. Carrier 5 proposes artifact integrity and runtime
  enforcement, but it is not built and its protection against replacement, injection, or
  fine-tuning has not been established.
- **It does not replace the security baseline.** Runtime enforcement, least privilege, input
  validation, CI/CD controls, dependency scanning, and human review are all necessary and none are replaced. The
  claim is that they are *insufficient alone*, not that they are optional.
- **It does not guarantee alignment.** It changes the governance layer at which the question is
  asked and attempts to make harmful action incoherent with the stated mission. Whether that changes
  behavior, or by how much, has not been measured.
- **It is not a prompt style guide.** The structure carries real architecture: identity, shared
  kernel, propagation, audit. Reducing it to formatting advice loses the part that does the work.
- **It is not measured.** The carrier statuses above record deployment and informal observation,
  not controlled evaluation. `docs/evaluation.md` provides a design outline, not a runnable study.

## What it does do

It is designed to give an agent a coherent answer to *what am I for* when the instructions run out,
in the novel case, under adversarial pressure, and in moments no rule anticipated. The written
mission defines harmful action as **incoherent with success** rather than merely prohibited. Whether
the agent follows that framing more reliably than rules alone is the central untested hypothesis.

Whether that is worth the context it occupies is a fair question, and
[`docs/context-engineering.md`](docs/context-engineering.md) answers it directly.
