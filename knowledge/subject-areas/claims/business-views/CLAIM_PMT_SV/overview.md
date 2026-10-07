---
type: Business View Group Overview
title: CLAIM_PMT_SV
description: CLAIM_PMT_SV holds one row per payment transaction, with PMT_TYPE_CD values L, E and S.
tags: [data, claims, business-view-group-overview]
status: draft
generated: {by: archivist-author/1, at: 2026-10-07T13:07:47Z}
sources:
  - {resource: sources/processed/2026-09-30-claims-dw-office-hours--claim-pmt-sv.md, title: "CLAIM_PMT_SV — payment type codes and grain"}
okfx_structure: data-view-group
okfx_placement: {outcome: new}
okfx_subject_area: claims
okfx_physical_views: [CLAIM_PMT_SV]
okfx_code_repo: https://github.com/example-org/sample-claims-etl
okfx_product_owner: claims-data@example.com
okfx_gaps:
  - kind: unregistered_source_system
    origin: documentation
    description: The Data Sources & Ingestion Route section contains only a stub. The claims
      subject area has two registered source systems (Sample Claims Platform and Sample Policy
      Admin), but neither is named in the concept.
  - kind: undefined_acronym
    origin: documentation
    description: The concept uses VOID_IND in the Data Granularity section ("then there is
      a second row with VOID_IND Y") and Attribute Information section, but the acronym IND
      is not expanded. Neither the naming-standards registry nor the cited source document
      expands IND, leaving its meaning undefined.
  - kind: missing_section
    origin: author
    description: 'Overview and Business Rules & Usage Notes sections contain only stubs. Source
      provides substantive content: "Payment types: L (loss payment), E (expense with legal
      and adjuster fees), S (salvage recovery); one row per payment transaction; voided payments
      shown with VOID_IND Y" from sources/processed/2026-09-30-claims-dw-office-hours.md.'
verified:
  - {by: process:archivist-verifier/1, at: 2026-10-07T13:08:17Z}
okfx_confidence: 0.65
---

## Overview

*[Awaiting source material.]*

## Source

*[Awaiting source material.]*

## Data Sources & Ingestion Route

*[Awaiting source material.]*

## Data Granularity

One row per payment transaction, PMT_ID. A payment can be voided; then there is a second row with VOID_IND Y.

*Source: [CLAIM_PMT_SV — payment type codes and grain](sources/processed/2026-09-30-claims-dw-office-hours--claim-pmt-sv.md), retrieved 2026-10-07*

## Business Rules & Usage Notes

*[Awaiting source material.]*

## Other Key Concepts

*[Awaiting source material.]*

## Attribute Information

One row per payment transaction (PMT_ID). A payment can be voided; the void appears as a second row with VOID_IND Y.

*Source: [CLAIM_PMT_SV — payment type codes and grain](sources/processed/2026-09-30-claims-dw-office-hours--claim-pmt-sv.md), retrieved 2026-10-07*

## Code Set Information

PMT_TYPE_CD:
- L: loss payment
- E: expense; legal and adjuster fees go under E
- S: salvage recovery, which comes in as a negative amount

*Source: [CLAIM_PMT_SV — payment type codes and grain](sources/processed/2026-09-30-claims-dw-office-hours--claim-pmt-sv.md), retrieved 2026-10-07*

## Known Issues

*[Awaiting source material.]*

## FAQ

*[Awaiting source material.]*

## Glossary

*[Placeholder. Terms are reconciled against the registries in a later phase.]*
