---
title: Designing with the Typology
layout: default
nav_order: 8
---

# Designing with the Typology

## From Decision Models to Visualization Design

The typology is not only a descriptive tool. It can also guide visualization design.

A decision diagram helps designers move from a general problem to a structured problem definition, and then from that problem definition to interface design. This aligns with the double-diamond model of design, where designers first formulate the problem and then construct a solution.

The paper **“The Power of Typologies in Visualization Design”** argues that typologies can support visualization design by giving designers structured vocabularies for externalizing, organizing, and carrying forward problem structure. However, the paper also finds that the usefulness of a typology depends on how well its structure matches how designers think about the task.

## Why This Typology Helps Design

The decision-making typology is task-specific. Because it is designed for decision-making, it can align more closely with how designers reason about decision-support problems than a general visualization typology.

In the study described in *The Power of Typologies in Visualization Design*, participants using the task-specific decision-making typology were able to construct problem representations directly within the typology, reason about loops and dependencies, and carry that structure into interface design.

## Design Workflow

Use the typology in four steps.

### Step 1: Identify the Top-Level Decision

Ask:

> What is the main decision the user needs to make?

Then classify it as **choose**, **activate**, or **create**.

### Step 2: Decompose the Decision

Ask:

> What smaller decisions must happen before this decision can be made?

Add supporting tasks below the top-level decision.

### Step 3: Add Information Flow and Iteration

Ask:

> What information is passed from one decision to the next?

Use arrows to show flow. Add loops when users need to revisit criteria, regenerate options, or refine selections.

### Step 4: Translate Tasks into Interface Components

Map each decision task to design support:

| Decision Task | Possible Design Support |
| --- | --- |
| **Choose** | Comparison views, rankings, final selection panels |
| **Activate** | Filters, thresholds, validation indicators, rule controls |
| **Create** | Generators, annotations, simulations, feature extraction, report builders |

The tutorial proposal explicitly connects this step to interface design, noting that **activate** tasks often suggest filtering controls, **create** tasks suggest generative or analytical components, and **choose** tasks suggest comparison or final selection mechanisms.

## Design Questions to Ask

When designing with the typology, ask:

- Which decisions are well supported?
- Which decisions are currently implicit?
- Which decisions are automated?
- Which decisions require human judgment?
- Where does the user need comparison?
- Where does the user need control over criteria?
- Where does the user need explanation?
- Where does the user need to create or revise information?
- Where should the interface support iteration?