# Tradeify — Funded Phase

Rules that apply once an account is funded: simulated capital, real payouts.

> **Read `Tr_Rules_General.md` first.** Trading hours, position limits, prohibited and
> permitted conduct, instruments, platforms, inactivity and the general drawdown mechanic
> apply here and are not repeated. This document covers only what is specific to the
> funded phase, plus the parameters of each account type.

Consequence codes:
- **KILL** account lost immediately
- **LOCK** trading halted until next session
- **BLOCK** payout blocked or denied
- **STRIP** profits removed
- **BAN** consequences beyond this account

Two questions are answered separately for each account type: **what can take the account
away**, and **what caps the money you can actually withdraw**.

---

## 1. What is specific to the funded phase

Five things change the moment you are funded. Each is expanded below.

| | |
|---|---|
| The drawdown locks | Section 2 |
| Daily loss limits take their funded values and rise at 6% profit | Section 3 |
| Select loses full contract size and must scale up | Section 4 |
| The 10-second rule starts gating payouts | Section 5 |
| Resets effectively disappear | Section 6 |

Consistency rules also appear or change: Growth gains a **35%** rule it did not have
during its evaluation, Lightning runs a **progressive 20% → 25% → 30%** rule, and Select
**loses** the 40%/50% rule it had during the evaluation.

---

## 2. The drawdown lock

**Before the lock**, the floor behaves exactly as described in `Tr_Rules_General.md`: it
sits the drawdown distance below the highest end-of-day balance, moves up on new closing
highs, never moves down, and ignores intraday peaks.

**The lock.** The floor stops trailing permanently once **either** of these happens,
whichever comes first:

1. Your end-of-day balance exceeds starting balance + drawdown + \$100, or
2. **You request a payout.**

Once locked, the floor becomes a fixed value at **starting balance + \$100** and never
moves again.

**This is the most valuable milestone in the funded phase.** Before the lock, every dollar
you carry into a close converts a dollar of cushion into profit you must defend. After the
lock, all profit above starting balance + \$100 is yours to risk freely — you can give
back an unlimited amount and the account survives, provided you stay above that fixed
floor.

**Requesting a payout locks the floor immediately**, even if your balance has not reached
the normal trigger. Taking an early payout is therefore a risk-reduction action as well as
a withdrawal.

**Lock trigger balances and the resulting fixed floor:**

| Size | Growth | Lightning | Select Flex | Select Daily | Locked floor |
|---|---|---|---|---|---|
| 25K | \$26,100 | \$26,100 | \$26,100 | \$26,100 | \$25,100 |
| 50K | \$52,100 | \$52,100 | \$52,100 | \$52,100 | \$50,100 |
| 100K | \$103,600 | \$104,100 | \$103,100 | \$102,600 | \$100,100 |
| 150K | \$155,100 | \$155,350 | \$154,600 | \$153,600 | \$150,100 |
| 300K Select | — | — | \$308,100 | \$306,100 | \$300,100 |

**Funded drawdown amounts.** These differ from the evaluation figures on several products,
and differ between the two Select paths:

| Size | Growth | Lightning | Select Flex | Select Daily |
|---|---|---|---|---|
| 25K | \$1,000 | \$1,000 | \$1,000 | \$1,000 |
| 50K | \$2,000 | \$2,000 | \$2,000 | \$2,000 |
| 100K | \$3,500 | \$4,000 | \$3,000 | \$2,500 |
| 150K | \$5,000 | \$5,250 | \$4,500 | \$3,500 |
| 300K | — | — | \$8,000 | \$6,000 |

Inter Miami uses a **static** floor that never trails and therefore never needs to lock:
\$500 / \$1,000 / \$1,500 below the starting balance at 10K / 25K / 50K.

---

## 3. Daily loss limit when funded

