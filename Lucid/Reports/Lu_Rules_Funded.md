# Lucid — Funded Phase

Rules that apply once an account is funded: simulated capital, real payouts.

> **Read `Lu_Rules_General.md` first.** Trading hours, position limits, prohibited and
> permitted conduct, instruments, platforms, inactivity, fees and the general Max Loss
> Limit mechanic apply here and are not repeated. This document covers only what is
> specific to the funded phase, plus the parameters of each account type.

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

| | |
|---|---|
| Consistency rules appear or change | Section 2 |
| The Daily Loss Limit may convert to LucidScale | Section 3 |
| LucidFlex loses full contract size and must scale up | Section 4 |
| Payout buffers lock capital in the account | Per product, sections 6–9 |
| A breach is terminal — no reset exists | Section 5 |

**Nothing about the funded account can be changed once you are in it.** The Daily Loss
Limit, and on LucidDaily the drawdown type, were fixed when the evaluation was bought.

**Consistency by product once funded:**

| Product | Evaluation | Funded |
|---|---|---|
| LucidPro | None | **40%** (35% if purchased or reset before 11/28/2025, 3:00 PM EST) |
| LucidFlex | 40% or 50% | **None** |
| LucidDaily | 40% or 50% | **None** |
| LucidDirect | — | **20%** |

LucidPro is the only product that *gains* a consistency rule on funding. LucidFlex and
LucidDaily drop theirs entirely.

---

## 2. The Max Loss Limit when funded

The mechanic is unchanged from `Lu_Rules_General.md`: the floor trails the highest closing
balance until the account closes above the Initial Trail Balance, then locks permanently at
starting balance + \$100.

**The funded account starts fresh.** It is a new account at its base size — \$50,000 on a
50K — with the floor back at the full drawdown distance below it. **Nothing carries over
from the evaluation**: not the balance, not the profit, and not the locked floor. Whatever
you did to clear the Initial Trail Balance during the evaluation has to be done again.

**So every funded trader begins in the trailing phase.** On a 50K the floor starts at
\$48,000 and trails your closing balance until you close above \$52,100, at which point it
locks at \$50,100. Until then, profit you carry into a close converts part of your original
cushion into profit you must defend.

**LucidDirect has the same trailing phase**, reached by purchase rather than by passing an
evaluation. The difference is only that a Direct trader has never traded the mechanic
before, where a Pro, Flex or Daily trader has already been through it once during the
evaluation.

**Funded Max Loss Limits, Initial Trail Balances and locked floors:**

| Size | MLL (Pro / Flex / Daily) | MLL (Direct) | Initial Trail Balance | Locked floor |
|---|---|---|---|---|
| \$25,000 | \$1,000 | \$1,000 | \$26,100 | \$25,100 |
| \$50,000 | \$2,000 | \$2,000 | \$52,100 | \$50,100 |
| \$100,000 | \$3,000 | \$3,500 | \$103,100 — Direct \$103,600 | \$100,100 |
| \$150,000 | \$4,500 | \$5,000 | \$154,600 — Direct \$155,100 | \$150,100 |

**LucidFlex locks the floor on a payout request**, immediately and regardless of balance.
Requesting a payout is therefore a risk-reduction action as well as a withdrawal, and it is
the one way to leave the trailing phase early.

**What the floor follows depends on the product.** LucidPro, LucidFlex and LucidDirect
track the highest **closing** balance. **LucidDaily tracks whichever was bought** —
real-time P&L on an intraday build, or the closing balance on an end-of-day build. On an
intraday build the floor can rise, and the trailing phase can end, without any day having
closed higher.

> **Documentation conflict.** The LucidDirect Daily Loss Limit table gives the 25K Initial
> Trail Balance as "None"; the LucidDirect Drawdown table gives it as \$26,100.

---

## 3. Daily loss limit when funded

| Size | LucidPro | LucidFlex | LucidDaily | LucidDirect |
|---|---|---|---|---|
| \$25,000 | \$600 or off | \$600 or off | \$600 or off | **None** |
| \$50,000 | \$1,200 or off | \$1,200 or off | \$1,200 or off | \$1,200 |
| \$100,000 | \$1,800 or off | \$1,800 or off | \$1,800 or off | \$2,100 |
| \$150,000 | \$2,700 or off | \$2,700 or off | \$2,700 or off | \$3,000 |

