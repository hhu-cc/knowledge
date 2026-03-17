---
name: decision-tradeoff-review
description: This skill should be used when several viable options exist and Claude needs to compare tradeoffs, eliminate weak choices, surface risks, and recommend the most appropriate path under explicit constraints.
---

# Decision Tradeoff Review

## Overview

Compare meaningful options without collapsing into generic pros-and-cons.
Make tradeoffs explicit, highlight what should not be chosen, and recommend the strongest path for the current context.

## When to Use

Use this skill when any of the following is true:

- more than one viable option exists
- the user asks what should be prioritized or deprioritized
- an apparently correct choice may still be wrong for the current stage
- the team needs to balance speed, quality, risk, reversibility, or resource limits
- too many candidate ideas are creating decision noise

Do not use this skill when the real problem is still ambiguous. Use `problem-framing` first when the target itself is unclear.

## Required Inputs

Collect these inputs before comparing:

- the decision to be made
- the available options
- the decision horizon
- constraints, including budget, time, skills, and dependencies
- decision criteria and their relative weight
- downside risk and failure cost
- reversibility of each option
- who bears the consequences

Use `references/evaluation-matrix.md` for the comparison template.
Use `references/risk-prompts.md` to pressure-test the analysis.

## Workflow

### Step 1: Define the decision

State the actual decision in one sentence.
Make sure the decision is concrete enough to compare options against the same target.

### Step 2: Filter invalid options

Remove options that violate non-negotiable constraints.
Avoid spending analysis time on choices that cannot realistically be executed.

### Step 3: Compare on explicit criteria

Score or describe each option across the most relevant dimensions.
Typical dimensions include:

- expected upside
- implementation cost
- time to value
- execution risk
- reversibility
- long-term strategic fit
- team capability match

### Step 4: Identify tradeoffs

Name what each option optimizes and what it sacrifices.
Look for hidden tradeoffs, not just obvious ones.

### Step 5: Stress-test the preferred option

Ask what would make the preferred option fail.
Check whether the recommendation depends on fragile assumptions.

### Step 6: Eliminate and recommend

Explicitly eliminate weaker options and explain why.
Recommend one option, plus a fallback if the assumptions change.

## Output Structure

Return the result in this structure:

1. Decision statement
2. Options considered
3. Evaluation criteria
4. Comparison summary
5. Main tradeoffs
6. Options eliminated and reasons
7. Recommended option
8. Conditions that would change the recommendation
9. Key risks and mitigations
10. Next action

## Quality Bar

Ensure the decision review:

- compares a small set of real options instead of infinite possibilities
- surfaces opportunity cost, not just direct cost
- distinguishes reversible from irreversible bets
- matches the recommendation to the current stage, not an abstract ideal
- states what not to do

## Boundaries

Do not pretend the tool can remove decision ownership.
Do not hide value judgments behind fake objectivity.
Do not recommend an option without making the winning criteria visible.
When consequences are material and uncertainty is high, recommend a validation step before commitment.
