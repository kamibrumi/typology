---
title: Tutorial Walkthrough
layout: default
nav_order: 2
---

# Tutorial Walkthrough

This tutorial guides participants through a decision-support design process using the **Typology of Decision-Making Tasks**. The goal is to move from an open-ended domain scenario to a structured decision model, and then from that model to a visualization design.

The structure follows the logic of the **double diamond** design process:

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

## Before the Tutorial

Before starting, participants should have access to:

- the tutorial scenario,
- the dataset or dataset description,
- the typology reference,
- the domain expert context file, if using an LLM as the domain expert,
- paper, sticky notes, or a digital whiteboard for diagramming,
- and a sketching surface for interface design.

Participants may work individually, in pairs, or in small groups.

---

# Stage 1: Problem Definition

The first stage focuses on understanding and structuring the decision-making problem. Participants should resist the urge to immediately design charts, dashboards, or interfaces.

In the double diamond framing, this stage corresponds to moving from a broad, ambiguous situation toward a clearer definition of the decision problem.

---

## Step 1: Read the Scenario

Participants begin by reading the scenario brief.

The goal is to understand:

- who the decision-maker is,
- what decision they need to make,
- what options or entities are involved,
- what data is available,
- what constraints matter,
- and what makes the decision difficult.

For the embryology scenario, the decision-maker is an embryologist. The final decision is to **choose an embryo or shortlist of embryos for selection**, while preserving expert judgment and documenting uncertainty.

---

## Step 2: Interview the Domain Expert

Participants then interact with the domain expert. In this tutorial, the domain expert may be represented by an LLM using the provided embryologist context file.

During this stage, participants should ask questions about the decision problem, not the interface.

Good problem-definition questions include:

- What is the main decision you need to make?
- What smaller decisions happen before the final decision?
- What information do you look at first?
- What options are you comparing?
- What criteria matter?
- What constraints or thresholds do you use?
- What makes the decision uncertain?
- What would make a case require extra review?
- What output do you need at the end?

Participants should avoid jumping too quickly to questions such as “What chart do you want?” or “What should the dashboard look like?” Those questions belong to the design construction stage.

---

## Step 3: Identify the Top-Level Decision

Participants identify the highest-level decision in the scenario.

Ask:

> What is the final decision the user needs to make?

Then classify it using the typology:

- **Choose**: selecting one option or a subset from alternatives.
- **Activate**: applying criteria, rules, thresholds, or constraints.
- **Create**: generating or synthesizing a new option, artifact, or piece of information.

For the embryology scenario, the top-level decision is:

> Choose an embryo or embryo shortlist for selection.

This is a **choose** decision because the final output is a selected candidate or prioritized subset of candidates.

---

## Step 4: Decompose the Decision into Supporting Decisions

Participants now ask:

> What smaller decisions must happen before the final decision can be made?

For the embryology scenario, supporting decisions might include:

| Supporting Decision | Possible Typology Task |
| --- | --- |
| Narrow embryo candidates based on eligibility or review criteria | **Activate** |
| Flag embryos with high uncertainty or conflicting evidence | **Activate** |
| Compare embryos with similar morphology or PGT categories | **Choose** |
| Create a short rationale for the selected candidate | **Create** |
| Create a shortlist for further expert review | **Choose / Create** |
| Decide which evidence should be included in the final explanation | **Choose** |

The goal is not to force every activity into a perfect category. The goal is to make the reasoning structure visible enough to discuss, revise, and eventually design around.

---

## Step 5: Add Information Flow

Once participants have identified the major decisions, they add arrows showing how information moves between them.

Ask:

> What information is passed from one decision to the next?

For example:

```text
Embryo image + metadata
        ↓
Activate eligibility and caution flags
        ↓
Choose candidates for closer comparison
        ↓
Create comparison summary
        ↓
Choose final embryo or shortlist
        ↓
Create selection rationale
```

This step helps participants see that decision-support tools are not only about showing data. They also need to support transitions between decision stages.

---

## Step 6: Add Iteration and Feedback Loops

Real decision-making is rarely linear. Participants should mark places where the user may need to revisit an earlier decision.

Ask:

