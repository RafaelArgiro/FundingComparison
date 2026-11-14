# Apex Data Health

Status of the Apex source material in `Apex/Data/`, for the purpose of comparing funding
options for daytrading.

Files reviewed:

- `LegacyAccountsPlans.md`
- `LegacyProductOverview.md`
- `legacyEvaluationAccounts.md`
- `lefacyPerfAccountTradingRules.md`
- `LegacyPayouts.md`
- `LegacyTrailingDrawdown.md`
- `newFeatEarlyAccountUpdateNotifications.md`

---

## 1. Status: Legacy accounts are on sale again

`LegacyAccountsPlans.md` is a capture of the live Apex purchase page and shows Legacy
evaluation accounts **available for purchase right now**, in 6 sizes across 3 platforms,
described as "Legacy Accounts – Available Now – Limited Time".

This supersedes `LegacyProductOverview.md`, which states that Legacy accounts were retired
on March 1, 2026 and are "no longer available for purchase to anyone". That help-centre
article is stale. The purchase page acknowledges the split directly: "These are Legacy
Products, a different program than other product offerings."

Apex is therefore comparable on the Legacy program. Two caveats:

- **The offer is time-boxed.** The page carries a countdown ("Ends in: 4d 09h 27m 05s").
  Whether Legacy remains purchasable at decision time must be re-checked.
- **Intraday PA and EOD PA are still undocumented.** The site-wide promo banner reads
  "90% OFF ALL EVALS! INTRADAY • EOD • LEGACY • ANY SIZE!", confirming all three programs
  are sold concurrently. Nothing in this folder describes the Intraday or EOD rules,
  drawdown model, contract limits, pricing or payout parameters. A complete Apex
  comparison still needs them; a Legacy-only comparison no longer does.

---

## 2. Pricing

Evaluations are **monthly subscriptions**, not one-time purchases. Every plan card shows
two prices: a list price and a coupon price at 90% off. **The coupon sale is permanent**,
so the coupon price is the price actually paid and the list price is never charged. The
figures below are the coupon prices.

| Size | Contracts | Profit goal | Trailing threshold | Tradovate | WealthCharts | Rithmic |
|---|---|---|---|---|---|---|
| 25K Full | 4 (40 micros) | $1,500 | $1,500 | $22.70/mo | $17.70/mo | $17.70/mo |
| 50K Full | 10 (100 micros) | $3,000 | $2,500 | $24.70/mo | $19.70/mo | $19.70/mo |
| 100K Full | 14 (140 micros) | $6,000 | $3,000 | $44.70/mo | $39.70/mo | $39.70/mo |
| 150K Full | 17 (170 micros) | $9,000 | $5,000 | $64.70/mo | $59.70/mo | $59.70/mo |
| 250K Full | 27 (270 micros) | $15,000 | $6,500 | $44.70/mo | $39.70/mo | $39.70/mo |
| 300K Full | 35 (350 micros) | $20,000 | $7,500 | $44.70/mo | $39.70/mo | $39.70/mo |

Five-pack prices, also at coupon, quoted as a total per month for five accounts:

| Size | Tradovate | WealthCharts | Rithmic |
|---|---|---|---|
| 25K Full | $113.50/mo | $88.50/mo | $88.50/mo |
| 50K Full | $123.50/mo | $99.50/mo | $99.50/mo |
| 100K Full | $223.50/mo | $198.50/mo | $198.50/mo |
| 150K Full | $323.50/mo | $298.50/mo | $298.50/mo |
| 250K Full | $223.50/mo | $198.50/mo | $198.50/mo |
| 300K Full | $223.50/mo | $198.50/mo | $198.50/mo |

On top of the subscription there is a **one-time PA activation fee of $99.00**, shown
identically on all 18 plan cards, payable once the evaluation is passed.

Structural points that follow from this table:

- **Tradovate costs $5/month more per account than Rithmic and WealthCharts at every
  size** ($50/month at list). Rithmic and WealthCharts are identically priced. This matters
  because Tradovate is also the platform on which the evaluation trailing drawdown never
  stops (see section 8).
- **The 150K is the most expensive plan sold**, more than both the 250K and the 300K,
  which are priced identically to the 100K.
- **The five-pack is not a discount.** It is exactly 5× the single price in every case
  except one, where it is $1/month more expensive (see contradiction 4).
- **The PA fee dominates the subscription cost.** At $99 it is more than five months of a
  25K Rithmic or WealthCharts evaluation, and roughly 18 months of the difference between
  the cheapest and most expensive platform.
- **The ratio of profit goal to trailing threshold rises sharply with account size**: 1.0
  on the 25K, 1.2 on the 50K, 2.0 on the 100K, 1.8 on the 150K, 2.3 on the 250K and 2.7
  on the 300K. The 25K is the only plan where the profit goal equals the drawdown.

---

## 3. Internal contradictions

