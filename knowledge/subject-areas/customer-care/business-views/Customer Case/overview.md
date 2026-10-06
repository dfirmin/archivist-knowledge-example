---
type: Business View Group Overview
title: Customer Case
description: CUSTCASE holds one row per customer support case opened in Sample CRM.
tags: [data, customer-care, business-view-group-overview]
status: draft
generated: {by: archivist-author/1, at: 2026-10-06T01:46:39Z}
sources:
  - {resource: sources/processed/catalog-custcase-essential-information.md, title: "CUSTCASE (Customer Case) - Essential Information"}
  - {resource: sources/processed/2026-09-30-claims-dw-office-hours--custcase-incrmtl-sv.md, title: "CUSTCASE_INCRMTL_SV — timezone of LAST_UPDT_TS"}
  - {resource: sources/processed/catalog-custcase-code-sets.md, title: "CUSTCASE (Customer Case) - Code Sets"}
  - {resource: sources/processed/re-incremental-feed-columns.md, title: "RE: incremental feed - which columns change?"}
verified:
  - {by: process:archivist-verifier/1, at: 2026-10-06T01:46:58Z}
okfx_structure: data-view-group
okfx_placement: {outcome: new}
okfx_subject_area: customer-care
okfx_physical_views: [CUSTCASE, CUSTCASE_INCRMTL_SV]
okfx_code_repo: https://github.com/example-org/sample-case-etl
okfx_product_owner: customer-care@example.com
okfx_confidence: 0.40
okfx_gaps:
  - kind: unregistered_source_system
    origin: author
    description: 'Data Sources & Ingestion Route names "CRM extract" but omits the registered
      source system "Sample CRM," although the cited source states: "CUSTCASE holds one row
      per customer support case opened in Sample CRM."'
  - kind: missing_section
    origin: author
    description: 'Four required sections contain only stubs: Source, Other Key Concepts, Known
      Issues, and FAQ. Sources contain information for at least Known Issues (the timezone
      discrepancy documented in "ugh ok that explains the off by four hours thing" from 2026-09-30-claims-dw-office-hours--custcase-incrmtl-sv.md)
      and FAQ (Q&A content in re-incremental-feed-columns.md and timezone discussion).'
  - kind: undefined_acronym
    origin: documentation
    description: The Attribute Information section uses "UTC" without defining it. UTC is
      not listed in the glossary or naming-standards registries, and cited sources (sources/processed/2026-09-30-claims-dw-office-hours--custcase-incrmtl-sv.md)
      reference it as a timezone fact without defining the acronym.
---

## Overview

CUSTCASE holds one row per customer support case opened in Sample CRM.

*Source: [CUSTCASE (Customer Case) - Essential Information](sources/processed/catalog-custcase-essential-information.md), retrieved 2026-10-05*

## Source

*[Awaiting source material.]*

## Data Sources & Ingestion Route

Cases are loaded nightly from the CRM extract and a case appears once it has been assigned a case number.

*Source: [CUSTCASE (Customer Case) - Essential Information](sources/processed/catalog-custcase-essential-information.md), retrieved 2026-10-05*

## Data Granularity

One row per case (CASE_ID). Closed cases are retained for seven years.

*Source: [CUSTCASE (Customer Case) - Essential Information](sources/processed/catalog-custcase-essential-information.md), retrieved 2026-10-05*

## Business Rules & Usage Notes

Use CUSTCASE_INCRMTL_SV for change-data loads; it carries only cases touched since the last run.

*Source: [CUSTCASE (Customer Case) - Essential Information](sources/processed/catalog-custcase-essential-information.md), retrieved 2026-10-05*

## Other Key Concepts

*[Awaiting source material.]*

## Attribute Information

LAST_UPDT_TS on CUSTCASE_INCRMTL_SV is UTC. Everything on the incremental views is UTC, while the base CUSTCASE view is eastern.

*Source: [CUSTCASE_INCRMTL_SV — timezone of LAST_UPDT_TS](sources/processed/2026-09-30-claims-dw-office-hours--custcase-incrmtl-sv.md), retrieved 2026-10-05*

In CUSTCASE_INCRMTL_SV only the status columns change between loads. CASE_STATUS_CD and CASE_STATUS_TS are updated when a case moves, and LAST_UPDT_TS is set on every change. Everything else is insert-only. Dedupe on CASE_ID + LAST_UPDT_TS and take the latest. Cases are never deleted; a withdrawn case just gets CASE_STATUS_CD = 'W'.

*Source: ["RE: incremental feed - which columns change?"](sources/processed/re-incremental-feed-columns.md), retrieved 2026-10-05*

## Code Set Information

CASE_STATUS_CD values: O (open), P (pending customer), C (closed).

*Source: [CUSTCASE (Customer Case) - Essential Information](sources/processed/catalog-custcase-essential-information.md), retrieved 2026-10-05*

A withdrawn case gets CASE_STATUS_CD = 'W'.

*Source: ["RE: incremental feed - which columns change?"](sources/processed/re-incremental-feed-columns.md), retrieved 2026-10-05*

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

*Source: [CUSTCASE (Customer Case) - Code Sets](sources/processed/catalog-custcase-code-sets.md), retrieved 2026-10-05*

## Known Issues

*[Awaiting source material.]*

## FAQ

*[Awaiting source material.]*

## Glossary

*[Placeholder. Terms are reconciled against the registries in a later phase.]*
