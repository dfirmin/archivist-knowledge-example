---
type: Metric Definition
title: Loss Ratio
description: Loss ratio measures how much of the premium is paid back out in losses, reported monthly by line of business.
tags: [data, claims, metric-definition]
status: draft
generated: {by: archivist-author/1, at: 2026-10-06T01:52:15Z}
sources:
  - {resource: sources/processed/metric-loss-ratio.md, title: Loss Ratio — metric definition (Finance & Claims Analytics)}
  - {resource: sources/processed/2026-09-30-claims-dw-office-hours--loss-ratio.md, title: "Loss Ratio — denominator changed to earned premium"}
verified:
  - {by: process:archivist-verifier/1, at: 2026-10-06T01:52:30Z}
okfx_structure: ratio-metric
okfx_placement: {outcome: new}
okfx_metric_code: LOSS_RATIO
okfx_subject_area: claims
okfx_source_views: [CLAIM_PMT_SV, POLICY_EXPOSURE_SV]
okfx_product_owner: claims-data@example.com
okfx_gaps: []
okfx_confidence: 1.0
---

## Definition

Loss ratio measures how much of the premium is paid back out in losses. *Source: [Loss Ratio — metric definition (Finance & Claims Analytics)](sources/processed/metric-loss-ratio.md), retrieved 2026-10-05*

## Formula

### Numerator

Incurred losses, which are paid losses (CLAIM_PMT_SV, PMT_TYPE_CD = 'L') plus the change in case reserves over the month. *Source: [Loss Ratio — metric definition (Finance & Claims Analytics)](sources/processed/metric-loss-ratio.md), retrieved 2026-10-05*

### Denominator

Earned premium (EARNED_PREM_AMT from POLICY_EXPOSURE_SV). Finance changed the denominator in Q3 from written premium to earned premium, starting with the July close. *Source: [Loss Ratio — denominator changed to earned premium](sources/processed/2026-09-30-claims-dw-office-hours--loss-ratio.md), retrieved 2026-10-05*

## Grain & Time Window

Reported monthly by line of business. The ratio is calculated for the same line of business and accounting month, expressed as a percentage. *Source: [Loss Ratio — metric definition (Finance & Claims Analytics)](sources/processed/metric-loss-ratio.md), retrieved 2026-10-05*

## Data Sources

- CLAIM_PMT_SV, for paid losses.
- POLICY_EXPOSURE_SV, for earned premium (EARNED_PREM_AMT).

*Source: [Loss Ratio — denominator changed to earned premium](sources/processed/2026-09-30-claims-dw-office-hours--loss-ratio.md), retrieved 2026-10-05*

## Exclusions

Catastrophe-coded claims (CAT_IND = 'Y') are excluded from the standard loss ratio and reported separately. *Source: [Loss Ratio — metric definition (Finance & Claims Analytics)](sources/processed/metric-loss-ratio.md), retrieved 2026-10-05*
