# Case 2: Grow One Account and Withdraw Profits

## 1. Goal

Use **one account** to learn and build trading profits, withdraw **\$5,000 to \$10,000 in hand**, then stop and transition to trading own capital. Reaching \$5,000 would be a good outcome; \$10,000 is preferred if attainable.

The money is not needed for living expenses. Losing the account without reaching the target is an acceptable possible outcome, although the purchase cost and any unwithdrawn profit would be lost.

Both routes are in scope:

- **Evaluation:** pass one evaluation, then trade its funded account.
- **Straight to funded:** purchase a funded account without an evaluation.

The funded account is simulated unless the provider moves it to live. A move to live is acceptable but not preferred, particularly if it requires rebuilding a trading cushion. The handling of remaining simulated profits and live-account starting capital must be checked for each product.

---

## 2. Trading approach

The underlying trading style is described in `Trading_Style_Info.md`: NQ and MNQ, a 50–100 point stop, a 1:2 reward-to-risk target, and 1–3 trades per session. The initial frequency is 1–2 sessions per week, with more sessions possible later if the funded account is going well. The 50% win rate is an **assumption**, not a measured result.

### 2.1 Increase size as the cushion grows

Position size can increase as the distance between the account balance and the applicable drawdown floor grows. Size also depends on the stop distance of the individual trade: a wider stop risks more per contract and can require fewer contracts.

For MNQ, the planned loss before costs and slippage is:

**Number of MNQ contracts × stop distance in points × \$2 per point.**

For example, one MNQ risks \$100 with a 50-point stop or \$200 with a 100-point stop. Two MNQ risk \$200 and \$400 respectively. Actual loss can be greater because of commissions, fees, slippage or gaps.

Sizing must consider the **current** cushion, the daily loss limit, any permitted contract limit and the risk already taken that session. A daily loss limit is not necessarily a guarantee that the account survives: the drawdown floor may be closer, and execution can overshoot a limit.

The exact fraction of the cushion to risk per trade and how quickly to scale down after losses remain open. Increasing contract size raises expected dollar profit under the assumed edge, but also raises dollar losses and the amount that can be lost in one session.

### 2.2 Drawdown behaviour controls when room grows

**Trading cushion** means the distance from the current balance to the account's drawdown floor. It is not necessarily the same as a provider's **payout buffer**, which is a balance threshold for withdrawals.

On an end-of-day trailing account, new closing highs move the floor upward until it locks. Before the lock, gains to a new closing high generally move both balance and floor up, so the available cushion does not grow simply because profit grows. After the floor locks, additional retained profit increases the distance to the floor. A static floor allows cushion to grow with profit from the start.

Intraday-trailing accounts can also move the floor on unrealised gains. The floor can then remain higher even if those gains are given back. Enforcement may apply to open-position losses regardless of whether the floor updates intraday or at the end of day. Exact rules, lock levels and the effect of a payout request vary by product.

---

## 3. Growth and withdrawal strategy

Payouts do not have to be requested as soon as they become available. One possible approach is to retain profits, increase size as the cushion permits, and begin withdrawing once the account has enough profit for the target and the applicable payout rules.

| Retain profits longer | Request payouts earlier |
|---|---|
| More cushion can support a larger position after the floor locks | Cash received is no longer exposed to an account breach |
| Fewer withdrawals while building the account | Withdrawals reduce the balance and may require smaller positions |
| More profit remains exposed to losses, rule breaches or a forced move | Some products lock the floor on a payout request; the exact effect must be checked |

Neither approach guarantees a better outcome. The preferred balance depends on the account's floor, withdrawal rules, contract limits and the amount at risk. Retaining profit does not make it withdrawable: payout eligibility still has to be satisfied.

When extraction begins, trading smaller positions may help control risk while meeting trading-day requirements. **A day is not automatically a qualifying day:** some products require a minimum net profit, and a small trade may not meet that threshold. Losses, consistency rules, minimum withdrawals and the timing of payout-cycle resets also matter.

### 3.1 The arithmetic of extraction

Money received differs from simulated profit earned for three reasons:

