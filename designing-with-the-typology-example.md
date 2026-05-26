---
title: Example Scenario
layout: default
parent: Designing with the Typology
nav_order: 1
---

# Designing Example: Collaborative Satellite Design Selection

This example shows how the decision-making typology can be used to move from a design problem to a visualization interface concept. The example is based on a collaborative satellite design scenario in which multiple stakeholders must explore, evaluate, and select a next-generation satellite design.

The goal is not to produce one correct interface. Instead, the goal is to show how the typology helps designers externalize the decision structure, identify where different forms of support are needed, and translate those decision tasks into visualization components. To showcase this, we will go through a design scenario.

---

## Scenario
The international space community is convening a multi-agency task force to design the next-generation satellite.

The satellite must support diverse purposes, including:

- Communication
- GPS
- Scientific research
- Security and defense needs
- Long-term space operations

The design process must balance the priorities of several stakeholder groups, including communication experts, security agencies, engineers, scientists, and mission planners.

The task force needs a decision-support tool that helps stakeholders collaboratively explore possible satellite designs, evaluate tradeoffs, and select a final design while respecting strict constraints.

---

## Design Challenge

Design a decision-support tool that helps stakeholders collaboratively explore and select satellite designs.

The tool may be a single visualization, a dashboard, or a coordinated set of visualizations. It should support both individual analysis and collaborative discussion.

The tool should help users reason about:

1. **Budgetary constraints**  
   The total manufacturing cost must not exceed a fixed budget.

2. **Feasibility**  
   The satellite must remain functional, durable, and technically feasible as features are added.

3. **Timeline**  
   The satellite must be designed and built within a specified timeframe.

4. **Tradeoffs**  
   Stakeholders must compare competing priorities, such as:

   - Higher modularity for future upgrades, which may increase cost and reduce payload capacity.
   - Greater specificity for immediate mission needs, which may reduce cost but limit future adaptability.
   - Higher load capacity, which may conflict with shielding, mobility, or modularity.

5. **Stakeholder satisfaction**  
   The selected design should reflect the needs of diverse stakeholder groups, including communication specialists, security experts, engineers, and scientists.

---

## Available Input Data

The starting point is a tabular dataset of potential satellite designs.

Each row represents a possible satellite design. Each column represents a design attribute or performance criterion.

Example columns include:

| Attribute | Description |
| --- | --- |
| **Cost** | Estimated manufacturing cost |
| **Weight** | Total weight of the satellite |
| **Modularity %** | Hardware upgradeability and extensibility |
| **Load Capacity** | Payload capacity of the satellite |
| **Life Expectancy** | Expected operational lifespan in space |
| **Upgradeability** | Ability to remotely update or replace components |
| **Shielding** | Protection against radiation and space debris |
| **Mobility** | Ability to move autonomously in orbit |

This dataset provides the initial design space that stakeholders can explore, filter, extend, simulate, and compare.

Here is [a link to a synthetic dataset](https://docs.google.com/spreadsheets/d/138pUNkI97CZFEYYArpmeH6Hqd1YwnJbvH0YMFUa0fjg/edit?usp=sharing).

---

## Available Analytical Tools

The design-support system can include analytical tools that either create new information or estimate properties of existing designs.

### Generators

Generators create new rows, columns, or derived information.

| Tool | Description |
| --- | --- |
| **Design Generator** | Adds new rows to the dataset by generating new satellite designs with distinct configurations. |
| **Attribute Generator** | Adds new columns by deriving additional attributes, criteria, or performance measures. |

### Estimators

Estimators evaluate existing satellite options, often on a selected subset of designs.

| Tool | Description |
| --- | --- |
| **Design Comparison Estimator** | Produces similarity scores, design lineage information, or pattern summaries across satellite designs. |
| **Flight Estimator** | Simulates a test flight and estimates feasibility with probabilistic outcomes. It can also help determine whether a design should remain under consideration. |
| **Stakeholder Satisfaction Estimator** | Predicts satisfaction for different stakeholder groups and can help identify designs that meet minimum satisfaction thresholds. |

These tools are not the final decision by themselves. Instead, they create or refine information that stakeholders can use in later activation and choice tasks.


