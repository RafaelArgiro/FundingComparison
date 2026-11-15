# Lucid — Evaluation Phase

Rules that apply while trading an evaluation account, before funding.

> **Read `Lu_Rules_General.md` first.** Trading hours, position limits, prohibited and
> permitted conduct, instruments, platforms, inactivity, fees and the general Max Loss
> Limit mechanic apply here and are not repeated. This document covers only what is
> specific to the evaluation phase, plus the parameters of each account type.

Consequence codes:
- **KILL** account lost immediately
- **LOCK** trading halted until next session
- **BLOCK** payout blocked (funded phase only)
- **STRIP** profits removed
- **BAN** consequences beyond this account

---

## 1. What is specific to the evaluation phase

- **No time limit.** Take as long as you need to reach the profit target. The 30-day
  inactivity rule still applies.
- **No scaling plan.** Full contract size is available from the first trade on every
  product. Scaling exists only on LucidFlex funded accounts.
- **No consistency rule on LucidPro.** It applies to LucidFlex and LucidDaily evaluations,
  and to LucidPro only once funded.
- **Real-time activation.** The funded account is created **within 5 to 30 minutes** of
  hitting the profit target, with **no activation fee**.
- **The configuration you buy is permanent.** Daily Loss Limit, consistency percentage and
  drawdown type are chosen at checkout, apply to **both** the evaluation and the funded
  account, and cannot be changed afterwards. A different configuration requires buying a
  new account.
- **Resets must be purchased.** There is no billing cycle, so nothing resets automatically.
  A reset returns the account to its original balance and risk parameters.
- **A breached evaluation stays resettable for 30 days**, then is deleted automatically.

**Shared evaluation parameters.** These are identical across LucidPro, LucidFlex and
LucidDaily at every size:

| Size | Profit target | Max Loss Limit | Max size |
|---|---|---|---|
| \$25,000 | \$1,250 | \$1,000 | 2 mini or 20 micro |
| \$50,000 | \$3,000 | \$2,000 | 4 mini or 40 micro |
| \$100,000 | \$6,000 | \$3,000 | 6 mini or 60 micro |
| \$150,000 | \$9,000 | \$4,500 | 10 mini or 100 micro |

LucidDirect has no evaluation — see section 7.

---

## 2. The floor locks before you pass

The Max Loss Limit lock described in `Lu_Rules_General.md` applies **during the
evaluation**, not only once funded. This matters more than it first appears.

The Initial Trail Balance sits **below** the balance you need to pass, at every size:

| Size | Initial Trail Balance | Balance at profit target | Margin |
|---|---|---|---|
| \$25,000 | \$26,100 | \$26,250 | \$150 |
| \$50,000 | \$52,100 | \$53,000 | \$900 |
| \$100,000 | \$103,100 | \$106,000 | \$2,900 |
| \$150,000 | \$154,600 | \$159,000 | \$4,400 |

**So on any route to passing, the floor locks at or before the moment you pass.** Once the
account closes above the Initial Trail Balance the floor fixes permanently at starting
balance + \$100 — \$25,100 / \$50,100 / \$100,100 / \$150,100 — and the trailing give-back
mechanic stops applying for the rest of the evaluation.

**The practical effect:** the dangerous part of a Lucid evaluation is the stretch from the
starting balance up to the Initial Trail Balance. After that the risk is static and the
remaining distance to the target can be traded against a fixed floor. On a \$50,000
account that dangerous stretch is the first \$2,100 of profit.

**The lock does not transfer.** It belongs to the evaluation account only. The funded
account is a new account at its base size, with its own floor trailing again from the
start — see `Lu_Rules_Funded.md`. Neither the balance nor the locked floor carries over.

---

## 3. Choosing your configuration at purchase

Four settings are sold, and which are available depends on the product. All are permanent
and all are priced.

| Setting | LucidPro | LucidFlex | LucidDaily | LucidDirect |
|---|---|---|---|---|
| Daily Loss Limit On / Off | Yes | Yes | Yes | No — fixed by size |
| Consistency | No — fixed | 40% / 50% | 40% / 50%, or 30% / 40% under funded EOD | No — fixed at 20% |
| Evaluation drawdown EOD / Intraday | No — EOD | No — EOD | Yes | No — EOD |
| **Funded drawdown Intraday / EOD** | No — EOD | No — EOD | **Yes, if eval is EOD** | No — EOD |
| Number of configurations | 2 | 4 | **12** | 1 |

