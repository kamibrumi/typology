---
title: Step 3 - Define dependencies
layout: default
parent: Designing with the Typology
nav_order: 4
---

# Problem Formulation
## Step 3: Add Information Flow and Iteration
Once participants have identified the major decisions, they add arrows showing how information moves between them.

Ask:
> What information is passed from one decision to the next?

Use arrows to show flow. 
* Add loops when users need to revisit criteria, regenerate options, or refine selections. 
* When you think that users might run out of options after doing an activate, then connect the activate decision to a create decision.
* When users might want to adjust the threshold of an activate decision add a self loop for the activate decision.

This step helps participants see that decision-support tools are not only about showing data. They also need to support transitions between decision stages.

## Homebuying Example
The decision process is unlikely to be linear. Buyers may discover that no existing home satisfies all constraints, or that the most feasible homes fail to satisfy important preferences.

This means the interface should support iteration.

For example:

```text
Generate home candidates
  ↓
Estimate affordability and fit
  ↓
Filter by constraints
  ↓
Compare tradeoffs
  ↓
Revise criteria or generate new homes
  ↺
```

### Example Loops

#### Loop 1: Constraint Revision

Buyers may apply budget, commute, or move-in-timeline filters and discover that too few homes remain.

```text
Activate feasible homes
  ↓
Too few viable options
  ↓
Revise thresholds or generate new homes
```

The interface should make this visible by showing how many homes are removed by each constraint and which constraints are most restrictive.

#### Loop 2: Tradeoff Exploration

Buyers may compare price, location, size, commute time, school quality, and renovation effort and realize that their priorities conflict.

```text
Compare tradeoffs
  ↓
Identify conflict between price and location
  ↓
Adjust weights, constraints, or design goals
```

The interface should support interactive tradeoff exploration rather than forcing users into a fixed ranking.

#### Loop 3: Stakeholder Negotiation

A home may satisfy one household member but fail to satisfy another, such as when budget and neighborhood preferences conflict.

```text
Estimate household satisfaction
  ↓
Find disagreement
  ↓
Discuss priorities and revise criteria
```

The interface should help buyers see where agreement and disagreement occur.
