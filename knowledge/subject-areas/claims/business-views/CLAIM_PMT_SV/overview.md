---
type: Business View Group Overview
title: CLAIM_PMT_SV
description: CLAIM_PMT_SV has one row per payment transaction, and its PMT_TYPE_CD codes are L, E and S.
tags: [data, claims, business-view-group-overview]
status: draft
generated: {by: archivist-author/1, at: 2026-10-06T01:56:21Z}
verified: [{by: process:archivist-verifier/1, at: 2026-10-06T01:56:34Z}]
sources:
  - {resource: sources/processed/2026-09-30-claims-dw-office-hours--claim-pmt-sv.md, title: "CLAIM_PMT_SV — PMT_TYPE_CD values and grain"}
okfx_structure: data-view-group
okfx_placement: {outcome: new}
okfx_subject_area: claims
okfx_physical_views: [CLAIM_PMT_SV]
okfx_code_repo: https://github.com/example-org/sample-claims-etl
okfx_product_owner: claims-data@example.com
okfx_gaps:
  - kind: missing_section
    origin: documentation
    description: 'Eight required author-owned sections lack substantive content: Overview,
      Source, Data Sources & Ingestion Route, Business Rules & Usage Notes, Other Key Concepts,
      Attribute Information, Known Issues, and FAQ each contain only placeholder text. The
      cited source addresses only PMT_TYPE_CD values and data granularity.'
  - kind: unregistered_source_system
    origin: documentation
    description: The Data Sources & Ingestion Route section contains only an 'Awaiting source
      material' stub. The cited source (2026-09-30-claims-dw-office-hours--claim-pmt-sv.md)
      does not name any registered source system for the claims subject area (Sample Claims
      Platform or Sample Policy Admin).
  - kind: undefined_acronym
    origin: documentation
    description: Body uses IND (in VOID_IND, line 34) which does not appear in naming-standards,
      glossary, or in the cited source 2026-09-30-claims-dw-office-hours--claim-pmt-sv.md.
okfx_confidence: 0.30
---

## Overview

*[Awaiting source material.]*

## Source

*[Awaiting source material.]*

## Data Sources & Ingestion Route

*[Awaiting source material.]*

## Data Granularity

One row per payment transaction (PMT_ID). A payment can be voided, in which case there is a second row with VOID_IND Y.

*Source: [CLAIM_PMT_SV — PMT_TYPE_CD values and grain](sources/processed/2026-09-30-claims-dw-office-hours--claim-pmt-sv.md), retrieved 2026-10-05*

## Business Rules & Usage Notes

*[Awaiting source material.]*

## Other Key Concepts

*[Awaiting source material.]*

## Attribute Information

*[Awaiting source material.]*

## Code Set Information

PMT_TYPE_CD values:

- L: loss payment
- E: expense; legal and adjuster fees go under E
- S: salvage recovery, which comes in as a negative amount

*Source: [CLAIM_PMT_SV — PMT_TYPE_CD values and grain](sources/processed/2026-09-30-claims-dw-office-hours--claim-pmt-sv.md), retrieved 2026-10-05*

## Known Issues

*[Awaiting source material.]*

## FAQ

*[Awaiting source material.]*

## Glossary

*[Placeholder. Terms are reconciled against the registries in a later phase.]*
