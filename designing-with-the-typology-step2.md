---
title: Step 2 - Decompose
layout: default
parent: Designing with the Typology
nav_order: 3
---

# Problem Formulation
## Step 2: Decompose the Decision
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

Classify these intermediate decisions as **choose**, **activate**, or **create**.

The goal is not to force every activity into a perfect category. The goal is to make the reasoning structure visible enough to discuss, revise, and eventually design around.

## Home-buying Example
The final choice depends on several smaller decisions. Buyers cannot choose a home directly from the full listing set without first creating, evaluating, and narrowing the option space.

Possible subdecisions are:

| Decision Task | Decision Description |
| --- | --- |
| **Create** | Create affordability and reachability estimates (deriving new features) |
| **Create** | Create new ideal homes (or list of characteristics) by putting together features from different homes |
| **Activate** | Filter out homes that violate hard constraints (affortability) |
| **Activate** | Filter out homes that violate soft constraints (distance to work, number of bathrooms) |
| **Create** | Generate shortlist of candidates based on subjective criteria (perceived beauty of the surrounding area) |
| **Choose** | Select the final home |

These mapped decisions become the workflow in the next step.

