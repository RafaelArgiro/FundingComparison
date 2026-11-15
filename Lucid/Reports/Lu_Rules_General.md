# Lucid — General Rules

Rules that apply in **every phase** and to **every account type**.

Phase-specific rules and the per-account-type parameters belong in `Lu_Rules_Evaluation.md`,
`Lu_Rules_Funded.md` and `Lu_Rules_Live.md`, which do not repeat anything covered here.

Consequence codes:
- **KILL** account lost immediately
- **LOCK** trading halted until next session
- **BLOCK** payout blocked or denied
- **STRIP** profits removed
- **BAN** consequences beyond this account

---

## 1. General — applies to every account type

### 1.1 Trading hours

- **All positions must be closed by 4:45 PM EST**, Monday to Friday.
- Any open position is **closed automatically** by Lucid at 4:45 PM EST. **Holding a
  position past this time does not fail the account** — it is explicitly stated not to be
  a breach.
- Trading resumes at **6:00 PM EST**, Sunday through Thursday.
- On market holidays with altered closing times, all positions must be closed before the
  market closes, regardless of the usual 4:45 PM cutoff.
- No swing trading on live accounts. Live hold times differ by broker: 4:45 PM EST on
  Tradovate Live, **4:15 PM EST on Rithmic Live**.

> **Data gap.** The Allowed Trading Times article covers "LucidPro, LucidFlex and
> LucidDirect Accounts" and "LucidLive Accounts" only. **LucidDaily is not mentioned
> anywhere in it.** Whether the 4:45 PM EST flat rule applies to LucidDaily is unconfirmed.

### 1.2 Position limits

- Contract limits are per account size and are identical across LucidPro, LucidFlex,
  LucidDirect and LucidDaily:

| Account size | Max size |
|---|---|
| \$25,000 | 2 mini or 20 micro |
| \$50,000 | 4 mini or 40 micro |
| \$100,000 | 6 mini or 60 micro |
| \$150,000 | 10 mini or 100 micro |

- Whether the full limit is available immediately or has to be earned depends on the
  product and the phase. Only LucidFlex funded accounts carry a scaling plan; LucidPro and
  LucidDirect state "no scaling plan, access to max contract size immediately".
- Minis and micros may be combined within one account, including in opposing directions on
  the same contract — see 1.3.

### 1.3 Prohibited — these end the account or worse

**Hedging.** BAN. All forms are prohibited:

- Across multiple accounts held by the same user
- Between different users' accounts
- **Between different firms or funded platforms**
- Any other form designed to bypass risk management rules

What is and is not allowed:

| Situation | Allowed? |
|---|---|
| Long and short the same contract, same account | **No** |
| Long and short the same contract, separate accounts | **No** |
| Long minis and short micros of the same contract, **same account** | **Yes** |
| Long minis and short micros of the same contract, **separate accounts** | **No** |
| Long and short *different* contracts, same account | **Yes** |
| Long and short correlated contracts, separate accounts (e.g. long ES / short NQ) | **No** |

Correlated groupings run by asset class — equities, metals, energies and so on.

**The first-offence penalty is unusual and worth understanding.** On a flagged hedge you
receive an email notice and the associated accounts are **reset to the prior day's
balance** — but **the drawdown is not reset with it**. You lose the profit while keeping
the reduced drawdown room that profit had bought you, which leaves the account strictly
worse off than before the trading day began. Repeated offences breach all involved
accounts and may trigger a permanent ban.

**Hedging a live account is a permanent ban**, prohibited by both Lucid and the CME.

**Microscalping.** STRIP, then BAN. You are flagged when **more than 50% of your profits
come from trades held 5 seconds or less**. Flagging triggers a manual review; a confirmed
bad-faith finding brings a written warning; continued behaviour forfeits all microscalping
profits and may permanently restrict you from Lucid. Appeals are permitted.

**High-frequency trading.** BAN. Automated detection. First offence is a written warning;
repeated offences remove all HFT profits, close the accounts and permanently restrict you.
Appeals are permitted.

**Exploiting the simulated environment.** BAN under the Trade with Integrity policy:
taking advantage of system errors or update delays, exploiting discrepancies in simulated
prices, or any tactic that does not reflect real-world trading conditions.

### 1.4 Explicitly allowed

