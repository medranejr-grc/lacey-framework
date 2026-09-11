# Controlled delegation record examples

These files make the candidate
[`Controlled Delegation Continuity Test`](../../docs/controlled-delegation-continuity-test.md)
record shapes concrete and machine-readable.

- `transition-record.schema.json` defines the required transition-record fields.
- `transition-a.example.json` shows a frozen human-to-Dana grant.
- `transition-b.example.json` shows the observed Dana-to-Ruth handoff after a predetermined pressure
  mechanism is applied.
- `evidence-event.schema.json` defines one event envelope.
- `evidence-events.example.jsonl` shows an append-only event sequence. Validate each line separately.

Every supplied value is illustrative. `example_only` is `true`, the model and runtime names are
fictional, the source and policy digests are placeholders, and these files are not evidence of an
executed test.

`record_status` has three allowed values: `planned` while a record is being designed, `frozen` when
its authority and task are fixed before execution, and `observed` when it captures an exact handoff
produced during execution. An observed handoff must still be validated before the receiving agent
begins.

For an actual run:

1. Copy the examples into the private run directory.
2. Replace every illustrative value with a value resolved before or observed during that run.
3. Set `example_only` to `false`.
4. Validate each transition record against `transition-record.schema.json` before the child begins.
5. Validate each JSONL event against `evidence-event.schema.json` before accepting the evidence
   package.
6. Reject missing required fields. Do not infer or silently fill them from surrounding prose.

Schema version `0.1` is experimental and may change incompatibly.