1. **Evaluation profit:** on products where the funded account starts fresh, the profit needed to pass does not carry over. A straight-to-funded account has no evaluation target.
2. **Profit left in the funded account:** payout buffers, percentage limits, payout caps or a voluntarily retained cushion can leave profit behind. How much remains depends on the withdrawal sequence and product rules.
3. **Profit split:** at a 90% trader share, receiving \$5,000 requires at least \$5,555.56 gross, and receiving \$10,000 requires at least \$11,111.12 gross, assuming cent rounding.

For an evaluation followed by a fresh funded account, a useful accounting identity is:

**Evaluation profit + funded trading profit = evaluation profit + gross withdrawals + funded profit remaining.**

This assumes no other balance adjustments. It is not a formula for the minimum achievable profit: the profit remaining is determined by the actual payout rules, trading outcomes and chosen cushion. Trading fees, payout fees and taxes need separate treatment.

### 3.2 Worked extraction requirements on a 50K account

The following are **derived illustrations**, not provider quotes or complete payout plans. Assume a \$3,000 evaluation target, a fresh funded account, a 90% trader share, no fees or additional trading after the funded profit is built, and a locked drawdown floor at \$50,100.

| Illustrative payout structure | Funded profit left after withdrawals | Total simulated profit for \$5,000 in hand | Total simulated profit for \$10,000 in hand |
|---|---|---|---|
| Withdraw down to a \$52,100 payout buffer | \$2,100 | approximately \$10,655.56 | approximately \$16,211.12 |
| No payout buffer; voluntarily leave balance at \$51,100 | \$1,100, including \$1,000 above the floor | approximately \$9,655.56 | approximately \$15,211.12 |
| One request limited to 50% of current profit | At least as much profit as the gross request | approximately \$14,111.12 | approximately \$25,222.24 |

The last row assumes a single request can be made without a cap. It does **not** mean half of all lifetime profit must remain: multiple requests may be possible, subject to the actual rules. Section 4.2 shows how repeated 50% requests work under a simplified current-profit formula.

The buffer row assumes withdrawals can reach the buffer and that all other eligibility requirements are satisfied. In practice, per-request caps, qualifying days, consistency, minimum payouts and additional trading can change the total and the amount left behind. A straight-to-funded route removes the assumed \$3,000 evaluation component, but not necessarily the other requirements.

### 3.3 What remains outside the payout

In the buffered illustration, receiving \$5,000 requires approximately \$10,655.56 in combined simulated profit: \$3,000 in the evaluation, \$2,100 left in the funded account, and approximately \$555.56 retained by the provider through the split. At the \$10,000 target, the same components total approximately \$6,211.12.

The funded profit left behind is not necessarily lost while the account remains open: it can provide a cushion and support position sizing. Its eventual treatment on a live transition or closure depends on the product. Evaluation profit is not a cash expense, but reaching the target takes trading time and exposes the account to failure.

---

## 4. Payout rules that determine the exit

### 4.1 Net target and profit split

The target is cash **received after the provider's profit split**, before any taxes or payment-processing fees. At a 90% trader share, the minimum gross withdrawals needed are:

| Cash received | Gross withdrawals at 90% |
|---|---|
| \$5,000 | approximately \$5,555.56 |
| \$10,000 | approximately \$11,111.12, rounded up to cents |

Other splits change these amounts. Fees, taxes, minimum request sizes, payout caps, and provider rounding can increase the gross amount required. Evaluation profit generally does not become funded-account profit; verify the transition for each product.

### 4.2 Percentage-based withdrawals

A limit of **50% of profit per request** can substantially constrain extraction even when the account has accumulated enough profit. Whether profit means current account profit or profit since the previous payout matters, as do payout caps and cycle requirements.

Illustration only: suppose a product allows 50% of the **current profit above starting balance**, with no cap, and no further trading profit or losses. Starting with \$10,000 of profit:

| Request | Gross withdrawal | Profit left in account |
|---|---|---|
| 1 | \$5,000 | \$5,000 |
| 2 | \$2,500 | \$2,500 |
| 3 | \$1,250 | \$1,250 |
| 4 | \$625 | \$625 |
| 5 | \$312.50 | \$312.50 |

These are mathematical limits, not a feasible payout schedule: actual products can require new qualifying days or positive cycle profit, impose minimum requests and caps, or end the account after a set number of payouts. Any additional trading changes the balances shown. At a 90% split the five illustrative withdrawals total \$9,687.50 gross, or \$8,718.75 before fees and tax.

