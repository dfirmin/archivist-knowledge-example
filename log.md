# Directory Update Log

## 2026-10-06

* **Creation**: [Case Handling Process](/knowledge/subject-areas/case-handling-process/overview.md) — how support cases are worked: the process framework, components and roles, not a data product.
* **Creation**: [Customer Care](/knowledge/subject-areas/customer-care/overview.md) — the customer care subject area: contacts, cases and how cases move from open to closed, loaded nightly from Sample CRM [Customer Care].
* **Quarantined**: [Salvage assignment](/quarantine/br-clm-031-salvage-notes.md) — The document states no line of business ("LOB to be confirmed with product"), so the required okfx_line_of_business has no value [Claims].
* **Creation**: [CLAIM_PMT_SV](/knowledge/subject-areas/claims/business-views/CLAIM_PMT_SV/overview.md) — one row per payment transaction, with the PMT_TYPE_CD codes L, E and S [Claims].
* **Creation**: [Open Claim Count](/knowledge/subject-areas/claims/metrics/Open%20Claim%20Count.md) — OPEN_CLAIM_CNT, claims in open or reopened status by line of business, with the exclusion window moving from 24 to 48 hours [Claims].
* **Creation**: [Loss Ratio](/knowledge/subject-areas/claims/metrics/Loss%20Ratio.md) — LOSS_RATIO, incurred losses over earned premium (denominator corrected from written premium), monthly by line of business [Claims].
* **Creation**: [Total Loss Determination](/knowledge/subject-areas/claims/rules/auto/BR-CLM-014.md) — BR-CLM-014, personal auto total loss threshold (75%, 70% from 2027-01-01) and leased-vehicle exception [Claims].
* **Creation**: [Customer Case](/knowledge/subject-areas/customer-care/business-views/Customer%20Case/overview.md) — CUSTCASE and CUSTCASE_INCRMTL_SV, one row per customer support case, with code sets and timezone notes [Customer Care].
* **Creation**: [Claim Header](/knowledge/subject-areas/claims/business-views/Claim%20Header/overview.md) — CLAIM_HDR_SV, one row per claim, the starting point for claim counts [Claims].
* **Quarantined**: [LEGACY_FEED — what it is](/quarantine/2026-09-30-claims-dw-office-hours--legacy-feed.md) — Out of scope: the inventory row for LEGACY_FEED has subject_area UNKNOWN (unresolved subject area for LEGACY_FEED).
* **Quarantined**: [FW: RE: what is LEGACY_FEED??](/quarantine/fw-legacy-feed-question.md) — Out of scope: the inventory row for LEGACY_FEED has subject_area UNKNOWN (unresolved subject area for LEGACY_FEED).
* **Quarantined**: [Policy Churn Rate (draft definition)](/quarantine/metric-policy-churn-rate.md) — Out of scope: no metrics row for Policy Churn Rate; the document itself says it is not yet on the approved metric list.

## Initial scaffold

* **Initialization**: Created foundational directory structure.
