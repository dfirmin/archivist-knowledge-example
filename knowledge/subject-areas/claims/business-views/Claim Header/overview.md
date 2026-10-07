---
type: Business View Group Overview
title: Claim Header
description: CLAIM_HDR_SV holds one row per claim reported to the Sample Claims Platform.
tags: [data, claims, business-view-group-overview]
status: draft
generated: {by: archivist-author/1, at: 2026-10-07T13:06:18Z}
verified: [{by: process:archivist-verifier/1, at: 2026-10-07T13:06:37Z}]
sources:
  - {resource: sources/processed/catalog-claim-header-essential-information.md, title: "CLAIM_HDR_SV (Claim Header) - Essential Information"}
okfx_structure: data-view-group
okfx_placement: {outcome: new}
okfx_subject_area: claims
okfx_physical_views: [CLAIM_HDR_SV]
okfx_code_repo: https://github.com/example-org/sample-claims-etl
okfx_product_owner: claims-data@example.com
okfx_gaps:
  - kind: missing_section
    origin: documentation
    description: 'Three required author-owned sections hold only stubs: Business Rules & Usage
      Notes, Other Key Concepts, and FAQ. The cited source (catalog-claim-header-essential-information.md)
      provides no content for these sections.'
  - kind: missing_code_value_semantics
    origin: documentation
    description: Code Set Information lists LOB_CD values (AUTO, HOME, COMM) without their
      business meanings. The cited source also names only the values without explaining what
      each abbreviation represents.
  - kind: undefined_acronym
    origin: documentation
    description: The body uses "ET" in "Loaded nightly from the Sample Claims Platform at
      02:00 ET" without defining the acronym. The abbreviation does not appear in naming-standards
      or glossary registries, and the cited source also uses it without expansion.
okfx_confidence: 0.65
---

## Overview

CLAIM_HDR_SV holds one row per claim reported to the Sample Claims Platform, with the claim's status, loss date, reported date and line of business. It is the starting point for claim counts and for joining payments (CLAIM_PMT_SV) and exposure.

*Source: [CLAIM_HDR_SV (Claim Header) - Essential Information](sources/processed/catalog-claim-header-essential-information.md), retrieved 2026-10-07*

## Source

Loaded nightly from the Sample Claims Platform.

*Source: [CLAIM_HDR_SV (Claim Header) - Essential Information](sources/processed/catalog-claim-header-essential-information.md), retrieved 2026-10-07*

## Data Sources & Ingestion Route

Loaded nightly from the Sample Claims Platform at 02:00 ET.

*Source: [CLAIM_HDR_SV (Claim Header) - Essential Information](sources/processed/catalog-claim-header-essential-information.md), retrieved 2026-10-07*

## Data Granularity

One row per claim (CLAIM_ID). A claim reopened after closing keeps its CLAIM_ID; the reopen is visible in CLAIM_STATUS_CD and REOPEN_DT.

*Source: [CLAIM_HDR_SV (Claim Header) - Essential Information](sources/processed/catalog-claim-header-essential-information.md), retrieved 2026-10-07*

## Business Rules & Usage Notes

*[Awaiting source material.]*

## Other Key Concepts

*[Awaiting source material.]*

## Attribute Information

| Column | Meaning |
|--------|---------|
| CLAIM_ID | Claim identifier |
| LOB_CD | Line of business: AUTO, HOME, COMM |
| CLAIM_STATUS_CD | O open, C closed, R reopened |
| LOSS_DT | Date of loss |
| RPT_DT | Date the claim was reported |
| REOPEN_DT | Most recent reopen date, null if never reopened |

*Source: [CLAIM_HDR_SV (Claim Header) - Essential Information](sources/processed/catalog-claim-header-essential-information.md), retrieved 2026-10-07*

## Code Set Information

- LOB_CD: AUTO, HOME, COMM
- CLAIM_STATUS_CD: O open, C closed, R reopened

*Source: [CLAIM_HDR_SV (Claim Header) - Essential Information](sources/processed/catalog-claim-header-essential-information.md), retrieved 2026-10-07*

## Known Issues

Claims migrated from the old platform before 2019 have RPT_DT equal to LOSS_DT.

*Source: [CLAIM_HDR_SV (Claim Header) - Essential Information](sources/processed/catalog-claim-header-essential-information.md), retrieved 2026-10-07*

## FAQ

*[Awaiting source material.]*

## Glossary

*[Placeholder. Terms are reconciled against the registries in a later phase.]*
