# Case 2 — Pass One Evaluation and Extract \$5,000–\$10,000

## 1. The goal

Buy **one** account, pass its evaluation, then withdraw **\$5,000 to \$10,000** of real
money from that **single funded account**, and then move to trading own capital.

No second account, no scaling, no long-term income. The account is a **one-off extraction
vehicle**.

Figures below use the central assumptions from `Relevant_for_Comparison.md`: **one MNQ**,
**50% win rate**, **\$200 stop / \$400 target**, **15 trades per month across roughly 6–7
sessions**, giving **+\$1,500 per month** and about **\$230 per session**.

---

## 2. How this differs from Case 1

Case 1 could ignore every payout rule and did not even need to pass. This case inverts
that completely.

| | Case 1 | Case 2 |
|---|---|---|
| Passing the evaluation | Optional | **Mandatory** |
| Profit target | Irrelevant | **First hurdle, and pure overhead** |
| Payout caps and cadence | Irrelevant | **Primary constraint** |
| Consistency rules | Irrelevant | **Binding at every payout** |
| Profit split | Irrelevant | **Costs 10% of everything** |
| Holding period | ~2 months | **6 to 12 months** |
| Account survival | Nice to have | **The entire thesis** |
| Lifetime per-account ceilings | Irrelevant | **Can make \$10,000 impossible** |

What still does not matter: scaling plans, contract limits, the terms of the live account
itself, and anything about running several accounts in parallel.

---

## 3. The arithmetic of extraction

Money received is not money earned. Three layers sit between them.

### 3.1 The three layers

1. **The evaluation profit target.** Earned, then discarded — the funded account starts
   fresh at the base balance. Nothing carries over.
2. **Capital that cannot leave the account.** Either a named buffer, or the half of profit
   a 50% payout formula leaves behind, or simply the distance you must keep above the
   drawdown floor.
3. **The profit split.** At 90/10, receiving \$10,000 requires withdrawing **\$11,111**
   gross.

So:

> **Total simulated profit required = evaluation target + gross withdrawal + capital
> parked in the account.**

### 3.2 What that costs on a 50K account

Gross withdrawal needed: **\$5,556** for \$5,000 received, **\$11,111** for \$10,000
received.

| Payout structure | Parked capital, 50K | Total profit for \$5,000 | Total profit for \$10,000 |
|---|---|---|---|
| **Buffered** (balance can never fall below start + drawdown + \$100) | \$2,100 | **\$10,656** | **\$16,211** |
| **50%-of-profit formula** (half of each cycle stays behind) | ~\$2,000–\$2,500 | **\$10,556–\$11,056** | **\$16,111–\$16,611** |
| **Flat cap, no buffer** (only the locked floor stops you) | ~\$100 | **\$8,656** | **\$14,211** |
| **100% split on the first \$25,000** (one provider only) | \$2,600 | \$10,600 | \$15,600 |

**Derived values.** These follow from the published buffers, caps and splits; they are not
quoted figures.

### 3.3 The overhead is 60–90%

To receive \$5,000 you must generate roughly **\$9,000–\$11,000** of simulated profit. To
receive \$10,000 you must generate roughly **\$14,000–\$16,500**.

**Between 37% and 46% of everything earned never reaches you.** The evaluation target is
the single largest component of that and buys nothing.

---

## 4. How long it takes

### 4.1 Generation time at one contract

At \$1,500 per month:

| Total profit required | Sessions needed | Months |
|---|---|---|
| \$8,656 | 38 | **5.8** |
| \$10,656 | 46 | **7.1** |
| \$14,211 | 62 | **9.5** |
| \$16,211 | 70 | **10.8** |

At the low end of the trading frequency (one session per week, 8 trades per month) these
roughly double, to **11 to 21 months**.

**This is not a two-month project.** At one contract, \$5,000 received is a six-to-seven
month commitment and \$10,000 is closer to a year.

### 4.2 Payout cadence stretches badly, because qualifying days must be profitable

Most payout cycles are counted in **qualifying days** — days closing with a minimum
profit, typically \$150 on a 50K — not in sessions traded.

At a 50% win rate with 1–3 trades per session, roughly **58% of sessions end profitable
enough to qualify**. So:

| Requirement | Sessions needed | Calendar time at 1–2 sessions/week |
|---|---|---|
| 3 trading days | ~3 | 1.5–3 weeks |
| 3 profitable days (40% consistency) | ~5 | 2.5–5 weeks |
| 5 qualifying days | **~9** | **4.5–9 weeks** |
| 8 trading days | ~8 | 4–8 weeks |
| Daily eligibility | 1 | days |

### 4.3 Cadence against generation

Cycles run **in parallel** with profit generation, so the binding constraint is whichever
is longer, not the sum.

| Payout cadence | Cycles for \$11,111 gross | Sessions consumed | Binds? |
|---|---|---|---|
| Daily eligibility | 1–9 | 1–15 | No |
| 3 trading days, cap \$2,500 | 5 | ~25 | No |
| 5 qualifying days, cap \$2,000–\$2,500 | 5 | **~43** | **Close to binding** |
| 8 trading days, cap \$2,000 | 5 | ~40 | Close to binding |

