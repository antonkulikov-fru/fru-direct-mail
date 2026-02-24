# Direct Mail Channel Surface Strategy

## Why this exists
Capital allocation decisions require a concrete view of which execution surfaces Fundraise Up should support for direct-mail-originated donor intent.

## Ontology alignment
From the domain model:
- `direct_mail` is an intent-capture channel.
- Primary digital execution surfaces: `website`, `donor_portal`.
- `virtual_terminal` supports assisted/offline operator flows.

## Surface map by flow stage

| Flow stage | Channel context | Recommended execution surface | Notes |
|---|---|---|---|
| Donor receives appeal and decides to give online | Direct mail | Website checkout | Primary migration path via QR/pURL/short URL |
| Donor calls to give by phone | Direct mail + phone | Virtual terminal (assisted) | Needed for older cohorts and call-center conversion |
| Donor mails check/coupon | Direct mail + lockbox/caging or in-house scanner ops | Intake orchestration data layer + partner rails | Support both outsourced and in-house intake; ingest normalized events/data |
| Donor mails credit-card details/coupon | Direct mail + internal gift processing | Website checkout or virtual terminal recovery path | Replace rejections/manual re-entry with secure assisted or self-serve completion |
| Post-gift account management | Cross-channel | Donor portal | Receipts, updates, recurring management, payment method updates |

## Capability stack by surface

### Website checkout
- Personalized landing from mail identifier (QR/pURL/campaign code).
- Fast one-time and recurring setup.
- Attribution persisted to CRM and campaign analytics.

### Virtual terminal
- Assisted conversion for call-in donors.
- Agent workflow with campaign attribution and donor lookup.
- Consent and receipting controls.

### Intake orchestration data layer (not a public donor surface)
- Inbound file/event adapters from lockbox/caging and in-house scanner workflows.
- Batch QC, donor matching, exception handling.
- Reconciliation support to CRM/finance.
- Maker-checker approval support and audit trail coverage.

### Donor portal
- Self-serve recurring migration and payment updates.
- Receipt archive and communication preferences.

## Surface prioritization (recommended)
1. Website checkout for direct-mail-originated traffic.
2. Partner intake data layer for check/coupon processing continuity.
3. Virtual terminal enhancements for assisted migration.
4. Donor portal nudges for recurring conversion and retention.

## Core metrics by surface
- Website: mail-to-online conversion rate, recurring attach rate.
- Virtual terminal: assisted conversion rate, average handling time.
- Intake layer: match rate, time-to-post, exception rate, maker-checker cycle time.
- Donor portal: payment update completion, recurring retention.

## Design principle
Preserve donation capture across legacy behaviors while moving execution to digital surfaces wherever donor readiness allows.
