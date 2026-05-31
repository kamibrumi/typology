---
title: Tutorial Walkthrough
layout: default
nav_order: 2
---

# Tutorial Walkthrough

This tutorial guides participants through a decision-support design process using the **Typology of Decision-Making Tasks**. The goal is to move from an open-ended domain scenario to a structured decision model, and then from that model to a visualization design.

The structure follows the logic of the [Double-Diamond Design Methodology](https://www.thefountaininstitute.com/blog/what-is-the-double-diamond-design-process) design process:

![double-diamond](img/designing/double-diamond.png)

1. **Problem Definition**: understand, decompose, and structure the decision-making problem.
2. **Design Construction**: translate the structured decision model into visualization and interaction ideas.

Participants should not begin by sketching dashboards. The first goal is to understand the decision problem. The design comes later.

---

## Overview of the Tutorial Flow

Participants will move through the tutorial in two main stages.

| Stage | Double Diamond Phase | Main Question | Main Output |
| --- | --- | --- | --- |
| **Stage 1: Problem Definition** | Define the problem | What decision is being made, and what smaller decisions support it? | A decision diagram using choose, activate, and create |
| **Stage 2: Design Construction** | Construct the solution | How can the decision diagram guide the design of a visualization decision-support tool? | A visualization/interface sketch |

The decision diagram acts as the bridge between the two stages. It is not just a representation of the problem; it becomes a blueprint for design.

---

# What Participants Should Leave With

By the end of the tutorial, participants should have:

- practiced interviewing a domain expert,
- identified a top-level decision,
- decomposed the decision into choose, activate, and create tasks,
- represented hierarchy, information flow, and iteration,
- used a decision diagram as a design blueprint,
- sketched a visualization decision-support tool,
- and reflected on how problem definition shapes design construction.

The central takeaway is:

> A decision-support visualization should not begin with a chart type. It should begin with a clear model of the decision being supported.

---

## Suggested Tutorial Artifacts

Participants may produce the following artifacts:

| Artifact | Stage | Purpose |
| --- | --- | --- |
| Domain interview notes | Problem definition | Capture what the expert says about decisions, criteria, and uncertainty |
| Decision diagram | Problem definition | Represent the decision workflow using the typology |
| Design mapping table | Bridge between stages | Connect decision tasks to possible interface components |
| Interface sketch | Design construction | Show how the tool supports the decision workflow |
| Reflection notes | Both stages | Document assumptions, tradeoffs, and open questions |

---

## A Simple Participant Checklist

Before moving from problem definition to design, participants should be able to answer:

- What is the final decision?
- Is it choose, activate, or create?
- What are the main supporting decisions?
- What information flows between them?
- Where are the loops?
- Where is uncertainty?
- What needs to remain human judgment?

Before finishing the design construction stage, participants should be able to answer:

- Which interface component supports each decision?
- How does the user move through the decision workflow?
- How can the user compare options?
- How can the user apply criteria or constraints?
- How can the user create or document a rationale?
- How does the interface support iteration?
- How does the design avoid over-automation?

---

## Optional Extension: Using an LLM as the Domain Expert

If participants use the provided LLM context file, they should treat the LLM as a simulated domain expert, not as an authority on clinical practice.

During the problem definition stage, participants should ask the LLM about workflow, decision criteria, uncertainty, and constraints.

During the design construction stage, participants may ask the LLM about visualization preferences, interaction needs, and what would make a tool helpful or misleading.

The key is to keep the two stages separate:

- first, understand the decision problem;
- then, design the visualization support.