**Turning the Daily Loss Limit off forces On Demand Payouts off.** This is the single most
consequential choice, because it is not really a risk setting — it is a payout setting:

- **DLL On** → a daily loss cap applies in both phases, **and** the funded account can
  request payouts intraday, from profit made that session (6:00 PM to 3:45 PM ET).
- **DLL Off** → no daily loss cap in either phase, **and** payouts follow the regular
  end-of-day schedule only.

You cannot have both no daily cap and intraday payouts.

**The 50% consistency option** raises the limit on your largest single day from 40% to 50%
of total profit, which lowers the number of days needed to pass. A cushion is built in so
that a two-day pass is achievable.

**LucidDaily sells two separate drawdown choices.** The **evaluation** drawdown may be
end-of-day or intraday, and the **funded** drawdown may be intraday or end-of-day. The
funded choice only appears if the evaluation is set to end-of-day; choosing intraday for
the evaluation forces an intraday funded account. Intraday is the cheaper option in both
cases, and an end-of-day funded drawdown is the single most expensive option Lucid sells.

**Choosing an end-of-day funded drawdown changes the consistency tiers** from 40% / 50% to
**30% / 40%**. The 50% option is not selectable alongside it.

---

## 4. Account type: LucidPro

**1 day pass · 3 days to payout · Customizable**

The fastest evaluation. No consistency requirement, so the whole profit target may be
earned in a single session.

- **Profit target can be met in one day.** No minimum number of trading days.
- **No consistency rule during the evaluation.** The 40% rule appears only once funded.
- **End-of-day drawdown**, not selectable.
- **Daily Loss Limit**: \$600 / \$1,200 / \$1,800 / \$2,700, or off.
- Full contract size from the first trade.

**Pricing** (coupon price with code `VAULT`, a flat 30% off):

| Size | DLL On | DLL Off | Reset, DLL On | Reset, DLL Off |
|---|---|---|---|---|
| 25K | \$75.60 | \$90.30 | \$75 | \$90 |
| 50K | \$120.40 | \$150.50 | \$120 | \$150 |
| 100K | \$190.40 | \$225.40 | \$190 | \$225 |
| 150K | \$255.50 | \$300.30 | \$255 | \$300 |

Turning the DLL off costs +\$14.70 / +\$30.10 / +\$35.00 / +\$44.80.

> **Documentation conflict.** The plan cards show a \$600 Daily Loss Limit on the 25K Pro
> in both phases. The help-centre DLL tables list the 25K as "None". The cards are the
> more recent source and also price the option to remove it, which implies it exists.

---

## 5. Account type: LucidFlex

**2/3 day pass · 5 days to payout · Customizable**

The cheapest route to funding, at the cost of a consistency requirement during the
evaluation and a scaling plan once funded.

- **Minimum 3 trading days** at 40% consistency, or **2 days** with the 50% option.
- **Consistency applies during the evaluation only.** The funded account has none.
- **End-of-day drawdown**, not selectable.
- **Daily Loss Limit**: \$600 / \$1,200 / \$1,800 / \$2,700, or off.
- Full contract size from the first trade — the scaling plan starts only when funded.

**Pricing**, all four configurations:

| Size | DLL On / 40% | DLL On / 50% | DLL Off / 40% | DLL Off / 50% |
|---|---|---|---|---|
| 25K | \$45.50 | \$50.40 | \$60.20 | \$70.00 |
| 50K | \$80.50 | \$90.30 | \$115.50 | \$130.20 |
| 100K | \$150.50 | \$170.10 | \$195.30 | \$215.60 |
| 150K | \$226.10 | \$250.60 | \$265.30 | \$295.40 |

**The surcharges are not independent.** The price of each toggle depends on where the
other is set, so no configuration can be worked out by addition:

| Size | 50% consistency, DLL on | 50% consistency, DLL off | DLL off, at 40% | DLL off, at 50% |
|---|---|---|---|---|
| 25K | +\$4.90 | +\$9.80 | +\$14.70 | +\$19.60 |
| 50K | +\$9.80 | +\$14.70 | +\$35.00 | +\$39.90 |
| 100K | +\$19.60 | +\$20.30 | +\$44.80 | +\$45.50 |
| 150K | +\$24.50 | +\$30.10 | +\$39.20 | +\$44.80 |

