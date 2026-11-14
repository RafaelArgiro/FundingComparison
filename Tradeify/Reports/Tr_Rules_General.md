# Tradeify — General Rules

Rules that apply while trading an evaluation account, before funding.

Consequence codes:
- **KILL** account lost immediately·
- **LOCK** trading halted until next session
- **BLOCK** payout blocked (funded phase only)
- **STRIP** profits removed
- **BAN** consequences beyond this account.

---

## 1. General — applies to every account type

### 1.1 Trading hours

- **All positions must be flat by 4:45 PM ET.** On holiday half-days, 12:59 PM ET.
- Open positions are closed automatically at the deadline. This does **not** fail the
  account, but fills may be unfavourable.
- No overnight, no weekend, no swing trading.
- Session runs 6:00 PM ET to 5:00 PM ET the next day, with a 5:00–6:00 PM ET maintenance
  break. A position may be held across that whole ~23-hour window, but never through the
  break or the weekend.
- A trading day is one trade placed within a session. Trades at 10:00 AM and 7:00 PM on
  the same calendar date count as **two** trading days.

### 1.2 Position limits

- Contract limits are per account size. **10 micros = 1 mini.**
- Minis and micros may be held at the same time, provided the combined position stays
  within the limit at that 10:1 ratio.
- **No scaling plan during the evaluation.** Full contract size is available from the
  first trade on every account type. Scaling applies only once funded.
- Exceeding the limit may result in the day's profit being wiped if done deliberately.

### 1.3 Prohibited — these end the account or worse

- **Hedging.** BAN. No opposing positions on the same instrument or on two products from
  the same Product Group, whether in one account or spread across several of your
  accounts. Consequences: disqualification of the evaluation, violation status on every
  account involved, forfeiture of profits from the violating period, possible permanent
  ban.
- Automated hedging detection breaches only when all three are true: opposing positions,
  held longer than 10 seconds, and more than \$150 of profit generated from the hedge.
  Cross-account and correlated-product hedging is reviewed manually with no published
  threshold.
- **High-frequency trading bots.** BAN.
- **Exploiting platform errors** — price display errors, update delays, or any strategy
  designed to create them. BAN under the Good Faith policy.
- **Account sharing**, and paying with a card not in your own name.
- Logging in via VPN or VPS. A VPS may be used for trading after a normal login.

### 1.4 Explicitly allowed

- **News trading, with no restrictions at all.** Slippage is your own risk.
- **Dollar cost averaging and scaling into trades.**
- **Martingale**, provided it does not become hedging.
- **Genuine scalping.** The 10-second microscalping rule is a payout gate and **does not
  apply during an evaluation**.
- **Automated and algorithmic trading**, provided you solely own the strategy, can prove
  it on request, do not share it across firms, and it is not HFT.
- **Trade copying in the same direction** across your own accounts.

### 1.5 Account lifecycle

- **No time limit** to complete an evaluation.
- **At least one trade per week** (Monday–Friday) per account, or the account is closed
  for inactivity after an email warning.
- **Profit earned during the evaluation does not carry over.** The funded account starts
  at the base account size regardless of where the evaluation ended.
- Activation after passing is instant from the dashboard with no activation fee — but
  instant activation is documented as **Tradovate only**.
- A passed evaluation can be banked and activated later when a funded slot is free.
- Maximum 5 funded accounts per user and per household, so passing more than 5 evaluations
  does not give more funded accounts.

### 1.6 Instruments and platforms

- 48 supported root symbols across CME, CBOT, COMEX, NYMEX, and EUREX on Tradovate only.
- No crypto, stocks, forex, options or single stock futures.
- Broker is chosen at checkout — Tradovate, Rithmic/Tradesea or WealthCharts — and
  **cannot be switched** without buying a new account. All are the same price.
- Level 1 CME data is free; the Non-Professional Agreement must be signed or a \$300/month
  professional fee may apply.
- CME exchange halts are not compensated.

---

## 2. General risk limits — apply to every account type

### 2.1 Overview

- **Trailing Max Drawdown is the only thing that fails an evaluation.** KILL.
- The drawdown limit **updates only at the end of each day**, trailing the highest-ever
  end-of-day balance. It moves up, never down.
- The limit is **enforced in real time against net liquidation value**, which includes
  unrealised P&L on open positions. Touching it at any moment during the session fails the
  account immediately, even if the day closes green.
- **The drawdown does not lock during an evaluation.** Locking at starting balance + \$100
  applies to funded accounts only.
- **Daily Loss Limit is a soft breach.** LOCK. Trading pauses until the next session opens
  at 6:00 PM ET. The account survives.
- Never use the DLL as a stop loss. It is not a hard stop, and slippage past it can breach
  the drawdown, which does fail the account.
