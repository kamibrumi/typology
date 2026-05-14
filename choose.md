---
title: choose
layout: default
parent: Decision Tasks
nav_order: 1
---

# Choose

A **choose** task selects the best option or subset of options from a set of alternatives.

Use **choose** when the decision depends on comparison among options.

<hr>

## Typical Questions

- Which option is best?
- Which design should we select?
- Which embryo should be transferred?
- Which candidate should be prioritized?
- Which alternative should be chosen from the shortlist?

<hr>

## Definition

In a **choose** task, options are evaluated relative to one another. Whether an option is selected depends on how it compares with the other available options.

For example, when buying a car, a user may choose the best car among four available cars. The chosen car may not satisfy every ideal criterion, but it is considered the best among the available alternatives.

The typology paper emphasizes that **choose** guarantees the **quantity** of returned options — such as the top one or top *k* — but does not guarantee that those options meet a fixed quality threshold.

<hr>

## When to Use Choose

Use a **choose** task when:

- the user must select one or more options;
- the decision involves ranking, comparison, or trade-offs;
- the output should be a fixed number of options;
- the user is asking for “the best” rather than “all acceptable” options.

<hr>

## Design Implications

**Choose** tasks often require visual support for comparison.

Useful design patterns include:

- ranked lists;
- comparison tables;
- side-by-side views;
- scorecards;
- multi-criteria comparison panels;
- summary dashboards;
- selected/final candidate views.

<hr>

## Example

In **EmbryoProfiler**, the final IVF decision is a **choose** task: clinicians compare embryos and select the best embryo for transfer, while deciding which others to freeze or avoid.

The paper describes this final comparison stage as selecting optimal candidates based on viability scores and prior grading steps.