- **Scaling into trades and dollar cost averaging.** No limits on entry method.
  Martingaling is strongly discouraged but not prohibited.
- **Genuine scalping**, provided it stays within the microscalping policy above.
- **Automated strategies and trade copiers.** You are fully responsible for software
  errors, malfunctions and unintended outcomes.
- **Flipping** — quick in-and-out trades purely to satisfy minimum trading day
  requirements — is explicitly permitted and not restricted.
- **News trading on LucidPro, LucidFlex and LucidDirect.** Traders may enter or exit around
  scheduled or unscheduled news events without breaching. Slippage and velocity-logic
  triggers are the trader's own risk.

**News trading is a hard breach on LucidDaily funded accounts.** KILL. The restriction
applies only when **both** conditions hold: impact is **High** and currency is **USD**. You
must be flat from **one minute before through one minute after** the event, and may
neither hold nor open positions through that window.

### 1.5 Account lifecycle

- **Inactivity: 30 calendar days.** An account that has not been traded to produce at least
  \$1 of net profit or loss within 30 calendar days is deemed abandoned and **permanently
  deleted**.
- **Breached evaluations remain eligible for a reset** but are **automatically deleted
  after 30 days** if not reset. They can also be removed manually from the dashboard at any
  time before that.
- **Account limits per household or family:**

| | Limit |
|---|---|
| Evaluation accounts | 10 |
| Funded accounts | 5 |
| Combined evaluation + funded | **10 total** |
| LucidLive accounts | 5 |

  The combined cap binds first: holding 5 funded accounts leaves room for only 5
  evaluations. Evaluations held in reserve may still be traded.

> **Data gap.** The Maximum Number of Accounts article names only evaluation accounts,
> funded accounts, LucidDirect, LucidPro and LucidLive. **LucidFlex and LucidDaily are not
> addressed.** Whether they count toward the same caps is unconfirmed.

### 1.6 Instruments and platforms

- **35 approved products** across CME, CBOT, NYMEX and COMEX. No crypto, equities, forex
  spot or options.
- **All listed platforms work with all Lucid account types.**

| Data feed | Platforms |
|---|---|
| CQG | NinjaTrader, Tradovate, TradingView |
| Rithmic | Quantower, Tradesea, MotiveWave, Sierra Chart, Jigsaw, Bookmap, ATAS, R\|Trader Pro, MultiCharts |

- **Commissions are published per side.** Double them for a round-trip comparison:

| Product | Per side | Round trip |
|---|---|---|
| ES, NQ, RTY, YM, NKD | \$1.75 | \$3.50 |
| MES, MNQ, M2K, MYM | \$0.50 | \$1.00 |
| CL, QM, NG | \$2.00 | \$4.00 |
| MCL | \$0.50 | \$1.00 |
| GC, SI, HG, PL | \$2.30 | \$4.60 |
| MGC | \$0.80 | \$1.60 |
| Currencies (6A, 6B, 6C, 6E, 6J, 6S, 6N) | \$2.40 | \$4.80 |
| Grains and livestock (ZS, ZC, ZL, ZM, ZW, HE, LE) | \$2.80 | \$5.60 |

- Lucid is unavailable to citizens or residents of roughly 80 restricted countries. The
  list is residency-based and must be checked by name.

### 1.7 Fees, payments and payouts

- **Every account is a one-time purchase.** No subscription, no monthly rebilling, no
  automatic renewal.
- **No activation fee** to upgrade a passed evaluation to a funded account.
- **Resets are never free or automatic.** Because there is no billing cycle, a failed
  evaluation must be reset by purchase if you want to continue on that account.
- Payment by Visa, Mastercard, American Express, Discover, Diners Club or Maestro.
- **Profit split is 90% to the trader / 10% to Lucid** on every funded product. Accounts
  purchased or reset before **11/28/2025 at 3:00 PM EST** keep 100% of the first \$10,000.
- **Payouts have no fixed window.** Once approved, funds leave the account within minutes
  and are disbursed within 2 business days.

| Method | Availability |
|---|---|
| Plaid | Instant bank transfer, US only |
| WorkMarket by ADP | US and international, bank transfer or PayPal, often next business day |
| Crypto | International only — BTC, ETH, LTC, USDT, USDC |

---

## 2. General risk limits — apply to every account type

### 2.1 Overview

