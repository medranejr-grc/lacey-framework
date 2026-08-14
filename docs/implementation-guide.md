# Implementing the Lacey Framework

Status: practical guidance for placing and loading the text artifacts described as Carriers 1–4.
These patterns are not runtime enforcement or evidence that the model followed the constitution.

This guide answers the question the conceptual architecture does not answer by itself:

> I use a particular agent platform. Which artifacts do I create, where do I put them, and what
> should be loaded in what order?

The short answer is: keep one vendor-neutral constitution as the authoritative source, then connect
it to each platform through that platform's entry point. A filename such as `CLAUDE.md` or
`AGENTS.md` is a carrier. It should not become the source of the mission merely because one product
recognizes it.

## The four artifacts

| Artifact | Purpose | Suggested name | Changes when |
|---|---|---|---|
| **Project constitution** | Defines the mission, people served, betrayals, human authority, and shared reasoning posture. | `PROJECT_CONSTITUTION.md` | The accountable human approves a material constitutional change. |
| **Platform entry point** | Makes the constitution discoverable in a particular agent environment. | `AGENTS.md`, `CLAUDE.md`, Project Instructions, or runtime configuration | The platform or loading mechanism changes. |
| **Role constitution** | Narrows the shared mission into one agent's calling, watchman statement, authority, and escalation path. | `agents/<role>.md` | That role's durable responsibility changes. |
| **Task brief** | Gives one bounded objective, inputs, constraints, deliverable, and decisions reserved to the human owner. | A prompt, issue, job record, or run artifact | Every task or run. |

The project constitution is authoritative among the user-authored artifacts. A role may narrow it but
must not silently broaden or replace it. A task may narrow the role for one run but must not rewrite
the role or mission. Platform and system instructions remain above all user-authored artifacts and
are a ceiling the framework does not control.

```text
Accountable human approval
          |
          v
PROJECT_CONSTITUTION.md       <- canonical mission and authority
          |
          v
Platform entry point          <- AGENTS.md, CLAUDE.md, Project Instructions, or runtime loader
          |
          v
One role constitution         <- optional for a single-agent deployment
          |
          v
Bounded task brief
          |
          v
Output, action, evidence, and human review
```

## Minimum single-agent setup

1. Copy [`templates/constitutional-document-skeleton.md`](../templates/constitutional-document-skeleton.md)
   into your project as `PROJECT_CONSTITUTION.md`.
2. Complete the Operating Card and the six constitutional parts. Name the accountable human owner,
   intended beneficiaries, mission, betrayal conditions, escalation path, and map-runs-out behavior.
3. Run the [`mission-integrity audit`](mission-integrity.md). A polished mission that encodes
   extraction or institutional self-interest is not ready to deploy.
4. Choose the platform entry point below. Put the Operating Card in that entry point and direct the
   agent to read the complete constitution before substantive work. Record the constitution's
   version, date, or digest in the entry point and update the card when the constitution changes.
5. Start a clean session. Ask the agent to identify the authoritative constitution, the human owner,
   the people served, one named betrayal, and the escalation rule. This is a loading check, not proof
   of behavioral effect.
6. Give the agent one bounded task. Preserve the task, output, model and platform details, human
   review, and any observed divergence.

A single-agent deployment does not need Dana, Elena, or a multi-agent hierarchy. Those are worked
roles from one deployment, not mandatory framework components.

## Platform entry points

Platform behavior changes. Confirm current loading behavior in the platform's documentation and
record the version or date used for a test.