| Size | Growth | Lightning | Select Daily | Select Flex | Inter Miami |
|---|---|---|---|---|---|
| 10K | — | — | — | — | \$300 |
| 25K | \$600 | **none** | \$500 | **none** | \$600 |
| 50K | \$1,250 | \$1,250 | \$1,000 | **none** | \$900 |
| 100K | \$2,500 | \$2,500 | \$1,250 | **none** | — |
| 150K | \$3,750 | \$3,000 | \$1,750 | **none** | — |
| 300K | — | — | \$3,000 | \$4,000 | — |

**The DLL increases at 6% profit.** Once the balance reaches the threshold below, the DLL
rises to match the drawdown amount, effective from the **next** session rather than
immediately:

| Size | Balance required | Growth DLL becomes | Lightning DLL becomes |
|---|---|---|---|
| 25K | \$26,500 | \$1,000 | n/a |
| 50K | \$53,000 | \$2,000 | \$2,000 |
| 100K | \$106,000 | \$3,500 | \$4,000 |
| 150K | \$159,000 | \$5,000 | \$5,250 |

**The DLL often gives no protection at all.** If the drawdown floor is nearer than the DLL
distance, the floor is hit first and the account fails before the DLL ever triggers. On a
50K Growth with \$1,250 of DLL room but only \$800 of drawdown room remaining, the DLL is
irrelevant.

**Select Flex has no DLL.** Its only risk limit is the trailing drawdown, enforced in real
time. A single bad session can end the account with nothing to halt it first.

---

## 4. Contract scaling when funded

- **Growth and Lightning: full contract size from the first trade.** No scaling plan.
- **Select: a scaling plan applies.** You start below your maximum and earn your way up as
  end-of-day profit grows.
- **Inter Miami: micros only** at every size.

| EOD profit | Select 25K | Select 50K | Select 100K | Select 150K |
|---|---|---|---|---|
| Start | 1 mini | 2 minis | 3 minis | 3 minis |
| \$1,500+ | 2 minis | 3 minis | 4 minis | 4 minis |
| \$2,000+ | — | 4 minis | 5 minis | 5 minis |
| \$3,000+ | — | — | 8 minis | 8 minis |
| \$4,500+ | — | — | — | 12 minis |

- Scaling is calibrated at end of day and is **cumulative** — once a tier is reached you
  keep it even if the balance later falls.
- **Taking a payout can scale you back down**, because it reduces the balance the tier is
  measured against.
- The 300K scales 3 → 4 → 6 → 10 → 16 minis at \$1,500 / \$3,000 / \$5,000 / \$7,000 of
  end-of-day profit.

---

## 5. The 10-second rule

This gate does not exist during an evaluation. It appears the moment you are funded.

- To request a payout, **both** of the following must be true:
  - over 50% of your trades are held longer than 10 seconds, **and**
  - over 50% of your profit comes from trades held longer than 10 seconds.
- Failing it does **not** fail the account. BLOCK — it simply makes you ineligible to
  request a payout until the ratios recover.
- It is measured on the account, so a single heavy scalping session can push both ratios
  out and block payouts until enough longer-held trades dilute them.

---

## 6. Account lifecycle when funded

- **A funded account cannot be reset.** A drawdown breach terminates it permanently, and
  the normal route back is to buy and pass a new evaluation.
- **Funded Reset** is the one exception and is narrowly scoped: Select funded accounts at
  50K, 100K and 150K only, on both the Daily and Flex paths. Conditions:
  - the breach must have occurred within the last 30 days,
  - **no payout may ever have been taken on that account's history** — this is absolute
    and cannot be waived,
  - a maximum of two uses per account history, the second costing 10% more than the first,
  - you must not hold, and nobody in your household may hold, a live account.
  - The new account starts with zero profit, a full drawdown, a reset payout clock and
    reset consistency progress. The price is not published anywhere.
- Funded Reset is **not available** for Growth, Lightning, any 25K account, or Inter Miami.
- Tradeify reserves the right to move you to a live account at any time after a successful
  payout.

---

## 7. Account type: Growth — funded

### 7.1 Rules and risk