On LucidPro, LucidFlex and LucidDaily the presence of a DLL was decided when the evaluation
was purchased and is permanent. On LucidDirect it is fixed by account size.

**What the DLL does.** It is a soft breach. LOCK. Lose the stated amount in one session and
you are blocked from placing further trades until the next session opens at 6:00 PM EST.
The account survives. Only the Max Loss Limit can end it.

### 3a. The LucidScale DLL

On **LucidPro and LucidDirect**, the fixed DLL is not permanent. Once the account closes
above the Initial Trail Balance — that is, once the trailing phase ends and the floor locks
— the fixed amount is replaced by a **LucidScale DLL**:

```
LucidScale DLL = highest end-of-day account profit × 60%
```

Three properties matter:

- **It is calculated from your best-ever day-end profit**, not your current balance.
- **It only ratchets up.** It never falls, even if you subsequently give the profit back.
  A \$4,000 peak sets the DLL at \$2,400 and it stays at \$2,400 until a higher end-of-day
  profit replaces it.
- **It starts roughly where the fixed DLL left off and then grows.** On a 50K Pro the
  trailing phase ends at \$52,100, which is \$2,100 of profit, giving a LucidScale DLL of
  \$1,260 against the \$1,200 fixed amount it replaces.

**It is still a daily loss limit.** Only the size of the allowance changes. It is a
per-session loss budget measured from your balance at the start of the session, it resets
every session, and hitting it locks you out until the next one. It is **not** a balance
level. The Max Loss Limit is the balance level.

**Why that distinction matters.** Both limits are live at once, and the one that is
**nearer** is the one you hit first:

- The **DLL** sits a fixed distance below *today's opening balance* — it moves with you.
- The **MLL** sits at a fixed balance — \$50,100 on a locked 50K — and does not move.

Early on the DLL is the nearer of the two, so it acts as a brake: you get locked out, the
account survives, you come back tomorrow. As the LucidScale allowance grows, it can become
larger than your remaining distance to the floor, at which point it can never trigger
first.

**Worked comparison, 50K Pro with the floor locked at \$50,100:**

| | Peak EOD profit | LucidScale DLL | Session opens at | DLL would halt you at | MLL ends you at | Which hits first |
|---|---|---|---|---|---|---|
| Just past the trail | \$2,100 | \$1,260 | \$52,100 | \$50,840 | \$50,100 | **DLL** — you survive |
| After a good run, then a giveback | \$10,000 | \$6,000 | \$51,000 | \$45,000 | \$50,100 | **MLL** — account gone |

In the second row the \$6,000 daily allowance is meaningless: you only have \$900 of room
before the floor, so the account ends before the DLL has any say.

**So the DLL's protective value declines the more successful you have been.** The
allowance is set by your best day ever, but the risk is set by where your balance is now.

**LucidDaily keeps the fixed DLL permanently.** It does not convert to LucidScale, so its
daily cap stays at \$600 / \$1,200 / \$1,800 / \$2,700 for the life of the account.

**LucidFlex funded cards show no LucidScale row at all**, only a fixed DLL below the
Initial Trail Balance. Whether it converts above the trail is not documented either way.

### 3b. What turning the DLL off actually does

The effect is **not** the same across products, because it only removes whichever cap the
product would otherwise have applied:

| Product | Below the Initial Trail Balance | Above it |
|---|---|---|
| LucidPro | No daily cap | **LucidScale DLL still applies** |
| LucidDirect | n/a — not a choice | LucidScale DLL applies |
| LucidFlex | No daily cap | No cap shown on the card |
| LucidDaily | No daily cap | No daily cap — the fixed DLL is simply gone |

**On LucidPro the choice only affects the trailing phase** — and that is the phase where it
matters most. The Pro DLL-off funded card still shows the LucidScale DLL above the trail,
so you are buying freedom from a daily cap precisely while the floor is still trailing up
behind you and your cushion is at its smallest, then having a cap reinstated once the floor
has locked and the risk is static. That is the opposite of the order you would choose.

