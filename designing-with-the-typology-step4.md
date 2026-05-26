---
title: Step 4 - Map diagram
layout: default
parent: Designing with the Typology
nav_order: 5
---

# Design Construction
## Step 4: Map the diagram to the interface
### Step 4a: Map tasks to Interface Components/Visualizations
Mapping the decision tasks to views/visualizations/interface components.

Map each decision task to design support:

| Decision Task | Possible Design Support |
| --- | --- |
| **Choose** | Comparison views, rankings, final selection panels |
| **Activate** | Filters, thresholds, validation indicators, rule controls |
| **Create** | Generators, annotations, simulations, feature extraction, report builders |

Note: sometimes some decisions will not end up in the frontend, but in the backend. For example, if an activate decision represents a hard constraint, such as budget in a project, then that constraint might be applied automatically without the need of the user to make that decision. Thus, in this case, the typology could be useful to separate the tasks that need to be done in the backend automatically from the ones that need human involvement.

### Step 4b: Map connections between decisions to connection between views and interactions
The fact that the typology externalizes the connection between different decisions and where there are more feedback loops informs the designers where there is interaction between different visual components that represent those decisions. For instance, if I change this threshold for the activate decision that is connected to a create report decision, how would the create report decision change? Will it show different data? Or if it is connected to a choose decision, how would the view representing the choose decision change depending on the number of alternatives?



## Satellite Example
Once the decision tasks are identified, they can be mapped to interface components.

| Decision Task | Role in the Satellite Example | Possible Interface Support |
| --- | --- | --- |
| **Create** | Generate new satellite designs | Design generator panel, parameter controls, generated design table |
| **Create** | Add derived attributes | Attribute generation controls, derived metric explanations, provenance indicators |
| **Create** | Estimate performance and satisfaction | Simulation outputs, uncertainty intervals, stakeholder satisfaction predictions |
| **Activate** | Remove designs that violate hard constraints | Budget filters, feasibility checks, timeline thresholds, validation badges |
| **Activate** | Identify designs acceptable to stakeholders | Stakeholder-specific filters, minimum satisfaction sliders, conflict indicators |
| **Choose** | Select the final design | Comparison matrix, ranked shortlist, voting tools, final recommendation panel |

This mapping helps the designer move from abstract decision structure to concrete visualization design.

## Possible Interface Concept

One possible design is a coordinated dashboard with four main areas.

### 1. Design Space Overview

This view shows all candidate satellite designs.

Possible encodings include:

- Scatterplots for major tradeoffs, such as cost vs. load capacity or modularity vs. life expectancy.
- Parallel coordinates for comparing many attributes at once.
- A sortable table for inspecting exact values.
- Color or icons to indicate feasibility status.

This area primarily supports **activate** and **choose** tasks by helping users see which designs are available and which are promising.

---

### 2. Constraint and Criteria Panel

This panel lets users define hard constraints and soft preferences.

Possible controls include:

- Maximum cost
- Maximum weight
- Minimum load capacity
- Minimum life expectancy
- Minimum shielding
- Required upgradeability
- Required timeline feasibility

This area supports **activate** tasks by letting users determine which designs remain eligible.

A useful design feature would be to show the effect of each constraint immediately. For example, the interface could show that a cost constraint removes 40% of designs, while a shielding constraint removes only 10%.

---

### 3. Tradeoff and Simulation View

This view helps stakeholders understand tradeoffs and uncertainty.

It could include:

- Tradeoff curves
- Sensitivity analysis
- Flight simulation results
- Uncertainty ranges
- Warnings about feasibility risks
- Explanations of why a design passed or failed a simulation

This area supports **create** tasks because it produces new information about each design. It also supports **choose** tasks because stakeholders use this information to compare alternatives.

---

### 4. Stakeholder Collaboration View

This view shows how well each design satisfies different stakeholder groups.

It could include:

- Satisfaction scores for engineers, scientists, security agencies, and communication experts
- Areas of agreement and disagreement
- Comments or annotations from each group
- Voting or ranking mechanisms
- A shared shortlist of candidate designs

This area supports **choose** tasks by helping the group move toward a final selection. It also supports **activate** tasks if the group sets minimum satisfaction thresholds.

---

## Example Walkthrough

A stakeholder group might use the system as follows.

### 1. Start with the initial design dataset

The group begins with a table of existing candidate satellite designs.

```text
Input: Existing satellite design table
```

### 2. Generate additional candidate designs

The group uses the Design Generator to create new options with different combinations of modularity, shielding, mobility, and load capacity.

```text
Create: Generate new satellite designs
```

### 3. Generate new attributes

The group uses the Attribute Generator to add derived measures, such as:

- Estimated build complexity
- Adaptability score
- Risk score
- Maintenance difficulty
- Mission compatibility score

```text
Create: Add derived attributes
```

### 4. Estimate performance

The group runs the Flight Estimator on a subset of promising designs to estimate feasibility and risk.

```text
Create: Estimate flight feasibility
```

The group also runs the Stakeholder Satisfaction Estimator to predict how well each design meets the needs of different groups.

```text
Create: Estimate stakeholder satisfaction
```

### 5. Filter designs using hard constraints

The group removes designs that exceed the budget, violate timeline requirements, or fail feasibility thresholds.

```text
Activate: Keep only feasible and affordable designs
```

### 6. Explore tradeoffs

The group compares the remaining designs. For example, they may find that the most modular design has lower load capacity, while the highest-capacity design has limited upgradeability.

```text
Choose support: Compare tradeoffs among remaining designs
```

### 7. Negotiate stakeholder priorities

The group examines satisfaction scores and identifies designs that produce broad agreement or strong disagreement.

```text
Activate: Identify stakeholder-acceptable designs
```

### 8. Select a final design

The group chooses a final design and records the rationale for the decision.

```text
Choose: Select final satellite design
```

---

## What the Typology Reveals

Using the typology helps reveal that the satellite design problem is not just a final selection problem.

It includes several connected decision tasks:

- Users must **create** new candidate designs and derived information.
- Users must **activate** designs that satisfy hard constraints and stakeholder criteria.
- Users must **choose** among the remaining options.
- Users may need to loop back when constraints are too strict, tradeoffs are unacceptable, or stakeholder groups disagree.

This structure helps designers avoid building an interface that only shows a table of designs. Instead, the typology suggests an interface that supports generation, filtering, simulation, comparison, negotiation, and final selection.
