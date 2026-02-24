# Actors and Entities Map (Direct Mail and Offline Donations)

## Scope
This map covers the ecosystem around direct-mail and offline donation handling, including check/cash/card-mail workflows and migration to digital checkout.

## 1) Actors

Tag legend for FRU relationship:
- `Direct competitor`
- `Indirect competitor`
- `Customer`
- `Customer stakeholder`
- `Partner`
- `Regulator`
- `Neutral infrastructure`
- `Self`

### A. Core market actors
| Actor | Role in the flow | Primary incentives | FRU relationship |
|---|---|---|---|
| Donors (individuals, households) | Respond to outreach; give via check, cash, mailed card details, phone, or online | Trust, convenience, control, mission impact, low friction | Customer-end user |
| Nonprofits (organization) | Own donor relationships, campaigns, compliance obligations, and revenue outcomes | Net revenue, donor retention, compliance, operational efficiency | Customer |
| Fundraise Up | Orchestration/execution/value-realization layer across donation journeys | Growth in processed digital value, retention uplift, product defensibility | Self |
| Stripe (and payment processing layer) | Processes online card/wallet payments and related rails | Payment volume, reliability, risk control, platform expansion | Partner |

### B. Nonprofit internal actors
| Actor | Role in the flow | Primary incentives | FRU relationship |
|---|---|---|---|
| Development/Fundraising leadership | Strategy, campaign mix, ROI accountability | Revenue growth, donor LTV, channel performance | Customer stakeholder |
| Donor relations / gift processing | Mail intake, batching, posting, receipting, donor care | Accuracy, throughput, controls, donor satisfaction | Customer stakeholder |
| Database/CRM admins | Data quality, identity matching, integration operations | Clean data, low rework, dependable reporting | Customer stakeholder |
| Finance/Accounting/Treasury | Reconciliation, deposits, audit trails, cash controls | Financial accuracy, control integrity, close speed | Customer stakeholder |
| Compliance/Legal/InfoSec | PCI/privacy/retention policy governance | Risk reduction, regulatory compliance | Customer stakeholder |
| Call center / donor support | Assisted gifts, issue resolution, migration conversations | Conversion, quality, service levels | Customer stakeholder |

### C. External operational actors
| Actor | Role in the flow | Primary incentives | FRU relationship |
|---|---|---|---|
| Outreach vendors (direct mail agencies, canvassing, telemarketing) | Generate offline response and donor intent | Campaign performance, contract renewal | Partner (sometimes channel partner) |
| Print and mail houses | Produce and distribute appeal materials | Throughput, quality, SLA adherence | Partner |
| USPS / postal carriers / couriers | Physical transport of appeals and remittances | Delivery performance | Neutral infrastructure |
| Lockbox/caging providers | Open mail, process remittances, create deposit/data files | Operational efficiency, processing accuracy | Indirect competitor and partner |
| Banks (nonprofit bank, lockbox bank, issuer/acquirer banks) | Deposit, settlement, treasury controls | Transaction volume, risk control, client retention | Indirect competitor and partner |
| Card networks and ACH rails | Move payment instructions and settlement | Network reliability, transaction growth | Partner infrastructure |

### D. Platform/data ecosystem actors
| Actor | Role in the flow | Primary incentives | FRU relationship |
|---|---|---|---|
| Digital fundraising checkout platforms (e.g., Classy/GoFundMe Pro, Donorbox, Givebutter, Bloomerang+Qgiv) | Competing donation checkout and fundraising execution stack | Volume growth, platform adoption, retention | Direct competitor |
| CRM platforms (e.g., Raiser’s Edge, Bonterra/EveryAction, Salesforce-based stacks) | System of record for donor/gift data; some have native giving workflows | Platform stickiness, data centrality | Indirect competitor and integration partner |
| Accounting/ERP platforms | Financial posting and reconciliation records | Integrity and controllership | Integration partner |
| PSP-first custom stacks / SIs (build directly on payment rails) | Substitute implementation path for nonprofit digital giving | Service revenue, custom control | Direct competitor (implementation path) |
| Enrichment/identity vendors | Append/validate contact identity for migration workflows | Data usage, match performance | Partner |
| Address/NCOA validation providers | Postal data quality and deliverability support | Accuracy and volume | Partner |
| Fraud/risk vendors | Fraud scoring and risk controls | Detection performance | Partner |

### E. Governance and oversight actors
| Actor | Role in the flow | Primary incentives | FRU relationship |
|---|---|---|---|
| IRS | Federal tax treatment and charitable status oversight | Tax compliance | Regulator |
| State charity regulators (AG/SoS, US state level) | Solicitation and charitable compliance oversight | Donor protection, legal compliance | Regulator |
| PCI DSS ecosystem (card brands/assessors) | Card data security standards | Security compliance | Regulator/standards body |
| External auditors | Process and financial control assurance | Audit quality and compliance | Oversight stakeholder |

## 2) Entities (Non-actor objects)

### Donation and payment entities
- Donation intent
- Appeal/campaign
- Gift transaction
- Payment instrument (`check`, `cash`, `mailed card details`, `phone card`, `online card/wallet`, `ACH`)
- Recurring mandate/subscription
- Refund/chargeback/reversal

### Data and identity entities
- Donor profile
- Contact identifiers (email, phone, postal address)
- Matching keys and confidence scores
- Consent and communication preferences
- Gift attribution metadata (campaign/fund/appeal/source)

### Operations and controls entities
- Mail piece, return envelope, reply coupon
- Batch, deposit log, control reports, reconciliation reports
- Exception queue items (USD checks, post-dated, unscannable, rejected cards)
- Audit trail records
- Retention/shredding records

### Compliance entities
- Tax receipt / acknowledgment
- PCI-sensitive data artifacts
- Policy documents and procedure controls

## 3) Relationship map (high-level)

| From | To | Relationship |
|---|---|---|
| Donor | Nonprofit | Gives and receives stewardship |
| Nonprofit | Outreach vendors | Contracts for donor acquisition/appeal execution |
| Outreach vendors | Donor | Creates offline donation intent |
| Donor | Postal/courier | Sends remittance (check/cash/card slip/coupon) |
| Postal/courier | Lockbox/caging or in-house team | Delivers physical donations |
| Lockbox/caging / in-house processing | Bank | Deposits funds |
| Lockbox/caging / in-house processing | CRM + accounting | Sends batch/deposit data for posting and reconciliation |
| Nonprofit | Fundraise Up | Uses orchestration/conversion capabilities |
| Fundraise Up | Stripe / payment rails | Executes digital checkout transactions |
| Fundraise Up | CRM/accounting | Synchronizes donor/gift/attribution data |
| Nonprofit + vendors + Fundraise Up | Donor | Runs migration from offline repeat behavior to digital recurring |
| IRS / regulators / PCI / auditors | Nonprofit + vendors + platforms | Enforce/verify legal and control compliance |

## 4) Modeling note
- `Actors` are decision-making parties (people/orgs/systems that perform actions).
- `Entities` are things acted on (transactions, batches, records, artifacts).
- `Offline donations` belong in entities, not actors.
