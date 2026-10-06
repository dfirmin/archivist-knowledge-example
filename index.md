---
okf_version: "0.2"
---

# Subject areas

## Claims

* [CLAIM_PMT_SV](knowledge/subject-areas/claims/business-views/CLAIM_PMT_SV/overview.md) - CLAIM_PMT_SV has one row per payment transaction, and its PMT_TYPE_CD codes are L, E and S. Confidence 0.30.
* [Claim Header](knowledge/subject-areas/claims/business-views/Claim%20Header/overview.md) - CLAIM_HDR_SV holds one row per claim reported to the Sample Claims Platform and is the starting point for claim counts. Confidence 0.60.
* [Loss Ratio](knowledge/subject-areas/claims/metrics/Loss%20Ratio.md) - Loss ratio measures how much of the premium is paid back out in losses, reported monthly by line of business. Confidence 1.00.
* [Open Claim Count](knowledge/subject-areas/claims/metrics/Open%20Claim%20Count.md) - The open claims KPI in the Monday deck is a count of claims in CLAIM_HDR_SV whose status is open or reopened, broken out by line of business. Confidence 1.00.
* [Total Loss Determination](knowledge/subject-areas/claims/rules/auto/BR-CLM-014.md) - Declares a personal auto vehicle a total loss when estimated repair cost reaches the threshold share of its actual cash value. Confidence 1.00.

## Customer Care

* [Customer Care](knowledge/subject-areas/customer-care/overview.md) - The customer care subject area covers customers contacting the company for help, including contacts, cases, and how cases move from open to closed. Confidence 0.85.
* [Customer Case](knowledge/subject-areas/customer-care/business-views/Customer%20Case/overview.md) - CUSTCASE holds one row per customer support case opened in Sample CRM. Confidence 0.40.

## Sources

- Waiting to be authored: `sources/inbox/`
- Authored and cited: `sources/processed/`
