---
type: Metric Definition
title: Open Claim Count
description: The open claims KPI in the Monday deck is a count of claims in CLAIM_HDR_SV whose status is open or reopened, broken out by line of business.
tags: [data, claims, metric-definition]
status: draft
generated: {by: archivist-author/1, at: 2026-10-06T01:54:20Z}
sources:
  - {resource: sources/processed/kpi-open-claims-email.md, title: 're: "open claims" number in the Monday deck — how we count it'}
  - {resource: sources/processed/2026-10-03-rules-triage-call--open-claim-cnt.md, title: "OPEN_CLAIM_CNT — exclusion window change from 24 to 48 hours"}
verified: [{by: process:archivist-verifier/1, at: 2026-10-06T01:54:36Z}]
okfx_structure: count-metric
okfx_placement: {outcome: new}
okfx_metric_code: OPEN_CLAIM_CNT
okfx_subject_area: claims
okfx_source_views: [CLAIM_HDR_SV]
okfx_product_owner: claims-data@example.com
okfx_gaps: []
okfx_confidence: 1.00
---

## Definition

The open claims KPI for the Monday deck is a count of claims in CLAIM_HDR_SV. *Source: [re: "open claims" number in the Monday deck — how we count it](sources/processed/kpi-open-claims-email.md), retrieved 2026-10-05*

## What Is Counted

Claims where CLAIM_STATUS_CD is O or R; a reopened claim counts as open. *Source: [re: "open claims" number in the Monday deck — how we count it](sources/processed/kpi-open-claims-email.md), retrieved 2026-10-05*

## Grain & Time Window

The count is as of end of day Sunday. CLAIM_HDR_SV has one row per claim, so no dedupe is needed. The count is broken out by LOB_CD, with no weighting. *Source: [re: "open claims" number in the Monday deck — how we count it](sources/processed/kpi-open-claims-email.md), retrieved 2026-10-05*

## Data Sources

- CLAIM_HDR_SV

*Source: [re: "open claims" number in the Monday deck — how we count it](sources/processed/kpi-open-claims-email.md), retrieved 2026-10-05*

## Exclusions

Claims reported within the exclusion window are not included. Starting with the October 12th deck the window is 48 hours, because weekend intake is slower; Finance asked for the change and it was agreed on the 2026-10-03 triage call (raised from 24 hours, the window used before that, when the exclusion was because intake was still validating recently reported claims). *Source: [OPEN_CLAIM_CNT — exclusion window change from 24 to 48 hours](sources/processed/2026-10-03-rules-triage-call--open-claim-cnt.md), retrieved 2026-10-05* *Source: [re: "open claims" number in the Monday deck — how we count it](sources/processed/kpi-open-claims-email.md), retrieved 2026-10-05*
