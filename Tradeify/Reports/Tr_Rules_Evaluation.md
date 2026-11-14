# Tradeify — Evaluation Phase

Rules that apply while trading an evaluation account, before funding.

> **Read `Tr_Rules_General.md` first.** Trading hours, position limits, prohibited and
> permitted conduct, instruments, platforms, inactivity and the general drawdown mechanic
> apply here and are not repeated. This document covers only what is specific to the
> evaluation phase, plus the parameters of each account type.

Consequence codes:
- **KILL** account lost immediately
- **LOCK** trading halted until next session
- **BLOCK** payout blocked (funded phase only)
- **STRIP** profits removed
- **BAN** consequences beyond this account

---

## 1. What is specific to the evaluation phase

- **Full contract size from the first trade.** There is no scaling plan during an
  evaluation on any account type. The limit shown for your account size is available
  immediately.
- **The drawdown never locks.** It keeps trailing your highest end-of-day balance right up
  to the moment you pass, so the give-back mechanic described in `Tr_Rules_General.md`
  applies for the entire evaluation.
- **The 10-second rule does not apply.** It is a payout gate on funded accounts only, so
  scalping is unconstrained here.
- **No time limit.** There is no deadline to reach the profit target. The weekly inactivity
  rule still applies.
- **Profit does not carry over.** The funded account starts at its base size regardless of
  where the evaluation ended. Ending at \$53,200 on a 50K still gives you a \$50,000
  funded account.
- **Activation is instant and free** once every objective is met — but instant activation
  is documented as **Tradovate only**.
- **A passed evaluation can be banked.** You may hold it and activate later when a funded
  slot is free, subject to the 5-funded-account cap.
- **Resets are available** on Growth and Select, at a price below the original purchase.
  See the account-type sections below.

---

## 2. Drawdown at the profit target

Because the floor keeps trailing throughout, the room below you at the moment you pass is
still the full drawdown amount — but the floor by then sits well above your starting
balance.

| Product | Size | Drawdown | Starting floor | Balance at target | Floor at target |
|---|---|---|---|---|---|
| Growth | 25K | \$1,000 | \$24,000 | \$26,500 | \$25,500 |
| Growth | 50K | \$2,000 | \$48,000 | \$53,000 | \$51,000 |
| Growth | 100K | \$3,500 | \$96,500 | \$106,000 | \$102,500 |
| Growth | 150K | \$5,000 | \$145,000 | \$159,000 | \$154,000 |
| Select | 25K | \$1,000 | \$24,000 | \$26,500 | \$25,500 |
| Select | 50K | \$2,000 | \$48,000 | \$53,000 | \$51,000 |
| Select | 100K | \$3,000 | \$97,000 | \$106,000 | \$103,000 |
| Select | 150K | \$4,500 | \$145,500 | \$159,000 | \$154,500 |
| Select | 300K | \$8,000 | \$292,000 | \$314,000 | \$306,000 |
| Inter Miami | 10K | \$500 static | \$9,500 | \$11,000 | \$9,500 — never moves |
| Inter Miami | 25K | \$1,000 static | \$24,000 | \$27,000 | \$24,000 — never moves |
| Inter Miami | 50K | \$1,500 static | \$48,500 | \$53,500 | \$48,500 — never moves |

---

## 3. Account type: Growth

The fastest evaluation. Has a daily loss limit, no consistency rule.

- **Minimum 1 trading day.** Can be passed the same day the profit target is hit.
- **No consistency rule.** 100% of the profit may come from a single day.
- **Daily Loss Limit applies** (soft breach): \$600 / \$1,250 / \$2,500 / \$3,750 for
  25K / 50K / 100K / 150K.
- Profit targets: \$1,500 / \$3,000 / \$6,000 / \$9,000.
- Trailing Max Drawdown: \$1,000 / \$2,000 / \$3,500 / \$5,000.
- Max contracts: 1 / 4 / 8 / 12 minis.
- **No purchase limit** on Growth evaluations.
- Resets available: \$60 / \$95 / \$169 / \$229.
- Maximum **5 Growth funded accounts may be activated per day**, resetting every 24 hours
  (UTC).
- Payout policy once funded is **fixed** — there is no choice to make.

---

## 4. Account type: Select

Slower to pass, but no daily loss limit and a choice of payout policy afterwards.

- **Minimum 3 trading days**, or 2 with the 50% consistency add-on. The profit target can
  be reached earlier, but the account cannot pass before the minimum.