**The 50% limit applies to each request, not necessarily to total lifetime withdrawals.** Nevertheless, a finite payout count or minimum payout can leave substantial profit in the account. The definition of profit is unresolved in the LucidFlex documentation, so both interpretations need checking before relying on an extraction plan.

### 4.3 Caps, qualifying days and consistency

- **Per-request caps** can require multiple payouts even with a large balance. Check whether caps change with payout number or product configuration.
- **Qualifying days** may require a minimum net profit per day, not merely a trade. Check whether the requirements restart after each payout and whether additional cycle profit is required.
- **Consistency rules** can limit the largest profitable day as a share of the relevant profit calculation. Larger positions can create larger days, potentially delaying eligibility. Trading small afterwards may help dilute the largest day, but it takes additional net profit and losses can delay it further.
- **Buffers and floors** can restrict the balance after withdrawal. The remaining cushion must also be sufficient for the smaller positions used during extraction.
- **Payout count limits and forced live transitions** can end the simulated account before the target is extracted. Provider discretion and the treatment of remaining profit must be checked separately.

As an example of a hard ceiling, five requests capped at \$2,000 each produce at most \$10,000 gross, or \$9,000 at a 90% split before fees and tax. That can satisfy the \$5,000 goal but not \$10,000 in hand from those five requests alone. A live transition could have separate terms; it should not be assumed to provide the difference.

---

## 5. Time and cost

At the illustrative fixed size of one MNQ, a 100-point stop, 1:2 reward-to-risk and an assumed 50% win rate give **\$100 expected gross profit per trade**, before trading costs. At 15 trades per month that is **\$1,500 expected gross profit per month**. This is a fixed-size reference, not a forecast or a guarantee of reaching a target.

### 5.1 Fixed-size reference

Using the buffered examples in section 3.2 and dividing their total simulated profit by the assumed \$100 per trade gives a simple reference:

| Cash target | Combined simulated profit | Trades at \$100 average | Months at 15 trades per month |
|---|---|---|---|
| \$5,000 | approximately \$10,656 | approximately 107 | approximately 7.1 |
| \$10,000 | approximately \$16,211 | approximately 162 | approximately 10.8 |

At eight trades per month, the same arithmetic gives approximately 13.3 and 20.3 months respectively. These are **profit divided by average expectancy**, not estimated times to first reach the target: actual paths vary, the account can fail, and costs and payout eligibility can increase the time. The evaluation and funded phases each have their own drawdown risk.

Scaling can change the timeline, but a credible estimate needs an explicit sizing rule, trade-by-trade outcomes, the drawdown mechanics and payout rules. Returns are path-dependent: early losses can prevent scaling or end the account; profits can support larger positions once the cushion grows; withdrawals reduce the balance. Payout requirements may continue to take time after the desired account balance has been reached.

### 5.2 Payout cadence and qualifying days

At 1–2 sessions per week, a requirement of three trading days takes at least roughly 1.5–3 weeks, five days 2.5–5 weeks, and eight days 4–8 weeks. These are calendar conversions, not estimates of eligibility: some products require profitable days or a minimum profit on each day.

For illustration, assume independent trades with a 50% win rate, one MNQ, a \$200 stop and \$400 target, no costs, and one, two or three trades per session with equal frequency. The probabilities of a session ending at least \$150 profitable are 50%, 75% and 50%, respectively. Their average is approximately **58%**. Under these assumptions, collecting five such qualifying days takes about **8.6 sessions on average**, or roughly 4–9 weeks at 1–2 sessions per week.

This is not a measured qualifying rate. Different stop sizes, contract sizes, session trade counts, costs, dependent outcomes or a different threshold change it. Scaling down for extraction can also make a winning day too small to qualify.

### 5.3 Cadence versus profit generation

Profit generation and qualifying days can overlap within a payout cycle, but caps, cycle resets, processing times and minimum new profit can require further cycles after the account reaches the desired balance. Evaluation and funded requirements occur in sequence. Neither the payout cadence nor profit generation can be assumed to be the limiting factor without modelling the chosen product and withdrawal plan.

### 5.4 Cost

