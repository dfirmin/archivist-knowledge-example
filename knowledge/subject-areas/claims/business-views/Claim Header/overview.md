---
type: Business View Group Overview
title: Claim Header
description: CLAIM_HDR_SV holds one row per claim reported to the Sample Claims Platform and is the starting point for claim counts.
tags: [data, claims, business-view-group-overview]
status: draft
generated: {by: archivist-author/1, at: 2026-10-06T01:42:28Z}
verified:
  - {by: process:archivist-verifier/1, at: 2026-10-06T01:42:39Z}
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
    description: 'Four required sections contain only "Awaiting source material" stubs: Source,
      Business Rules & Usage Notes, Other Key Concepts, and FAQ. The cited source (catalog-claim-header-essential-information.md)
      provides no substantive content for these sections.'
  - kind: missing_code_value_semantics
    origin: documentation
    description: LOB_CD code values (AUTO, HOME, COMM) are listed without business meaning.
      The source document and concept show these codes but do not explain what each stands
      for.
  - kind: undefined_acronym
    origin: documentation
    description: The concept uses undefined acronyms DT, RPT, and LOB. DT appears in LOSS_DT,
      RPT_DT, and REOPEN_DT; RPT in RPT_DT; LOB in LOB_CD. None are defined in the naming-standards
      or glossary registries, and the sole cited source catalog-claim-header-essential-information.md
      does not expand them.
okfx_confidence: 0.60
---

## Overview

CLAIM_HDR_SV holds one row per claim reported to the Sample Claims Platform, with the claim's status, loss date, reported date and line of business. It is the starting point for claim counts and for joining payments (CLAIM_PMT_SV) and exposure.

*Source: [CLAIM_HDR_SV (Claim Header) - Essential Information](sources/processed/catalog-claim-header-essential-information.md), retrieved 2026-10-05*

## Source

*[Awaiting source material.]*

## Data Sources & Ingestion Route

Loaded nightly from the Sample Claims Platform at 02:00 ET.

*Source: [CLAIM_HDR_SV (Claim Header) - Essential Information](sources/processed/catalog-claim-header-essential-information.md), retrieved 2026-10-05*

## Data Granularity

One row per claim (CLAIM_ID). A claim reopened after closing keeps its CLAIM_ID; the reopen is visible in CLAIM_STATUS_CD and REOPEN_DT.

*Source: [CLAIM_HDR_SV (Claim Header) - Essential Information](sources/processed/catalog-claim-header-essential-information.md), retrieved 2026-10-05*

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

*Source: [CLAIM_HDR_SV (Claim Header) - Essential Information](sources/processed/catalog-claim-header-essential-information.md), retrieved 2026-10-05*

## Code Set Information

- LOB_CD (line of business): AUTO, HOME, COMM
- CLAIM_STATUS_CD: O open, C closed, R reopened

*Source: [CLAIM_HDR_SV (Claim Header) - Essential Information](sources/processed/catalog-claim-header-essential-information.md), retrieved 2026-10-05*

## Known Issues

Claims migrated from the old platform before 2019 have RPT_DT equal to LOSS_DT.

*Source: [CLAIM_HDR_SV (Claim Header) - Essential Information](sources/processed/catalog-claim-header-essential-information.md), retrieved 2026-10-05*

## FAQ

*[Awaiting source material.]*

## Glossary

*[Placeholder. Terms are reconciled against the registries in a later phase.]*
