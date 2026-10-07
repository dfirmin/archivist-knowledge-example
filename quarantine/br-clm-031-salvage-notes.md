---
type: Business Rule
title: Salvage assignment
description: Salvage must be assigned to a salvage vendor within 3 business days of the total-loss decision.
tags: [data, claims, business-rule]
status: quarantined
generated: {by: archivist-author/1, at: 2026-10-07T13:05:29Z}
sources:
  - {resource: sources/quarantine/br-clm-031-salvage-notes.md, title: "BR-CLM-031 salvage assignment (notes)"}
okfx_structure: business-rule
okfx_rule_id: BR-CLM-031
okfx_subject_area: claims
okfx_product_owner: claims-data@example.com
okfx_quarantine:
  reason: The document states no line of business ("LOB to be confirmed with product"), so the required okfx_line_of_business has no value.
  needs: A line-of-business key from lines-of-business (auto, home or commercial) confirmed by product for BR-CLM-031, stated in the document.
---

## Rule Statement

Once a vehicle is declared a total loss, salvage must be assigned to a salvage vendor within 3 business days of the total-loss decision.

*Source: [BR-CLM-031 salvage assignment (notes)](sources/quarantine/br-clm-031-salvage-notes.md), retrieved 2026-10-07*

## Applies To

*[Awaiting source material.]*

## Effective Dates

Effective 2025-06-01.

*Source: [BR-CLM-031 salvage assignment (notes)](sources/quarantine/br-clm-031-salvage-notes.md), retrieved 2026-10-07*

## Data Implementation

Assignment is recorded in the claims platform and shows as SALVAGE_ASSIGN_DT on the claim.

*Source: [BR-CLM-031 salvage assignment (notes)](sources/quarantine/br-clm-031-salvage-notes.md), retrieved 2026-10-07*
