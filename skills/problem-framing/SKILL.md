---
name: problem-framing
description: This skill should be used when a request is ambiguous, symptom-driven, or poorly scoped, and Claude needs to clarify the real problem, desired outcome, constraints, and success metrics before proposing solutions.
---

# Problem Framing

## Overview

Turn a vague request into a problem that can be solved well.
Collect the missing context, separate symptoms from causes, identify false requirements, and define what success actually means.

## When to Use

Use this skill when any of the following is true:

- the user describes pain, confusion, or underperformance without a clear target
- the request jumps to a solution before the problem is validated
- goals, stakeholders, constraints, or metrics are missing
- multiple different root causes could explain the same symptom
- the work would be expensive if the team solved the wrong problem

Do not use this skill when the problem statement is already precise, validated, and bounded enough for direct execution.

## Required Inputs

Collect as much of the following as possible:

- current situation or triggering signal
- desired outcome
- observable symptoms
- constraints and non-negotiables
- stakeholders and affected parties
- current assumptions about the cause
- existing metrics or evidence
- time horizon and urgency

When information is missing, state the gap explicitly instead of inventing certainty.
Use `references/intake-template.md` to structure the intake.
Use `references/examples.md` to calibrate the difference between a symptom and a real problem statement.

## Workflow

### Step 1: Restate the situation

Restate the request in plain language.
Describe what is known, what is assumed, and what is still unclear.

### Step 2: Separate symptom from cause

List the visible symptoms.
For each symptom, ask what deeper condition could create it.
Reject the temptation to treat the first explanation as the root cause.

### Step 3: Expose false requirements

Identify solution-shaped assumptions embedded in the request.
Rewrite statements such as “need more process,” “need a new feature,” or “need more content” into neutral problem language.

### Step 4: Define the actual objective

Name the real objective in outcome terms.
Prefer business, operational, or behavioral results over activity counts.

### Step 5: Define success criteria

Specify how success would be observed.
Prefer leading and lagging indicators when possible.
State the difference between a success metric, a proxy metric, and a vanity metric.

### Step 6: Identify constraints and stakeholders

List constraints that shape the solution space.
Call out who benefits, who bears cost, who can block progress, and who decides.

### Step 7: Produce the framed problem

Convert the analysis into a concise problem statement that is ready for solution generation or decision review.

## Output Structure

Return the result in this structure:

1. Situation summary
2. Observed symptoms
3. Most plausible underlying problem
4. False requirements or assumptions to remove
5. Desired outcome
6. Success metrics
7. Key constraints
8. Stakeholders and decision owners
9. Open questions and evidence gaps
10. Reframed problem statement

## Quality Bar

Ensure the final framing:

- describes a problem, not a preferred solution
- is specific enough to guide action
- makes assumptions visible
- names uncertainty honestly
- defines success in observable terms

## Boundaries

Do not pretend to know the true root cause without evidence.
Do not compress political, relational, or cultural problems into purely technical language.
Do not produce a solution recommendation unless the framed problem is stable enough for that next step.
When the stakes are high and evidence is weak, recommend further validation.
