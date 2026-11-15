# Lucid — Live Phase

Rules that apply once an account is moved to LucidLive: real capital, real markets.

> **Read `Lu_Rules_General.md` first.** Prohibited and permitted conduct, instruments and
> platforms apply here and are not repeated.

> **Which structure applies.** Three sets of live rules exist in the documentation. The
> **New Live Structure** is the current one and is what this document describes. The
> per-product "X Live (Legacy)" articles apply only to accounts **purchased or reset on
> 2/27/26 and prior** and are summarised in section 9. LucidDaily runs its own variant —
> section 8.

Consequence codes:
- **KILL** account lost immediately
- **LOCK** trading halted until next session
- **BLOCK** payout blocked or denied
- **STRIP** profits removed
- **BAN** consequences beyond this account

---

## 1. What is specific to the live phase

| | |
|---|---|
| Capital | **Real**, not simulated |
| Starting balance | **\$0** |
| Profit split | 90% / 10% — unchanged from funded |
| Payout frequency | **Daily** |
| Drawdown | End-of-day |
| Daily Loss Limit | **None** |
| Consistency | **None** |
| Simulated accounts | **All closed** on transition |
| Household | No household member may trade simulated accounts while you are live |

**The split does not change.** Lucid pays 90/10 at live, the same as funded. The Live Bonus
is also subject to the 90/10 split.

**Every live account starts at \$0.** You are not allocated a balance. The account is
funded by what you earn, against a starting drawdown set by the size of the funded account
you came from.

**Hedging a live account is a permanent ban**, enforced by both Lucid and the CME, and
explicitly includes copy-trader malfunctions.

---

## 2. Getting there

**You enter the live review pool** when one or more of the following is true:

- You receive the **final payout (Payout 5)** on a Flex, Pro or Direct account
- You have been **paid out a significant amount of capital** over your lifetime
- You **earn the Maximum Daily Profit** for your LucidDaily account size
- You show **exceptional performance** in sim funded
- You have **previously been moved live**

Payout 5 is the maximum payout level, not a guaranteed minimum for eligibility. **All live
transitions occur at the discretion of the Lucid risk team.**

**One live account per eligible funded account**, and each funded account must have
received **at least one payout** to qualify.

**All eligible funded accounts move at once.** You do not transition account by account.

**What happens to the rest:** every simulated account is closed on transition, including
evaluations held in reserve. If a funded account is not moved live because it is
ineligible, its evaluation cost is refunded — **but only if the account has at least 50%
of its total drawdown remaining**. The explicit advice is not to hold evaluations in
reserve if you are uncomfortable with them being closed.

---

## 3. The cashout option

A trader who does not want to trade live capital may take a **cashout instead of the
transition**.

- The cashout is **50% of your live starting balance**, subject to the 90/10 split.
- **You have 24 hours** from receiving the move-to-live email to choose.
- **If you do not respond, the accounts move to live automatically.**

This is the only documented route to decline the transition. Taking it closes the
simulated accounts in the same way.

---

## 4. Live risk limits

**Starting live drawdown and contract limits**, set by the size of the funded account you
transitioned from:

| Funded account size | Starting live drawdown | Max live contract limit |
|---|---|---|
| \$25,000 | \$1,000 | 2 minis or 20 micros |
| \$50,000 | \$2,000 | 4 minis or 40 micros |
| \$100,000 | \$3,000 | 6 minis or 60 micros |
| \$150,000 | \$4,500 | 10 minis or 100 micros |

Certain highly volatile contracts carry reduced position sizing so that a single position
cannot exceed the live drawdown.

**Locking the live Max Loss Limit.** Live accounts use end-of-day drawdown. The floor rises
with the highest closing balance up to a defined point, then locks. Two triggers:

- Once live profits **equal your starting live drawdown**, the Max Loss Limit locks at
  **\$100**.
- **If you request a payout before** generating profits above the live drawdown, the Max
  Loss Limit locks to \$100 immediately.

**There is no Daily Loss Limit at live** on any account, and no consistency requirement.

