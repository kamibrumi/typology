---
title: Available Analytical Tools
layout: default
parent: Embryo Selection Scenario
nav_order: 4
---

## Available Analytical Tools

The decision-support system can include analytical tools that either create new information or estimate properties of existing embryo candidates.

In this scenario, it is important to distinguish between tools that operate on the **current patient cohort** and tools that operate on the **historical clinic dataset**.

### Generators

Generators create new columns, summaries, annotations, shortlists, or decision artifacts.

| Tool | Description |
| --- | --- |
| **Hormonal Pattern Summary Generator** | Groups hormone measures into interpretable flags, such as low ovarian reserve signal, elevated progesterone, or elevated TSH. |
| **Current Cohort Shortlist Generator** | Creates a preliminary shortlist from the current patient’s embryos based on user-defined criteria. The shortlist is not the final decision; it is a starting point for expert review. |
| **Similar Case Set Generator** | Creates a reference set of historical embryos that are similar to a selected current embryo based on morphology, developmental day, PGT category, fertilization method, patient age group, BMI, ovarian reserve, or hormone pattern. |

### Estimators

Estimators evaluate existing embryo candidates or historical patterns, often on a selected subset of cases.

| Tool | Description |
| --- | --- |
| **Morphology Pattern Estimator** | Estimates how morphology attributes such as fragmentation, symmetry, and zona pellucida thickness relate to historical outcome patterns. |
| **Patient Context Estimator** | Summarizes how pregnancy outcomes vary across patient age group, BMI category, ovarian reserve category, and hormonal pattern flags. |
| **Hormone Pattern Estimator** | Estimates how hormone-related patterns, such as AMH, FSH, estradiol, progesterone, TSH, or prolactin, relate to historical outcomes. |
| **Uncertainty Estimator** | Identifies embryos with incomplete, conflicting, or borderline evidence that may require closer expert review. |

These tools are not the final decision by themselves. Instead, they create or refine information that embryologists can use in later activation, comparison, and choice tasks.