- Trailing Max Drawdown: \$1,000 / \$2,000 / \$3,500 / \$5,000 for 25K / 50K / 100K / 150K.
- Daily Loss Limit: \$600 / \$1,250 / \$2,500 / \$3,750, rising to equal the drawdown at
  6% profit.
- **Full contract size from the first trade**: 1 / 4 / 8 / 12 minis. No scaling plan.
- **Consistency rule: 35%**, applying to every payout. This does not exist during the
  Growth evaluation — it appears only once funded.
- Payout policy is **fixed**. There is no Flex/Daily choice.
- No Funded Reset. A breach means buying and passing a new evaluation.

### 7.2 What caps your earnings

| Lever | Value (25K / 50K / 100K / 150K) |
|---|---|
| Minimum balance to request | \$26,500 / \$53,000 / \$104,500 / \$156,500 |
| Qualifying days per cycle | 5 days with profit above \$100 / \$150 / \$200 / \$250 |
| Consistency | 35% — largest day ≤ 35% of total profit |
| Minimum payout | \$250 / \$500 / \$1,000 / \$1,500 |
| Profit split | 90% to you |

Maximum payout per request, by payout number:

| Payout | 25K | 50K | 100K | 150K |
|---|---|---|---|---|
| 1 | \$1,000 | \$1,500 | \$2,000 | \$2,500 |
| 2 | \$1,000 | \$2,000 | \$2,500 | \$3,000 |
| 3 | \$1,000 | \$2,500 | \$3,000 | \$4,000 |
| 4+ | \$1,000 | \$3,000 | \$4,000 | \$5,000 |

**The cap never lifts.** Payouts after the fourth stay at the fourth-tier amount forever.
There is no point at which Growth becomes uncapped.

**The 25K is fixed at \$1,000 for every payout**, with no progression at all.

**Worked throughput, 50K at steady state:** \$3,000 per 5 qualifying days, so roughly
**\$600 per trading day** maximum extraction, before the 90% split. Reaching that steady
state takes three earlier payouts at \$1,500, \$2,000 and \$2,500.

**To take the first payout on a 50K** you need the balance at \$53,000 — \$3,000 of profit
— and can then withdraw \$1,500 of it. Profit required per dollar withdrawn: **2:1**.

---

## 8. Account type: Select Flex — funded

Chosen permanently at activation. No daily loss limit, no consistency rule, larger payouts
but less frequent.

### 8.1 Rules and risk

- Trailing Max Drawdown: \$1,000 / \$2,000 / \$3,000 / \$4,500, and \$8,000 on the 300K.
- **No Daily Loss Limit at all.** The trailing drawdown is the only risk limit, enforced
  in real time. Nothing halts a bad session before the account dies.
- **No consistency rule** once funded. The 40%/50% requirement ended at the evaluation.
- **Contract scaling applies** — see section 4.
- Funded Reset available at 50K, 100K and 150K, subject to the conditions in section 6.

### 8.2 What caps your earnings

| Lever | Value (25K / 50K / 100K / 150K) |
|---|---|
| Minimum balance to request | **None** |
| Buffer | **None** |
| Winning days per cycle | 5 days with profit above \$100 / \$150 / \$200 / \$250 |
| Payout formula | **50% of total profit** (current balance − starting balance) |
| Payout cap | \$1,250 / \$2,500 / \$3,500 / \$4,500 |
| Payout cap with the 50% consistency add-on | — / \$2,000 / \$3,000 / \$4,000 |
| Minimum payout | \$250 |
| Profit split | 90% to you |

The 300K uses a \$750 winning-day threshold and a \$10,000 cap.

**The 50% formula is measured against total profit, not cycle profit.** If your balance is
\$54,000 on a 50K, total profit is \$4,000 and you may request \$2,000 — regardless of how
that profit was accumulated or how much you withdrew previously.

**Profit required per dollar withdrawn: 2:1, permanently.** Half of all profit you
generate must remain in the account at any moment you request.

