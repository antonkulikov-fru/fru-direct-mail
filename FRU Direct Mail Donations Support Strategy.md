# FRU Direct Mail Donations Support Strategy

## **Decision**

We should **not** invest in becoming a commodity check-processing provider.

We should invest in becoming the **orchestration and migration layer** that:

1. Helps nonprofits enrich CRM data and reach some donors with electronic receipts by ingesting results of offline payment processing into FRU.
2. Converts reachable offline donors to online giving and monetizes digital lifetime value through our commission model.

---

## **Context**

- Enterprise nonprofits already operate low-cost, well-controlled lockbox and in-house check workflows.
- Competing on per-check processing price is economically weak and strategically misaligned with our business model.
- Generational behavior is bifurcated:
    - Older cohorts still contribute a disproportionate share of charitable dollars and over-index on checks.
    - Younger cohorts are digital-first and frequently complete online even when prompted by mail.

Immediate check abandonment is unrealistic.

Long-term digital migration is inevitable.

The opportunity is not in replacing check processing — it is in capturing the digital lifetime value created when offline donors move online.

---

## **Where Fundraise Up Wins**

Fundraise Up is not:

- A lockbox replacement,
- A low-cost processor,
- A CRM substitute.

Fundraise Up is:

- The execution and orchestration layer between donor intent and payment infrastructure,
- The system that optimizes conversion, identity continuity, and recurring growth.

Direct mail should be treated as **intent capture**, not as a payment rail.

---

## **Strategic Approach**

### **Vector 1 — Continuity & Ingestion (Revenue Protection)**

Goal: Preserve offline revenue without operational disruption.

- Ingest lockbox/in-house outcomes via bulk upload/API pathways.
- Normalize data and support reconciliation.
- Perform lightweight donor matching where identifiers exist.
- Enable electronic receipting when possible.
- Maintain compliance-grade traceability.

Economic role:

- No direct revenue target.
- Protects revenue base.
- Creates the identity substrate for digital migration.

Explicit boundary:

If donor email is missing and no QR/PURL journey is used, orchestration stops at posting and receipting; no digital lift is created.

---

### **Vector 2 — Migration Engine (Revenue Growth)**

Goal: Convert reachable offline donors to digital recurring pathways.

- QR/PURL-enabled campaign flows.
- FRU-built capability to generate and track QR codes and personalized URLs for nonprofits.
- For participating campaigns, every outbound direct-mail pack should include QR and/or personalized URL on envelope and insert/letter.
- Mobile-first optimized checkouts.
- Mandatory email capture at digital touchpoints.
- Recurring attach where appropriate.
- Lifecycle stewardship through digital channels.

Economic role:

- Commission-bearing.
- Creates incremental LTV and recurring growth.
- Aligns with core business model.

Capital concentration should favor this vector.

---

## **Economic Discipline**

We will not monetize ingestion.

Revenue comes only from:

- Digital conversion,
- Recurring adoption,
- Increased donor lifetime value.

Offline processing at enterprise nonprofits is already cost-efficient (often ~$3/check or lower).

We should not allocate capital to compete as a commodity processor.

Investment in ingestion must remain tightly scoped and bounded.

Locked planning assumptions (current):

- Target payback window: **12 months**
- Effective net take rate (`r_take`): **2.9%**
- Major donor threshold: **$5,000+ single donation** (routed to separate major-donor experience)
- Initial ROI modeling unit: **per flagship enterprise account** (portfolio roll-up later)
- Vector 1 investment scope cap: **bulk ingestion + lightweight CRM mapping only** (no full lockbox replacement build)
- Vector 2 capability scope: **QR/PURL generation + tracking + campaign checkout support** (print/distribution execution remains with nonprofit/vendors)

---

## **Risk Framework**

Key risks:

- Forced migration alienates older/high-value donors.
- Identity resolution limits digital reach.
- Enterprise workflow misfit blocks adoption.
- Migration assumptions overstated.

Mitigation:

- Segment-based migration, not forced replacement.
- Treat identity capture as explicit gating metric.
- Pilot by cohort before scale investment.
- Maintain partner-compatible posture with banks and lockbox vendors.

---

## **Staged Capital Plan**

Stage 1 — Instrument & protect offline flows

Stage 2 — Pilot QR/PURL-driven migration by cohort

Stage 3 — Scale commission-bearing digital conversion

Stage 4 — Maintain legacy coverage for non-convertible and major-donor segments

---

## **Bottom Line**

This is not a “checks vs digital” decision.

Instead we are leading the charge and helping nonprofits convert offline donors to online (while routing major donors to a tailored experience) and protect legacy giving by helping ingest lockbox/offline outcomes into nonprofit systems.

Primary revenue creation starts only when offline donors complete FRU-powered online checkout and enter digital lifecycle stewardship.

---




## ROI Model
The detailed migration economics model has been split into a dedicated file:

- [FRU Direct Mail Migration ROI Model.md](./FRU%20Direct%20Mail%20Migration%20ROI%20Model.md)