**With the DLL off, nothing stops a bad session except the Max Loss Limit**, and reaching
that is terminal. There is no soft brake, no forced pause, and no opportunity to come back
the next day.

### 3c. What turning the DLL off does to your payouts

This is the part most easily missed, because it is a payout setting disguised as a risk
setting.

| | DLL On | DLL Off |
|---|---|---|
| Daily loss cap | Yes | No |
| **On Demand Payouts** | **Available** | **Not available** |
| When you can request | During the session, 6:00 PM to 3:45 PM ET, from profit made that session | End-of-day schedule only |

**With the DLL on**, you may request a payout intraday from profit earned in the current
session. Trading on that account is then paused until the end of the trading day.

**With the DLL off**, that option is removed entirely and every payout waits for the
end-of-day cycle. The toggle is locked red on the plan card — you cannot have both no daily
cap and intraday payouts.

**This costs the most on LucidDaily**, whose entire proposition is daily payouts: turning
the DLL off downgrades the product's headline feature. It costs least on LucidPro and
LucidFlex, where the payout cadence is already 3 and 5 days respectively, so same-session
access saves hours rather than days.

**LucidDirect follows the same logic without a choice:** the 25K has no DLL and therefore
takes end-of-day payouts only, while 50K and above have a DLL and get On Demand Payouts.

**A hedging violation permanently removes intraday payout eligibility**, regardless of
which configuration you bought.

LucidDirect follows the same logic without a choice: the 25K has no DLL and so takes
end-of-day payouts only, while 50K and above have On Demand Payouts.

---

## 4. Contract scaling when funded

- **LucidPro and LucidDirect: full contract size immediately.** Both state "no scaling
  plan, access to max contract size immediately".
- **LucidDaily: no scaling plan row appears on the cards.**
- **LucidFlex: a scaling plan applies**, based on simulated profit in the account:

| Simulated profit | 25K | 50K | 100K | 150K |
|---|---|---|---|---|
| \$0 – \$999 | 1 mini | 2 minis | 3 minis | 4 minis |
| \$1,000 – \$1,999 | 2 minis | 3 minis | 4 minis | 5 minis |
| \$2,000 – \$2,999 | — | 4 minis | 5 minis | 6 minis |
| \$3,000 – \$4,499 | — | — | 6 minis | 8 minis |
| \$4,500+ | — | — | — | 10 minis |

**The LucidFlex scaling plan moves both ways.** Limits "move up and down" with profit and
update at the end of each session, not in real time. Because a payout reduces the balance,
**taking a payout can scale you down**. The table also has no open-ended top row, so the
limit above the highest listed tier is not explicitly stated.

---

## 5. Account lifecycle when funded

- **A breached funded account cannot be reset.** The reset product described in the fees
  article covers evaluation accounts. No equivalent exists for funded accounts anywhere in
  the documentation.
- **The 30-day inactivity rule still applies.** An account with less than \$1 of net profit
  or loss across 30 calendar days is permanently deleted.
- **Maximum 5 funded accounts per household**, and a combined cap of 10 across evaluation
  and funded accounts.
- **No ongoing fees.** Nothing is charged once the account is funded.
- **Each account is independent.** Payout cycles run in parallel across accounts.

---

## 6. Account type: LucidPro — funded

### 6.1 Rules and risk

- Max Loss Limit: \$1,000 / \$2,000 / \$3,000 / \$4,500. End-of-day drawdown.
- Daily Loss Limit: \$600 / \$1,200 / \$1,800 / \$2,700, or off, converting to the
  **LucidScale DLL** above the Initial Trail Balance.
- **Consistency: 40%**, applying to every payout. This does not exist during the LucidPro
  evaluation — it appears only once funded. Accounts purchased or reset before 11/28/2025
  at 3:00 PM EST retain 35%.
- **Full contract size immediately**: 2 / 4 / 6 / 10 minis. No scaling plan.
- **Days to payout: 3.**

### 6.2 What caps your earnings

