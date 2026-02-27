# NPO ROI Model (Direct Mail: Offline vs Hybrid Offline+Online)

## 1) Purpose
Estimate whether moving part of direct-mail donation flow from offline processing to online checkout improves **nonprofit net donation dollars**.

## 2) Inputs
- `R` = direct-mail reached donors (count)
- `c0` = baseline conversion rate to donation (offline-only), decimal
- `c1` = hybrid conversion rate to donation (offline+online), decimal
- `A` = average donation amount (USD)
- `h` = online share of donations in hybrid scenario, decimal
- `u_off` = offline processing cost per donation (lockbox/caging + internal), USD
- `f` = online processing/commission rate (default `0.029`)
- `s_check, s_cash, s_bank, s_other` = offline payment-form split (sum to `1.0`)  
  Note: split is for form-level volume visibility; core economics use `u_off`.

## 3) Baseline Scenario (Offline-Only)
- `D0 = R * c0`
- `G0 = D0 * A`
- `C0 = D0 * u_off`
- `N0 = G0 - C0`

Where:
- `D0` = donations count
- `G0` = gross donation dollars
- `C0` = processing cost
- `N0` = net donation dollars

## 4) Hybrid Scenario (Offline + Online)
- `D1 = R * c1`
- `D1_off = D1 * (1 - h)`
- `D1_on = D1 * h`
- `G1 = D1 * A`
- `C1_off = D1_off * u_off`
- `C1_on = (D1_on * A) * f`
- `C1 = C1_off + C1_on`
- `N1 = G1 - C1`

## 5) Split Visibility (Offline Portion)
- `Check_count = D_off * s_check`
- `Cash_count = D_off * s_cash`
- `Bank_count = D_off * s_bank`
- `Other_count = D_off * s_other`

Apply for `D_off = D0` (baseline) and `D_off = D1_off` (hybrid).

## 6) Core Decision Metrics
- `Delta_donations = D1 - D0`
- `Delta_gross = G1 - G0`
- `Delta_cost = C1 - C0`
- `Delta_net = N1 - N0`

Interpretation:
- `Delta_net > 0` -> switching case is positive.
- `Delta_net <= 0` -> switching case is not justified under current assumptions.

## 7) Required Hybrid Conversion (Break-even)
Solve `N1 = N0` for `c1`:

- `c1_required = c0 * (A - u_off) / (A - (1 - h)*u_off - h*A*f)`

Decision:
- If `c1 > c1_required`, hybrid outperforms baseline.
- If `c1 <= c1_required`, baseline is equal or better.

## 8) Practical Guardrails
- `c1` should be greater than `c0` for a real switching thesis.
- Keep `A` realistic by channel/campaign cohort (do not overfit with optimistic gift size).
- Validate `u_off` with actual finance + ops data (not only vendor quote).
- Track offline split changes over time, but avoid overcomplicating cost model unless form-specific costs materially differ.