- **Consistency rule applies during the evaluation**: no single day may exceed **40%** of
  total profit, or 50% with the add-on. It does not cap how much you may earn in a day —
  it only delays passing until total profit is large enough.
- **No Daily Loss Limit** at 25K–150K. The only risk limit is the trailing drawdown, which
  still applies in real time.
- **Exception: the 300K evaluation carries a \$4,000 Daily Loss Limit.**
- Profit targets: \$1,500 / \$3,000 / \$6,000 / \$9,000 / \$14,000.
- Trailing Max Drawdown: \$1,000 / \$2,000 / \$3,000 / \$4,500 / \$8,000.
- Max contracts: 1 / 4 / 8 / 12 / 16 minis, full size available throughout.
- **Maximum 15 Select evaluations per rolling 30 days.** Each may be reset up to 10 times
  in a 30-day period.
- Resets: \$75 / \$109 / \$169 / \$239. **No resets on the 300K** — a failed 300K evaluation
  requires a new purchase.
- The 300K additionally requires **KYC approval before purchase**, is limited to 5
  purchases per rolling 30 days, and does not count toward the 15-evaluation limit.
- On passing, you choose **Flex or Daily** permanently for that account. The choice is made
  at activation, not at purchase.
- The consistency rule **ends at the evaluation**. It does not apply once funded.

---

## 5. Account type: Lightning

**Lightning has no evaluation phase.** It is instant funding — the funded rules apply from
the first trade.

Consequences for this document:

- None of the evaluation-specific rules above apply.
- There is **no reset**. If the account fails, a replacement must be purchased at full
  price.

---

## 6. Account type: Inter Miami

A one-step evaluation with a **static** drawdown — the only Tradeify product that does not
trail.

- **Static drawdown**: \$500 / \$1,000 / \$1,500 for 10K / 25K / 50K. The floor never moves,
  up or down.
- Profit targets: \$1,000 / \$2,000 / \$3,500.
- **Daily Loss Limit**: \$300 / \$600 / \$900, with a "Soft / None" type selectable on the
  plan card.
- **Micros only**: 10 / 20 / 30 micros. No mini contracts at any size.
- **No minimum trading days.**
- **No consistency rule.**
- **Tradovate only.** Not offered on Rithmic or WealthCharts.
- Sizes are 10K, 25K and 50K — smaller than every other Tradeify product.

> **Data gap.** Everything above comes from the plan cards in `Data/Plans.md`. Inter Miami
> has no help-centre article, so it is unknown whether the general rules in
> `Tr_Rules_General.md` apply to it unchanged — specifically trading hours, hedging
> enforcement, inactivity, reset availability and whether the static floor is enforced on
> net liquidation in real time. Treat the general rules as unverified for this product.

---

## 7. Side-by-side

| | Growth | Select | Lightning | Inter Miami |
|---|---|---|---|---|
| Evaluation exists | Yes | Yes | No | Yes |
| Minimum trading days | 1 | 3 (2 with add-on) | — | None |
| Consistency in evaluation | None | 40% or 50% | — | None |
| Daily loss limit in evaluation | Yes | No (300K: \$4,000) | — | Yes |
| Drawdown type | EOD trailing | EOD trailing | EOD trailing | **Static** |
| Contracts in evaluation | Full size | Full size | — | Full size, micros only |
| Resets | Yes | Yes (not 300K) | **No** | Not published |
| Purchase limit | None | 15 / 30 days | None | Not published |
| Platforms | All three | All three | All three | **Tradovate only** |

---

## 8. What actually fails an evaluation

In order of how likely it is to catch a normal daytrader:

1. **An intraday spike through the trailing drawdown floor.** The floor is enforced on net
   liquidation value, so an open position that dips far enough fails the account before it
   can recover. This is the single failure mode that matters, and it is invisible on the
   dashboard, which updates the drawdown figure only once per day.
2. **Misreading how far the floor has trailed up.** After a profitable day the floor rises
   to match, so the room below shrinks as the account grows.
3. **The DLL being irrelevant when the drawdown is nearer.** On Growth, a \$1,250 daily loss
   limit on a 50K gives no protection if only \$800 of drawdown room remains.
4. **Hedging across your own accounts**, including accidentally, when running more than one
   account at a time.
5. **Inactivity**, if an account is left untouched for a week while you concentrate on
   another.

Everything else — news, scalping, DCA, martingale, algorithms, copy trading — is
permitted during an evaluation.
