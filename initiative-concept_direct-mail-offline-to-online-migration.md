**Status:** Draft

**Owner:** Product Strategy / Growth

**Type:** Strategic Concept

**Target decision:** Include on roadmap as a staged initiative with pilot-gated scale decision

---

## Executive Summary (Decision-Grade)

- **OKR:** Increase enterprise penetration and net revenue by converting direct-mail-originated donor intent into FRU-processed digital donations, while protecting legacy offline revenue.
- **Strategic role:** Expansion into new demand surface + monetization/yield optimization.
- **Core thesis:** Enterprise nonprofits already run cost-effective offline payment operations; FRU should not replace those rails, but should become the orchestration and migration layer that converts offline intent into digital lifetime value.
- **Expected impact & ROI:** Revenue impact is conversion-led only (no ingestion monetization). Payback target is 12 months per flagship account at 2.9% effective take rate; pilot scaling is gated by a numeric viability threshold table (not directional signals only).
- **Decision scope:** Commit now to Vector 1 (bounded ingestion support) + Vector 2 pilot capabilities (QR/PURL generation/tracking and migration journeys). Defer any proprietary check-scanning/lockbox operations pending stronger evidence.

---

# WHY — Strategic Rationale

---

## 1. Strategic Placement (Relevance Filter)

### 1.1 Initiative Type

Primary classification:

- ☑ Expansion into new demand surface

Secondary effects:

- Monetization / yield optimization
- Enterprise readiness / deal unblock

---

### 1.2 Strategic Vectors Advanced

- ☑ GPV expansion via new execution paths
- ☑ Enterprise readiness / deal unblock
- ☑ Donor lifetime value & retention
- ☑ Compliance / trust moat
- ☑ Channel or surface unification
- ☑ Attribution or data correctness

---

### 1.3 Strategic Capability Established

> “Today, the company cannot reliably convert direct-mail-originated offline donor activity into a unified, measurable digital lifecycle without relying on fragmented nonprofit-specific processes.
>
> This initiative establishes the capability to orchestrate partner-based offline intake into FRU and systematically migrate reachable donors to FRU-powered online checkout and recurring pathways.”

---

### 1.4 Strategic Non-Goals

- Not a lockbox or caging replacement strategy.
- Not a commodity check-processing margin play.
- Not a CRM replacement.
- Not a forced donor migration program that removes check pathways for older/high-value cohorts.

---

## 2. Market Reality & Demand (Reality Filter)

---

### 2.1 Market Size (Execution-Compatible)

**TAM — Total Economic Surface**

- Definition: U.S. charitable giving volume where direct-mail and offline-origin donor intent can influence final payment channel.
- Value range: upper bound is total U.S. charitable giving (`$592.5B`, 2024). Channel-attributable direct-mail/check share is not published as a single authoritative figure.
- Unit of analysis: donation dollars and donation execution flows.
- Includes non-serviceable demand by definition.

**Confidence**: Medium (for upper bound), Low (for direct-mail/check-specific split)

---

**SAM — Serviceable Addressable Market**

- Subset: enterprise nonprofits with material direct-mail/offline intake and willingness to run partner-compatible ingestion plus migration campaigns.
- Inclusion criteria:
  - meaningful offline/check flow,
  - CRM + finance workflow where FRU can ingest outcomes,
  - readiness to deploy QR/PURL-enabled mail-to-online journeys.
- Exclusion criteria:
  - organizations requiring immediate full replacement of treasury rails,
  - low-mail organizations with minimal offline volume.
- Structural constraints: legacy controls, vendor contracts, identity data quality, and compliance workflows.

**Confidence**: Medium

---

**SOM — Serviceable Obtainable Market (Phased)**

- Preconditions:
  - partner-compatible intake adapters,
  - donor matching and reconciliation integrity,
  - QR/PURL campaign capability with measurable conversion funnel.
- Adoption assumptions:
  - Phase 1: 3-5 flagship enterprise pilots,
  - Phase 2: expansion to adjacent archetypes if 12-month payback is achieved.
- Horizon: 12-month payback test per flagship account; 24-month scale horizon.

**Confidence**: Medium

---

### 2.2 Demand Evidence (Existence vs Realization)

