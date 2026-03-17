---
name: systems-thinking
description: This skill should be used when a problem involves multiple interacting variables, delays, feedback loops, incentives, or constraints, and Claude needs to analyze the system structure instead of giving a single-point fix.
---

# Systems Thinking

## Overview

Analyze the structure that produces repeated outcomes.
Map variables, constraints, delays, and feedback loops so the response targets leverage points instead of isolated symptoms.

## When to Use

Use this skill when any of the following is true:

- the same issue keeps returning after local fixes
- multiple teams, incentives, or constraints interact
- a change in one area creates side effects elsewhere
- delays or feedback loops matter
- the problem looks simple locally but complex globally

Do not use this skill for narrow issues with a single obvious cause and low system interaction.

## Required Inputs

Collect as many of these as possible:

- recurring outcomes or failure patterns
- key variables that appear to move together
- constraints and bottlenecks
- stakeholders and incentives
- delays between action and result
- previous interventions and their effects
- scope boundaries of the system under review

Use `references/causal-loop-checklist.md` to inspect interactions and delays.
Use `references/leverage-patterns.md` to search for higher-impact intervention points.

## Workflow

### Step 1: Define the system boundary

State what is inside the analysis and what is outside it.
Avoid mixing every possible factor into one vague map.

### Step 2: List key variables

Name the variables that meaningfully shape the outcome.
Prefer variables that can change over time or be influenced by action.

### Step 3: Map interactions

Describe how one variable affects another.
Mark whether the effect is reinforcing, balancing, delayed, or uncertain.

### Step 4: Identify loops and constraints

Look for reinforcing loops that amplify outcomes and balancing loops that stabilize them.
Identify the main constraint, bottleneck, or policy that shapes the system.

### Step 5: Examine second-order effects

Ask what happens after the immediate effect.
Check whether an apparently helpful change creates delayed harm or displaces the problem.

### Step 6: Find leverage points

Prioritize places where a relatively small intervention could change the system behavior.
Avoid recommending activity where the real leverage is structural.

## Output Structure

Return the result in this structure:

1. System boundary
2. Key variables
3. Important interactions
4. Feedback loops and delays
5. Main constraints or bottlenecks
6. Why local fixes may fail
7. Highest-leverage intervention points
8. Risks of unintended consequences
9. Suggested next experiment or intervention

## Quality Bar

Ensure the systems analysis:

- explains recurring behavior, not just isolated events
- accounts for delays and incentives where relevant
- distinguishes local optimization from system optimization
- identifies at least one plausible leverage point
- stays bounded enough to remain actionable

## Boundaries

Do not turn uncertainty into false diagrams.
Do not inflate a simple issue into needless complexity.
Do not assume the largest visible variable is the strongest leverage point.
When critical variables are unknown, state the missing information and recommend what to observe next.