**Worked throughput, 50K:** \$2,500 per 5 winning days, so roughly **\$500 per trading
day** maximum, and only if total profit is at least \$5,000.

**Buying the 50% consistency add-on lowers your funded payout cap.** It speeds up passing
the evaluation by a day and then costs you \$500 per payout on a 50K, permanently.

**From payout 2 onward you must be net positive for the cycle.** Losses after a payout
must be earned back before you can request again.

---

## 9. Account type: Select Daily — funded

The other permanent choice at activation. Tighter risk parameters, much faster access to
profit.

### 9.1 Rules and risk

- Trailing Max Drawdown: \$1,000 / \$2,000 / \$2,500 / \$3,500, and \$6,000 on the 300K.
  **Smaller than Flex at 100K and 150K** — choosing Daily reduces your drawdown by \$500
  and \$1,000 respectively.
- Daily Loss Limit: \$500 / \$1,000 / \$1,250 / \$1,750. LOCK.
- **No consistency rule** once funded.
- Contract scaling identical to Flex — see section 4.
- Funded Reset available at 50K, 100K and 150K, subject to the conditions in section 6.

### 9.2 What caps your earnings

| Lever | Value (25K / 50K / 100K / 150K) |
|---|---|
| Buffer — balance you can never withdraw below | \$26,100 / \$52,100 / \$102,600 / \$153,600 |
| Buffer amount above starting balance | \$1,100 / \$2,100 / \$2,600 / \$3,600 |
| Payout frequency | **Daily eligibility** |
| Payout formula | **2× profit earned since the last payout** |
| Payout cap | \$600 / \$1,250 / \$1,750 / \$2,500 |
| Minimum payout | \$250 |
| Profit split | 90% to you |

The 300K uses a \$6,100 buffer, a \$4,000 daily cap, and requires 50% of each payout to
come from new profit since the last request.

**The 2× multiplier is the most generous formula Tradeify offers.** Earn \$625 on a 50K
and you may withdraw \$1,250 — twice what you made that cycle. You are drawing down
previously accumulated profit, which is why the buffer exists to stop it going too far.

**Profit required per dollar withdrawn: 0.5:1.** This is the only Tradeify payout formula
where you can withdraw more than you earned in the cycle.

**Worked throughput, 50K:** up to **\$1,250 per trading day**, sustainable if you average
\$625 per day. That is roughly double the per-day ceiling of Growth and 2.5× that of Flex
at the same account size.

**The buffer is permanently locked capital.** On a 50K, \$2,100 of profit can never be
withdrawn while the account lives. It is only released if the account moves live, and
even then it funds the live drawdown rather than being paid out.

**You must be net positive for the cycle.** A losing day after a payout must be recovered
before the next request.

**Only one payout request can be open at a time.** Daily eligibility means you can become
eligible each session, not that requests can overlap — so processing time effectively
sets the real cadence.

---

## 10. Account type: Lightning — funded

Instant funding, no evaluation. The funded rules apply from the first trade.

### 10.1 Rules and risk

- Trailing Max Drawdown: \$1,000 / \$2,000 / \$4,000 / \$5,250 — **the largest drawdowns of
  any Tradeify funded product** at 100K and 150K.
- Daily Loss Limit: **none at 25K**, then \$1,250 / \$2,500 / \$3,000, rising to equal the
  drawdown at 6% profit.
- **Full contract size from the first trade**: 1 / 4 / 8 / 12 minis. No scaling plan.
- **No reset of any kind.** Not an evaluation reset, not a Funded Reset. A breach means
  buying a new Lightning account at full price.

### 10.2 What caps your earnings

| Lever | Value (25K / 50K / 100K / 150K) |
|---|---|
| Consistency | **Progressive: 20% → 25% → 30%** for payouts 1, 2, 3+ |
| Profit goal, payout 1 | \$1,500 / \$3,000 / \$6,000 / \$9,000 |
| Profit goal, payout 2+ | \$1,000 / \$2,000 / \$3,500 / \$4,500 |
| Minimum payout | \$1,000 |
| Profit split | 90% to you |