| # | Contradiction | Where |
|---|---|---|
| 1 | **One-time PA activation fee: $99 or tiered.** The purchase page shows "One-Time PA Fee $99.00" identically on all 18 plan cards. The help centre gives a tiered Legacy PA Lifetime Fee of $125 / $140 / $175 / $200 / $250 / $300 by size. On a 300K the difference is $201. | `LegacyAccountsPlans.md` vs `legacyEvaluationAccounts.md` |
| 2 | **Micro contract ratio: 10:1 or 1:1.** The purchase page states every plan's limit as minis with a 10× micro equivalent (25K = "4 (40 Micros)"). The help centre says "You can trade micro contracts **up to the maximum contract size listed for your plan**", which reads as 1:1, and its worked example counts only full-size contracts. On a 25K this is the difference between 4 micros and 40. | `LegacyAccountsPlans.md` vs `legacyEvaluationAccounts.md` |
| 3 | **Scaling: None, or half contracts until the safety net.** Every plan card lists "Scaling: None". The Legacy PA Trading Rules open with a Contract Scaling Rule restricting traders to half their maximum contracts until the end-of-day balance exceeds the trailing threshold. The plan card most likely refers to the evaluation phase only, but it is stated unqualified. | `LegacyAccountsPlans.md` vs `lefacyPerfAccountTradingRules.md` |
| 4 | **Five-pack arithmetic on the 50K.** WealthCharts and Rithmic price the 50K at $19.70/month and the five-pack at $99.50/month. Five times $19.70 is $98.50, so the pack costs $1/month more than buying five singles. The same gap appears at list price ($995 against 5 × $197 = $985). Every other size and platform multiplies out exactly. | `LegacyAccountsPlans.md`, within one page |
| 5 | **Legacy accounts cannot be purchased, but are on sale.** The overview states Legacy evaluations are "no longer available for purchase to anyone" as of March 1, 2026. The purchase page sells them. | `LegacyProductOverview.md` vs `LegacyAccountsPlans.md` |
| 6 | **Purchases on or after March 1, 2026.** The activation article says accounts purchased "on or after March 1, 2026" are only eligible for the one-time lifetime PA fee, not the monthly option. The overview says nothing can be purchased on or after that date. Given section 1, the activation article is the one that now reads correctly, and the monthly PA fee option appears to be withdrawn for anything bought today. | `legacyEvaluationAccounts.md` vs `LegacyProductOverview.md` |
| 7 | **100K Static safety net math does not hold.** The safety net is defined as drawdown + $100, which gives $625 + $100 = $100,725. The payout table lists the minimum required balance as **$102,600**, and the contract scaling rule separately refers to a static safety net of **$2,600**. The discrepancy is $1,875. The Static account is not on the purchase page, so this no longer blocks a decision. | `LegacyPayouts.md` vs `legacyEvaluationAccounts.md` vs `lefacyPerfAccountTradingRules.md` |
| 8 | A qualifying trading day requires a profit of **$50 or more** under the payout criteria, but **$150 per day** under the post-violation restoration criteria. The documents do not state that these are two different thresholds for two different situations. | `LegacyPayouts.md` vs `newFeatEarlyAccountUpdateNotifications.md` |
| 9 | The payout split is stated as "100% of the first $25,000 per account, and 90% of the profit after that". A separate section states that 100% payouts require five approved payouts first, from the sixth payout onward. These are two different mechanisms presented as if they were one rule. | `LegacyPayouts.md` |
| 10 | The activation document says "You can activate and pay for up to 20 PA accounts" (per user), while the overview states the cap of 20 is per household. | `legacyEvaluationAccounts.md` vs `LegacyProductOverview.md` |

---

## 4. Resolved by the purchase page

These were open gaps and are now closed:

- **Evaluation profit targets** — full table for all six sizes sold.
- **Monthly evaluation subscription price** — full table, per size and per platform, at
  the coupon price actually charged.
- **Contract limits** — confirmed, with micro equivalents.
- **Trailing thresholds** — the purchase page figures match the help-centre drawdown table
  exactly for all six sizes.
- **75K Full and 100K Static** — neither is on the purchase page. Their absence from the
  PA fee and payout tables is consistent with their no longer being sold, rather than
  being an omission.
- **What the subscription includes** — Tradovate plans include a Tradovate license,
  NinjaTrader ($75 value) and real-time data ($55 value). Rithmic plans include NinjaTrader
  and data. WealthCharts plans include data only, with no platform license line.

---

## 5. Still missing

- **Intraday PA and EOD PA documentation.** Sold concurrently, described nowhere.
- **Reset fee.** Resets are described repeatedly and are the only route to restart a failed
  evaluation. The amount is still not given anywhere, including on the purchase page.
- **Whether the coupon price carries into renewals.** The coupon is applied at checkout and
  the sale is permanent, so a new evaluation always costs the coupon price. Whether an
  existing subscription renews at the coupon price or reverts to list is not stated.
  Evaluations have no time limit, so on a long evaluation this is the difference between
  $17.70 and $177 a month on a 25K.
- **Commission and fee schedule.** The profit goal is explicitly net of commissions, but
  per-contract rates are given nowhere.
- **Contract scaling rounding rule.** Half of 17, 27 and 35 contracts is undefined.
- **Payout processing time, payment method and any payout fees.**
- **Tradable instruments for full-size contracts.** Only the eight micro contracts are
  listed anywhere.