| Lever | Value (25K / 50K / 100K / 150K) |
|---|---|
| Buffer — balance you cannot withdraw below | \$26,100 / \$52,100 / \$103,100 / \$154,600 |
| Minimum profit goal per cycle | \$250 / \$500 / \$750 / \$1,000 |
| Consistency | 40% — largest day ≤ 40% of cycle profit |
| Days to payout | 3 |
| Minimum payout | \$500 |
| Profit split | 90% to you |
| Payouts before the move to live | 5 |

Maximum payout and the balance needed to take it:

| Size | Max payout 1 | Balance needed | Max payout 2+ | Balance needed |
|---|---|---|---|---|
| 25K | \$1,000 | \$27,100 | \$1,500 | \$27,600 |
| 50K | \$2,000 | \$54,100 | \$2,500 | \$54,600 |
| 100K | \$2,500 | \$105,600 | \$3,000 | \$106,100 |
| 150K | \$3,000 | \$157,600 | \$3,500 | \$158,100 |

**The buffer is permanently locked capital.** On a 50K, \$2,100 of profit can never be
withdrawn while the account lives.

**The minimum profit goal is rarely binding.** On a 25K it is \$250 against a \$500 minimum
payout, so the payout minimum controls. The consistency rule and the buffer are the real
constraints.

**The 40% consistency rule forces at least three profitable days.** Combined with the
3-day payout requirement, that is the floor on cycle length.

**Worked throughput, 50K:** \$2,500 per 3 trading days, so roughly **\$833 per trading
day** at steady state — the highest per-day ceiling of any Lucid product with a payout cap.

---

## 7. Account type: LucidFlex — funded

### 7.1 Rules and risk

- Max Loss Limit: \$1,000 / \$2,000 / \$3,000 / \$4,500. End-of-day drawdown.
- Daily Loss Limit: \$600 / \$1,200 / \$1,800 / \$2,700, or off. No LucidScale row on the
  cards.
- **No consistency rule.** The 40%/50% requirement ended at the evaluation.
- **Contract scaling applies** — see section 4. This is the only Lucid product where it
  does.
- **The floor locks the moment you request a payout.**

### 7.2 What caps your earnings

| Lever | Value (25K / 50K / 100K / 150K) |
|---|---|
| Buffer | **None** |
| Minimum balance to request | **None** |
| Qualifying days per cycle | 5 days with profit above \$100 / \$150 / \$200 / \$250 |
| Net profit for the cycle | Must be positive — even \$1 |
| Payout formula | **50% of profit**, capped |
| Payout cap | \$1,000 / \$2,000 / \$2,500 / \$3,000 |
| Minimum payout | \$500 |
| Profit split | 90% to you |
| **Payouts per account** | **5, then moved live** |

**There is no buffer and no minimum balance.** LucidFlex is the only Lucid funded product
that locks no capital at all — you can request a payout after 5 qualifying days regardless
of account balance.

**The caps do not scale with payout number.** Unlike every other Lucid product, the figures
above apply to all five payouts.

#### How the 50% formula works

**You may withdraw half the profit sitting in the account, and half must stay behind** —
subject to the cap. "Profit" means `current balance − starting balance`. Because every
payout is deducted from the balance, previous withdrawals drop out of the calculation
automatically; there is no running ledger of what you have taken before.

The half you leave behind is **not** dead money. It stays in the account and counts toward
the next cycle's profit, so each payout is larger than the last even if your trading is
unchanged — until the cap takes over.

**Worked example: 50K LucidFlex, cap \$2,000, earning \$2,500 per cycle.**

| Cycle | Earned | Balance before | Profit in account | 50% of profit | Capped? | Withdrawn | Balance after |
|---|---|---|---|---|---|---|---|
| 1 | \$2,500 | \$52,500 | \$2,500 | \$1,250 | no | \$1,250 | \$51,250 |
| 2 | \$2,500 | \$53,750 | \$3,750 | \$1,875 | no | \$1,875 | \$51,875 |
| 3 | \$2,500 | \$54,375 | \$4,375 | \$2,187 | **yes** | \$2,000 | \$52,375 |
| 4 | \$2,500 | \$54,875 | \$4,875 | \$2,437 | **yes** | \$2,000 | \$52,875 |
| 5 | \$2,500 | \$55,375 | \$5,375 | \$2,687 | **yes** | \$2,000 | \$53,375 |