Reset fees track the configured price, rounded down:

| Size | DLL On / 40% | DLL On / 50% | DLL Off / 40% | DLL Off / 50% |
|---|---|---|---|---|
| 25K | \$45 | \$50 | \$60 | \$70 |
| 50K | \$80 | \$90 | \$115 | \$130 |
| 100K | \$150 | \$170 | \$195 | \$215 |
| 150K | \$225 | \$250 | \$265 | \$295 |

**The 50% consistency option is cheap on this product.** At DLL on it costs between
\$4.90 and \$24.50 to cut a trading day off the minimum and remove the risk that one good
day forces you to keep trading past the profit target.

**The DLL-off surcharge at 40% consistency is not monotonic**: +\$14.70, +\$35.00,
+\$44.80, then *falling* to +\$39.20 at 150K. At 50% consistency it rises cleanly, so the
anomaly is confined to that one row.

---

## 6. Account type: LucidDaily

**2-4 days to pass · Daily payouts · Customizable**

The most configurable product, and the only one where the drawdown type is a purchase
choice in either phase.

- **2 to 4 trading days to pass**, depending on the consistency setting.
- **Consistency applies during the evaluation only.** The funded account has none.
- **Evaluation drawdown is selectable**: end-of-day or intraday.
- **Funded drawdown is also selectable**: intraday or end-of-day — but only if the
  evaluation is set to end-of-day.
- **Consistency tiers depend on the funded drawdown**: 40% / 50% under intraday,
  **30% / 40%** under end-of-day.
- **Daily Loss Limit**: \$600 / \$1,200 / \$1,800 / \$2,700, or off.

**Pricing**, all nine captured configurations:

| Eval DD | Funded DD | DLL | Cons. | 25K | 50K | 100K | 150K |
|---|---|---|---|---|---|---|---|
| Intraday | Intraday | On | 40% | \$50.40 | \$65.80 | \$110.60 | \$160.30 |
| Intraday | Intraday | On | 50% | \$55.30 | \$75.60 | \$125.30 | \$180.60 |
| Intraday | Intraday | Off | 40% | \$65.10 | \$90.30 | \$150.50 | \$210.00 |
| Intraday | Intraday | Off | 50% | \$75.60 | \$100.10 | \$170.10 | \$235.20 |
| EOD | Intraday | On | 40% | \$60.20 | \$85.40 | \$140.00 | \$200.20 |
| EOD | Intraday | On | 50% | \$65.10 | \$95.20 | \$155.40 | \$220.50 |
| EOD | Intraday | Off | 40% | \$80.50 | \$115.50 | \$180.60 | \$250.60 |
| EOD | Intraday | Off | 50% | \$90.30 | \$130.20 | \$200.20 | \$280.00 |
| **EOD** | **EOD** | **Off** | **40%** | **\$160.30** | **\$235.20** | **\$350.00** | **\$490.00** |

Reset fees track the price, rounded down. Three configurations remain uncaptured, all in
the funded-EOD branch: DLL on at 30% and 40%, and DLL off at 30%.

**The surcharges are not independent.** Each toggle's price depends on where the others
are set, so no configuration can be worked out by addition. The headline surcharges:

| Choice | 25K | 50K | 100K | 150K |
|---|---|---|---|---|
| EOD evaluation drawdown | +\$9.80 | +\$19.60 | +\$29.40 | +\$39.90 |
| **EOD funded drawdown** | **+\$55.30** | **+\$79.80** | **+\$130.20** | **+\$184.80** |
| DLL off, funded intraday | +\$20.30 | +\$30.10 | +\$40.60 | +\$50.40 |
| DLL off, funded EOD | +\$44.80 | +\$70.00 | +\$79.80 | +\$105.00 |

**The end-of-day funded drawdown is the most valuable option Lucid sells and the most
expensive.** It removes the intraday drawdown that otherwise defines a funded LucidDaily
account, meaning an unrealised run-up that is given back no longer costs you room. At 50K
it takes the account from \$65.80 to \$235.20 — **3.6 times the cheapest build**.