| Environment | Entry point | Minimum setup |
|---|---|---|
| **Codex in a repository or local project** | Root `AGENTS.md` | Put the approved Operating Card in `AGENTS.md`; instruct Codex to read `PROJECT_CONSTITUTION.md` before substantive work. Codex documents `AGENTS.md` as its repository guidance file and loads a hierarchy of such files. See the [official Codex guidance](https://learn.chatgpt.com/docs/agent-configuration/agents-md). |
| **Claude Code** | Root `CLAUDE.md` or `.claude/CLAUDE.md` | Import `PROJECT_CONSTITUTION.md` from `CLAUDE.md`, then add only Claude-specific project instructions. Claude Code documents `CLAUDE.md` and `@path` imports. See the [official Claude Code guidance](https://code.claude.com/docs/en/memory). |
| **ChatGPT Project** | Project Instructions plus an uploaded or connected source | Put the approved Operating Card and load-order instruction in Project Instructions; add `PROJECT_CONSTITUTION.md` as a project source. Project instructions apply across the project's chats. See the [official ChatGPT Projects guidance](https://learn.chatgpt.com/docs/projects). |
| **API or custom runtime** | System/developer context or an explicit configuration loader | Load the canonical constitution for every run, then append exactly one role constitution and the current task. Record the resolved artifacts and their versions with the run. |
| **Another agent platform** | Its documented persistent-instruction mechanism | Preserve the hierarchy rather than copying a vendor filename blindly. Verify that the intended files actually enter the effective context. |

Copyable starting points are in
[`templates/platform-entry-points/`](../templates/platform-entry-points/). They are intentionally
small. The canonical constitution belongs in `PROJECT_CONSTITUTION.md`, not in several drifting
vendor-specific copies.

## Single-agent repository layout

```text
your-project/
|-- PROJECT_CONSTITUTION.md
|-- AGENTS.md                    # if Codex is used
|-- CLAUDE.md                    # if Claude Code is used
|-- evidence/
|   `-- runs/
`-- project files...
```

Keep both entry-point files when the repository is used across platforms. They should point to the
same constitution. Do not maintain separate Codex and Claude missions.

## Multi-agent repository layout

```text
your-project/
|-- PROJECT_CONSTITUTION.md
|-- AGENTS.md or CLAUDE.md
|-- agents/
|   |-- coordinator.md
|   |-- risk-reviewer.md
|   `-- specialist.md
|-- tasks/
|   `-- task-001.md
`-- evidence/
    `-- task-001/
```

For each run, load:

1. the platform and system instructions;
2. the approved project constitution or shared kernel;
3. exactly one role constitution;
4. the bounded task brief; and
5. only the tools and data authorized for that task.

There are two valid packaging patterns:

- **Separated kernel, preferred for maintenance:** keep one canonical shared kernel and load it before
  each role. Role files contain only role-specific extensions.
- **Embedded kernel, useful for standalone agents:** generate each role document with a byte-identical
  copy of the approved kernel. Record a version or digest so copies cannot drift unnoticed.

Do not hand-edit multiple embedded kernels independently. The public
[`multi-agent release-team pack`](../examples/multi-agent-release-team/) demonstrates the separated
pattern.

## Verify the installation before evaluating behavior

Three different questions require three different checks.

### 1. Did the platform load the intended artifacts?

Record:

- platform and model identifier, where exposed;
- entry-point filename or Project Instructions version;
- constitution and role versions or digests;
- the working directory, project, or runtime configuration used; and
- the agent's identification of the mission, owner, betrayal, and escalation rule.

An accurate restatement is evidence that the text was available in that moment. It is not evidence
that the system will follow it under pressure.

### 2. Did the constitution change a decision?

Use a task with a real ambiguity or optimization pressure. Preserve the task, output or action,
review criterion, and human judgment. When possible, compare against a predefined baseline while
holding the model, tools, task, and context budget constant. See [`evaluation.md`](evaluation.md).

### 3. Did meaning survive delegation?

For every handoff, record:

- the originating mission and relevant betrayal condition;
- the authority and task received by the delegating agent;
- the exact downstream instruction and authority granted;
- the downstream output or attempted action;
- the evidence used to judge mission continuity; and
- whether the result was accepted, repaired, escalated, or rejected.

A chain of locally permitted steps can still lose the originating mission. A delegation test should
therefore inspect transitions, not only the final output.

Use the copyable [`implementation and flow-down record`](../templates/implementation-test-record.md)
to preserve the installation, loading check, delegation transitions, evidence, human disposition,
provenance, and limitations without representing a field observation as a controlled evaluation.

## What successful installation does not prove

- A recognized filename does not prove that the full artifact entered context.
- A correct summary does not prove mission-consistent behavior.
- Identical kernels do not prove identical interpretation.
- Role separation does not prove independent judgment.
- Text instructions do not enforce tool permissions or prevent prompt replacement.
- Logs do not prove completeness when instrumentation can be bypassed.

Treat installation, behavioral evaluation, runtime enforcement, and audit evidence as separate
claims. Report positive, neutral, and negative results through the repository's structured issue
forms.
