# Task Decomposition Template

Use this template to break a goal into a repeatable human + AI workflow.

## 1. Workflow objective

- What reliable output should this workflow produce?
- What scope is in and out?

## 2. Stages

For each stage, capture:

- stage name
- input required
- output produced
- owner: human, AI, or mixed
- failure modes
- review point

## 3. Dependencies

- Which stages depend on earlier outputs?
- Which stages can run in parallel?
- Which stage is the main bottleneck?

## 4. Context requirements

- What context is required for each stage?
- What context should be excluded to reduce noise?

## 5. Escalation rules

- When must a human intervene?
- What confidence threshold or failure signal triggers escalation?

## 6. Pilot scope

- What is the smallest safe first rollout?
- How will the workflow be evaluated before wider adoption?
