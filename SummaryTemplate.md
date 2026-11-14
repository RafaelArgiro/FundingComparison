# Provider Summary — Template

Template for the summary written for each provider. The goal is a document short enough to
read in full, structured identically across providers so rows can be lifted straight into
a final cross-provider comparison.

Full detail stays in `<Provider>/Data/`. Data quality caveats stay in
`<Provider>/data_health.md`. This document carries only what affects the decision.

The weight of the document sits in sections 3, 4 and 5: the rules of each phase, and the
payout rules that cap earnings. Everything else is kept to tables.

---

## Normalisation rules

Apply these in every provider summary, or the numbers will not be comparable.

| Item | Rule |
|---|---|
| Anchor account size | **$50K** for all worked figures. Other sizes only where they change the conclusion. |
| Phase names | Use **Evaluation**, **Funded**, **Live** regardless of the provider's own naming. Note their term once in brackets. |
| Prices | **Price actually paid**, i.e. after any standing discount code. Note the code and whether it is permanent. |
| Recurring vs one-off | State explicitly. Monthly subscriptions are quoted per month **and** as a 3-month cost. |
| Commissions | **Round trip, per contract.** Double any per-side figure before entering it. |
| Time | **Trading days**, not calendar days. |
| Drawdown | State both *how it updates* (intraday / end-of-day / static) and *how it is enforced* (real-time on net liquidation, or end-of-day only). These are independent and both matter. |
| Unknowns | Write "not published" rather than omitting the row or guessing. |

## Consequence codes

Used in every rule table. The distinction between these is the whole point — a rule that
costs a day's trading is not comparable to one that ends the account.

| Code | Meaning |
|---|---|
| **KILL** | Account lost immediately. No recovery, no reset. |
| **LOCK** | Trading halted until the next session. Account survives. |
| **BLOCK** | Account survives, but payouts are blocked or denied. |
| **STRIP** | Profits removed from the account. |
| **BAN** | Consequences beyond this account: probation, closure, permanent ban. |

## Limiting rating

How much the rule constrains normal daytrading, independent of its severity.

**High** — changes how you size, time or exit trades.
**Medium** — occasionally binding; you will notice it.
**Low** — unlikely to bind if you are trading normally.

---

## Template starts here

---

# `<Provider>` — Summary


## 1. Key facts

| | |
|---|---|
| Products | |
| Account sizes | |
| Entry cost, 50K | |
| Cost model | one-time / monthly subscription |
| Standing discount | code, %, permanent or promotional |
| Profit split | |
| Max funded accounts | per user / per household |
| Platforms | |
| Availability | restricted countries, US-only concerns |
| Phases | their names for Evaluation / Funded / Live |

## 2. Products

One row per product. Figures at the 50K anchor.

| Product | Path | Price | Reset | Profit target | Drawdown | Daily loss limit | Consistency | Payout cadence |
|---|---|---|---|---|---|---|---|---|
| | eval / instant | | | | | | | |

> One sentence: which product a daytrader should actually consider, and why not the others.

---

## 3. Phase 1 — Evaluation

**To pass:** profit target, minimum trading days, any consistency constraint, time limit.

**Cost to retry:** reset price, and whether the clock or billing cycle resets with it.

### Rules

| Rule | What you must do | If broken | Limiting |
|---|---|---|---|
| Max loss / drawdown | | KILL | |
| Daily loss limit | | LOCK / KILL / n/a | |
| Session close | | | |
| Contract limit | | | |
| Consistency | | BLOCK (delays passing) | |
| Inactivity | | | |
| Conduct (hedging, HFT, etc.) | | BAN | |

> **Most likely to catch you:** one or two sentences naming the concrete scenario. Not the
> rule that sounds scariest — the one that actually trips a normal daytrader.

---

## 4. Phase 2 — Funded

The phase that matters most: real payouts on simulated capital.

### 4a. Rules

