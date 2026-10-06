---
type: Business Rule
title: Total Loss Determination
description: Declares a personal auto vehicle a total loss when estimated repair cost reaches the threshold share of its actual cash value.
tags: [data, claims, business-rule, auto]
status: draft
generated: {by: archivist-author/1, at: 2026-10-06T01:50:20Z}
verified:
  - {by: process:archivist-verifier/1, at: 2026-10-06T01:50:34Z}
sources:
  - {resource: sources/processed/br-clm-014-auto-total-loss.md, title: BR-CLM-014 Total Loss Determination (Auto)}
  - {resource: sources/processed/2026-10-03-rules-triage-call--br-clm-014.md, title: "BR-CLM-014 — leased vehicle exception to the auto total loss rule"}
  - {resource: sources/processed/memo-total-loss-threshold-change.md, title: "Memo: change to the auto total-loss threshold (BR-CLM-014)"}
okfx_structure: business-rule
okfx_placement: {outcome: new}
okfx_rule_id: BR-CLM-014
okfx_line_of_business: auto
okfx_subject_area: claims
okfx_product_owner: claims-data@example.com
okfx_gaps: []
okfx_confidence: 1.0
---

## Rule Statement

A vehicle is declared a total loss when the estimated repair cost is 75% or more of its actual cash value (ACV) at the date of loss (for losses before 2027-01-01; see the change below). *Source: [BR-CLM-014 Total Loss Determination (Auto)](sources/processed/br-clm-014-auto-total-loss.md), retrieved 2026-10-05*

The threshold drops from 75% to 70% of actual cash value for losses on or after 2027-01-01; losses before that date keep the 75% threshold. *Source: [Memo: change to the auto total-loss threshold (BR-CLM-014)](sources/processed/memo-total-loss-threshold-change.md), retrieved 2026-10-05*

## Applies To

All personal auto physical damage claims (collision and comprehensive). *Source: [BR-CLM-014 Total Loss Determination (Auto)](sources/processed/br-clm-014-auto-total-loss.md), retrieved 2026-10-05*

## Exceptions

Leased vehicles are an exception: they go to the lessor's guide instead of the ACV threshold, and the adjuster documents which guide on the claim. This is effective November 1st, 2026, for auto only. *Source: [BR-CLM-014 — leased vehicle exception to the auto total loss rule](sources/processed/2026-10-03-rules-triage-call--br-clm-014.md), retrieved 2026-10-05*

## Effective Dates

- 2024-01-01: the rule takes effect. *Source: [BR-CLM-014 Total Loss Determination (Auto)](sources/processed/br-clm-014-auto-total-loss.md), retrieved 2026-10-05*
- November 1st, 2026: the leased vehicle exception takes effect, for auto only. *Source: [BR-CLM-014 — leased vehicle exception to the auto total loss rule](sources/processed/2026-10-03-rules-triage-call--br-clm-014.md), retrieved 2026-10-05*
- 2027-01-01: the 70% threshold applies to losses on or after this date. *Source: [Memo: change to the auto total-loss threshold (BR-CLM-014)](sources/processed/memo-total-loss-threshold-change.md), retrieved 2026-10-05*

## Data Implementation

The rule is flagged in the claims platform; the flag lands in CLAIM_HDR_SV as TOTAL_LOSS_IND = 'Y'. *Source: [BR-CLM-014 Total Loss Determination (Auto)](sources/processed/br-clm-014-auto-total-loss.md), retrieved 2026-10-05* There is no change to how the flag is stored. *Source: [Memo: change to the auto total-loss threshold (BR-CLM-014)](sources/processed/memo-total-loss-threshold-change.md), retrieved 2026-10-05*

## Rationale

Aligns with the state threshold most of the book is written in and with salvage recovery norms. *Source: [BR-CLM-014 Total Loss Determination (Auto)](sources/processed/br-clm-014-auto-total-loss.md), retrieved 2026-10-05*