Maximum payout per request:

| Payout | 25K | 50K | 100K | 150K |
|---|---|---|---|---|
| 1–3 | \$1,000 | \$2,000 | \$2,500 | \$3,000 |
| 4+ | \$1,000 | \$2,500 | \$3,000 | \$3,500 |

**The profit goal is not the payout.** On a 150K you must earn \$9,000 to unlock the first
payout, then may withdraw at most \$3,000 of it. Profit required per dollar withdrawn on
payout 1: **3:1**.

**Profit goals reset to zero and do not carry over.** After a payout you must earn fresh
profit from new trades to reach the next goal. Leftover profit from the previous cycle
counts for nothing toward the next.

**The 20% consistency rule on payout 1 forces at least five profitable days.** On a 50K
needing \$3,000, no single day may exceed \$600. The progression to 25% and then 30% eases
this but never removes it.

**The 25K is fixed at \$1,000** for both minimum and maximum, every payout.

> **Open question.** The payout policy states "No Minimum Trading Day Count", while every
> Lightning plan card states "Payout Frequency: 5 Days". These conflict and the real
> cadence is unresolved.

---

## 11. Account type: Inter Miami — funded

### 11.1 Rules and risk

- **Static drawdown**: \$500 / \$1,000 / \$1,500 at 10K / 25K / 50K. The floor never moves,
  so the cushion grows with every dollar of profit rather than staying fixed below a
  trailing peak.
- Daily Loss Limit: \$300 / \$600 / \$900, with a "Soft / None" type selectable.
- **Micros only**: 10 / 20 / 30 micros.
- **Tradovate only.**

### 11.2 What caps your earnings

| Lever | Value (10K / 25K / 50K) |
|---|---|
| Minimum gross payout | \$200 / \$400 / \$600 |
| Payout frequency | Daily |
| Profit split | **80% / 10% / 10%** |
| Path to live | After **\$12,000 in payouts** |

**The split is materially worse than every other Tradeify product**, which pay 90%. The
cards describe it as "80% profit split + 10% to Live Funds"; the destination of the final
10% is not explained.

**Micros-only caps absolute earnings.** At 30 micros on a 50K, the position size is
equivalent to 3 minis — a quarter of what a 50K on another Tradeify product can trade.

> **Data gap.** Everything above comes from the plan cards in `Data/Plans.md`. Inter Miami
> has no help-centre article, so it is unknown whether `Tr_Rules_General.md` and sections
> 1–6 above apply to it unchanged — specifically hedging enforcement, the 10-second rule,
> inactivity, maximum payout caps, consistency, whether it counts toward the
> 5-funded-account limit, and whether the static floor is enforced on net liquidation in
> real time.

---

## 12. Payout mechanics common to all

- **Profit split is 90/10** on Growth, Select and Lightning. Inter Miami is 80/10/10.
- **KYC must be completed before the first payout.** Residents of ten named countries must
  complete it before the funded account is even activated.
- **Only one payout request may be open per account at a time.** You cannot queue requests.
- Requests cannot be edited or cancelled once submitted.
- **Processing: within 24 hours of approval**, up to 72 hours over a weekend or outside
  Monday–Friday 08:00–17:00 ET.
- Paid via **Rise** (ACH or crypto); **Plane** is the fallback for those who cannot use
  Rise, taking up to 7 days. No PayPal.
- Rise issues the 1099, not Tradeify.
- **Trading after requesting but before approval is allowed**, but falling below the
  threshold gets the request denied.
- Profits made after approval in the same session count toward the **next** cycle.
- **Each account is treated independently.** With 5 funded accounts you can run 5 payout
  cycles in parallel.

---

## 13. Side-by-side

