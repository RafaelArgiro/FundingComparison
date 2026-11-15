# Relevant for Comparison

What the trading profile in `Trading_Style_Info.md` means for choosing a provider and
product. This document does not restate the profile; it derives consequences from it.

Figures use the central assumptions: **50% win rate**, **MNQ only**, **\$200 stop /
\$400 target**, **15 trades per month**.

---

## 1. Hard filters

Applied before anything else, because they remove options outright.

### 1.1 Netherlands residency

| Provider | Status | Note |
|---|---|---|
| Lucid | **Available** | Netherlands is not on the restricted-country list |
| Tradeify | **Available** | Netherlands is not among the 65 restricted countries |
| Apex | **Must be verified** | The purchase-page risk disclosure states services "are intended for **U.S. users only**" |

**The Apex position needs settling before any further work on it.** The same page links to
a separate Restricted Countries list that was not captured, and the two statements imply
different scopes. If the US-only disclosure is enforced, Apex is out.

**Payout rails are also affected.** Instant US-only bank transfer options are unavailable;
the usable routes are the international providers each firm offers, plus crypto. Tax
paperwork is issued by US processors and will need handling as a non-US resident.

### 1.2 Tradovate preference

| Provider | Tradovate | Consequence |
|---|---|---|
| Lucid | Yes, via CQG | No penalty |
| Tradeify | Yes | **Instant funded-account activation is Tradovate-only** — a positive |
| Apex | Yes | **Two penalties, see below** |

**Choosing Tradovate at Apex is doubly expensive.** It costs \$50 per month more than
Rithmic or WealthCharts at every account size, and it is the only Apex platform where the
evaluation drawdown **never stops trailing** — on Rithmic and WealthCharts it stops once
the threshold reaches the profit target. The preferred platform is the worst platform at
that provider.

### 1.3 Accidental news exposure

The session traded is **09:00–11:00 New York**, which contains the 10:00 ET release slot —
ISM, consumer confidence, JOLTS and similar. These are US high-impact events and they fall
inside the trading window, not outside it.

| Rule | Provider | Risk |
|---|---|---|
| News trading unrestricted | Tradeify, Lucid Pro / Flex / Direct, Apex | None |
| **US high-impact news is a hard breach** | **LucidDaily funded accounts** | **Account-ending** |

**LucidDaily carries real accidental-breach risk for this profile.** The requirement is to
be flat from one minute before to one minute after the event. Given the session traded and
a stated preference not to lose an account to an accident, this is a material mark against
LucidDaily despite it being the cheapest and most flexible Lucid product on other measures.

---

## 2. Minimum viable account size

### 2.1 The stop is wide relative to prop drawdowns

One MNQ at a \$200 stop, against each account's typical drawdown:

| Account size | Typical drawdown | One trade as % of drawdown | Consecutive losses to breach |
|---|---|---|---|
| 25K | \$1,000 | **20%** | **5** |
| 50K | \$2,000 | 10% | 10 |
| 100K | \$3,000 | 6.7% | 15 |
| 150K | \$4,500 | 4.4% | 22 |

Halve the percentages and double the streak counts for a 50-point (\$100) stop.

### 2.2 Streak risk at a 50% win rate

An all-or-nothing 1:2R system loses half its trades by assumption. Rough odds of hitting a
given losing run:

| Run length | Probability of that exact run | Likelihood over ~30 trades |
|---|---|---|
| 5 losses | 1 in 32 | **More likely than not** |
| 10 losses | 1 in 1,024 | Unlikely |
| 15 losses | 1 in 32,768 | Remote |

**A 25K account at a \$200 stop will probably be ended by an ordinary losing streak.** Five
consecutive losses is not a tail event at a 50% loss rate — it is something to expect within
a few months of trading.

### 2.3 Workable combinations

| Account | \$100 stop (50 pt) | \$200 stop (100 pt) |
|---|---|---|
| 25K | 1 MNQ — marginal | **Not viable** |
| 50K | 2 MNQ | 1 MNQ |
| 100K | 3 MNQ | 1 MNQ |
| 150K | 4 MNQ | 2 MNQ |

**Conclusion: 50K is the minimum sensible account size**, and only at one contract if the
full 100-point stop is used.

**Contract limits are irrelevant to this profile.** Every product permits 2 to 10 minis
(20 to 100 micros). At one or two MNQ, no published limit and no scaling plan will ever
bind. Scaling plans, usually a significant negative, can be ignored here.

**Full-size NQ is unusable.** One NQ at a 100-point stop risks \$2,000 — the entire
drawdown of a 50K account.

---

## 3. Time to pass, and what it costs

### 3.1 Expectancy

At 50% win rate, one MNQ, \$200 risk and \$400 target:

- Expectancy per trade = 0.5 × \$400 − 0.5 × \$200 = **+\$100**
- At 15 trades per month = **+\$1,500 per month** per contract

### 3.2 Time to reach each profit target

| Target | Account | Trades needed | Months at 15/month | Months at 8/month |
|---|---|---|---|---|
| \$1,250 | 25K Lucid | 13 | 0.9 | 1.6 |
| \$1,500 | 25K Tradeify | 15 | 1.0 | 1.9 |
| \$3,000 | 50K | 30 | **2.0** | 3.8 |
| \$6,000 | 100K | 60 | 4.0 | 7.5 |
| \$9,000 | 150K | 90 | 6.0 | 11.3 |

These assume one contract. Two contracts halve the time but double the risk per trade.

### 3.3 The consequence for pricing models

**Minimum-trading-day rules are irrelevant.** Every product's "pass in 1 day" or "3 days
minimum" requirement is cleared long before the profit target is reached. The binding
constraint is accumulation time, not day count.