- If the drawdown floor is closer than the DLL, the drawdown is hit first and the account
  fails before the DLL ever triggers.

### 2.2 Trailing max drawdown

**The floor.** Every account starts with a loss floor set at `starting balance − drawdown
amount`. On a 50K Growth that is \$50,000 − \$2,000 = **\$48,000**. Your balance may never
touch or go below it.

**What moves the floor.** The floor trails the **highest end-of-day balance the account
has ever reached** — the high water mark — and always sits exactly the drawdown distance
below it. At each session close:

- If the closing balance is a new all-time high, the floor moves up by the same amount.
- If the closing balance is lower than a previous high, **the floor does not move.** It
  never recalculates downward and never falls.

**Intraday highs do not count.** Only closing balances move the floor. Running +\$3,000
intraday and closing flat leaves the floor exactly where it was. Only the balance you
actually carry into the close costs you room.

**Worked example** (100K Growth, \$3,500 drawdown):

| | Balance | Floor |
|---|---|---|
| Start | \$100,000 | \$96,500 |
| Day 1 close | \$103,000 (new high) | \$99,500 |
| Day 2 close | \$101,000 | \$99,500 — unchanged |
| Day 3 intraday peak \$104,500, closes \$102,000 | \$102,000 | \$99,500 — the intraday peak is ignored |

**The consequence most people miss.** The room between your balance and the floor is
always the drawdown amount, and never changes. What does change is how much of your
**original starting balance** you are still allowed to lose. On a 50K Growth:

| | Balance | Floor | Room below balance | Floor vs. \$50,000 start |
|---|---|---|---|---|
| Start | \$50,000 | \$48,000 | \$2,000 | \$2,000 below |
| Close day 1 at +\$1,500 | \$51,500 | \$49,500 | \$2,000 | **\$500 below** |

At the start you could lose \$2,000 of your deposit before failing. After closing one day
\$1,500 up, you can lose only \$500 of it. A \$2,000 loss from \$51,500 takes you to
\$49,500 and fails the account, at which point you are down just \$500 against your
starting balance.

Every dollar of profit you carry into a close converts a dollar of your original cushion
into profit you must then defend. The drawdown is a *distance from your peak*, not a
*loss from your deposit*, and cumulative give-back from the high water mark is capped at
the drawdown amount, forever.

**No locking during an evaluation.** On funded accounts the floor stops trailing once it
reaches starting balance + \$100. **Evaluation accounts never lock** — the floor keeps
trailing right up to the moment you pass.

**Starting floors and the floor at the profit target:**

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

Inter Miami is the exception: a **static** floor that never trails at all. It gives a
larger and growing cushion as the account becomes profitable, which is the opposite
behaviour to every other Tradeify product.

### 2.3 Real time enforcement

**The floor updates end-of-day but is checked continuously.** These are two separate
things, and conflating them is the most expensive mistake available on this platform.

**What is checked:** your **net liquidation value** — cash balance plus unrealised profit
and loss on any open position. Not your closed balance.

**When it is checked:** continuously, throughout the session.

**What happens:** the instant net liquidation value touches or crosses the floor, the
account fails. This is a hard breach. There is no recovery, no reset of the breach, and
closing the day green changes nothing.

**Worked example** (25K, \$1,000 drawdown, floor \$24,000):

- 10:15 AM — an open position pushes net liquidation value down to \$22,000.
- The account failed the moment it touched \$24,000 on the way down.
- Closing the session at \$25,500 is irrelevant. The account was already gone.

**What follows from this:**

- **An open losing position can kill the account before you close it.** You do not get to
  decide when the loss is realised.
- **Your stop must sit inside the floor, not at it.** Slippage past your stop breaches it.
  This is why the documentation repeatedly warns never to use the Daily Loss Limit as a
  stop loss — in fast markets the DLL may not trigger before the floor is hit.
- **Your usable drawdown is less than the stated amount.** You must reserve room for
  adverse excursion on open trades and for slippage, neither of which the headline figure
  accounts for.
- **The dashboard cannot help you intraday.** Every dashboard metric updates in real time
  *except* the Trailing Max Drawdown figure, which refreshes once per day at the session
  close. The number you need most is the one number that is stale while you trade.

**To see the live distance you must use the platform, not the dashboard:**

| Platform | Where |
|---|---|
| Tradovate | Accounts widget → add the "Dis Drawdown Net Liq" column |
| NinjaTrader | Control Center → Accounts → add the "Trailing Max Drawdown" column |

**The label is misleading.** "End-of-day trailing drawdown" describes only how the floor
moves. Enforcement is continuous and counts unrealised losses, so an open trade that never
gets closed at a loss can still end the account.
