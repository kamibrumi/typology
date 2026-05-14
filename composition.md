---
title: Composition of Decision Tasks
layout: default
nav_order: 4
---

# Composing Decision Tasks

Real-world decisions are rarely isolated. A user may need to generate options, filter them, compare them, revise criteria, and repeat the process.

The typology supports this complexity through **composability** and **hierarchy**.

<hr>

## Why Composability Matters for Design

Composability helps designers answer practical design questions:

* What does the user need to decide first?
* Which decisions depend on earlier outputs?
* Where does the user need to iterate?
* Which information should be passed between views?
* Which decisions are unsupported in the current interface?
* Which tasks should be automated, interactive, or collaborative?

A decision diagram can therefore become a blueprint for visualization design.

<hr>

## Diagramming Decision Problems

Decision problems can be represented as node-link diagrams:

* circles represent choose tasks;
* squares represent activate tasks;
* triangles represent create tasks;
* arrows represent information flow;
* loops represent iteration;
* levels represent hierarchy.

The typology paper introduces this diagramming approach to show how decision tasks relate to one another in a larger decision-making process.

<hr>

## Composability

Decision tasks are composable when the output of one task becomes the input to another.

For example:

```text
Create candidate options → Activate acceptable options → Choose the best option
```

This structure is common in decision-support systems. A system may first create alternatives, then activate those that satisfy constraints, and finally help the user choose among the remaining options.

The original typology paper describes composability as a way to represent how decision-making processes are structured as sequences of information transformations. This supports a process-centric view of decision-making and helps designers understand how information informs and transforms decisions.

<hr>

## Hierarchy

Decision tasks can also be decomposed hierarchically.

```text
A top-level decision may depend on several lower-level decisions. For example:

Level 1: Choose the best evacuation location

Level 2:
- Create possible evacuation locations
- Activate locations that meet safety and capacity criteria
- Choose the final location
```

The hierarchy shows which sub-decisions support the overall decision. This helps designers decide which parts of the workflow need visualization support and which parts may be automated, hidden, or simplified.