- **Trading restrictions around news events**, and any restriction on holding through the
  daily close other than the 4:59 PM ET flat rule.
- **Country availability.** The purchase page risk disclosure states "Services are intended
  for **U.S. users only** and are not offered where prohibited by local laws or
  regulations", while the same page links to a Restricted Countries list that was not
  captured. These two statements imply different scopes and the question is decisive for a
  non-US trader.
- **Tax treatment.**
- **Platform capability rows for two of three platforms.** The Tradovate cards list
  TradingView, browser, mobile and Mac compatibility. The WealthCharts and Rithmic cards
  omit those rows entirely, so the platforms cannot be compared on capability.

---

## 6. Broken and missing references

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
- Restricted Countries (linked from the purchase page footer)
- The Legacy Product Details FAQ referenced at the top of the purchase page

All embedded videos and images are absent. This matters most for the trailing drawdown
explanation, which refers to illustrations of a 25-point drawdown on 5 NQ contracts and a
10.5-point static drawdown on 3 NQ contracts that are not present.

The **Live Prop Trading Account** is referenced as the point at which the 30% consistency
rule stops applying, but it is not described anywhere in the captured material.

---

## 7. File and formatting issues

- `lefacyPerfAccountTradingRules.md` — filename is misspelled ("lefacy" should be
  "legacy"), and the first line of the file reads "legacy evaluation accounts", which does
  not match the content (Legacy Performance Account Trading Rules).
- `newFeatEarlyAccountUpdateNotifications.md` — the first line also reads "legacy
  evaluation accounts", which does not match the content.
- `LegacyAccountsPlans.md` is a raw page scrape and retains site chrome: navigation menu,
  cookie policy links, the promo countdown timer and the mailing address. The plan cards
  are flattened into label/value line pairs rather than tables, and the "One Pack" and
  "Five Pack" labels appear *after* their prices rather than before.
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

## 8. Verified figures

### Plan parameters

| Plan | Contracts | Profit goal | Trailing drawdown | Sold today |
|---|---|---|---|---|
| 25K Full | 4 (40 micros) | $1,500 | $1,500 | Yes |
| 50K Full | 10 (100 micros) | $3,000 | $2,500 | Yes |
| 75K Full | 12 | not given | $2,750 | No |
| 100K Full | 14 (140 micros) | $6,000 | $3,000 | Yes |
| 150K Full | 17 (170 micros) | $9,000 | $5,000 | Yes |
| 250K Full | 27 (270 micros) | $15,000 | $6,500 | Yes |
| 300K Full | 35 (350 micros) | $20,000 | $7,500 | Yes |
| 100K Static | 2 | not given | $625 | No |

Trailing thresholds on the purchase page match the help-centre drawdown table for every
size that appears in both. The profit goals also match the two worked examples in the help
centre ($50K passes at $53,000; $300K passes at $320,000).

### Payout thresholds

| Account | Minimum balance to request | Maximum payout (first five) | PA lifetime fee (help centre) |
|---|---|---|---|
| $25K | $26,600 | $1,500 | $125 |
| $50K | $52,600 | $2,000 | $140 |
| $100K | $103,100 | $2,500 | $175 |
| $150K | $155,100 | $2,750 | $200 |
| $250K | $256,600 | $3,000 | $250 |
| $300K | $307,600 | $3,500 | $300 |
| $100K Static | $102,600 (see contradiction 7) | $1,000 | not given |

All minimum balances except the Static account equal starting balance + drawdown + $100.
The purchase page shows $99 for every size instead of the tiered fee column.

### Mechanics confirmed across documents

- The trailing drawdown follows the **peak unrealized** balance, not closed trade values.
  A trade that peaks at +$875 and is closed at +$100 moves the threshold by $875.
- There is no daily maximum drawdown. Confirmed on every plan card ("Daily Drawdown: None").
- In a Performance Account the trailing drawdown stops once the threshold reaches starting
  balance + $100.
- **Platform changes evaluation difficulty.** During an evaluation, Rithmic and
  WealthCharts accounts stop trailing once the threshold reaches the profit target.
  Tradovate accounts continue to trail and never stop. Platforms cannot be converted and
  there are no refunds for choosing the wrong one. Tradovate is also the most expensive of
  the three, by $50/month at every size.
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
- Maximum 20 active Performance Accounts per household, across Legacy PA, Intraday PA and
  EOD PA combined. No limit on evaluations.

---

## 9. Next steps

1. Confirm the PA activation fee: $99 for all sizes, or the tiered $125–$300 schedule.
2. Confirm whether an existing subscription renews at the coupon price or reverts to list.
   Evaluations have no time limit, so on a long evaluation this dominates the cost model.
3. Confirm the micro contract ratio: 10 micros per mini, or 1:1 against the contract count.
4. Obtain the reset fee.
5. Confirm availability for non-US traders, given the "U.S. users only" disclosure.
6. Obtain the commission schedule per instrument.
7. Capture the Intraday PA and EOD PA documentation if Apex is to be compared on its
   current flagship products rather than on Legacy alone.
8. Re-check that Legacy is still purchasable at decision time; the offer carries a
   countdown.
