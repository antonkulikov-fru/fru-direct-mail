# FRU Direct Mail Migration ROI Model

## Locked planning assumptions
- Target payback window: **12 months**
- Effective FRU take rate (`r_take`): **2.9%**
- Major donor threshold (`T_major`): **$5,000+ single gift**
- Initial decision unit: **one flagship enterprise nonprofit account**
- Channel execution assumption: FRU provides QR/PURL generation + tracking + checkout capability; nonprofit and its mail vendors handle printing/distribution

## Model structure
Use two linked models:
1. FRU investment ROI model (primary capital allocation decision).
2. Nonprofit economic value model (customer business case).

## 1) FRU ROI model

### 1.1 Modeling unit and segmentation
Model first at flagship-account level, then roll up to ICP portfolio.

Segment by `s` (recommended):
- donor cohort (Silent/Boomer/Gen X/Millennial/Gen Z),
- gift band (major vs non-major),
- source vendor/process path where relevant.

Route `gift >= T_major` to the major-donor experience and exclude from standard migration math unless intentionally scoped in.

### 1.2 Dual-path migration funnel (per segment `s`)
Let:
- `V_offline_s` = annual offline donation dollars in segment `s` (checks/cash/money order outcomes)
- `p_known_s` = share of offline dollars linked to donors with known digital contact before campaign
- `u_amount_s` = average gift amount multiplier after migration (`online gift amount / prior offline amount`)
- `u_freq_s` = average annual gift frequency multiplier after migration

Path A: Known-contact migration
- `p_engage_known_s` = probability known-contact donors engage outreach
- `p_checkout_known_s` = probability engaged donors complete online checkout
- `p_stick_known_s` = probability converted donors remain online for subsequent gifts
- `V_known_conv_s = V_offline_s * p_known_s * p_engage_known_s * p_checkout_known_s * p_stick_known_s * u_amount_s * u_freq_s`

Path B: QR/PURL acquisition migration (from unknown-contact base)
- `p_visit_qr_s` = probability unknown-contact donors visit FRU journey via mailed QR/PURL
- `p_id_capture_qr_s` = probability visit yields usable donor identity (email at minimum)
- `p_checkout_qr_s` = probability identified QR/PURL visitors complete checkout
- `p_stick_qr_s` = probability QR/PURL-converted donors remain online for subsequent gifts
- `V_qr_conv_s = V_offline_s * (1 - p_known_s) * p_visit_qr_s * p_id_capture_qr_s * p_checkout_qr_s * p_stick_qr_s * u_amount_s * u_freq_s`

Total converted online dollars:
- `V_converted_s = V_known_conv_s + V_qr_conv_s`
- `V_converted_total = Σ_s V_converted_s`

Reporting bridge to legacy `p_reachable`:
- `p_reachable_equiv_s = p_known_s + (1 - p_known_s) * p_visit_qr_s * p_id_capture_qr_s`

Use `p_reachable_equiv` for dashboard compatibility; keep dual-path math for investment decisions.

### 1.3 FRU revenue and contribution
Revenue:
- `R_FRU_t = V_converted_total_t * r_take` (default planning value: `r_take = 2.9%`)

Costs:
- `C_v1_build` = Vector 1 build (bulk upload adapters, lightweight CRM mapping, controls compatibility)
- `C_v2_build` = Vector 2 build (QR/PURL generation, tracking, campaign tooling, experimentation foundation)
- `C_build = C_v1_build + C_v2_build`
- `C_fixed_t` = fixed operating cost in period `t` (support, CSM, product maintenance)
- `C_var_t` = variable cost in period `t` (campaign ops, messaging, testing)
- `C_total_t = C_fixed_t + C_var_t`

Contribution:
- `CM_t = R_FRU_t - C_total_t`

Investment return:
- `Payback period` = first `t` where cumulative `CM_t >= C_build`
- `ROI_12m = (Σ_{t=1..12} CM_t - C_build) / C_build`
- Optional: `NPV = -C_build + Σ_{t=1..N} CM_t / (1 + d)^t`

### 1.4 Break-even shortcuts (12-month planning lens)
Required converted online dollars for 12-month break-even:
- `V_required_12m = (C_build + Σ_{t=1..12} C_total_t) / r_take`

Required blended conversion from offline base:
- `p_convert_required_12m = V_required_12m / (Σ_s (V_offline_s * u_amount_s * u_freq_s))`

