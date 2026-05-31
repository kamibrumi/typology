---
title: activate
layout: default
parent: Decision Tasks
nav_order: 2
---

# Activate

An **activate** task determines which options meet or exceed a threshold, rule, or criterion.

Use **activate** when each option can be evaluated independently.

<hr>

## Typical Questions

- Which options satisfy the criteria?
- Which embryos should be excluded?
- Which homes are within budget?
- Which transactions are suspicious?
- Which satellite designs are feasible?
- Which alerts should be triggered?

<hr>

## Definition

In an **activate** task, each option is assessed independently. The decision does not require comparing every option against every other option. Instead, an option is returned if it passes a threshold or meets a criterion.

For example, in a car-buying scenario, a user might activate only cars below a certain price and mileage. Any number of cars may pass the filter: none, one, many, or all.

Unlike **choose**, **activate** does not guarantee how many options will be returned. It guarantees that returned options meet a level of acceptability defined by the criteria.

<hr>

## When to use activate

Use an **activate** task when:

- options are filtered, accepted, rejected, or flagged;
- thresholds or criteria matter;
- the number of returned options is unknown;
- the task is about acceptability rather than optimality;
- each option can be evaluated on its own.

<hr>

## Home-buying Example

In a homebuying scenario, the buyer filters homes by criteria such as budget, commute time, number of bedrooms, school rating, and move-in date.

Each home is evaluated independently. A home is returned if it passes the threshold or satisfies the buyer’s constraints. Any number of homes may pass the filter: none, one, many, or all.

This is an **activate** task because the goal is to identify which homes are acceptable, not to rank every home against every other home.s