**Trading hours differ by broker at live**: positions may be held until **4:45 PM EST on
Tradovate Live** but only **4:15 PM EST on Rithmic Live**. Swing trading is not permitted.
An auto-liquidate option can be enabled during onboarding to close positions before the
cutoff.

---

## 5. The Live Bonus

A **repeatable** bonus, subject to the 90/10 split. Two objectives must both be met:

1. Generate live profits above the starting balance equal to the **Live Profit Target**
2. Complete **20 trading days**

| Funded account size | Live profit target | Trading days | Live Bonus |
|---|---|---|---|
| \$25,000 | \$2,000 | 20 | \$1,000 |
| \$50,000 | \$4,000 | 20 | \$2,000 |
| \$100,000 | \$6,000 | 20 | \$3,000 |
| \$150,000 | \$9,000 | 20 | \$4,500 |

- A **trading day** is one or more trades generating at least +\$1 or −\$1 of net P&L, net
  of fees, at the end of the session.
- **Taking payouts does not reduce the profit target calculation.**
- The bonus is **repeatable** and may be earned on every account moved live.
- **Contract flipping or similar exploitation of the trading-day count may trigger review.**
- **LucidMaxx traders are not eligible.**

---

## 6. Live scaling plan

Live contract limits depend on **both account size and exchange**, and adjust at the end of
each trading day as profits rise and fall. COMEX products are consistently restricted
relative to CME, CBOT and NYMEX.

Example, **\$50,000 live account**:

| Profit range | CME | CBOT | NYMEX | COMEX |
|---|---|---|---|---|
| \$0 – \$1,999.99 | 2 minis | 2 minis | 2 minis | 1 mini |
| \$2,000 – \$3,999 | 3 minis | 3 minis | 3 minis | 1 mini / 15 micros |
| \$4,000+ | 4 minis | 4 minis | 4 minis | 2 minis |

The same pattern applies at 25K, 100K and 150K, with the 150K account additionally capping
CBOT at 8 minis, NYMEX at 6 minis and COMEX at 5 minis even at full scale.

**The limits move down as well as up**, in direct correlation with profit, calculated at
the end of each trading day.

---

## 7. What is forfeited on the move

This is the part that most affects the economics of the whole programme.

**Under the current structure**, live accounts start at \$0 and the documentation does not
describe simulated profit transferring at all — the cashout option (50% of live starting
balance) is the stated alternative to transitioning.

**LucidDaily is explicit and different** — see section 8.

**Under the legacy structures** simulated profit was transferred up to per-account caps
with the excess forfeited, and most of it held in escrow — see section 9.

---

## 8. LucidDaily's separate route

LucidDaily transitions differently and the terms are materially worse.

- **Entry triggers**: earning the Maximum Daily Profit for your account size, significant
  lifetime payouts, exceptional sim performance, or having previously been live.
- **The buffer balance funds the starting live drawdown and may not be withdrawn.** On a
  50K that is \$2,100 of simulated profit converted into drawdown cushion rather than cash.
- **Simulated profit above the buffer may be paid out** after KYC with the broker partner
  and sub-account approval — but **capped at \$15,000 in total**.
- **The \$15,000 cap is absolute.** It is the same whether you hold one 25K account or five
  150K accounts. Anything above it cannot be withdrawn.
- **Transitions run every evening** after the final session report at 6:00 PM EST, and can
  take several hours. Accounts are paused and **all positions flattened**.
- **You may be moved live mid-position.** To keep this fair, Lucid uses your **prior day's
  closing balance** as the amount moved live; profits or losses made during the session of
  the move do not count.

Live parameters afterwards are the same as section 4: \$0 start, daily payouts, end-of-day
drawdown, no daily loss limit.

---

## 9. Legacy structures

These apply only to accounts **purchased or reset on 2/27/26 and prior**. Four different
mechanisms are described across the product articles.

**Move-to-live caps per account**, with profit above the cap forfeited:

| Size | LucidPro | LucidFlex | LucidDirect |
|---|---|---|---|
| \$25,000 | \$15,000 | \$4,000 | \$4,000 |
| \$50,000 | \$20,000 | \$8,000 | \$8,000 |
| \$100,000 | \$25,000 | \$12,000 | **not published** |
| \$150,000 | \$30,000 | \$16,000 | \$16,000 |