| Org / Segment | Signal Type | Evidence | Realization Blocker | Risk |
| --- | --- | --- | --- | --- |
| Enterprise nonprofits (general) | Operational workaround | Established lockbox/caging and in-house scanner+CRM workflows | Existing flows optimize deposit/control, not cross-channel donor conversion | Low |
| Older donor-heavy nonprofits | Behavioral signal | Silent+Boomers account for large giving share (~26% + ~43% in cited research) | Abrupt check removal risks donor loss and internal resistance | Med |
| Mixed-age donor files | Behavioral signal | Millennials respond to mail but often complete online (53% in cited source set) | Mail and digital journeys are disconnected in most stacks | Med |
| FRU target enterprise accounts | Expansion blocker | Need for audit-grade ingestion and reconciliation before migration programs | Without intake continuity, GTM cannot credibly promise revenue protection | High |
| Industry channel trend | Market signal | U.S. checks decline structurally; online giving share increased (7.2% in 2014 to 12.8% in 2024 in compiled research) | Growth opportunity unrealized without identity continuity and campaign instrumentation | Low |

---

### 2.3 Demand Shape & Concentration (Optional)

- Concentrated in enterprise and high-volume direct-response organizations.
- Continuous demand with episodic peaks around major campaign windows.
- Realization is incremental (pilot-to-scale), not binary.

---

## 3. Problem Statements (Causality Filter)

1. Nonprofits process offline donations effectively for deposit and controls, but those flows are weakly connected to digital donor lifecycle and conversion outcomes.
2. FRU lacks a standardized way to ingest heterogeneous offline outcomes (lockbox, caging, in-house scanner workflows) into a conversion-ready donor identity layer.
3. Without QR/PURL-driven migration instrumentation, direct-mail-origin intent is under-monetized in digital channels where FRU has strongest economics.

---

## 4. Competitive Position & Non-Competition

- **Where FRU competes:**
  - mail-to-digital conversion performance,
  - donor identity continuity and attribution,
  - recurring adoption and lifecycle value realization.
- **Where FRU does not compete:**
  - physical mail opening/scanning operations,
  - commodity per-check clearing economics,
  - core treasury banking rails.
- **Why boundaries are intentional:**
  - incumbent lockbox/bank economics are structurally hard to beat on price,
  - FRU differentiation and monetization align with conversion and stewardship, not commodity check handling.

---

## 5. Alternatives & Trade-offs

### Considered Alternatives

- **Build full proprietary check stack**
  - Optimizes for rail ownership and process control.
  - Fails structurally now due to commodity economics, operational burden, and strategic misalignment with FRU value creation.
- **Partner-only, minimal product**
  - Optimizes for low effort and speed.
  - Fails structurally by creating weak differentiation and limited monetization upside.
- **Partner-first + owned migration layer (recommended)**
  - Optimizes for speed-to-value and defensible conversion outcomes.
  - Requires disciplined integration and measurement, but aligns with FRU business model.

### Explicit Trade-offs Accepted

- We do not optimize for lowest possible offline processing cost.
- We accept coexistence with legacy check pathways for non-convertible and major-donor segments.
- We prioritize measurable conversion lift over ownership of every operational step.

---

## 6. Strategic Priority & Opportunity Cost

- This initiative outranks generic feature work because it addresses a structural enterprise penetration constraint (existing offline operations) while opening a commission-bearing growth path.
- Cost of delay:
  - slower enterprise adoption where offline continuity is required,
  - lost digital conversion from direct-mail-origin donor intent,
  - weaker data continuity across channels.
- This is strategic, not incremental, because it adds a durable capability layer across channel, surface, and lifecycle boundaries.

---

# WHAT — System Definition

---

## 7. Ontological Placement

This initiative operates at the following levels:

- Channel: `direct_mail` (intent capture, not owned by FRU)
- Execution surfaces: `website`, `donor_portal`, `virtual_terminal`, `api`
- Donation model support: campaign and related recurring upgrades
- Execution mechanics: ingestion orchestration, identity resolution, conversion routing
- Lifecycle/system of record bridge: CRM and finance writeback support

Explicitly excluded layers:

- Owning channels/demand generation
- Replacing nonprofit CRM as source of truth
- Owning physical lockbox/caging operations

---

## 8. Glossary

