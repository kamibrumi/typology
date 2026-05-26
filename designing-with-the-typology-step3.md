---
title: Step 3 - Define dependencies
layout: default
parent: Designing with the Typology
nav_order: 4
---

# Problem Formulation
## Step 3: Add Information Flow and Iteration

Ask:

> What information is passed from one decision to the next?

Use arrows to show flow. 
* Add loops when users need to revisit criteria, regenerate options, or refine selections. 
* When you think that users might run out of options after doing an activate, then connect the activate decision to a create decision.
* When users might want to adjust the threshold of an activate decision add a self loop for the activate decision.

## Satellite Example
The decision process is unlikely to be linear. Stakeholders may discover that no existing design satisfies all constraints, or that the most feasible designs fail to satisfy important stakeholder groups.

This means the interface should support iteration.

For example:

```text
Generate designs
  ↓
Estimate performance
  ↓
Filter by constraints
  ↓
Compare tradeoffs
  ↓
Revise criteria or generate new designs
  ↺
```

### Example Loops

#### Loop 1: Constraint Revision

Stakeholders may apply budget, timeline, or feasibility filters and discover that too few designs remain.

```text
Activate feasible designs
  ↓
Too few viable options
  ↓
Revise thresholds or generate new designs
```

The interface should make this visible by showing how many designs are removed by each constraint and which constraints are most restrictive.

#### Loop 2: Tradeoff Exploration

Stakeholders may compare modularity, load capacity, cost, and life expectancy and realize that their priorities conflict.

```text
Compare tradeoffs
  ↓
Identify conflict between modularity and load capacity
  ↓
Adjust weights, constraints, or design goals
```

The interface should support interactive tradeoff exploration rather than forcing users into a fixed ranking.

#### Loop 3: Stakeholder Negotiation

A design may satisfy engineers and scientists but fail to satisfy security agencies or communication specialists.

```text
Estimate stakeholder satisfaction
  ↓
Find stakeholder disagreement
  ↓
Discuss priorities and revise criteria
```

The interface should help stakeholders see where agreement and disagreement occur.