- When would the embryologist go back and inspect another embryo?
- When would a threshold need to be adjusted?
- When would a case need another expert review?
- When would the shortlist change?
- When would new evidence alter the final selection?

For example, an embryologist might choose a candidate for closer review, notice conflicting evidence, return to the candidate pool, and compare alternatives again.

In the diagram, this can be represented as a loop.

```text
Choose candidate for closer review
        ↓
Inspect evidence and uncertainty
        ↓
If evidence conflicts, return to candidate comparison
```

Iteration is important because it often reveals where the eventual interface needs to support backtracking, refinement, and explanation.

---

## Step 7: Reflect on the Problem Definition

Before moving to design, participants should review their decision diagram.

Useful reflection questions include:

- Is the top-level decision clear?
- Are the supporting decisions specific enough?
- Are there missing decisions that were implicit in the conversation?
- Are criteria, constraints, and options represented?
- Are there feedback loops?
- Which decisions require expert judgment?
- Which decisions could be supported computationally?
- Which decisions should not be automated?
- Where does uncertainty enter the workflow?

At the end of Stage 1, each group should have a decision diagram that captures the structure of the problem.

This diagram is the main output of the problem definition stage.

---

# Stage 2: Design Construction

The second stage focuses on using the decision diagram to construct a visualization decision-support tool.

In the double diamond framing, this stage corresponds to moving from a defined problem toward possible design solutions.

Participants should now ask:

> Given the decision structure we modeled, what kind of interface would support this workflow?

---

## Step 8: Map Decision Tasks to Interface Components

Participants begin by translating each decision task into possible design support.

| Decision Task | Design Implication |
| --- | --- |
| **Choose** | Comparison views, ranked lists, shortlist panels, final selection views |
| **Activate** | Filters, thresholds, rule controls, flags, eligibility indicators |
| **Create** | Summary generators, annotation tools, report builders, simulation or explanation components |

For the embryology scenario:

- A **choose** task might become a side-by-side embryo comparison view.
- An **activate** task might become a filter for developmental day, PGT category, or high-fragmentation cases.
- A **create** task might become a rationale builder that documents why an embryo was selected.

---

## Step 9: Design Around the Decision Flow

Participants should use the arrows in their decision diagram to think about interaction flow.

Ask:

- What does the user need to see first?
- What happens after the user applies a filter?
- How does the user move from a broad overview to candidate comparison?
- How does the user add an embryo to a shortlist?
- How does the user return to earlier steps?
- How does the final rationale get created?

The decision diagram can become a rough navigation structure for the tool.

For example:

```text
Overview
  → Filter / flag candidates
  → Compare shortlisted embryos
  → Inspect case details
  → Select embryo or shortlist
  → Generate rationale
```

---

## Step 10: Sketch the Visualization Tool

Participants now sketch an interface that supports the modeled decision workflow.

The sketch does not need to be polished. It should show how the tool supports the major decisions from the diagram.

A sketch might include:

- an overview of embryo candidates,
- filters for developmental day, PGT category, or morphology ranges,
- an image gallery,
- a side-by-side candidate comparison view,
- uncertainty or caution flags,
- a case-detail panel,
- a shortlist area,
- and a final selection rationale panel.

The key is that each interface component should connect back to a decision in the diagram.

---

## Step 11: Check Alignment Between Diagram and Design

After sketching, participants should compare their interface against their decision diagram.

Ask:

- Does every major decision in the diagram have design support?
- Are there interface elements that do not support any decision?
- Are the most important decisions visually emphasized?
- Are supporting decisions placed in the right sequence?
- Are loops and revisions supported?
- Does the interface preserve expert judgment?
- Does the interface make uncertainty visible?
- Does the design help the user explain the final decision?

This step helps participants avoid designing attractive but poorly aligned dashboards.

---

## Step 12: Share and Discuss

Each group presents both their decision diagram and their design sketch.

The presentation should explain:

1. the top-level decision,
2. the supporting decisions,
3. the main information flows,
4. the important loops or uncertainties,
5. how the interface supports each major decision,
6. and what tradeoffs the group faced while moving from problem definition to design.

The discussion should focus on the transition between the two diamonds:

> How did the structured problem definition shape the design?

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
