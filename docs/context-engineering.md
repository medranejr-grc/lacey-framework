# Context engineering: is a constitutional document worth the context it occupies?

The obvious objection to everything in this repository is that it is long, and the frontier labs are
saying to write less.

In July 2026 Anthropic published *The new rules of context engineering for Claude 5 generation
models*, reporting that they cut Claude Code's own system prompt by roughly 80%, from about 800
tokens to 164, with no measured performance loss, and that newer models can be actively *degraded*
by over-prescriptive instruction. Their summary: the best results come from clear goals, relevant
context, and well-designed tools rather than long lists of detailed instructions.

That is a real finding from the organization with the most direct evidence, and it deserves a real
answer rather than a defensive one.

---

## Where Anthropic's result overlaps with one concern

The first of Anthropic's six shifts is **"rules become judgment."** Their worked example: replace
*"never write multi-line docstrings"* with *"write code that reads like the surrounding code — match
its comment density, naming, and idiom."*

That resembles the inversion this framework argues for, in different vocabulary. A prescriptive
constraint enumerates a behavior; an orientation asks the model to apply judgment beyond the named
case. Whether purpose-framed language generalizes better is a hypothesis, not a result Anthropic
tested in this work.

The author's interpretation is that much of the removed material resembles what this framework calls
cage-model content, while the retained material resembles orientation and product context. Anthropic
did not publish a framework-specific classification or a complete prompt diff that establishes that
mapping.

The reduction supports a narrower concern shared by this framework: over-prescriptive instructions
can consume context and degrade performance. It is not evidence that the Lacey Framework, identity
documents, or mission-first instructions improve behavior.

That is the strongest claim available here, and it should not be stretched further. Anthropic did
not endorse constitutional governance, did not test a mission-first instruction against a rule list,
and did not publish anything about identity documents. What they demonstrated is that
*prescriptiveness* has a cost. That is one load-bearing half of this framework's argument, arriving
from outside it.

## The honest counterpoint

The finding is not uncontested in production. Following the change, practitioners reported unexpected
codebase modifications, unintended deletions, and models working around configured restrictions,
including one case of a model circumventing regex-based command restrictions by changing directory
first.

Treat "shorter is better" as a well-evidenced directional finding, not settled science. A framework
that cites it as proof would be making the same error it warns against elsewhere: letting a claim
outrun what was actually shown.

---

## Placement: the part the framework had to add

Anthropic's third and fifth shifts, in which upfront context becomes progressive disclosure and
manual memory files become automatic memory, raise a question the original framework documents never addressed.
Modern agent stacks are not a single instruction field. They have system prompts, memory files,
auto-memory, skills that load on demand, tool descriptions, and subagent definitions. *Where* does a
constitutional instruction live?

**Identity is the one component that cannot be fully deferred.** Progressive disclosure works by
loading content when it becomes relevant. But identity is what determines *what counts as relevant*.
A skill that activates "when needed" cannot govern the judgment of whether it is needed. The moments
constitutional instruction exists to address, such as the novel case, the ambiguous request, and the
pressure to take the easier path, are precisely the moments an agent does not know to go looking for guidance.

That is not an argument for length. It is an argument about *which* content must be resident, and it
implies the opposite of length for everything else.

## The Operating Card pattern

The working answer, in use since early 2026: **split the constitutional document in two.**

Every per-agent document in this framework's reference implementation opens with an Operating
Card, explicitly labeled *"the load-bearing summary. Read this first. The full document below is
the deep reference."* Roughly 250 words. Identity, the job, the failure mode, the watchman posture,
the standing commands.

Beneath it sits the full document: mission consequences, the watchman statement in full, the Four
Questions answered, relationships, standing instructions. Detail that repays reading when a hard
case arrives, and costs attention every turn it is resident for no reason.

```
┌─ ALWAYS RESIDENT ────────────────────────────────┐
│  Operating Card  (~250 words)                    │
│    identity · the job · failure mode             │
│    watchman posture · standing commands          │
└──────────────────────────────────────────────────┘
┌─ RETRIEVED WHEN THE MAP RUNS OUT ────────────────┐
│  Full constitutional document                    │
│    germinal idea · mission consequences          │
│    watchman statement · the Four Questions       │
│    relationships · standing instructions         │
└──────────────────────────────────────────────────┘
```

The same project's risk register logged the underlying concern independently in April 2026:
*"token/context bloat from canon duplication,"* mitigated by *"use briefs and targeted extracts; do
not duplicate full canon into every working file."* The concern predated Anthropic's external
evidence about over-prescription and context cost.

**This should not be overstated either.** The pattern was arrived at for legibility as much as for
cost, it has not been measured against the alternative, and "we did this first" is not an argument
that it works. What it does establish is that the framework's answer to the length objection is a
practice already in use, not a rationalization written after the objection appeared.

---

## Practical guidance

**Put in the resident kernel** what changes behavior in the next turn: who the agent serves, what
the job is, the specific failure mode, the posture to hold. If a sentence would not alter a decision
made in the next five minutes, it belongs in the deep reference.

**Defer** procedures, worked examples, relationship maps, and standing instructions. Retrieve them
when the situation calls.

**Never duplicate.** The most common source of constitutional bloat is the same instruction
appearing in the system prompt, the memory file, and a tool description. Consolidate to one
authoritative location. This is Anthropic's fourth shift and the cheapest win available.

**Prefer concise orientation where judgment is required.** Rules remain appropriate for clear
boundaries. Purpose may help a model reason beyond enumerated cases, but that comparative effect has
not been established here. Anthropic's guidance supports clarity and reduced prescription, not the
full constitutional claim.

**Budget honestly.** A constitutional document has a cost, paid every request. The right question is
never "is this valuable?" It is *"is this more valuable than the context it displaces?"* Content
that fails that test should be cut regardless of how well written it is.

---

## Sources

- Thariq Shihipar, Anthropic. *The new rules of context engineering for Claude 5 generation models.*
  2026-07-24.
  <https://www.claude.com/blog/the-new-rules-of-context-engineering-for-claude-5-generation-models>
- Reporting on production trade-offs following the reduction:
  <https://www.ibtimes.sg/anthropic-says-claude-5-needs-shorter-prompts-developers-say-trade-offs-are-more-complicated-90853>