After the fifth payout the account is moved live.

**Reading the example:**

- **The cap binds from cycle 3.** On a 50K it starts biting once profit in the account
  reaches \$4,000, because half of that is the \$2,000 cap. From then on the percentage is
  irrelevant and you simply receive the cap.
- **Total generated: \$12,500. Total withdrawn: \$9,125** gross, or \$8,212 after the 90/10
  split.
- **\$3,375 of profit is still sitting in the account** when the fifth payout forces the
  move to live. What happens to it is not documented — see `Lu_Rules_Live.md`.
- **The floor locks on the first payout request**, so from cycle 1 onward the Max Loss
  Limit is fixed at \$50,100 and the trailing phase is over.

**The first payout needs \$1,000 of profit, not \$500.** The minimum request is \$500 and
you can only ask for half, so \$1,000 in the account is the real threshold. The 5 qualifying
days at \$150 only guarantee \$750, so profit — not day count — is usually the binding
constraint on the first cycle.

**Worked throughput, 50K:** \$2,000 per 5 qualifying days, so roughly **\$400 per trading
day**, and only once profit reaches \$4,000.

**Lifetime ceiling per account: \$10,000 gross** at 50K — five payouts at the \$2,000 cap —
reachable only if profit exceeds \$4,000 before the third cycle.

> **Documentation defect.** The payouts article says traders "may request 50% of their
> account **balance**", while the table on the same page says "50% of **Profit**". On a 50K
> the first reading would permit a \$25,000 withdrawal. The table is the sensible one and
> is used throughout here.

> **Ambiguity.** Lucid does not state whether "profit" means profit currently in the
> account or profit earned since the last payout. This document uses the former, which
> matches how LucidDaily measures profit above its buffer. Under the latter reading every
> payout in the example above would be \$1,250 and the cap would never bind.

**The account ends after five payouts.** At 50K that caps total extraction from a single
LucidFlex account at \$10,000 before a forced move live.

**Taking a payout can shrink your contract limit**, because the scaling tier is measured
against the reduced balance.

---

## 8. Account type: LucidDirect — funded

### 8.1 Rules and risk

- Max Loss Limit: \$1,000 / \$2,000 / **\$3,500** / **\$5,000** — larger than the
  evaluation products at 100K and 150K. End-of-day drawdown.
- Daily Loss Limit: **none at 25K**, then \$1,200 / \$2,100 / \$3,000, converting to the
  **LucidScale DLL** above the Initial Trail Balance.
- **Consistency: 20%** — the strictest on the platform, applying to every payout.
- **Full contract size immediately**: 2 / 4 / 6 / 10 minis. No scaling plan.
- **Minimum 5 days to payout.**
- **Maximum 5 accounts.**
- **The floor trails from day one.** With no evaluation behind you, the account starts
  below the Initial Trail Balance and the give-back mechanic is live until it is cleared.

### 8.2 What caps your earnings

| Lever | Value (25K / 50K / 100K / 150K) |
|---|---|
| Consistency | **20%** — largest day ≤ 20% of cycle profit |
| Profit goal, payout 1 | \$1,500 / \$3,000 / \$6,000 / \$9,000 |
| Profit goal, payout 2+ | \$1,250 / \$2,500 / \$3,500 / \$4,500 |
| Minimum days to payout | 5 |
| Minimum payout | \$500 |
| Profit split | 90% to you |

Maximum payout per request:

| Payout | 25K | 50K | 100K | 150K |
|---|---|---|---|---|
| 1–3 | \$1,000 | \$2,000 | \$2,500 | \$3,000 |
| 4–5 | \$1,000 | \$2,500 | \$3,000 | \$3,500 |

**The profit goal is not the payout.** On a 150K you must earn \$9,000 to unlock the first
payout and may then withdraw at most \$3,000. Profit required per dollar withdrawn on
payout 1: **3:1**.