Generation needs ~70 sessions for \$10,000 received, so cadence does not usually decide the
outcome — **but it does decide how much is still trapped in the account when things go
wrong.** On a 5-qualifying-day product you are still collecting the final payouts at the
very end of the run, with the largest sum exposed.

**Daily-eligible payouts are worth a real premium in this case**, not because they are
faster overall, but because they move money out of reach of a breach sooner.

---

## 5. Constraints that can make the target unreachable

### 5.1 Lifetime ceilings on a single account

Several products end the account after a fixed number of payouts and move it live.

| Structure | Lifetime gross, 50K | Received after split | \$10,000 reachable? |
|---|---|---|---|
| 5 payouts capped at \$2,000 | \$10,000 | \$9,000 | **No** |
| 5 payouts, \$2,000 then \$2,500 | \$12,000 | \$10,800 | Only just — needs all five |
| Caps that never lift, unlimited payouts | unlimited | unlimited | Yes |
| No cap at all, buffer only | unlimited | unlimited | Yes |

**The upper half of the stated range eliminates whole product categories.** At \$5,000 every
structure works; at \$10,000 some cannot deliver from one account no matter how well you
trade.

### 5.2 Forced move to live

Two separate mechanisms end the simulated account on the provider's timetable:

- **A fixed payout count** (typically five), after which the account goes live
  automatically.
- **Provider discretion** after any successful payout.

Either way, **profit left in the account at that moment is of undocumented status**. In
this case the live account is unwanted — the exit is to own capital — so an early forced
move converts remaining profit into an open question.

**Practical consequence: do not leave profit in the account that you intend to withdraw.**
Take it as soon as the rules permit.

### 5.3 Consistency rules, measured against a single-contract day

A consistency rule caps the largest single day as a share of the cycle's profit. At one
MNQ the largest realistic day is three wins, **+\$1,200**.

Cycle profit required before that day is permitted:

| Largest day | 20% rule | 30% | 35% | 40% |
|---|---|---|---|---|
| +\$400 (1 win) | \$2,000 | \$1,333 | \$1,143 | \$1,000 |
| +\$800 (2 wins) | \$4,000 | \$2,667 | \$2,286 | \$2,000 |
| **+\$1,200 (3 wins)** | **\$6,000** | **\$4,000** | **\$3,429** | **\$3,000** |

Compare against the profit a cycle actually needs — typically \$2,000 to \$4,500 on a 50K:

- **40% and 35% rules are essentially non-binding**, except on a cycle that happens to
  contain a three-win day early.
- **30% is sometimes binding**, forcing extra days before the payout clears.
- **20% is routinely binding.** It can require double the profit the payout itself needs.

**A strict consistency rule does not reduce what you earn — it delays when you may take
it**, which in this case means more sessions of breach exposure per dollar extracted.

---

## 6. Survival over the holding period is the real risk

This case asks the account to live for **6 to 12 months and 100 to 160 trades**, against
Case 1's 8 to 17 sessions. Everything about risk changes scale.

### 6.1 Cushion above the floor is what keeps the account alive

Once the drawdown floor locks it stops moving, and the only thing between the account and
death is the distance from the current balance down to that floor.

After a maximum payout, that distance is exactly the parked capital:

| Payout structure | Balance after a maximum payout, 50K | Consecutive \$200 losses to death |
|---|---|---|
| Buffered | floor + \$2,000 | **10** |
| 50%-of-profit formula | floor + ~\$2,000–\$2,500 | 10–12 |
| Flat cap, no buffer | floor + as little as \$100 | **1** |

**The buffer is not purely a cost.** The capital it locks away is the same capital that
keeps the account alive. The structure that lets you extract the most per dollar earned
is the structure that leaves you closest to the floor.

### 6.2 Streak risk over the full holding period

At a 50% loss rate, over ~160 trades:

| Run length | Probability of occurring somewhere in the run |
|---|---|
| 5 losses | Near certain |
| 10 losses | **Roughly 15%** |
| 15 losses | Under 1% |

**Roughly a one-in-seven chance of a ten-loss streak** over the time this case requires. On
a 50K with a \$2,000 cushion that is a direct account loss, with every un-withdrawn dollar
gone with it.

### 6.3 The operating rule that follows

**Never withdraw down to the cap when the cap would leave less than five stops of room.**
On a \$200 stop that means keeping at least **\$1,000** above the floor at all times.

This voluntarily recreates, on an unbuffered product, the buffer that a buffered product
imposes — which largely erases the capital-efficiency advantage calculated in section 3.2.

---

## 7. Rules that become live risks only because the holding period is long

A rule with a 1% chance of firing per month is nearly harmless over two months and a real
threat over ten.

