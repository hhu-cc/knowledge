# Verification Patterns

Use these patterns to keep an AI workflow reliable.

## Pattern 1: Human review at high-consequence boundary

Apply when a mistake has material cost.
Place human review before external publication, irreversible action, or policy-sensitive output.

## Pattern 2: Sample-based audit

Apply when volume is high but full review is too expensive.
Review a defined sample and escalate if failure rate crosses a threshold.

## Pattern 3: Dual-pass generation and critique

Apply when drafts are useful but quality is uneven.
Generate first, then run a separate critique or checklist pass before approval.

## Pattern 4: Structured validation against source data

Apply when factual consistency matters.
Check the output against source material, required fields, or exact constraints.

## Pattern 5: Fallback to manual path

Apply when confidence is low or the model encounters unsupported edge cases.
Define the manual owner, expected turnaround, and handoff information.

## Pattern 6: Pilot metrics before scale

Apply before broad rollout.
Track at least:

- accuracy or acceptance rate
- cycle time
- review burden
- rework rate
- failure severity

## Reminder

Trustworthy automation comes from explicit checks, not optimism about prompts.