**The 20% consistency rule forces at least five profitable days.** On a 50K needing
\$3,000, no single day may exceed \$600. This is the tightest consistency requirement on
the platform and it never eases.

**Profit goals reset after each approved payout**, so leftover profit does not count toward
the next goal. The money stays in the account and continues to work as cushion — only the
eligibility counter resets.

> **Data gap.** The payout maximum table stops at "Payouts 4-5", with no row for a sixth,
> while the LucidDirect Live article refers to "their sixth and final LucidDirect payout".

---

## 9. Account type: LucidDaily — funded

### 9.1 Rules and risk

- Max Loss Limit: \$1,000 / \$2,000 / \$3,000 / \$4,500.
- **Drawdown type was chosen at purchase: intraday or end-of-day.** Intraday is the
  default and the cheaper option; under it the floor moves with real-time P&L, so an
  unrealised run-up that is given back permanently costs room. The end-of-day option
  removes that entirely and is the most expensive choice Lucid sells — at 50K it takes the
  account from \$65.80 to \$235.20. An end-of-day funded drawdown is only available if the
  evaluation was also bought as end-of-day.
- Daily Loss Limit: \$600 / \$1,200 / \$1,800 / \$2,700, or off. **Fixed — it does not
  convert to LucidScale.**
- **No consistency rule.**
- **News trading is a hard breach.** KILL. US high-impact events only; flat from one
  minute before to one minute after.
- No scaling plan shown on the cards.

### 9.2 What caps your earnings

| Lever | Value (25K / 50K / 100K / 150K) |
|---|---|
| Buffer — balance you cannot withdraw below | \$26,100 / \$52,100 / \$103,100 / \$154,600 |
| Payout frequency | **Daily** |
| Payout formula | **All simulated profit above the buffer** |
| Payout cap | **None** |
| Net profit since last payout | Must be positive |
| Minimum payout | \$500 |
| Profit split | 90% to you |
| Maximum daily profit | \$6,000 / \$8,000 / \$10,000 / \$12,000 |

**There is no payout cap.** LucidDaily is the only Lucid product where the withdrawable
amount is simply everything above the buffer. Profit required per dollar withdrawn is
**1:1** once the buffer is cleared.

**But there is a ceiling on a single day's profit.** Meeting or exceeding the maximum daily
profit **automatically moves the account to live**. That is not a breach, but it ends the
simulated account on Lucid's timetable rather than yours, and on the move only
\$15,000 of simulated profit in total is payable — see `Lu_Rules_Live.md`.

**The buffer is permanently locked capital** and, uniquely on this product, is never paid
out: on the move to live it funds the starting live drawdown instead.

**Worked throughput, 50K:** unlimited per day in principle, bounded in practice by the
\$8,000 maximum daily profit and, on an intraday-drawdown build, by the drawdown itself.

---

## 10. Payout mechanics common to all

- **Profit split is 90% to the trader / 10% to Lucid** on every funded product. Accounts
  purchased or reset before 11/28/2025 at 3:00 PM EST keep 100% of the first \$10,000.
- **There is no fixed payout window.** Request on any day once the criteria are met.
- **Requests are final** — they cannot be edited or cancelled once submitted.
- **Approved funds leave the account within minutes** and are disbursed within 2 business
  days.
- Paid via **Plaid** (US instant bank), **WorkMarket by ADP** (US and international, bank
  or PayPal) or **crypto** (international only).
- **Trading after a request but before approval is allowed**, but dropping into the buffer
  gets the request denied. Trade as though the money has already left.
- **Accounts with a hedging violation lose intraday payout eligibility.**

---

## 11. Side-by-side

