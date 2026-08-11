# Runbook: Constitutional Multi-Agent Release Review

This pack is platform-neutral. It can be implemented with separate agent sessions, subprocesses, or
repeated isolated review passes. Role separation is the variable the proposed comparison would
examine; model and platform remain recorded execution variables.

## Files

- `shared-kernel.md`: identical mission and human-authority boundary for every role.
- `dana.md`, `ruth.md`, `elena.md`: role extensions loaded one at a time after the kernel.
- `finding-record.md`: required record for blocker and material findings.
- `manifest.sha256`: integrity check for the shared kernel and role files.

## Precedence

| Order | Artifact | May vary by role? | Validation |
|---|---|---:|---|
| 1 | Platform and system instructions | Outside this pack | Confirm the platform permits the task. |
| 2 | Human owner's task and decision | Yes, by task | Record publication and waiver decisions. |
| 3 | `shared-kernel.md` | No | Verify its hash against `manifest.sha256`. |
| 4 | One role extension | Yes | Load exactly one role file per agent or isolated pass. |
| 5 | Task-specific review brief | Yes | Keep it bounded to named artifacts and questions. |

A lower row cannot broaden authority granted by a higher row. In particular, a role extension may
narrow but cannot override the shared human-authority boundary.

## Setup

1. Verify the files using a SHA-256 tool available on your system. A changed kernel is a new version,
   not the same experiment.
2. Give every participating role the same `shared-kernel.md`.
3. Give each participant exactly one role extension.
4. Keep initial review runs separate: do not show one reviewer's findings to another before both
   initial reviews are complete. Separate runs are not institutionally independent and may share
   model or platform blind spots.
5. Record the model, version if exposed, and reasoning setting used for each run. These are execution
   variables, not constitutional content.

## Execution

1. The owner gives Dana a bounded release objective and identifies decisions reserved to the owner.
2. Dana drafts or integrates the artifact and identifies review questions.
3. Ruth and Elena each receive the same artifact plus separate role-appropriate briefs.
4. Each reviewer returns blocker and material findings using `finding-record.md`. They may return no
   findings.
5. Dana assigns every material finding a disposition: accepted, rejected, escalated, or deferred.
6. Dana applies accepted repairs. A different pass by the originating role rechecks every blocker
   that caused a substantial change.
7. The owner decides any unresolved blocker, personal-disclosure boundary, authorship change, or
   publication action.
8. Retain the findings and dispositions with the release work. Do not claim documented review if
   those records are unavailable; describe separate runs accurately.

## Minimal review briefs

**Ruth:** "Find unsupported claims, evidentiary mismatches, hidden incentives, and the strongest
counterargument. Return only material findings using the finding record. Do not invent a finding."

**Elena:** "Find privacy, third-party, credential, licensing, legal-boundary, and reputation risks.
Return only material findings using the finding record. Do not treat this as legal advice."

## What to compare

To test the architecture rather than merely use it, run the same release task under at least two
conditions: this separated-role pack and one general-purpose agent performing sequential review
passes. Hold the task, sources, tools, model settings, and context budget constant; use repeated runs
and a predefined rubric scored without showing raters which condition produced each output. Possible
measures include unsupported claims found, valid findings accepted, reviewer overlap, false
positives, time, and token cost.

The historical private deployment documents related role-separated review passes. This public pack
has not yet been run, and no comparison has been performed.
