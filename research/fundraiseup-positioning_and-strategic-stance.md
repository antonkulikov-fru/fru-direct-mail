# Fundraise Up Positioning and Strategic Stance for Direct Mail Checks

## Strategic question
Should Fundraise Up build proprietary check digitization/scanning, or leverage partner rails and focus on donor migration to online checkout?

## Recommended stance (current evidence)
Adopt a hybrid, partner-first stance:
- Do not lead with "we replace lockbox/caging."
- Lead with "we convert direct-mail intent into digital lifetime value while preserving current check revenue."
- Integrate with existing lockbox/caging providers, bank rails, and in-house scanner workflows.
- Build owned capabilities in identity resolution, attribution, receipting, migration orchestration, and recurring conversion.

This is consistent with [generations-trends.md](./generations-trends.md):
- Older cohorts still drive large donation volume.
- Check usage is declining structurally.
- Digital completion is increasing, especially in younger cohorts and mixed-channel journeys.

Client-process evidence from [Indspire - Process for handling gifts received in the mail.md](./_inbox/Indspire%20-%20Process%20for%20handling%20gifts%20received%20in%20the%20mail.md) adds an important operating nuance:
- Not all nonprofits outsource intake to lockbox/caging providers.
- Some run in-house donor services workflows with bank cheque scanners and CRM batch controls.
- Exception handling is material (USD cheques, post-dated cheques, unreadable cheques, cash deposits, mailed credit card slips).

## Option comparison

| Option | Description | Upside | Downside | Strategic fit now |
|---|---|---|---|---|
| A. Build full check digitization stack | Own mail intake, scanning, and check operations end-to-end | Full rail control, potential long-term platform control | Commodity margin profile, operational burden, slower go-live, weaker differentiation if not tied to conversion | Medium to low (unless triggered by specific enterprise needs) |
| B. Partner-only with minimal product | Keep partners for checks, minimal FU product around it | Fast and low-cost | Limited differentiation, weak defensibility, low strategic upside | Low |
| C. Partner-first plus owned conversion layer | Partners handle capture/deposit, FU owns data/identity/conversion outcomes | Fast time-to-value plus differentiated growth story | Requires tight partner integrations and strong measurement discipline | High (recommended) |

## Positioning statement (internal)
Fundraise Up is not a lockbox replacement. Fundraise Up is the execution and value-realization layer that turns direct-mail responses into faster data, cleaner attribution, and higher digital lifetime value across outsourced and in-house intake models.

## What to build now
Priority capabilities:
- Standardized inbound schema for lockbox/caging files, bank scanner outputs, and manual batch events.
- Identity resolution and donor matching workflow.
- CRM writeback and reconciliation support.
- Mail-to-online conversion plays (QR, pURL, follow-up orchestration).
- Recurring migration journeys for check donors who are digitally reachable.
- Outcome measurement: conversion rate, repeat rate, and time-to-post.
- Exception workflow support for USD, post-dated, unreadable/unscannable cheques, and mailed credit-card entries.
- Maker-checker controls, audit trail, and document lifecycle controls (retention/shredding policy compatibility).

## What not to build now
- Full proprietary lockbox/scanning operations as primary GTM message.
- Pricing model anchored on percentage fee over check volume.

## Build trigger conditions (evidence-based, not hard-coded)
Re-evaluate proprietary check stack only when account-level data shows:
- Partner rails materially block conversion or data quality outcomes.
- High-value segments require tighter control that partners cannot provide.
- Economics with owned operations outperform partner model after fully loaded operational risk.

## Strategic narrative discipline
Use a two-track narrative:
- Track 1: protect legacy check revenue with low-friction partner-compatible flows.
- Track 2: accelerate migration of reachable donors to digital checkout and recurring.

Avoid binary framing ("checks or digital"). The evidence supports staged coexistence with directional migration.
