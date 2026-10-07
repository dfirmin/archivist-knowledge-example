---
title: "CLAIM_PMT_SV — payment type codes and grain"
extracted_from: sources/processed/2026-09-30-claims-dw-office-hours.md
---

About: CLAIM_PMT_SV PMT_TYPE_CD values, grain and voided payments.

> 00:01:04 Raj Iyer
> ok mine is CLAIM_PMT_SV, what are the PMT_TYPE_CD values
> 00:01:08 Sam Ortiz
> L is loss payment, E is expense, um, legal and adjuster fees go under E, and S is salvage recovery which comes in as a negative amount
> 00:01:17 Raj Iyer
> negative, got it. one row per payment?
> 00:01:20 Sam Ortiz
> one row per payment transaction, PMT_ID, and a payment can be voided, then there's a second row with VOID_IND Y