- **The Max Loss Limit is the only thing that fails an account.** KILL. Reaching it is a
  hard breach with no recovery.
- **Every Daily Loss Limit is a soft breach.** LOCK. Hitting one locks you out until the
  next session but does not fail the account, provided the Max Loss Limit has not also
  been reached.
- The Max Loss Limit **rises with the account** up to a fixed point called the Initial
  Trail Balance, then **locks permanently** at starting balance + \$100.
- **Drawdown type varies by product.** Most are end-of-day; LucidDaily funded accounts are
  intraday. See 2.3.
- The DLL does **not** trail upward with the MLL. If the MLL trails above the DLL, the MLL
  becomes the more restrictive of the two and a hard breach can occur before the soft one.

### 2.2 Max Loss Limit and the trail

**The floor.** Every account starts with a Max Loss Limit set a fixed distance below the
starting balance. On a \$50,000 account that distance is \$2,000, putting the floor at
\$48,000.

**What moves it.** At the end of each trading session the system takes the account's
highest closing balance and lifts the floor to stay the same distance below it. The floor
moves up only; a lower closing balance never pulls it back down.

**Where it stops.** The floor stops trailing permanently once the account closes above the
**Initial Trail Balance**, defined as:

```
Initial Trail Balance = starting balance + Max Loss Limit + $100
```

At that point the floor **locks** at:

```
Locked MLL = starting balance + $100
```

and never moves again.

**Worked example, \$50,000 account with a \$2,000 Max Loss Limit:**

| | Balance | Floor |
|---|---|---|
| Start | \$50,000 | \$48,000 |
| Close above \$52,100 (the Initial Trail Balance) | — | **locks at \$50,100** |
| Every session thereafter | any | \$50,100 — fixed forever |

**Before the lock, banked profit costs you cushion.** The floor follows your closing
balance up, so profit you carry into a close converts part of your original room into
profit you must then defend. **After the lock, that stops entirely** — every dollar above
\$50,100 can be lost without failing the account.

**LucidFlex locks the floor on a payout request.** Requesting a payout from a LucidFlex
funded account immediately moves the MLL to the Locked MLL Balance, regardless of whether
the Initial Trail Balance was reached. This makes an early payout a risk-reduction action
as well as a withdrawal.

### 2.3 Drawdown type: end-of-day versus intraday

Two different mechanics are in use, and the difference decides whether unrealised profit
and loss counts.

| Type | The floor follows | Unrealised P&L counts? |
|---|---|---|
| **End-of-day** | Account balance at session close | No — intraday swings do not move the floor |
| **Intraday** | Real-time P&L | Yes — the floor moves with live, unrealised profit |

- **LucidPro, LucidFlex and LucidDirect use end-of-day drawdown** in both phases.
- **LucidDaily funded accounts always use intraday drawdown.** Its evaluation can be bought
  with either type, and the intraday option is the cheaper of the two.
- Under intraday drawdown, a position that runs up and is then given back **permanently
  costs you room**, because the peak was counted as it happened. Under end-of-day
  drawdown the same round trip costs nothing.

### 2.4 Daily Loss Limit

- **All DLLs are soft breaches.** LOCK. You are restricted from placing further trades
  until the next trading session. The account survives as long as the Max Loss Limit has
  not been reached.
- **The DLL is fixed through the session** and does not trail upward with the MLL.
- Whether an account has a DLL at all, and at what amount, depends on the product and in
  several cases on a paid choice made at purchase. See the phase documents.
- **Two DLL mechanics exist:**

**Fixed DLL** — a constant dollar amount that never changes.

**LucidScale DLL** — replaces the fixed DLL on LucidPro and LucidDirect funded accounts
once the balance closes above the Initial Trail Balance:

```
LucidScale DLL = highest end-of-day account profit × 60%
```

It **only ratchets up**. It never decreases, even if the account later draws down. A
\$4,000 highest end-of-day profit sets the DLL at \$2,400 and it stays there until a higher
end-of-day profit is achieved.

> **Documentation conflict.** The LucidPro and LucidDirect funded account tables label this
> column "60% of Peak EOD **Balance**", while the Daily Loss Limit articles give the formula
> as 60% of peak end-of-day **profit**. On a \$50,000 account those differ by roughly
> \$30,000. The formula is the version that makes sense; the column header does not.
