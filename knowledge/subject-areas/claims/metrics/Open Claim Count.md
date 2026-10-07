---
type: Metric Definition
title: Open Claim Count
description: Open Claim Count is the number of claims in CLAIM_HDR_SV with status O or R, as counted for the Monday deck.
tags: [data, claims, metric-definition]
status: draft
generated: {by: archivist-author/1, at: 2026-10-07T13:11:30Z}
verified:
  - {by: process:archivist-verifier/1, at: 2026-10-07T13:11:32Z}
sources:
  - {resource: sources/processed/kpi-open-claims-email.md, title: "re: \"open claims\" number in the Monday deck — how we count it"}
  - {resource: sources/processed/2026-10-03-rules-triage-call--open-claim-cnt.md, title: "OPEN_CLAIM_CNT — change of the exclusion window for open claims"}
okfx_structure: count-metric
okfx_placement: {outcome: new}
okfx_metric_code: OPEN_CLAIM_CNT
okfx_subject_area: claims
okfx_source_views: [CLAIM_HDR_SV]
okfx_product_owner: claims-data@example.com
okfx_gaps: []
okfx_confidence: 1.0
---

## Definition

The open claims KPI for the Monday deck is a count of claims in CLAIM_HDR_SV where CLAIM_STATUS_CD is O or R.

*Source: [re: "open claims" number in the Monday deck — how we count it](sources/processed/kpi-open-claims-email.md), retrieved 2026-10-07*

## What Is Counted

Claims in CLAIM_HDR_SV where CLAIM_STATUS_CD is O or R; a reopened claim counts as open. There is one row per claim, so no dedupe is needed.

*Source: [re: "open claims" number in the Monday deck — how we count it](sources/processed/kpi-open-claims-email.md), retrieved 2026-10-07*

## Grain & Time Window

Counted as of end of day Sunday and broken out by LOB_CD, with no weighting.

*Source: [re: "open claims" number in the Monday deck — how we count it](sources/processed/kpi-open-claims-email.md), retrieved 2026-10-07*

## Data Sources

- CLAIM_HDR_SV

*Source: [re: "open claims" number in the Monday deck — how we count it](sources/processed/kpi-open-claims-email.md), retrieved 2026-10-07*

## Exclusions

Claims reported within a recent window are not counted. The window was the last 24 hours, because intake is still validating those claims. It is raised to 48 hours, starting with the October 12th deck; Finance asked for the change because weekend intake is slower.

*Source: [re: "open claims" number in the Monday deck — how we count it](sources/processed/kpi-open-claims-email.md), retrieved 2026-10-07*; *Source: [OPEN_CLAIM_CNT — change of the exclusion window for open claims](sources/processed/2026-10-03-rules-triage-call--open-claim-cnt.md), retrieved 2026-10-07*