| Term | Definition | Usage / Notes | Normative? |
| --- | --- | --- | --- |
| Direct-mail intent | Donor intent formed from physical mail appeal | Channel-level concept; can execute online or offline | Yes |
| Vector 1 (Continuity & Ingestion) | Support capability to ingest offline processing outcomes into FRU | No direct revenue target | Yes |
| Vector 2 (Migration Engine) | Conversion capability moving reachable offline donors to digital checkout | Revenue-bearing path | Yes |
| Reachable donor (`p_known`) | Offline donor with known digital contact before campaign | Known-contact migration base | Yes |
| QR/PURL acquisition path | Unknown-contact donor who enters digital journey via mailed QR or personalized URL | Expands reachable base through campaign mechanics | Yes |
| Major donor (`T_major`) | Donor with single gift >= `$5,000` | Routed to separate major-donor experience | Yes |
| `r_take` | Effective FRU net take rate on converted online dollars | Planning assumption: `2.9%` | Yes |
| Payback window | Time to recover build investment from contribution | Planning gate: `<= 12 months` | Yes |

---

## 9. Scope Boundaries

### 9.1 In Scope (System Responsibilities)

- Ingest lockbox/caging/in-house outcomes via bulk/API pathways.
- Normalize offline transaction and batch artifacts for reconciliation.
- Support lightweight donor matching and receipting where identity exists.
- Run an enrichment waterfall on unmatched records (name/address -> email/mobile append) through third-party identity providers to expand reachable base with auditable confidence scoring.
- Provide QR/PURL generation and tracking for campaign migration journeys.
- Route mail-origin traffic into optimized FRU checkout flows.
- Capture email at checkout and run recurring-upgrade prompts as a default optimization path.
- Maintain partner-compatible controls telemetry and auditability.

### 9.2 Out of Scope (Explicit Non-Goals)

- Building or operating physical lockbox/caging centers.
- Competing on per-check processing fees.
- Replacing nonprofit treasury systems or CRMs.
- Forcing all check donors to digital channels.

---

## 10. Concept-Level Invariants (Non-Negotiables)

- Ingestion/orchestration support is not monetized directly.
- Revenue starts only when donors complete FRU-powered digital checkout.
- Vector 1 must include identity enrichment to raise effective reachable base (`p_known_eff`) before Vector 2 spend is scaled.
- Vector 2 monetization assumes recurring-upgrade optimization is active in checkout and post-checkout lifecycle.
- Major-donor and non-convertible segments keep protected pathways.
- Partner compatibility with banks/lockbox/in-house controls is required.
- All scale decisions are pilot-gated by measured conversion and protection metrics.

---

## 11. Legal & Compliance Semantics

- Relevant constructs: tax receipting integrity, PCI/security handling, audit trail, retention/shredding policy compatibility, finance control evidence.
- Ownership of correctness:
  - nonprofit remains owner of legal/compliance obligations and system-of-record truth,
  - FRU owns orchestration semantics, data lineage, and execution telemetry within its platform boundary.
- Explicit non-computations by this initiative:
  - no independent tax/legal determination,
  - no replacement of regulatory reporting systems,
  - no independent check-clearing authority.

---

# HOW — Execution & Delivery

---

## 13. Sequencing & Validation

| Phase | Scope focus | Feasibility check | Desirability signal | Viability signal | Stop / Pause condition |
| --- | --- | --- | --- | --- | --- |
| Phase 0 | Baseline instrumentation on flagship account | Can ingest offline outcomes with reconciliation parity | Ops teams accept workflow fit | Baseline metrics captured | Ingestion breaks controls or data quality |
| Phase 1A | Vector 1 ingestion rollout | Match rate and time-to-post improve or hold | Low operational friction for gift processing teams | No material offline revenue disruption | Elevated exception/rework burden |
| Phase 1B | Vector 1 enrichment rollout | Enrichment append pipeline is compliant and stable | Teams accept enrichment-assisted receipting/matching | `p_known_eff` reaches minimum viable threshold | Enrichment lift too low or data-quality risk too high |
| Phase 2 | Vector 2 pilot (QR/PURL + campaign checkout) | End-to-end attribution and identity capture work | Donors engage QR/PURL journeys | Conversion-led contribution trend supports 12-month payback path | Conversion too low vs model threshold |
| Phase 3 | Controlled scale by archetype | Repeatability across 3-5 archetypes | Positive stakeholder adoption | Base-case payback <= 12 months per flagship account | Payback slips beyond threshold |

