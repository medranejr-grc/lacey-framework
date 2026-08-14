# [Project name] — runtime entry point

## Approved Operating Card

[Constitution version, approval date, or digest]

[Insert the approved Operating Card from the canonical project constitution.]

## Required load order

Resolve and load these artifacts for every run:

1. the platform's non-user-controlled system instructions;
2. the approved canonical project constitution and its version or digest;
3. exactly one role constitution, when the deployment uses roles;
4. the bounded task brief; and
5. the authorized tools and data for the task.

The project constitution is authoritative among user-authored artifacts. A role or task may narrow
authority but must not silently broaden or replace it.

Record the resolved artifact identifiers, model and runtime details where exposed, task, output or
attempted action, and human disposition. Fail closed or escalate when a required artifact cannot be
resolved according to the deployment's threat model.

[Translate these requirements into the actual configuration or loader used by the runtime. This
Markdown file alone does not load or enforce anything.]
