---
title: Step 4 - Map diagram
layout: default
parent: Designing with the Typology
nav_order: 6
---

# Design Construction
The second stage focuses on using the decision diagram to construct a visualization decision-support tool.

In the double diamond framing, this stage corresponds to moving from a defined problem toward possible design solutions.

Participants should now ask:

> Given the decision structure we modeled, what kind of interface would support this workflow?


## Step 4: Map the diagram to the interface
### Step 4a: Map tasks to Interface Components/Visualizations
Mapping the decision tasks to views/visualizations/interface components.

Map each decision task to design support:

| Decision Task | Possible Design Support |
| --- | --- |
| **Choose** | Comparison views, rankings, final selection panels |
| **Activate** | Filters, thresholds, validation indicators, rule controls |
| **Create** | Generators, annotations, simulations, feature extraction, report builders |

Visualization inspiration: 
- [100.datavizproject.com](https://100.datavizproject.com/)
- [datavizcatalogue](https://datavizcatalogue.com/search.html)

Note: sometimes some decisions will not end up in the frontend, but in the backend. For example, if an activate decision represents a hard constraint, such as budget in a project, then that constraint might be applied automatically without the need of the user to make that decision. Thus, in this case, the typology could be useful to separate the tasks that need to be done in the backend automatically from the ones that need human involvement.

### Step 4b: Map connections between decisions to connection between views and interactions
The fact that the typology externalizes the connection between different decisions and where there are more feedback loops informs the designers where there is interaction between different visual components that represent those decisions. For instance, if I change this threshold for the activate decision that is connected to a create report decision, how would the create report decision change? Will it show different data? Or if it is connected to a choose decision, how would the view representing the choose decision change depending on the number of alternatives?

Ask:
- What does the user need to see first?
- What happens after the user applies a filter?
- How does the user move from a broad overview to candidate comparison?
- How does the user add an alternative to a shortlist?
- How does the user return to earlier steps?
- How does the final rationale get created?

The decision diagram can become a rough navigation structure for the tool.

---

Participants now sketch an interface that supports the modeled decision workflow.

The sketch does not need to be polished. It should show how the tool supports the major decisions from the diagram.

## Home-buying Example
Once the decision tasks are identified, they can be mapped to interface components.

| Decision Task | Role in the Homebuying Example | Possible Interface Support |
| --- | --- | --- |
| **Create** | Generate shortlist candidates and derived features | Listing recommender, commute estimators, affordability calculators, generated comparison table |
| **Create** | Add derived attributes | Neighborhood summaries, school-score explanations, inspection notes, provenance indicators |
| **Create** | Estimate affordability and fit | Mortgage estimates, monthly payment projections, uncertainty intervals, household fit predictions |
| **Activate** | Remove homes that violate hard constraints | Budget filters, commute thresholds, move-in date checks, validation badges |
| **Activate** | Identify homes acceptable to the buyer | Preference filters, minimum-fit sliders, conflict indicators |
| **Choose** | Select the final home | Comparison matrix, ranked shortlist, voting tools, final recommendation panel |

This mapping helps the designer move from abstract decision structure to concrete visualization design.

## Possible Interface Concept

One possible design is a coordinated dashboard with four main areas.

### 1. Design Space Overview

This view shows all candidate homes.

Possible encodings include:

- Scatterplots for major tradeoffs, such as price vs. commute time or size vs. renovation effort.
- Parallel coordinates for comparing many attributes at once.
- A sortable table for inspecting exact values.
- Color or icons to indicate feasibility status.

This area primarily supports **activate** and **choose** tasks by helping users see which homes are available and which are promising.

---

### 2. Constraint and Criteria Panel

This panel lets users define hard constraints and soft preferences.

Possible controls include:

- Maximum price
- Maximum monthly payment
- Maximum commute time
- Minimum number of bedrooms
- Required school rating
- Required move-in date

This area supports **activate** tasks by letting users determine which designs remain eligible.

A useful design feature would be to show the effect of each constraint immediately. For example, the interface could show that a price constraint removes 40% of homes, while a commute constraint removes only 10%.

---

### 3. Tradeoff and Simulation View

This view helps buyers understand tradeoffs and uncertainty.

It could include:

- Tradeoff curves
- Sensitivity analysis
- Affordability projections
- Uncertainty ranges
- Warnings about feasibility risks
- Explanations of why a home passed or failed a constraint check

This area supports **create** tasks because it produces new information about each home. It also supports **choose** tasks because buyers use this information to compare alternatives.

---

### 4. Stakeholder Collaboration View

This view shows how well each home satisfies different household priorities.

It could include:

- Satisfaction scores for household members or co-buyers
- Areas of agreement and disagreement
- Comments or annotations from each person
- Voting or ranking mechanisms
- A shared shortlist of candidate homes

This area supports **choose** tasks by helping the group move toward a final selection. It also supports **activate** tasks if the group sets minimum satisfaction thresholds.

---

## Example Walkthrough

A homebuying group might use the system as follows.

### 1. Start with the initial design dataset

The group begins with a table of existing candidate homes.

```text
Input: Existing home listing table
```

### 2. Generate additional candidate designs

The group uses the recommendation tools to surface new options with different combinations of price, size, commute time, and neighborhood fit.

```text
Create: Generate new home candidates
```

### 3. Generate new attributes

The group uses the attribute generator to add derived measures, such as:

- Estimated monthly payment
- Commute score
- School-fit score
- Renovation difficulty
- Neighborhood compatibility score

```text
Create: Add derived attributes
```

### 4. Estimate performance

The group runs the mortgage estimator on a subset of promising homes to estimate affordability and risk.

```text
Create: Estimate affordability and fit
```

The group also runs the household satisfaction estimator to predict how well each home meets the needs of different people in the household.

```text
Create: Estimate household satisfaction
```

### 5. Filter designs using hard constraints

The group removes homes that exceed the budget, fail commute limits, or cannot meet move-in timing requirements.

```text
Activate: Keep only feasible and affordable homes
```

### 6. Explore tradeoffs

The group compares the remaining homes. For example, they may find that the most affordable home has a longer commute, while the closest home needs more renovation.

```text
Choose support: Compare tradeoffs among remaining homes
```

### 7. Negotiate stakeholder priorities

The group examines satisfaction scores and identifies homes that produce broad agreement or strong disagreement.

```text
Activate: Identify buyer-acceptable homes
```

### 8. Select a final design

The group chooses a final home and records the rationale for the decision.

```text
Choose: Select final home
```

---

## What the Typology Reveals

Using the typology helps reveal that the homebuying problem is not just a final selection problem.

It includes several connected decision tasks:

- Users must **create** new candidate homes and derived information.
- Users must **activate** homes that satisfy hard constraints and household criteria.
- Users must **choose** among the remaining options.
- Users may need to loop back when constraints are too strict, tradeoffs are unacceptable, or household members disagree.

This structure helps designers avoid building an interface that only shows a table of listings. Instead, the typology suggests an interface that supports recommendation, filtering, affordability estimation, comparison, negotiation, and final selection.