**Day-one capital**, with the remainder held in escrow:

| Size | LucidPro | LucidFlex | LucidDirect |
|---|---|---|---|
| \$25,000 | \$2,000 | \$1,200 | \$1,200 |
| \$50,000 | \$3,000 | \$2,400 | \$2,400 |
| \$100,000 | \$4,000 | \$3,600 | **not published** |
| \$150,000 | \$5,000 | \$4,800 | \$4,800 |

**Escrow release** required 10 profitable live trading days **and** \$10,000 of live
profits before any release could begin, then \$5,000 released per additional \$10,000 of
live profit, reviewed weekly. Withdrawal required waiting 60 days from account opening, and
reckless trading disqualified a trader from release entirely.

**An older Legacy Live Bonus** paid a **one-time** bonus for finishing a single session
with live profits at or above the starting live drawdown — targets \$1,100 / \$2,100 /
\$3,100 / \$4,600 for bonuses of \$1,000 / \$2,000 / \$3,000 / \$4,500. The current bonus
requires roughly double the profit plus 20 trading days, but is repeatable.

> **Documentation conflict.** Each product's legacy sub-section describes a *different*
> cap mechanism again: LucidFlex a flat \$5,000 per account regardless of size, LucidPro a
> \$150,000 total cap across all accounts, LucidDirect \$2,500 / \$5,000 / \$15,000. Which
> applied to whom is not resolvable from the documentation.

---

## 10. What takes the account away

1. **Reaching the live Max Loss Limit**, which starts at \$1,000 to \$4,500 depending on the
   funded size you came from, and locks at \$100 once you have earned profits equal to the
   starting drawdown. Until that lock, the usable room is small and real money is at stake.
2. **Hedging.** BAN, and a **permanent ban** at live — prohibited by both Lucid and the
   CME, explicitly including copy-trader malfunctions.
3. **Holding past the broker cutoff**, which is an hour earlier on Rithmic Live (4:15 PM
   EST) than on Tradovate Live (4:45 PM EST).

**After blowing a live account** there is a **standard 2-week cooldown** before you may
purchase a new evaluation. Repeatedly blowing live accounts through reckless trading can
extend the cooldown at the risk team's discretion.

---

## 11. What limits your profit

1. **Starting at \$0 with a small drawdown.** The live account is funded entirely by what
   you earn, against \$1,000 to \$4,500 of room. The early period carries the highest risk
   of ending the account with nothing to show.
2. **The \$15,000 total cap on simulated profit when coming from LucidDaily**, regardless
   of account count or size, with the buffer additionally converted into drawdown rather
   than cash.
3. **The exchange-based scaling plan**, which restricts COMEX positions well below the
   headline contract limit and recalculates daily in both directions.
4. **The 20-trading-day requirement on the Live Bonus**, which sets a floor on how quickly
   it can be earned regardless of performance.
5. **Loss of the simulated programme.** You cannot run simulated accounts while live, and
   neither can anyone in your household, so there is no parallel path.

**What does not limit you:** there is no consistency rule, no daily loss limit, no payout
cap and no fixed payout window at live. Payouts are daily.

---

## 12. Open questions

- **Whether simulated profit transfers at all under the current structure.** The legacy
  articles describe caps and escrow; the New Live Structure describes a \$0 start and a
  cashout alternative, without stating what happens to accumulated simulated profit on
  Pro, Flex and Direct.
- **Which structure applies to an account bought today.** The 2/27/26 cutoff is stated on
  the per-product legacy articles, but the LucidDaily Live article carries no cutoff at all.
- **LucidMaxx.** Referenced three times as a tier with daily uncapped payouts, a static
  rather than end-of-day live balance, and a starting balance above \$0 that is withdrawable
  from day one. The documentation it points to is not in the captured material.
- **LucidBlack.** Named once as the product that now holds the Live Bonus exclusively,
  which contradicts the bonus being available at live generally. Not documented anywhere.
- **The LucidDirect \$100,000 legacy figures**, absent from all three legacy tables despite
  the product being sold in that size.
- **Whether live commissions differ** from the simulated per-side schedule.
