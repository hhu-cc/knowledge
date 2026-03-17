---
name: ai-workflow-designer
description: This skill should be used when Claude needs to design a repeatable human-plus-AI workflow, including task decomposition, context handoff, validation checkpoints, and fallback rules rather than only generating a one-off answer.
---

# AI Workflow Designer

## Overview

Convert a goal into a repeatable operating workflow for humans and AI.
Break work into stages, assign responsibilities, define context requirements, and build verification loops that keep the workflow trustworthy.

## When to Use

Use this skill when any of the following is true:

- the user wants to integrate AI into an ongoing process instead of a one-time task
- the work contains multiple stages, handoffs, or quality checkpoints
- context management matters as much as raw generation quality
- the team needs a repeatable workflow with clear roles and review points
- failure modes need to be contained through verification or escalation

Do not use this skill when the goal is a single short answer with no workflow reuse.

## Required Inputs

Collect these inputs before designing the workflow:

- target outcome
- recurring task types
- available humans, tools, and AI capabilities
- quality threshold and acceptable error cost
- required turnaround speed
- compliance or approval constraints
- existing bottlenecks in the current process

Use `references/task-decomposition.md` to structure the workflow design.
Use `references/verification-patterns.md` to choose suitable validation loops.

## Workflow

### Step 1: Define the outcome and scope

State what the workflow must reliably produce.
Clarify where the workflow starts and ends.

### Step 2: Break the work into stages

Split the job into meaningful stages with visible outputs.
Keep each stage small enough to evaluate and hand off.

### Step 3: Assign human and AI roles

Decide what AI should draft, transform, summarize, classify, or explore.
Reserve judgment-heavy, high-consequence, or relationship-heavy steps for humans unless there is strong evidence otherwise.

### Step 4: Design context flow

Specify what context each stage needs.
Minimize unnecessary context while preserving the information required for quality.

### Step 5: Add validation and fallback

Place checks where errors are likely or costly.
Define what happens when a stage fails, produces low confidence, or conflicts with policy.

### Step 6: Define cadence and ownership

Specify who triggers the workflow, who reviews outputs, and how iteration happens.
Make the control points explicit.

## Output Structure

Return the result in this structure:

1. Workflow objective
2. Start and end conditions
3. Stage-by-stage breakdown
4. Human responsibilities
5. AI responsibilities
6. Required context by stage
7. Verification checkpoints
8. Failure and fallback rules
9. Metrics for workflow quality
10. Recommended first pilot

## Quality Bar

Ensure the workflow design:

- optimizes for reliable outcomes, not maximum AI usage
- keeps human judgment where consequences justify it
- includes explicit checks, not vague trust in generation quality
- can be piloted on a limited scope before broad rollout
- names what evidence would justify further automation

## Boundaries

Do not assume AI should own the whole workflow.
Do not remove approval, compliance, or accountability steps when they matter.
Do not design a workflow that depends on perfect prompts or perfect memory.
When the domain is high-risk, recommend stronger review and smaller pilot scope.
