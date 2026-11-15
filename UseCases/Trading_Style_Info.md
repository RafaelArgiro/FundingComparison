# Trading Style

The trading profile the funding comparison must be fitted to.

Implications for provider selection are in `relevant_for_comparison.md`. This document is
the profile itself.

---

## 1. Instruments

| | |
|---|---|
| Traded | **NQ** and **MNQ** (E-mini and Micro E-mini Nasdaq-100) |
| Watched for context | ES / MES — **reference only, never traded** |
| Everything else | Not traded |

Point values, for reference:

| Instrument | Value per point |
|---|---|
| NQ | \$20 |
| MNQ | \$2 |
| ES | \$50 |
| MES | \$5 |

---

## 2. Strategy

**Reversals traded into Fair Value Gaps (FVGs).**

Entries are taken against the prevailing short-term move, at an FVG acting as the
reference level.

---

## 3. Risk per trade

| | |
|---|---|
| Stop loss | **50 to 100 Nasdaq points** |
| In dollars, per MNQ | **\$100 to \$200** |
| In dollars, per NQ | \$1,000 to \$2,000 |
| Reward target | **1:2R** — 100 to 200 points |
| Profit per MNQ at target | \$200 to \$400 |

---

## 4. Frequency

| | |
|---|---|
| Trades per trading day | **1 to 3** |
| Trading days per week | **1 to 2** |
| Trading days per month | roughly **4 to 9** |
| Trades per month | roughly **4 to 27**, central estimate **15** |
| Trading days per year | roughly **52 to 104** |

---

## 5. Exit management

| | |
|---|---|
| Exit style | **All or nothing** |
| Partial profits | None |
| Breakeven stops / trailing | Not used |
| Scaling into a position | **No** — single entry fill |
| Outcome per trade | Either **+2R** or **−1R** |

**Assumed win rate: 50%**, pending measurement. At that rate and a \$200 stop, expectancy
is **+\$100 per trade** on one MNQ. Breakeven win rate for the system is 33.3%.

---

## 6. Session and timing

| | |
|---|---|
| Session traded | **US open, 09:00 to 11:00 New York** |
| Local time (Netherlands) | **15:00 to 17:00**, year-round — the six-hour offset holds through both DST changes |
| Typical trade duration | **Minutes**, not seconds |
| Positions held into the close | No |

---

## 7. Conduct

| | |
|---|---|
| News trading | **Not deliberate.** May occur accidentally — must not be account-ending |
| Automation / bots | **None** |
| Trade copying | **None** |
| Scaling in / averaging | **None** |

---

## 8. Practical constraints

| | |
|---|---|
| Country of residence | **Netherlands** |
| Platform preference | **Tradovate** |

---

## 9. Open inputs

Deferred to the case document rather than answered here:

| # | Input | Status |
|---|---|---|
| 1 | Longest historical losing streak | **Unknown** — assumptions used instead |
| 2 | Target monthly income | To be set per case |
| 3 | Budget, and number of parallel accounts | To be set per case |
| 4 | Appetite for the move to live capital | To be set per case |
| 5 | Tolerance for blown accounts | To be set per case |

Win rate is currently an assumption rather than a measurement. It is the input the
conclusions are most sensitive to.