> **Documentation conflict.** The plan cards show consistency tiers of 40% / 50%, or
> 30% / 40% under a funded EOD drawdown. The help-centre LucidDaily articles state a flat
> 50% requirement and mention no other option.

> **Documentation conflict.** A funded rules card bought with the funded drawdown set to
> EOD reads "Drawdown Type: EOD". The help centre states twice that funded LucidDaily
> accounts always use intraday drawdown. The help centre is wrong.

---

## 7. Account type: LucidDirect

**LucidDirect has no evaluation phase.** It is straight-to-funded — the funded rules apply
from the first trade.

Consequences for this document:

- None of the evaluation-specific rules above apply.
- **There is no configuration choice.** The Daily Loss Limit is fixed by account size and
  the consistency rule is fixed at 20%.
- The funded-phase rules apply immediately, including the **20% consistency requirement**
  and the payout profit goals, neither of which a Pro, Flex or Daily trader meets until
  after passing.
- Max Loss Limits at 100K and 150K are larger than on the evaluation products:
  \$3,500 and \$5,000 against \$3,000 and \$4,500.
- Price: \$230.30 / \$360.50 / \$490.00 / \$585.20 at coupon, which is three to five times
  the cost of any evaluation route.

> **Open question.** The fees article states that LucidDirect accounts "need a purchased
> reset to restart your evaluation account", but LucidDirect has no evaluation and the
> plan cards show no reset row at all. Whether a LucidDirect reset exists is unresolved.

---

## 8. Side-by-side

| | LucidPro | LucidFlex | LucidDaily | LucidDirect |
|---|---|---|---|---|
| Evaluation exists | Yes | Yes | Yes | **No** |
| Minimum trading days | 1 | 3 (2 at 50%) | 2–4 | — |
| Consistency in evaluation | **None** | 40% or 50% | 40% / 50%, or 30% / 40% | — |
| Daily loss limit | Optional | Optional | Optional | — |
| Evaluation drawdown | EOD | EOD | **EOD or intraday** | — |
| Funded drawdown | EOD | EOD | **Intraday or EOD** | EOD |
| Configurations | 2 | 4 | **12** | 1 |
| Contracts in evaluation | Full size | Full size | Full size | — |
| Cheapest 50K | \$120.40 | \$80.50 | **\$65.80** | \$360.50 |
| Dearest 50K | \$150.50 | \$130.20 | **\$235.20** | \$360.50 |
| Reset available | Yes | Yes | Yes | Not published |

Cheapest route to a funded account at each size: LucidFlex at 25K (\$45.50), LucidDaily at
50K (\$65.80), 100K (\$110.60) and 150K (\$160.30).

**LucidDaily has by far the widest price range**, because its configuration choices carry
the largest surcharges. At 50K it spans \$65.80 to \$235.20 for the same account size.

---

## 9. What actually fails an evaluation

In order of how likely it is to catch a normal daytrader:

1. **Reaching the Max Loss Limit before the floor locks.** The stretch from the starting
   balance to the Initial Trail Balance is where the floor is still trailing and profit
   you bank reduces your cushion. On a \$50,000 account that is the first \$2,100 of
   profit, and it is the only genuinely dangerous part of the evaluation.
2. **Choosing intraday drawdown on LucidDaily and then giving back an unrealised run-up.**
   Under intraday drawdown the floor rises with live P&L, so a position that goes +\$1,500
   and comes back to flat has permanently cost \$1,500 of room. Under end-of-day drawdown
   the same round trip costs nothing. The intraday option is the cheaper one at checkout,
   in both the evaluation and the funded phase.
3. **Turning the Daily Loss Limit off.** It is sold as flexibility, but it removes the only
   soft brake on a deteriorating session. With it off, the Max Loss Limit is the sole risk
   control and reaching it is terminal.
4. **Hedging across your own accounts**, including accidentally, when running more than one
   account at a time. The first-offence penalty resets the balance but not the drawdown,
   leaving the account worse off than before the day started.
5. **Inactivity**, if an account is left untraded for 30 calendar days while you
   concentrate on another. Deletion is permanent.

Note that **the profit target itself is never the binding constraint** — there is no time
limit, so a surviving account can always keep trying. Everything that ends an evaluation is
a risk-limit or conduct failure.
