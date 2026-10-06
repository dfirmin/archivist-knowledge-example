---
title: "CUSTCASE_INCRMTL_SV — timezone of LAST_UPDT_TS"
extracted_from: sources/processed/2026-09-30-claims-dw-office-hours.md
---

About: CUSTCASE_INCRMTL_SV and the timezone of its LAST_UPDT_TS column compared with the base CUSTCASE view.

> 00:00:14 Jo Park
> ok so first one, LAST_UPDT_TS on CUSTCASE_INCRMTL_SV, is that UTC or eastern

> 00:00:19 Sam Ortiz
> it's UTC. everything on the incremental views is UTC, the base CUSTCASE view is eastern, which, yeah, I know

> 00:00:26 Jo Park
> ugh ok that explains the off by four hours thing
