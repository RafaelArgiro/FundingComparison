# Apex Data Health

Status of the Apex source material in this folder, for the purpose of comparing funding
options for daytrading.

Files reviewed:

- `LegacyProductOverview.md`
- `legacyEvaluationAccounts.md`
- `lefacyPerfAccountTradingRules.md`
- `LegacyPayouts.md`
- `LegacyTrailingDrawdown.md`
- `newFeatEarlyAccountUpdateNotifications.md`

---

## 1. Blocking issue: all captured data describes retired products

Every Apex file in this folder documents **Legacy** products. `LegacyProductOverview.md`
states that Apex retired the previous Evaluation and Performance accounts as of
**March 1, 2026**, and that Legacy evaluation accounts are "no longer available for
purchase to anyone".

The products that can currently be purchased are **Intraday PA** and **EOD PA**. These
are named exactly once in the captured material (in the rule that the combined total of
active Legacy PA, Intraday PA and EOD PA must not exceed 20 per household) and are never
documented.

Consequence: Apex cannot be placed in a tradeoff against other providers using this data.
The following is missing for the new account types:

- Evaluation rules, profit targets and minimum trading days
- Drawdown model (the new EOD type implies a different drawdown mechanic than the Legacy
  intraday trailing drawdown)
- Contract limits per account size
- Pricing (evaluation subscription, activation fee, reset fee)
- Payout parameters (minimum balance, maximum payout, split, consistency rules)

---

## 2. Internal contradictions

| # | Contradiction | Where |
|---|---|---|
| 1 | "Legacy accounts purchased **on or after March 1, 2026**, are only eligible for the One-Time Lifetime PA Activation Fee option." But the overview states nothing can be purchased on or after that date. | `legacyEvaluationAccounts.md` (How to Activate your Legacy PA) vs. `LegacyProductOverview.md` |
| 2 | **100K Static safety net math does not hold.** The safety net is defined as drawdown + $100, which gives $625 + $100 = $100,725. The payout table lists the minimum required balance as **$102,600**, and the contract scaling rule separately refers to a static safety net of **$2,600**. The discrepancy is $1,875. | `LegacyPayouts.md` vs. `legacyEvaluationAccounts.md` vs. `lefacyPerfAccountTradingRules.md` |
| 3 | A qualifying trading day requires a profit of **$50 or more** under the payout criteria, but **$150 per day** under the post-violation restoration criteria. The documents do not state that these are two different thresholds for two different situations. | `LegacyPayouts.md` vs. `newFeatEarlyAccountUpdateNotifications.md` |
| 4 | The payout split is stated as "100% of the first $25,000 per account, and 90% of the profit after that". A separate section states that 100% payouts require five approved payouts first, from the sixth payout onward. These are two different mechanisms presented as if they were one rule. | `LegacyPayouts.md` |
| 5 | The activation document says "You can activate and pay for up to 20 PA accounts" (per user), while the overview states the cap of 20 is per household. | `legacyEvaluationAccounts.md` vs. `LegacyProductOverview.md` |

---

## 3. Missing data

Items that are required for a cost and feasibility comparison and are absent:

- **Evaluation profit targets.** There is no table. The targets can only be inferred from
  two worked examples: $50K account → $53,000, $300K account → $320,000. Nothing is given
  for 25K, 75K, 100K, 150K, 250K or 100K Static.
- **Monthly evaluation subscription price.** Not stated anywhere, for any account size or
  platform. This is the main recurring cost.
- **Reset fee.** The reset option is described repeatedly, but the fee amount is never
  given.
- **Monthly PA Activation Fee option.** Referred to as an alternative to the lifetime fee,
  with no prices.
- **Commission and fee schedule.** The profit goal is explicitly net of commissions, but
  the per-contract rates are never given.
- **75K plan** is absent from the PA Lifetime Fee table, the minimum required balance
  table and the maximum payout table. It appears only in the drawdown table.
- **100K Static** is absent from the PA Lifetime Fee table.
- **Contract scaling rounding rule.** Traders are limited to half their maximum contracts
  until the safety net is reached. Half of 17, 27 and 35 contracts is undefined.
- **Payout processing time, payment method and any payout fees.**
- **Tradable instruments for full-size contracts.** Only the eight micro contracts are
  listed.
- **Trading restrictions around news events**, and any restriction on holding through the
  daily close other than the 4:59 PM ET flat rule.
- **Country availability and tax treatment.**

---

## 4. Broken and missing references

The following are referenced as "for full details, visit the X page" or as hyperlinks, but
no URL and no content was captured:

- Legacy Contract Scaling Rule
- Legacy 30% Negative P&L Rule (MAE)
- Legacy 5:1 Risk-Reward Ratio Rule
- Hedging Rule
- One Direction Rule (Directionally Biased Trading)
- What are the Consistency Rules for Legacy PA and Funded Accounts?
- Trader Probation
- Benefits of Managing Multiple Accounts
- Legacy Billing: Subscriptions, Cancellations, & Resets (only partially covered by the
  Legacy Evaluation Subscription & Billing section)