| | LucidPro | LucidFlex | LucidDirect | LucidDaily |
|---|---|---|---|---|
| Drawdown type | EOD | EOD | EOD | **Intraday or EOD** |
| Max Loss Limit, 50K | \$2,000 | \$2,000 | \$2,000 | \$2,000 |
| Daily loss limit, 50K | \$1,200 or off | \$1,200 or off | \$1,200 | \$1,200 or off |
| LucidScale DLL | Yes | Not shown | Yes | **No — fixed** |
| Contract scaling | No | **Yes** | No | Not shown |
| Consistency when funded | **40%** | None | **20%** | None |
| Payout cadence | 3 days | 5 qualifying days | 5 days | **Daily** |
| Payout cap, 50K | \$2,000 → \$2,500 | \$2,000 | \$2,000 → \$2,500 | **None** |
| Payout formula | Flat cap | 50% of profit | Flat cap | All above buffer |
| Locked capital, 50K | \$2,100 buffer | **None** | None stated | \$2,100 buffer |
| Profit per \$1 withdrawn, 50K | ~1:1 | 2:1 | 1.5:1 then 1:1 | **1:1** |
| Payouts before live | 5 | 5 | 5 (6 per one article) | Not counted |
| Funded reset | No | No | No | No |

---

## 12. What takes the account away

In order of how likely it is to catch a normal daytrader:

1. **Reaching the Max Loss Limit.** KILL, with no reset and no second chance. For LucidPro,
   LucidFlex and LucidDaily the floor is usually already locked at starting balance + \$100,
   which makes this a fixed and knowable line. For **LucidDirect it is not** — the floor
   trails from day one until the Initial Trail Balance is cleared.
2. **Giving back an unrealised run-up on an intraday-drawdown LucidDaily.** Intraday
   drawdown counts the peak as it happens, so a trade that goes +\$1,500 and returns to
   flat has permanently removed \$1,500 of room. This applies only if the account was
   bought with the intraday funded drawdown — the default and cheaper option. An
   end-of-day funded build is immune to it.
3. **Trading US high-impact news on a funded LucidDaily account.** A hard breach, and the
   only product where news is restricted at all.
4. **Turning the Daily Loss Limit off at purchase.** With no soft brake, the Max Loss Limit
   is the only control and reaching it is terminal.
5. **Hedging across your own accounts.** The first-offence penalty resets the balance to the
   prior day but **not** the drawdown, leaving the account worse off than it started.
   Repeated offences breach every account involved.
6. **Microscalping**, if more than half your profit comes from trades held 5 seconds or
   less. Profits are forfeited and repeat offences end the relationship.
7. **Inactivity** for 30 calendar days. Permanent deletion.

---

## 13. What limits your profit

Ranked by how hard each binds.

1. **The payout cap and cadence together.** On LucidPro a 50K is capped at \$2,500 every 3
   days; on LucidFlex at \$2,000 every 5 qualifying days; on LucidDirect at \$2,500 every 5
   days. **LucidDaily has no cap at all**, which makes it the structural outlier.
2. **The five-payout ceiling.** LucidPro, LucidFlex and LucidDirect all end after five
   payouts and move you live. At 50K that caps lifetime extraction from a single account at
   roughly \$10,000 to \$12,000 before you lose control of the timing.
3. **The buffer.** \$2,100 on a 50K Pro or Daily can never be withdrawn while the account
   lives. On LucidDaily it is never paid out at all — it funds the live drawdown.
4. **Consistency rules.** 20% on LucidDirect forces at least five profitable days per cycle
   and never eases. 40% on LucidPro forces at least three. LucidFlex and LucidDaily have
   none once funded.
5. **Profit goals that reset.** On LucidDirect the first goal is up to 3× the payout cap,
   and unearned progress does not carry between cycles.
6. **The LucidFlex 50% formula.** Half of the profit in the account must stay behind at
   every request, which is the slowest conversion of profit to cash on the platform.
7. **Contract scaling on LucidFlex.** You start at 2 minis on a 50K and need \$2,000 of
   profit to reach 4 — and a payout can push you back down a tier.
8. **The maximum daily profit on LucidDaily.** Exceeding it forces a move to live, where
   only \$15,000 of simulated profit in total is payable regardless of how many accounts
   you hold.
9. **Maximum 5 funded accounts per household**, with a combined cap of 10 across evaluation
   and funded. Parallel accounts are the route to scale and this is the hard ceiling.
10. **The forced move to live**, which is covered in `Lu_Rules_Live.md` and is the point at
    which simulated profit stops being fully recoverable.
