---
title: Case Studies
layout: default
nav_order: 5
---

# Case Studies

## Learning from Decision-Support Systems

Case studies show how the typology can describe real visualization systems. They also demonstrate that the same three tasks can model decision-making across different domains.

The original typology paper presents four case studies: **Homefinder Revisited**, **Umbra**, **Centaurus**, and **WireVis**. Each case study uses the typology to describe the decision-making process supported by a visualization system.

<hr>

## Case Study: Homefinder Revisited

**Homefinder Revisited** supports users in finding an ideal home. The top-level decision is a **choose** task: select the best home.

This decision is supported by lower-level tasks:

```text
Create candidate homes → Activate homes that satisfy criteria → Activate homes to add to a wishlist → Choose the best home
```

This example resembles a multi-criteria decision-making workflow. Users specify preferences, refine criteria, narrow the option space, and finally choose a home.

<hr>

## Case Study: Umbra

**Umbra** supports data sanitization. The top-level decision is an activate task: determine whether a sanitized dataset is acceptable based on privacy and utility.

The workflow includes:

```text
Create sanitization schemes → Activate acceptable schemes → Choose a scheme → Create simulated attacks → Activate whether the modified data is acceptable
```

This case shows how create, activate, and choose can form iterative loops. Users may repeatedly generate schemes, test them, and decide whether the result is acceptable.

<hr>

## Case Study: Centaurus

**Centaurus** supports users in assessing the trustworthiness of news articles.

The top-level decision is an activate task: determine whether an article is trustworthy.

Supporting tasks include:

```text
Create search terms → Activate relevant articles → Choose articles to read → Activate similar articles → Activate article trustworthiness
```

The typology helps reveal similarities between Centaurus and Umbra, even though the domains are very different. Both systems involve creating candidates, filtering or activating them, and choosing items for deeper inspection.

<hr>

## Case Study: WireVis

**WireVis** supports financial fraud analysis.

The top-level decision is a create task: synthesize a previously unknown fraud strategy from suspicious transactions and account behavior.

Supporting tasks include:

```text
Choose accounts to investigate → Activate plausible suspicious transactions → Activate degree of fraud → Create a new fraud pattern
```

This case is important because the final goal is not selecting or filtering an option. The goal is insight generation. The typology makes this explicit by representing the top-level decision as create.