---

## 14. Dependencies & Risks

### Dependencies

| Dependency | Type (Tech / Legal / Data / Ops) | Impact if missing |
| --- | --- | --- |
| Inbound adapters for lockbox/caging/in-house files | Tech/Data | No credible continuity layer |
| CRM/finance reconciliation mapping | Data/Ops | Data trust breaks; adoption stalls |
| Identity enrichment partner(s) and policy-approved matching rules (e.g., Experian/LiveRamp-class) | Data/Legal/Ops | Reachable base remains too low for ROI |
| QR/PURL generation + campaign workflow support | Tech/Ops | No scalable migration path |
| Gift-processing control compatibility (maker-checker, audit artifacts) | Ops/Legal | Enterprise rejection risk |
| Account-level pilot sponsorship | Ops/GTM | Cannot validate economics |

### Risks & Mitigations

| Risk | Impact | Likelihood | Mitigation | Kill / Pause trigger |
| --- | --- | --- | --- | --- |
| Forced migration harms older donor retention | High | Med | Segment-based migration; preserve check path | Material revenue drop in protected cohorts |
| Low known-contact coverage | High | High | Run enrichment waterfall to lift `p_known_eff`; pair with QR/PURL acquisition path | `p_known_eff` remains below viable threshold |
| Weak QR/PURL response | High | Med | Campaign experimentation and placement standards | Cannot reach conversion required for 12-month payback |
| Enterprise process mismatch | High | Med | Fit to in-house and outsourced workflows; controls-first rollout | Persistent control exceptions/audit concerns |
| Overstated ROI assumptions | High | Med | Conservative/base/aggressive scenarios; pilot-calibrated inputs | Base-case payback > 12 months |

---

## 15. Expected Impact

### 15.1 Capability Impact

- FRU gains a repeatable capability to bridge offline-origin donor activity to digital lifecycle execution without owning physical payment rails.

### 15.2 Realization Path

- Capability -> ingestion + enrichment raise reachable base -> QR/PURL and outreach drive digital checkout -> recurring-upgrade prompts increase donation frequency -> FRU revenue via 2.9% take rate on converted digital volume.
- Nonprofit value realization includes faster stewardship loops and reduced reconciliation friction, improving adoption probability.

### 15.3 Sensitivity Drivers

- `p_known` (pre-campaign reachable share),
- QR/PURL visit and identity-capture rates,
- checkout completion and stickiness,
- bounded Vector 1 implementation cost,
- stability of offline protected revenue.

### 15.4 Viability Threshold Table (Board Gate)

| Metric | Minimum viable | Target | Kill threshold |
| --- | ---: | ---: | ---: |
| `p_known` (known-contact share) | `>= 35%` | `>= 45%` | `< 25%` |
| `p_enrich_match` (new reachable from enrichment on unknown base) | `>= 12%` | `>= 20%` | `< 8%` |
| `p_visit_qr` (QR/PURL visit from unknown base) | `>= 6%` | `>= 10%` | `< 3%` |
| `p_id_capture_qr` (identity captured on QR/PURL journey) | `>= 55%` | `>= 70%` | `< 40%` |
| `p_checkout_known` | `>= 55%` | `>= 65%` | `< 45%` |
| `p_checkout_qr` | `>= 45%` | `>= 60%` | `< 35%` |
| `p_stick_blended` (post-conversion stickiness) | `>= 60%` | `>= 70%` | `< 50%` |
| `p_recur_attach` (recurring attach from converted donors) | `>= 20%` | `>= 30%` | `< 12%` |
| `p_convert_blended` (offline base converted online) | `>= 5.0%` | `>= 8.0%` | `< 3.5%` |
| Base-case payback | `<= 12 months` | `<= 9 months` | `> 18 months` |

Example check from review:
- Given `p_known=40%`, `p_visit_qr=8%`, `p_checkout=60%`, viability is not determined by these 3 values alone.
- Using conservative companion assumptions (`p_enrich_match=12%`, `p_engage_known=25%`, `p_id_capture_qr=60%`, `p_stick_known=70%`, `p_stick_qr=65%`), estimated `p_convert_blended ≈ 6.1%`.
- Interpretation: borderline viable. It becomes clearly viable only if enrichment lift and recurring attach meet minimum thresholds and account-level 12-month payback still clears after full costs.