| Rule | Why it matters now |
|---|---|
| **Weekly inactivity requirement** | At 1–2 sessions per week there is no margin. Over 6–12 months a holiday, an illness or a quiet week is close to certain. **Account closed.** |
| **30-day inactivity requirement** | Comfortable even with a two-week gap. |
| **News trading as a hard breach** | The session contains the 10:00 ET release slot. Over ~50 sessions, accidental exposure is likely rather than possible, and the penalty is the account. |
| **Trailing drawdown before the lock** | Only dangerous in the opening weeks, but that danger is now one of many months rather than the whole project. |
| **Intraday drawdown enforcement** | Every unrealised peak over 6–12 months permanently costs room. Compounds badly across a long run. |

**The weekly inactivity rule and the hard news rule are the two that can end this case
outright**, and neither has anything to do with trading badly.

---

## 8. The early-payout decision

Requesting a payout **locks the drawdown floor immediately**, regardless of balance. That
makes the first payout a risk-reduction action, not just a withdrawal.

But on products offering a **Funded Reset** — a second chance after a breach — eligibility
is void the moment any payout has ever been taken.

| | Take the first payout as early as possible | Delay it to preserve a reset |
|---|---|---|
| Floor | Locked early, cushion stops shrinking | Still trailing |
| Money out of reach of a breach | Yes, immediately | No |
| Second chance after a breach | **Forfeited permanently** | Retained |

**For this case the early payout is the better side of the trade.** The goal is cash
extracted, not an account preserved; a reset returns a fresh account with zero profit and a
reset payout clock, which costs months that this case cannot easily absorb.

---

## 9. What this case requires from a product

A specification, in priority order:

| # | Requirement | Reason |
|---|---|---|
| 1 | **Lifetime extraction ceiling above \$11,111 gross on one account** | Otherwise \$10,000 is impossible |
| 2 | **No weekly inactivity requirement** | 1–2 sessions per week has no margin over 6–12 months |
| 3 | **No hard news-trading breach** | The 10:00 ET slot sits inside the session |
| 4 | **End-of-day or static drawdown** | 6–12 months of unrealised peaks under intraday trailing |
| 5 | **Daily or 3-day payout eligibility** | 5 qualifying days is ~9 sessions, ~4.5–9 weeks |
| 6 | **Consistency rule at 35% or looser, or none** | 20% roughly doubles the profit needed per cycle |
| 7 | **One-time pricing, not monthly** | A 6–12 month hold multiplies any subscription by 6–12 |
| 8 | **Drawdown of \$2,000 or more** | 10 consecutive losses at a \$200 stop |
| 9 | Low parked capital | Worth least — see section 6.1, the parked capital is also the cushion |

**Requirement 7 is far more important here than in Case 1.** A subscription that looks
cheap at \$20 per month costs \$120–\$240 over this holding period, plus any activation
fee, and the account is lost the moment a payment is missed.

---

## 10. Open questions for this case

### Would change the recommendation

1. **Is \$5,000 or \$10,000 the real target?** They are different projects. \$5,000 is
   roughly six months and every product structure can deliver it. \$10,000 is roughly a
   year and rules out any product with a five-payout, \$2,000-capped ceiling. **If the
   number is flexible, \$5,000 is disproportionately easier.**

2. **Is this money you need, or money you are happy to not receive?** At one contract the
   expected outcome is positive but the variance is large, and there is a realistic chance
   of ending the project with zero received and the purchase price spent.

3. **How many contracts are you willing to trade?** This is the only lever that
   meaningfully shortens the timeline. Two MNQ halves the time and doubles the risk per
   trade; on a 50K that means \$400 against a \$2,000 drawdown, which section 2.3 of
   `Relevant_for_Comparison.md` rules out. **Moving up a size to trade two contracts raises
   the evaluation target by as much as it raises the earnings rate**, so it buys risk
   capacity rather than speed.

4. **Can the session count rise?** Going from 1–2 sessions per week to 3 is a larger effect
   than any product choice in this document.

### Would narrow the choice

5. **If the account breaches at month eight, what happens?** Buy another and start again,
   or stop? This decides whether reset availability and a second purchase belong in the
   budget.

6. **Is a forced move to live acceptable?** The stated exit is own capital. If a live
   account is simply unwanted, products that automatically go live after five payouts carry
   a real risk of stranding profit that was never withdrawn.

7. **Would straight-to-funded be acceptable instead of passing an evaluation?** It removes
   the entire evaluation target — about two months and \$3,000 of pure overhead — at the
   cost of a much higher purchase price and, typically, a 20% consistency rule. **This is
   the single largest structural saving available in this case.**

8. **Is a longer holding period acceptable if it is cheaper?** The cheapest products are
   generally the slowest to pay out.

### Useful to confirm

9. **Is the \$5,000–\$10,000 figure gross or in hand?** This document assumes in hand, after
   the profit split. Gross would reduce every figure here by about 10%.

10. **Would you stop at the target, or keep going if the account is running well?** If the
    answer is "keep going", this is not Case 2 and the lifetime ceilings in section 5.1
    become the dominant criterion.