| Rule | What you must do | If broken | Limiting |
|---|---|---|---|
| Max loss / drawdown | | KILL | |
| Drawdown lock point | balance at which the floor stops trailing | | |
| Daily loss limit | | LOCK | |
| Contract scaling | whether size is restricted until profits build | | |
| Session close | | | |
| Holding-time / microscalping | | BLOCK | |
| Risk-management rules (MAE, R:R, one-direction) | | STRIP / BLOCK | |
| Conduct (hedging, copy trading, HFT) | | BAN | |
| Inactivity | | | |

> **Most likely to catch you:** one or two sentences.

> **What differs from the evaluation:** one or two sentences. Rules that appear only once
> funded are the ones people are least prepared for.

### 4b. Payout rules that cap earnings

Every lever that limits how much money actually reaches you.

| Lever | Value | Effect on earnings |
|---|---|---|
| Minimum balance / buffer | | capital that can never be withdrawn |
| Minimum payout request | | |
| Maximum payout per request | | |
| Cycle length between payouts | | |
| Qualifying days required | e.g. 5 days above $150 | |
| Profit goal per cycle | | must be earned before anything can be taken |
| Consistency requirement | | forces profit to be spread across days |
| Profit split | | |
| Payouts before forced move to live | | caps total extractable in this phase |
| Profit forfeited on transition | | |

**Derived figures** — calculate these, they are not published:

- **Withdrawal ceiling per cycle:** max payout ÷ cycle length = `$X per trading day`
- **Total extractable before forced transition:** max payout × number of payouts
- **Capital permanently locked:** buffer amount
- **Profit needed per $1 withdrawn:** accounts for the consistency rule and the profit
  goal, not just the split

> **The binding constraint:** one sentence naming which single lever caps earnings first.
> Usually it is the payout cap or the cycle length, not the profit split.

---

## 5. Phase 3 — Live

- **How you get there:** requirement, and whether it is automatic, discretionary or
  optional
- **Whether you can refuse**, and what happens if you do
- **What transfers:** simulated profit carried over, capped, or forfeited
- **Starting conditions:** balance, drawdown, contract limits
- **Split**, if different from the funded phase
- **Can you keep trading simulated accounts?**
- **If the live account breaches:** consequences, and whether you can return to simulated

### Rules

| Rule | What you must do | If broken | Limiting |
|---|---|---|---|
| Drawdown | | KILL | |
| Session close / swing trading | | | |
| Hedging | | BAN | |
| Payout rules | | | |

> **One sentence:** is this phase an upgrade or a downgrade relative to staying funded?

---

## 6. Rules that apply in every phase

Only those not already covered above, one line each.

- Trading hours and flat-by time
- News trading
- Hedging and correlated products
- Automated trading and copy trading
- Account sharing, IP and device rules
- Maximum accounts

## 7. Running costs

| Item | Cost |
|---|---|
| Commission, ES round trip | |
| Commission, MES round trip | |
| Market data | |
| Platform fees | |
| Other | |

## 8. Assessment

**Strengths**
- Three to four bullets, specific and falsifiable.

**Watch-outs**
- Three to four bullets. Include anything cheap to enter but expensive to survive.

**Confidence in this summary**
- One or two lines. What is verified, what is unpublished, and whether any open question
  could change the verdict. Point to `data_health.md` rather than repeating it.

---

## Length guide

| Section | Target |
|---|---|
| 1. Key facts | table only |
| 2. Products | table + 1 sentence |
| 3. Evaluation | table + 2 lines |
| 4a. Funded rules | table + 3 lines |
| 4b. Payout caps | table + 4 derived figures + 1 line |
| 5. Live | 7 bullets + table + 1 line |
| 6. All phases | 6 bullets |
| 7. Running costs | table only |
| 8. Assessment | 8-10 bullets |

Roughly 2.5 pages rendered. If a section runs longer, it belongs in `Data/` or
`data_health.md`.
