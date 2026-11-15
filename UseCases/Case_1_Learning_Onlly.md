# Case 1 — Learning Only

## 1. The goal

Spend roughly **two months** trading a simulated futures account to get a feel for how
futures trading works, then **move to trading own capital**.

The account is a **learning environment, not an income source**.

---

## 2. What this case does and does not care about

### Does not matter

| | Why |
|---|---|
| **All payout rules** | No payout will ever be requested |
| Payout caps, cadences, buffers | Same |
| Consistency rules | Only ever bind at payout time |
| Minimum trading days to payout | Same |
| Profit split | Nothing will be withdrawn |
| Move to live, and its terms | The exit is to own capital, not to a live prop account |
| Scaling plans and contract limits | 1–2 MNQ against limits of 20–100 micros |
| **Passing the evaluation** | Not required. An evaluation account is already a simulated trading account — it can simply be traded for two months and abandoned |

**The profit target is irrelevant.** Nothing needs to be reached. This removes the single
biggest driver from the general comparison.

### Does matter

| Rank | Criterion | Why |
|---|---|---|
| 1 | **Survivability of a session** | The account must not be destroyed by one bad day |
| 2 | **Total cost over two months** | As cheap as possible |
| 3 | **Drawdown type** | Determines how fast room erodes while learning |
| 4 | **Inactivity rules** | At 1–2 sessions per week, a weekly requirement has no margin |
| 5 | **Availability in the Netherlands** | Binary filter |
| 6 | Reset cost | Only if the account is blown and the experiment continues |

---

## 3. The risk requirement, made concrete

**"Must not lose the account in a single session."**

At 1–3 trades per session and a \$100–\$200 stop:

| | Worst session |
|---|---|
| 3 trades × \$200 stop | **−\$600** |
| 3 trades × \$100 stop | −\$300 |

Against each account's drawdown:

| Account | Drawdown | Worst session as % | Sessions to destroy |
|---|---|---|---|
| 25K | \$1,000 | **60%** | **under 2** |
| 50K | \$2,000 | 30% | 3.3 |
| 100K | \$3,000–3,500 | 17–20% | 5–6 |
| 150K | \$4,500–5,000 | 12–13% | 7.5–8 |

**A 25K account fails the stated requirement.** Two bad sessions ends it, and over 8–17
sessions of learning that is a likely outcome rather than a tail risk.

**A daily loss limit is the direct answer to this requirement.** It halts trading before
the drawdown is reached, so the account survives the session:

| Account | DLL (typical) | Drawdown | Room left after a maxed-out day |
|---|---|---|---|
| 50K | \$1,200–1,250 | \$2,000 | \$750–800 |
| 100K | \$1,800–2,500 | \$3,000–3,500 | \$1,000–1,700 |

**Conclusion: buy a product with the daily loss limit ON.** It is both the cheaper
configuration and the one that satisfies the primary requirement. Paying extra to remove it
would be paying to defeat the purpose.

---

## 4. The drawdown-type requirement

While learning, trades will frequently run to unrealised profit and give it back.

| Drawdown type | Effect over two months of learning |
|---|---|
| **Intraday trailing** | Every unrealised peak permanently reduces room, even on trades that close flat. Room erodes fastest. |
| **EOD trailing** | Only closing balances move the floor. Round trips cost nothing. |
| **Static** | Floor never moves at all. |

**Intraday-trailing products should be avoided for this case**, because a learning account
will generate many unrealised peaks that never convert to closed profit.

---

## 5. Cost basis

Two months at 1–2 sessions per week is **8 to 17 sessions**.

**One-time pricing is charged once**, regardless of how long the account is held.
**Subscription pricing is charged twice** over two months, and again for every further
month.

Cost should be compared as **total outlay for two months**, including one reset if the
account is expected to be blown.

---

## 6. Open questions for this case

### Would change the recommendation

1. **Why pay at all?** A plain broker demo or simulator costs nothing and has no drawdown
   rules. If the goal is purely to learn how futures behave before trading own capital,
   the prop-firm rule set is an artificial constraint that will not exist afterwards.
   Paying is only justified if the intent is also to experience trading **under
   restriction**, or to keep open the option of continuing into funding.
   **This is the most important question in this case.**

2. **Is blowing the account an acceptable outcome, or must it survive the full two
   months?** If it must survive, size up and accept the cost. If blowing it is simply part
   of learning, buy the cheapest option and treat a reset as optional.

3. **Hard budget ceiling.** "As cheap as possible" needs a number before the options can be
   ranked. The realistic range is roughly \$45 to \$225 for two months.

### Would narrow the choice

4. **Position size while learning.** One MNQ throughout, or scaling up to 2–3 as confidence
   builds? This changes the required drawdown directly.

5. **Is the option to continue into funding worth anything?** If the answer is a firm no,
   products can be chosen purely on cost and drawdown, ignoring everything about the funded
   phase. If it is a maybe, the evaluation chosen should be one whose funded terms are
   acceptable.

6. **How tolerant are you of a weekly inactivity requirement?** One provider requires at
   least one trade per week per account. At 1–2 sessions per week there is no margin — a
   holiday or a skipped week forfeits the account.

7. **Does the account need to feel realistic?** A daily loss limit protects the account but
   also stops the session early, which is not how trading own capital will work.

### Useful to confirm

8. **Would you run one account or two in parallel?** Two cheap accounts give two
   independent drawdowns and a spare if one is blown, often for less than one larger
   account.

9. **Is a specific platform required for the learning to transfer?** Tradovate is the
   stated preference; if the eventual own-money broker uses something else, learning on
   that platform instead may be worth more than the price difference.