**One-time pricing is strongly preferred over monthly subscription.** A 50K evaluation
taking two to four months costs:

| Model | Cost over 3 months |
|---|---|
| One-time purchase | the purchase price, once |
| Monthly subscription | **3× the monthly price**, plus the activation fee |

This weighs against Apex specifically, whose evaluations are monthly subscriptions, and
makes its headline coupon price misleading for a slow profile.

**Reset pricing matters more than usual**, because a blown evaluation discards two to four
months of accumulated progress, not two to four days.

---

## 4. Payout cadence fit

At 1–2 trading days per week, cadences counted in **trading days** stretch badly:

| Requirement | Calendar time for this profile |
|---|---|
| Daily eligibility | **Same week** |
| 3 trading days | 1.5 to 3 weeks |
| 5 qualifying or winning days | **2.5 to 5 weeks** |
| 8 trading days | 4 to 8 weeks |

**Daily-eligible payout products are worth substantially more to this profile than to a
full-time trader**, because the alternative is over a month per cycle.

Consistency rules compound this, since they are satisfied in profitable days rather than
calendar time:

| Consistency rule | Minimum profitable days | Calendar time |
|---|---|---|
| 20% | 5 | 2.5 to 5 weeks |
| 30% | 4 | 2 to 4 weeks |
| 35% | 3 | 1.5 to 3 weeks |
| 40% | 3 | 1.5 to 3 weeks |
| 50% | 2 | 1 to 2 weeks |
| None | — | — |

**Strict consistency rules are expensive in time for this profile.** A 20% rule is roughly
a month of trading before any payout can be requested.

---

## 5. Drawdown enforcement is the decisive mechanic

FVG reversals are entered **against** the prevailing move, so a position routinely sits at
an unrealised loss before resolving. That makes the enforcement basis more important than
the headline drawdown figure.

| Model | Effect on this strategy |
|---|---|
| **Intraday trailing, real-time enforced** | Worst. Both the unrealised excursion *and* unrealised peaks count. |
| **EOD trailing, real-time enforced** | An open position can breach before it resolves, but giving back an unrealised run-up costs nothing. |
| **EOD trailing, EOD-only enforced** | Best. An adverse excursion that recovers before the close is harmless. |
| **Static** | Floor never moves; cushion grows with profit. |

**The practical requirement: the stop must sit inside the drawdown floor with room for
slippage**, because on every real-time-enforced product the account can be ended by an
open trade before the stop is hit. With a \$200 stop that means never operating with less
than roughly \$300 of floor distance.

**Products using an intraday drawdown should be treated as materially worse for this
strategy**, regardless of price, unless the end-of-day variant is bought instead.

---

## 6. Rules that are non-issues for this profile

Worth recording so they do not consume attention in the tradeoff:

| Rule | Why it does not bind |
|---|---|
| **Holding-time / microscalping rules** | Trades are held minutes. The 5-second (Lucid) and 10-second (Tradeify) thresholds are never approached. |
| **Contract limits and scaling plans** | 1–2 MNQ against limits of 20–100 micros. |
| **Daily loss limits** | 1–3 trades at \$200 rarely reaches any published DLL. Paying to remove one buys nothing. |
| **Flat-by deadlines** | Trading ends 17:00 Netherlands time; deadlines are 22:45 or later. |
| **Hedging rules** | No automation, no copy trading, single instrument, no scaling in. Only becomes relevant if parallel accounts are run. |
| **Averaging / DCA rules** | Single entry fill, no scaling in. |
| **Commissions** | \$1.00 to \$1.82 round trip per MNQ, under 1% of a \$200 risk. |
| **ES/MES correlation rules** | Reference only, never traded, so no correlated-product exposure. |

**Paying a premium to disable a daily loss limit is poor value for this profile.** The DLL
is rarely the binding constraint, and at several providers removing it also removes
intraday payout eligibility.

---

## 7. Weighting for the tradeoff

Derived from everything above, in order:

| Rank | Criterion | Why it matters here |
|---|---|---|
| 1 | **Availability to a Netherlands resident** | Binary filter |
| 2 | **Drawdown enforcement basis** | Directly determines survival of an adverse excursion |
| 3 | **Drawdown size at 50K and above** | Sets the losing-streak tolerance |
| 4 | **One-time vs subscription pricing** | A 2–4 month evaluation multiplies subscription cost |
| 5 | **Payout cadence** | 5-day cycles become monthly; daily eligibility is worth a premium |
| 6 | **Consistency requirement** | Counted in profitable days, so strict rules cost weeks |
| 7 | **Reset cost** | A blown evaluation discards months of progress |
| 8 | **Accidental-breach exposure** | News rules, given the 10:00 ET release slot |
| 9 | **Forced move to live** | Deferred to the case document |
| 10 | **Payout caps** | Cannot be weighted until a target income is set |

Items 9 and 10 need the open inputs from `Trading_Style_Info.md` section 9 before they can
be assessed.

---

## 8. Provisional observations

Stated as leads to verify, not conclusions.

- **50K is the floor on account size**, and 100K or 150K buys meaningfully more streak
  tolerance at a cost that is small relative to a multi-month evaluation.
- **An end-of-day enforced drawdown is worth paying for.** On LucidDaily this is an
  explicit paid option; elsewhere it is a property of the product.
- **LucidDaily's news rule conflicts with the session traded**, which offsets its pricing
  and cadence advantages.
- **Apex has two independent problems**: unresolved Netherlands availability, and the fact
  that the preferred platform is its most expensive and most punitive one.
- **Monthly-subscription pricing is a structural disadvantage** at this trading frequency,
  independent of the headline rate.