Compare total outlay over the actual expected holding period, including evaluation or funded purchase price, recurring subscription charges, activation fees, and any reset or replacement costs. Straight-to-funded avoids the evaluation target and evaluation breach risk, but its purchase price, funded rules and payout conditions must be assessed on their own terms. Paying more is acceptable when the account better supports faster equity growth.

---

## 6. Account survival and cushion

The target depends on both building profit and keeping the account eligible long enough to withdraw it. Profit held in the account can support larger positions, but remains exposed to losses, rule breaches and any forced transition.

### 6.1 Cushion after a payout

For an illustrative 50K account with a locked floor at \$50,100:

| Balance after payout | Cushion above floor | Full \$200 losses to reach the floor, ignoring costs |
|---|---|---|
| \$52,100 | \$2,000 | 10 |
| \$51,100 | \$1,000 | 5 |
| \$50,300 | \$200 | 1 |

These are distances, not guarantees of survival: losses may be larger than planned, and real-time enforcement can breach the floor during an open trade. If the position is two MNQ with a 100-point stop, each planned loss is \$400 instead, so a \$2,000 cushion covers five such losses rather than ten. The floor and payout buffer vary by product.

A required payout buffer can therefore provide trading room as well as restrict withdrawals. With no required buffer, it may still be prudent to retain a voluntary cushion; the amount is a decision, not a universal rule.

### 6.2 Losing streaks and exposure

At an assumed 50% loss probability and independent outcomes, a specified sequence of ten losses has probability **1 in 1,024**. The probability of encountering such a run somewhere in a longer series is higher and depends on the number of trades. Neither figure alone is the probability of account failure: wins between losses, a moving floor, variable stops, position sizing, commissions and withdrawals all affect survival.

A fixed ten-loss example also becomes less representative as size changes. The relevant question is how much a sequence of losses would cost **at the position sizes actually used**, relative to the cushion at each trade.

### 6.3 Managing risk during growth and extraction

- **During growth:** increase size only when the actual cushion and product limits allow it; remember that a trailing floor can prevent cushion from growing until it locks.
- **Before withdrawing:** calculate the balance and cushion that will remain after the requested gross amount is deducted, using the provider's rules.
- **During extraction:** reassess size after each payout and allow for qualifying-day thresholds, daily limits and slippage. Smaller trades lower exposure but can take longer to meet payout requirements.
- **After a breach:** whether to reset, buy another account or move to own capital remains undecided and may depend on the experience and available funds.

---

## 7. Product selection criteria

| Criterion | Relevance to this case |
|---|---|
| Netherlands availability | Essential; verify any unresolved provider restrictions and payout methods |
| Drawdown size, update and enforcement | Determines starting risk capacity, when cushion can grow and how open trades can breach |
| Position limits, scaling and daily loss limits | Must support the intended size as cushion grows, in both growth and extraction phases |
| Payout formula and total extraction | Test whether one account can deliver \$5,000 and preferably \$10,000 in hand |
| Qualifying days and consistency | Determine whether smaller trades can satisfy payout requirements after growth |
| Forced live transition | Acceptable but not preferred; verify timing, starting cushion and treatment of remaining profits |
| Accidental news exposure | Avoid an account-ending rule that can be triggered accidentally during the trading session |
| Inactivity | Check requirements against 1–2 sessions per week and possible breaks |
| Cost and resets | Compare purchase, subscription, activation and any reset costs against the desired risk capacity |
| Platform | Tradovate is preferred |

No product is selected here. The comparison needs to model both accumulation and extraction, including the account-specific rules and any unresolved documentation conflicts.

---

## 8. Remaining decisions

1. **Sizing rule:** What fraction of the current cushion may be risked on one trade, and when should size be reduced after losses or a payout?
2. **Session risk:** How much can be lost in one session, including several stops and slippage, without taking more risk than intended?
3. **Withdrawal trigger:** At what balance or available payout should extraction begin, and how much cushion should remain during the payout cycles?
4. **Budget and retry:** What is the purchase budget, and would a breach justify a reset or another purchase? The decision may depend on the trading experience and available own capital at that time.
5. **Evidence for the edge:** What win rate, stop distribution and losing streaks emerge from actual trading? These determine whether the assumed expectancy and scaling plan are realistic.
6. **Payout verification:** For each candidate, confirm the applicable profit definition, caps, qualifying-day thresholds, split, fees, live-transition terms and payout methods.
