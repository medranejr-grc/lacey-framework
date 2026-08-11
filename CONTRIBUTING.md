# Contributing

The Lacey Framework is being published for use, criticism, testing, and repair. Agreement is welcome;
evidence that the framework fails is more useful.

This repository is maintained with limited capacity. Contributions are reviewed in batches, no
response time is promised, and an issue may be closed when it falls outside the framework's finite
scope. That is a maintenance boundary, not a judgment about the contributor or the idea.

## Choose the right path

- **Challenge a claim** when a statement outruns its evidence, hides a counterexample, or should be
  narrowed.
- **Report a field result** when you used a constitutional artifact and can describe what happened,
  including neutral or negative results. Flow-down tests using an existing runtime, authorization
  engine, policy gateway, evaluation system, or audit-evidence stack are especially useful.
- **Identify a framework gap** when the current architecture does not address a real governance
  problem. This includes missing manifest fields, weak trust assumptions, bypass paths, delegation
  failures, privacy risks, and existing standards that make part of the proposed execution layer
  unnecessary.
- **Open a pull request** for a concrete correction, clearer explanation, improved template, or
  well-bounded example.

Use the repository's issue forms. For a substantial change, open an issue before investing in a pull
request so scope can be tested early.

## What makes a useful contribution

A strong contribution separates:

- what was observed from what is inferred;
- a human decision from agent behavior;
- a deployed artifact from a controlled evaluation;
- the historical record from a proposed repair; and
- mission-layer governance from runtime enforcement.

Include enough context to inspect the claim, but remove credentials, private prompts, employer or
client information, personal data, and details about people who did not consent to publication.

AI-assisted contributions are welcome. The contributor remains responsible for every claim and
source. Name the model or tool when it is material to reproducing the result.

## Review standard

Maintainers evaluate a contribution by asking:

1. Does it make the framework easier to inspect, use, falsify, or repair?
2. Does the evidence support the language used?
3. Does it protect people and non-public information?
4. Does it preserve the distinction between mission, permissions, enforcement, and evaluation?
5. Can the repository accept it without creating an open-ended product or support commitment?

For execution-layer proposals, also state the threat model and trust assumptions, distinguish a
design from an implementation, and name what evidence would falsify the claim.

For a flow-down test, identify where the constitutional artifact entered the system, how its mission
and authorization were translated, which actions were mediated, what evidence was collected, and
where meaning or control was lost. Do not submit private prompts, credentials, or protected logs.

A contribution may be accepted, revised, deferred, or declined. Material disagreements should stay
visible in the issue or pull-request record.

## Pull requests

Keep each pull request focused. Explain the problem, the evidence, the change, and any known limit.
Update links or adjacent claims when your change makes them inaccurate. Do not include private source
files or generated extracts from material you do not have the right to publish.

By contributing, you agree that your contribution will be released under the license applying to its
destination path, as described in [`LICENSE.md`](LICENSE.md), and that you have the right to submit it.

## Scope and authority

The repository owner retains final decisions about mission, authorship, personal disclosure, release
scope, and merging. Acceptance does not certify a contribution as correct, and closure does not make
an idea invalid. The public record should show the reasoning either way.