### 15.5 Failure Mode Narrative

If `p_convert_blended` stays below `5.0%` across two pilot waves, this initiative should be treated as a defensive enterprise-enablement capability (ingestion/continuity) rather than a growth engine, and scale investment should pause.

---

## 16. Investment, Effort & ROI

### R&D Effort (One-time)

| Team | Scope | Est. MM | Est. Cost |
| --- | --- | --- | --- |
| Product + Engineering | Vector 1 core (ingestion adapters, normalization, reconciliation primitives) | 4-6 | TBD by staffing plan |
| Product + Engineering + Data | Vector 1B enrichment layer (provider connectors, matching confidence, suppression/consent controls) | 2-3 | TBD by staffing plan |
| Product + Engineering | Phase 2 MVP only (QR/PURL generation, campaign routing, baseline funnel telemetry) | 3-5 | TBD by staffing plan |
| Product + Engineering | Phase 2 scale pack (advanced experimentation/automation), conditional after gate | 5-9 | Deferred until pilot gates pass |
| Data/Analytics | Pilot instrumentation and threshold tracking | 1-2 | TBD |
| Security/Compliance | Controls and audit compatibility hardening | 1-2 | TBD |

**Total:** Modeled as `C_build = C_v1_build + C_v1b_build + C_v2_build` in ROI model.

Phase 2 MVP containment (explicit):
- No broad automation suite before pilot proof.
- No expansion to non-flagship segments before threshold pass.
- No additional scale-pack investment unless base-case payback remains `<= 12 months`.
- No Phase 2 scale spend unless recurring-upgrade metrics (`p_recur_attach`) clear minimum viable threshold.

### GTM / Operational Effort (Post-Launch)

| Workstream | Scope | Timeframe | Est. Cost |
| --- | --- | --- | --- |
| CSM + Solutions | Flagship pilot onboarding and workflow mapping | First 90-120 days | TBD |
| Campaign Ops | QR/PURL migration campaign setup and experimentation | Ongoing per pilot | TBD |
| Support/Ops | Exception monitoring and controls reporting | Ongoing | TBD |

### ROI (Cash-Flow Aware)

- Planning assumptions:
  - payback target: 12 months,
  - `r_take = 2.9%`,
  - major donor threshold: `$5,000+` routed separately,
  - initial model: per flagship enterprise account.
- Break-even requirement:
  - `V_required_12m = (C_build + Σ_{t=1..12} C_total_t) / r_take`
- Decision rule:
  - scale only if base-case pilot model indicates payback <= 12 months and no material erosion of protected offline revenue.
- Explicit separation:
  - capability build (Vector 1 + Vector 2) does not equal realized revenue; realization depends on conversion funnel performance.

---

## Appendix

- Research links and synthesized evidence:
  - [research/generations-trends.md](./research/generations-trends.md)
  - [research/nonprofit-profiles_jtbd.md](./research/nonprofit-profiles_jtbd.md)
  - [research/offline-payments_competitive-landscape.md](./research/offline-payments_competitive-landscape.md)
  - [research/actors-and-entities-map.md](./research/actors-and-entities-map.md)
  - [research/direct-mail-channel_surface-strategy.md](./research/direct-mail-channel_surface-strategy.md)
  - [research/capital-allocation_evidence-backlog.md](./research/capital-allocation_evidence-backlog.md)
- Strategy and economics inputs:
  - [FRU Direct Mail Donations Support Strategy.md](./FRU%20Direct%20Mail%20Donations%20Support%20Strategy.md)
  - [FRU Direct Mail Migration ROI Model.md](./FRU%20Direct%20Mail%20Migration%20ROI%20Model.md)
  - [FRU Business Model Overview.md](./_inbox/FRU%20Business%20Model%20Overview.md)
  - [ontology.json](./_inbox/ontology.json)
- Open questions:
  - Account-level baseline values for `p_known`, QR/PURL response, and exception mix by archetype
  - Final staffing-cost assumptions for `C_v1_build`, `C_v2_build`, and run-rate costs