- Apex Trader Funding Accounts (multiple user accounts policy)

All embedded videos and images are absent. This matters most for the trailing drawdown
explanation, which refers to illustrations of a 25-point drawdown on 5 NQ contracts and a
10.5-point static drawdown on 3 NQ contracts that are not present.

The **Live Prop Trading Account** is referenced as the point at which the 30% consistency
rule stops applying, but it is not described anywhere in the captured material.

---

## 5. File and formatting issues

- `lefacyPerfAccountTradingRules.md` — filename is misspelled ("lefacy" should be
  "legacy"), and the first line of the file reads "legacy evaluation accounts", which does
  not match the content (Legacy Performance Account Trading Rules).
- `newFeatEarlyAccountUpdateNotifications.md` — the first line also reads "legacy
  evaluation accounts", which does not match the content.
- Source URL paths are inconsistent. Some Legacy articles are under
  `/help-center/evaluation-accounts-ea/`, others under
  `/help-center/legacy-evaluation-accounts/`. One of the two path families is likely stale.
- The drawdown table in `legacyEvaluationAccounts.md` is flattened into plain text lines
  that merge the contract count and the drawdown amount (for example "50K Full Size 10
  Minis – 2500"). It is also labelled "Max Loss/Trailing Threshold" while the values are
  drawdown amounts, not threshold balances.
- `LegacyTrailingDrawdown.md` repeats the heading "Legacy Trailing Drawdown Rule" twice.
- Timezone references alternate between "midnight ET" and "midnight (EST)".
- `LegacyPayouts.md` discusses the safety net and the trailing drawdown stop point in the
  same paragraph without distinguishing them. They are different values: the trailing
  drawdown stops at starting balance + $100, while the minimum balance to request a payout
  is starting balance + drawdown + $100.

---

## 6. Verified figures

These were checked for internal consistency and hold up. They are usable, subject to the
caveat in section 1 that they describe retired products.

### Trailing drawdown and contract limits

| Plan | Max contracts (minis) | Trailing drawdown |
|---|---|---|
| 25K Full | 4 | $1,500 |
| 50K Full | 10 | $2,500 |
| 75K Full | 12 | $2,750 |
| 100K Full | 14 | $3,000 |
| 150K Full | 17 | $5,000 |
| 250K Full | 27 | $6,500 |
| 300K Full | 35 | $7,500 |
| 100K Static | 2 | $625 |

### Payout thresholds

| Account | Minimum balance to request | Maximum payout (first five) | PA lifetime activation fee |
|---|---|---|---|
| $25K | $26,600 | $1,500 | $125 |
| $50K | $52,600 | $2,000 | $140 |
| $75K | not given | not given | not given |
| $100K | $103,100 | $2,500 | $175 |
| $150K | $155,100 | $2,750 | $200 |
| $250K | $256,600 | $3,000 | $250 |
| $300K | $307,600 | $3,500 | $300 |
| $100K Static | $102,600 (see contradiction 2) | $1,000 | not given |

All minimum balances except the static account equal starting balance + drawdown + $100.

### Mechanics confirmed across documents

- The trailing drawdown follows the **peak unrealized** balance, not closed trade values.
  A trade that peaks at +$875 and is closed at +$100 moves the threshold by $875.
- There is no daily maximum drawdown.
- In a Performance Account the trailing drawdown stops once the threshold reaches starting
  balance + $100.
- **Platform changes evaluation difficulty.** During an evaluation, Rithmic and
  WealthCharts accounts stop trailing once the threshold reaches the profit target.
  Tradovate accounts continue to trail and never stop. Platforms cannot be converted and
  there are no refunds for choosing the wrong one.
- Evaluation requires a minimum of seven trading days, with no maximum time limit, and the
  balance must close at or above the profit goal net of commissions.
- All positions must be flat and all pending orders cancelled by 4:59 PM ET.
- Payouts require 8 trading days since the last request, with at least 5 of them showing a
  profit of $50 or more. Minimum payout is $500.
- Performance Account trading rules: half contract size until the safety net is reached,
  30% maximum adverse excursion against start-of-day profit (rising to 50% once the
  end-of-day profit balance is double the safety net), maximum 5:1 risk-reward, no
  hedging, one direction only.
- The 30% windfall consistency rule applies until the sixth payout.
- Maximum 20 active Performance Accounts per household. No limit on evaluations.

---

## 7. Next steps

1. Capture the Intraday PA and EOD PA documentation. Without it Apex cannot be compared.
2. Obtain current pricing: evaluation subscription per account size and platform, reset
   fee, and activation fee.
3. Obtain the commission schedule per instrument.
4. Resolve the 100K Static safety net discrepancy ($100,725 vs $102,600).
5. Confirm whether the Legacy figures in section 6 carry over to the new account types or
   whether the new types use different values.