| | Growth | Select Flex | Select Daily | Lightning | Inter Miami |
|---|---|---|---|---|---|
| Drawdown, 50K | \$2,000 | \$2,000 | \$2,000 | \$2,000 | \$1,500 static |
| Daily loss limit, 50K | \$1,250 | **None** | \$1,000 | \$1,250 | \$900 |
| Contract scaling | No | **Yes** | **Yes** | No | Not published |
| Consistency when funded | **35%** | None | None | **20→25→30%** | None |
| 10-second rule | Yes | Yes | Yes | Yes | Not published |
| Payout cadence | 5 qualifying days | 5 winning days | Daily | Profit goal | Daily |
| Payout cap, 50K | \$1,500 → \$3,000 | \$2,500 | \$1,250/day | \$2,000 → \$2,500 | Not published |
| Payout formula | Flat cap | 50% of total profit | 2× cycle profit | Flat cap | Not published |
| Locked capital | None | None | **\$2,100 buffer** | None | Not published |
| Profit per \$1 withdrawn, 50K | 2:1 | 2:1 | **0.5:1** | 1.5:1 then 1:1 | Not published |
| Funded Reset | No | Yes (50K+) | Yes (50K+) | **No** | Not published |
| Split | 90% | 90% | 90% | 90% | **80%** |

---

## 14. What takes the account away

In order of how likely it is to catch a normal daytrader:

1. **An intraday excursion through the trailing drawdown floor, before the lock.** Enforced
   on net liquidation value, so an open position that dips far enough fails the account
   before it can recover. Invisible on the dashboard, which refreshes the drawdown figure
   only once per day.
2. **Not reaching the lock.** Everything above is permanent risk until the floor locks at
   starting balance + \$100. The fastest way to lock it is to request a payout, which
   locks it immediately regardless of balance.
3. **Trading Select Flex with no daily loss limit.** Nothing halts a deteriorating session;
   the trailing drawdown is the only backstop and it is fatal rather than protective.
4. **Relying on the DLL as protection when the drawdown is nearer.** The DLL only helps
   when there is more drawdown room than DLL room.
5. **Hedging across your own accounts**, including accidentally, when running several
   funded accounts at once. All accounts involved are set to violation status.
6. **Inactivity**, if an account is left untouched for a week.

A breached funded account cannot be reset, except narrowly via Funded Reset on Select
50K–150K where no payout has ever been taken.

---

## 15. What limits your profit

Ranked by how hard each binds.

1. **The payout cap, not the profit split.** The 90/10 split is the headline but is almost
   never the binding constraint. On a 50K Growth the cap is \$3,000 per 5 qualifying days
   no matter how much you earn; the other \$10,000 you might have made simply sits in the
   account.
2. **Cycle length.** Growth and Select Flex both require 5 qualifying or winning days per
   payout, which fixes the maximum extraction rate at roughly \$500–\$600 per trading day
   on a 50K regardless of performance. Select Daily is the only path without this ceiling.
3. **The payout formula.** Growth and Lightning use flat caps; Select Flex requires half of
   all profit to stay in the account permanently; Select Daily allows 2× cycle profit.
   These differ by a factor of four in how fast profit converts to cash.
4. **Consistency rules.** 35% on Growth and 20→25→30% on Lightning force profit to be
   spread across multiple days before any payout is permitted. A single outsized day
   delays the payout until total profit is large enough to dilute it. Select has none once
   funded.
5. **Profit goals that reset.** On Lightning, unearned profit does not carry between
   cycles, and the first goal is up to 3× the payout cap.
6. **Contract scaling on Select.** You start at 2 minis on a 50K and need \$2,000 of
   end-of-day profit to reach 4. Taking a payout can scale you back down.
7. **The buffer on Select Daily.** \$2,100 on a 50K is permanently unwithdrawable while
   the account lives.
8. **The 10-second rule.** Does not cap earnings directly, but blocks payouts entirely
   until the trade and profit ratios recover.
9. **Maximum 5 funded accounts per household.** The practical route to scale is parallel
   accounts, and this is the hard ceiling on that.
10. **The forced move to live.** Tradeify may move you after any successful payout, and a
    denied live application means no return to simulated trading.
