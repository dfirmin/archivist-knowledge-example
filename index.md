---
okf_version: "0.2"
---

# Subject areas

## Case Handling Process

* [Case Handling Process](knowledge/subject-areas/case-handling-process/overview.md) - Describes how support cases are worked, as a process rather than a data product. Confidence 0.80.

## Claims

* [CLAIM_PMT_SV](knowledge/subject-areas/claims/business-views/CLAIM_PMT_SV/overview.md) - CLAIM_PMT_SV holds one row per payment transaction, with PMT_TYPE_CD values L, E and S. Confidence 0.65.
* [Claim Header](knowledge/subject-areas/claims/business-views/Claim%20Header/overview.md) - CLAIM_HDR_SV holds one row per claim reported to the Sample Claims Platform. Confidence 0.65.
* [Loss Ratio](knowledge/subject-areas/claims/metrics/Loss%20Ratio.md) - Loss ratio measures how much of the premium is paid back out in losses, reported monthly by line of business. Confidence 1.0.
* [Open Claim Count](knowledge/subject-areas/claims/metrics/Open%20Claim%20Count.md) - Open Claim Count is the number of claims in CLAIM_HDR_SV with status O or R, as counted for the Monday deck. Confidence 1.0.
* [Total Loss Determination](knowledge/subject-areas/claims/rules/auto/BR-CLM-014.md) - Business rule BR-CLM-014 declares a personal auto vehicle a total loss when repair cost reaches a threshold share of actual cash value. Confidence 1.0.

## Customer Care

* [Customer Care](knowledge/subject-areas/customer-care/overview.md) - The customer care subject area covers customers contacting the company for help, including contacts and cases. Confidence 0.85.
* [Customer Case](knowledge/subject-areas/customer-care/business-views/Customer%20Case/overview.md) - CUSTCASE holds one row per customer support case opened in Sample CRM. Confidence 0.58.

## Sources

- Waiting to be authored: `sources/inbox/`
- Authored and cited: `sources/processed/`
