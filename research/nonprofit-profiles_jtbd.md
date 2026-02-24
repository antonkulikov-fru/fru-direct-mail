# Nonprofit Profiles for Direct Mail Check Transition (JTBD Lens)

## Purpose
This document defines nonprofit archetypes for capital allocation decisions on direct-mail support.
It combines:
- generational evidence from [generations-trends.md](./generations-trends.md),
- process realities from the direct-mail flow artifacts,
- JTBD push/pull/inertia/anxiety framing.

## Baseline (U.S. market level)
Use this as default prior when sector data is missing:
- Boomers: ~43% of charitable dollars.
- Silent: ~26% of charitable dollars.
- Gen X: ~22% of charitable dollars.
- Millennials: ~11% of charitable dollars.
- Gen Z: growing online-first participation, low check affinity.

Source: [generations-trends.md](./generations-trends.md)

## Client process signal (important)
Observed in [Indspire - Process for handling gifts received in the mail.md](./_inbox/Indspire%20-%20Process%20for%20handling%20gifts%20received%20in%20the%20mail.md):
- In-house mail intake with cheque scanner deposits and CRM gift batching is a real operating model.
- Manual controls are extensive (batch limits, adding tapes, dual review/commit, filing/shredding).
- Exception branches are operationally significant (USD, post-dated, unreadable cheques, cash, mailed credit cards).

## Archetype Profiles
Note: donor-generation splits below are working hypotheses for ICP planning. Validate with CRM/export data per account.

| Archetype | Donor-by-generation split (working hypothesis) | Current check-processing setup (common) | JTBD push forces | JTBD pull forces | JTBD inertia/anxiety | Implication for Fundraise Up |
|---|---|---|---|---|---|---|
| In-house donor services teams (scanner + CRM batching) | Often older-biased check file; mix varies by mission | Internal mail pickup, sorting, cheque scanner deposits, manual CRM batches, maker-checker review | Manual workload, exception queues, reconciliation overhead, key-person risk | Workflow automation, stronger controls, faster time-to-post, reduced rework | Compliance and process-change anxiety; fear of breaking audit trail | High-fit for intake orchestration and exception management without replacing bank rails |
| Faith-based organizations | Silent+Boomer heavy (`60-80%` of check volume), Gen X secondary | Bank lockbox or in-house counting/deposit; monthly batch posting to CRM/finance | Slower deposit cycles; manual reconciliation; delayed receipts; aging donor file | Faster receipting, cleaner donor matching, migration to digital recurring for next gifts | Fear of alienating older donors; staff habit around weekly check handling; finance control concerns | Keep check path available; lead on "mail to digital recurring" journey for next gift, not forced first gift |
| Higher education and alumni programs | Boomer+Gen X dominant for major and annual mail gifts; Millennials rising in participation | Outsourced lockbox/caging + advancement CRM imports | Complex attribution (fund/designation); reconciliation workload across entities/funds | Better attribution and faster acknowledgment; pURL and QR conversion for younger alumni | Concern about gift designation errors; donor expectation for traditional pledge/remit process | Position as conversion + attribution layer; partner for lockbox intake |
| Health systems and hospital foundations | Older grateful-patient donors over-index in check usage; younger family donors more digital | Mix of lockbox and in-house posting; strong finance controls | Slow posting to patient/foundation systems; duplicate records; audit/QC burden | Faster batch QC, cleaner donor identity, immediate confirmation options | Compliance/privacy anxiety; treasury process lock-in | Focus on data quality + receipting speed + donor identity continuity |
| National direct-response charities (human services, animal welfare, veterans, etc.) | Mixed file; check-heavy legacy segments, online-heavy acquisition segments | Caging vendor or agency-managed lockbox; high-volume remittance operations | Cost and delay from manual exceptions; low visibility of donor migration opportunity | Segment-level migration programs; multi-touch conversion to online checkout | Existing agency/vendor contracts; uncertainty on migration ROI | Strong fit for partner-first ingestion + controlled migration experiments |
| Advocacy and membership organizations | Older donors still check-skewed for mail; younger cohorts digital-first and event-driven | Lockbox + CRM import + periodic reconciliation | Cycle-time pressure (campaign windows), fragmented channels | Real-time attribution and fast mobilization after gift | Risk that payment friction lowers campaign response | Emphasize speed to usable donor data and fast digital follow-up |

## JTBD statement (cross-profile)
When a donor responds to a direct-mail appeal, teams need to capture and clear the gift quickly, match the donor accurately, post it cleanly to CRM/finance, send acknowledgment promptly, and move eligible donors to easier digital repeat giving without reducing current response.

## Segmentation flags for go-to-market
Prioritize accounts with:
- High mail volume and delayed posting windows.
- Large `55+` donor share and weak digital follow-up motions.
- Multiple entities/banks causing reconciliation drag.
- Existing lockbox vendor in place but poor data handoff quality.
- In-house teams with high manual batch effort and frequent exception handling.

Deprioritize near-term:
- Organizations with low mail share and already high digital completion.
- Accounts requiring full replacement of entrenched treasury rails as first step.

## Evidence gaps to close per account
Before pricing/build decisions, capture:
- % revenue from mailed checks by segment and campaign type.
- Time from mail receipt to CRM-posted gift.
- Match rate from lockbox or scanner batch file to CRM contact.
- 12-month repeat rate of check donors vs digital donors.
- Share of check donors with valid email/mobile for migration.
- Exception mix (% USD, post-dated, unscannable, credit-card rejections).
