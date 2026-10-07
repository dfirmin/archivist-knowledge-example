---
type: Business View Group Overview
title: Customer Case
description: CUSTCASE holds one row per customer support case opened in Sample CRM.
tags: [data, customer-care, business-view-group-overview]
status: draft
generated: {by: archivist-author/1, at: 2026-10-07T13:08:03Z}
verified: [{by: process:archivist-verifier/1, at: 2026-10-07T13:08:28Z}]
sources:
  - {resource: sources/processed/catalog-custcase-essential-information.md, title: "CUSTCASE (Customer Case) - Essential Information"}
  - {resource: sources/processed/2026-09-30-claims-dw-office-hours--custcase-incrmtl-sv.md, title: "CUSTCASE_INCRMTL_SV — timestamp time zone"}
  - {resource: sources/processed/catalog-custcase-code-sets.md, title: "CUSTCASE (Customer Case) - Code Sets"}
  - {resource: sources/processed/re-incremental-feed-columns.md, title: "RE: incremental feed - which columns change?"}
okfx_structure: data-view-group
okfx_placement: {outcome: new}
okfx_subject_area: customer-care
okfx_confidence: 0.58
okfx_physical_views: [CUSTCASE, CUSTCASE_INCRMTL_SV]
okfx_code_repo: https://github.com/example-org/sample-case-etl
okfx_product_owner: customer-care@example.com
okfx_gaps:
  - kind: missing_section
    origin: documentation
    description: 'Three required author-owned sections contain only stubs: Other Key Concepts,
      Known Issues, and FAQ. The four cited sources provide no information for these sections.'
  - kind: unregistered_source_system
    origin: author
    description: 'Data Sources & Ingestion Route section names no registered source system
      for customer-care. The registered system Sample CRM is not named, although sources/processed/catalog-custcase-essential-information.md
      states: "CUSTCASE holds one row per customer support case opened in Sample CRM."'
  - kind: undefined_acronym
    origin: documentation
    description: The concept uses UTC to designate timestamp precision ("LAST_UPDT_TS...is
      UTC" and "Everything on the incremental views is UTC") without defining it. UTC does
      not appear in the glossary or naming-standards registries, and the cited source states
      only "it's UTC" without expansion.
---

## Overview

CUSTCASE holds one row per customer support case opened in Sample CRM.

*Source: [CUSTCASE (Customer Case) - Essential Information](sources/processed/catalog-custcase-essential-information.md), retrieved 2026-10-07*

## Source

Cases are opened in Sample CRM.

*Source: [CUSTCASE (Customer Case) - Essential Information](sources/processed/catalog-custcase-essential-information.md), retrieved 2026-10-07*

## Data Sources & Ingestion Route

Cases are loaded nightly from the CRM extract, and a case appears once it has been assigned a case number. CUSTCASE_INCRMTL_SV is used for change-data loads; it carries only cases touched since the last run.

*Source: [CUSTCASE (Customer Case) - Essential Information](sources/processed/catalog-custcase-essential-information.md), retrieved 2026-10-07*

## Data Granularity

One row per case (CASE_ID). Closed cases are retained for seven years.

*Source: [CUSTCASE (Customer Case) - Essential Information](sources/processed/catalog-custcase-essential-information.md), retrieved 2026-10-07*

## Business Rules & Usage Notes

LAST_UPDT_TS on CUSTCASE_INCRMTL_SV is UTC. Everything on the incremental views is UTC, while the base CUSTCASE view is eastern.

*Source: [CUSTCASE_INCRMTL_SV — timestamp time zone](sources/processed/2026-09-30-claims-dw-office-hours--custcase-incrmtl-sv.md), retrieved 2026-10-07*

To avoid double counting in CUSTCASE_INCRMTL_SV, dedupe on CASE_ID + LAST_UPDT_TS and take the latest.

*Source: [RE: incremental feed - which columns change?](sources/processed/re-incremental-feed-columns.md), retrieved 2026-10-07*

## Other Key Concepts

*[Awaiting source material.]*

## Attribute Information

In CUSTCASE_INCRMTL_SV, only the status columns change between loads. CASE_STATUS_CD and CASE_STATUS_TS get updated when a case moves, and LAST_UPDT_TS is set on every change. Everything else is insert-only.

*Source: [RE: incremental feed - which columns change?](sources/processed/re-incremental-feed-columns.md), retrieved 2026-10-07*

## Code Set Information

CASE_STATUS_CD: O (open), P (pending customer), C (closed).

*Source: [CUSTCASE (Customer Case) - Essential Information](sources/processed/catalog-custcase-essential-information.md), retrieved 2026-10-07*

CASE_STATUS_CD also takes the value W for a withdrawn case; cases are never deleted.

*Source: [RE: incremental feed - which columns change?](sources/processed/re-incremental-feed-columns.md), retrieved 2026-10-07*

CASE_PRIORITY_CD

| Code | Meaning |
|------|---------|
| 1 | Urgent: customer cannot use the product |
| 2 | High: major function impaired |
| 3 | Normal |

CASE_CHANNEL_CD

| Code | Meaning |
|------|---------|
| PH | Phone |
| EM | Email |
| WB | Web form |

*Source: [CUSTCASE (Customer Case) - Code Sets](sources/processed/catalog-custcase-code-sets.md), retrieved 2026-10-07*

## Known Issues

*[Awaiting source material.]*

## FAQ

*[Awaiting source material.]*

## Glossary

*[Placeholder. Terms are reconciled against the registries in a later phase.]*
