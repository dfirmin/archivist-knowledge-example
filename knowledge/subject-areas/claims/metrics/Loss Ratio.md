---
type: Metric Definition
title: Loss Ratio
description: Loss ratio measures how much of the premium is paid back out in losses, reported monthly by line of business.
tags: [data, claims, metric-definition]
status: draft
generated: {by: archivist-author/1, at: 2026-10-07T13:10:28Z}
verified: [{by: process:archivist-verifier/1, at: 2026-10-07T13:11:08Z}]
sources:
  - {resource: sources/processed/metric-loss-ratio.md, title: "Loss Ratio — metric definition (Finance & Claims Analytics)"}
  - {resource: sources/processed/2026-09-30-claims-dw-office-hours--loss-ratio.md, title: "Loss Ratio — denominator changed to earned premium"}
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

Loss ratio measures how much of the premium is paid back out in losses. It is reported monthly by line of business.

*Source: [Loss Ratio — metric definition (Finance & Claims Analytics)](sources/processed/metric-loss-ratio.md), retrieved 2026-10-07*

## Formula

Incurred losses divided by earned premium (changed from written premium, starting with the July close), for the same line of business and accounting month, expressed as a percentage.

*Source: [Loss Ratio — metric definition (Finance & Claims Analytics)](sources/processed/metric-loss-ratio.md), retrieved 2026-10-07*; *Source: [Loss Ratio — denominator changed to earned premium](sources/processed/2026-09-30-claims-dw-office-hours--loss-ratio.md), retrieved 2026-10-07*

### Numerator

Incurred losses = paid losses (CLAIM_PMT_SV, PMT_TYPE_CD = 'L') plus the change in case reserves over the month.

*Source: [Loss Ratio — metric definition (Finance & Claims Analytics)](sources/processed/metric-loss-ratio.md), retrieved 2026-10-07*

### Denominator

Premium = earned premium for the month from POLICY_EXPOSURE_SV (EARNED_PREM_AMT). This changed from written premium; finance changed it in Q3, starting with the July close.

*Source: [Loss Ratio — denominator changed to earned premium](sources/processed/2026-09-30-claims-dw-office-hours--loss-ratio.md), retrieved 2026-10-07*

## Grain & Time Window

Calculated for the same line of business and accounting month, and reported monthly by line of business.

*Source: [Loss Ratio — metric definition (Finance & Claims Analytics)](sources/processed/metric-loss-ratio.md), retrieved 2026-10-07*

## Data Sources

- CLAIM_PMT_SV
- POLICY_EXPOSURE_SV

*Source: [Loss Ratio — metric definition (Finance & Claims Analytics)](sources/processed/metric-loss-ratio.md), retrieved 2026-10-07*

## Exclusions

Catastrophe-coded claims (CAT_IND = 'Y') are excluded from the standard loss ratio and reported separately.

*Source: [Loss Ratio — metric definition (Finance & Claims Analytics)](sources/processed/metric-loss-ratio.md), retrieved 2026-10-07*
