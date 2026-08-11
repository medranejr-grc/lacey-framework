# Principles

Five principles, then the rules for representing them honestly. The second list matters as much as
the first. A framework about integrity that overstates itself has already failed its own test.

These principles are the center of the Lacey Framework. The proposed execution architecture is
intended to carry an approved identity into authorization, enforcement, and evidence. It supports
the constitutional thesis; it does not replace or redefine it.

---

## The five principles

**1. Mission Primacy**
Deployment begins with mission design as well as risk assessment. *What is this system for? What human
need does it serve? What would betrayal of that mission look like?* The answers are the primary
governance artifact, ahead of the technical specification and the risk register.

**2. Structural Incompatibility**
The mission defines success so that harmful outcomes are not merely prohibited but **structurally
incompatible with what counts as winning**. A proxy metric cannot convert harm to the people served
into mission success. This is not proof of safe behavior; it is a more demanding objective design.

**3. Contextual Richness**
Agents are given the fullest possible understanding of their purpose, their users, their impact, and
their place in the system they serve. Not just what to do, but who they are and why it matters. Richer
relevant context is intended to support judgment in situations no rule anticipated; the comparative
effect remains unmeasured.

**4. Human Values as Infrastructure**
Ethical principles are woven into the narrative of what the agent is trying to become, not listed as
rules alone. The instruction names who matters, what is owed to them, and what betrayal looks like,
giving the model relevant context when a finite rulebook is silent. Whether that context improves
behavior is testable; it should not be described as installing human conscience or character.

**5. Trust as the Primary Metric**
Not compliance alone. Not constraint adherence alone. Not audit pass rate alone. Trust from users,
operators, and society is an outcome to monitor alongside safety, behavior, compliance, and
mission-specific results. Perceived trust is gameable; discovering that it was manipulated is itself
evidence of mission failure.

---

## Representing this framework honestly

These are constraints on *advocacy*, and they apply to anyone using, teaching, extending, or selling
work based on this framework.

**Do not present it as replacing the security baseline.** Runtime enforcement, least privilege,
input validation, CI/CD controls, dependency scanning, and human review are all necessary and none
are replaced. The claim is that they are insufficient alone.

**Do not reduce it to a prompt-writing style guide.** The structure carries architecture: identity,
a shared kernel, propagation across agents, provenance, audit. Formatting advice is what is left
after the load-bearing parts are removed.

**Do not claim it guarantees alignment.** It changes the layer at which governance is expressed and
provides a richer artifact for audit and evaluation. It is intended to make harmful action
incoherent with the mission, but no controlled study has established a behavioral effect or effect
size.

**Do not let the intellectual lineage become vague branding.** The framework draws on a long
tradition of thinking about internalized governance versus external law. That lineage is real and it
must be argued precisely. Invoked as atmosphere rather than argument, it becomes exactly the
unfalsifiable mysticism critics expect.

**Do not let claims outrun build state.** Distinguish at all times between what is *proposed*, what
is *documented*, and what is *built and observed*. [`SCOPE.md`](SCOPE.md) marks this per carrier;
keep it accurate as it changes.

**Do not let adoption outrank trust.** Stars, citations, downloads, and impressive demonstrations
are not evidence the framework works. If it is being adopted faster than it is being validated, say
so plainly rather than letting the adoption stand in as proof.

---

## Claim language

A house style, used on this project since early 2026 and retained for the public release.

**Prefer:** "our current thesis is…" · "in an internal run…" · "the early pattern we are seeing…" ·
"we are building toward…" · "this is not yet the full execution layer…"

**Avoid:** "breakthrough" · "revolutionary" · "production-grade" · "compliant" · "certified" ·
"autonomous" · "first ever," unless narrowly scoped and independently verifiable.

The test for any claim: *would this survive a reader who checked it?* If the honest answer is that
it survives only a reader who does not check, it is not ready to publish.