Interpretation:
- if modeled combined path conversion (`known + QR/PURL`) is below `p_convert_required_12m`, do not scale.

## 2) Nonprofit economic value model (customer case)
Let:
- `V_converted_total_t` from above
- `m_margin_gain_t` = net margin effect on converted dollars after fees/handling mix
- `B_speed_t` = treasury value of faster cash availability
- `B_ops_t` = operational savings (manual handling/rework reduction)
- `B_leakage_t` = recovered value from reduced offline loss/failure
- `C_campaign_t` = campaign execution cost (copy/creative/vendor coordination)
- `C_change_t` = change-management effort

Nonprofit value by period:
- `Value_NP_t = (V_converted_total_t * m_margin_gain_t) + B_speed_t + B_ops_t + B_leakage_t - C_campaign_t - C_change_t`

Use this model for adoption narrative; FRU capital decision remains gated by FRU ROI.

## 3) Scope boundary (critical)
Vector 1 is support-only:
- bulk ingestion,
- lightweight mapping/integration,
- controls compatibility,
- no direct ingestion monetization.

Vector 2 is growth engine:
- QR/PURL capability must be available for nonprofit campaigns,
- participating direct-mail packs should carry QR/PURL on envelope and insert/letter,
- revenue starts only when donor completes FRU-powered online checkout.

If `p_known` is low and QR/PURL visit/identity capture rates are weak, ROI will not clear 12-month payback.

## 4) Recommended scenario framework
Run at least 3 scenarios per flagship account:
- `Conservative`: low known-contact share, low QR/PURL response, weak stickiness.
- `Base`: pilot-calibrated assumptions.
- `Aggressive`: stronger response and recurring lift.

For each scenario output:
- converted online dollars,
- FRU revenue,
- contribution margin,
- payback months (must be `<= 12` for go),
- `ROI_12m`,
- sensitivity to QR/PURL response and known-contact coverage.

## 5) Input sheet template
Populate this table before estimation.

| Input | Symbol | Unit | Notes |
|---|---|---|---|
| Annual offline dollars (total) | `V_offline_total` | USD/year | Flagship account baseline |
| Offline dollars by segment | `V_offline_s` | USD/year | By generation/gift band/source |
| Known-contact share | `p_known_s` | % | Pre-campaign reachable base |
| QR/PURL visit rate (unknown base) | `p_visit_qr_s` | % | Scan/type-to-visit from mailed assets |
| QR/PURL identity capture rate | `p_id_capture_qr_s` | % | Email captured (minimum) |
| Known-contact engagement rate | `p_engage_known_s` | % | Open/click/visit from outreach |
| Known-contact checkout completion | `p_checkout_known_s` | % | Engage-to-complete |
| QR/PURL checkout completion | `p_checkout_qr_s` | % | Visit/identified-to-complete |
| Known-path stickiness | `p_stick_known_s` | % | Persist online after conversion |
| QR/PURL-path stickiness | `p_stick_qr_s` | % | Persist online after conversion |
| Amount multiplier | `u_amount_s` | x | Online amount effect |
| Frequency multiplier | `u_freq_s` | x | Online frequency effect |
| FRU net take rate | `r_take` | % of processed USD | Planning default: `2.9%` |
| Major donor threshold | `T_major` | USD/gift | Planning default: `$5,000` |
| Vector 1 build cost | `C_v1_build` | USD | Bulk upload + light CRM mapping only |
| Vector 2 build cost | `C_v2_build` | USD | QR/PURL platform + campaign tooling |
| Fixed run cost | `C_fixed_t` | USD/period | Support/product/CSM |
| Variable run cost | `C_var_t` | USD/period | Campaign ops and experimentation |

## 6) Pilot instrumentation requirements
Capture:
- offline dollars by segment and major/non-major split,
- known-email rate among offline donors,
- QR/PURL placement coverage in mailed packages,
- QR scan/type-in visit rate by campaign asset,
- identity capture rate, checkout completion, recurring attach,
- donor retention post-conversion,
- exception/manual handling effort,
- time-to-cash and receipting deltas.

## 7) Go / No-go investment gates
Proceed with scaled investment only if pilot evidence shows:
- projected payback `<= 12 months` per flagship account (base case),
- no material erosion of protected offline revenue,
- viable QR/PURL-led expansion of reachable donor base,
- major-donor flow remains stable via dedicated experience.
