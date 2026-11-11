# Lucid Data Health

Status of the Lucid Trading source material in this folder, for the purpose of comparing
funding options for daytrading.

Files reviewed:

- `GeneralInfo.md`
- `FeesPaymentsPayouts.md`
- `LucidPro.md`
- `LucidPro copy.md`
- `LucidFlex.md`
- `LucidDirect.md`
- `LucidDaily.md`
- `Rules_n_guidelines.md`
- `LiveTrading.md`

---

## 1. Blocking issue: there are no prices

`FeesPaymentsPayouts.md` describes the pricing *model* in full (one-time fee, no
subscription, no rebilling, no activation fee, paid resets) but contains **no prices at
all**. Not one account size, product line or add-on has a figure attached.

This is compounded across the product files, which repeatedly describe price as a
relative quantity without ever giving the absolute:

- "Results in a lower evaluation purchase price" (Daily Loss Limit On)
- "Results in a higher evaluation purchase price" (Daily Loss Limit Off)
- "Added at checkout for a small fee" (50% consistency add-on)
- "Cheapest version of LucidFlex" / "Mid-tier pricing" / "Most expensive version"

Missing figures:

- Evaluation price per size for LucidPro, LucidFlex and LucidDaily
- LucidDirect purchase price per size
- Reset price per product and size
- The DLL On/Off price delta
- The 50% consistency add-on price
- The LucidDaily Intraday vs End-of-Day evaluation drawdown price delta

Lucid's cost side cannot be modelled from this data. Everything in sections 5 and 6 is
usable; the cost column is empty.

---

## 2. Duplicate file

`LucidPro copy.md` is a duplicate of `LucidPro.md`. Both contain the same eight articles
with the same content. Keeping both creates a risk that one is updated and the other is
not, and that a later comparison reads the stale copy. One of the two should be removed.

---

## 3. Internal contradictions

| # | Contradiction | Where |
|---|---|---|
| 1 | **Number of payouts before the move to live: 5 or 6.** LucidFlex Payouts states "Traders may take up to **5** payouts from each LucidFlex account after which they will be moved live." LucidFlex Live (Legacy) states traders are moved live "After completing their **sixth** and final LucidFlex payout". The same 5/6 split exists for LucidPro and LucidDirect. | `LucidFlex.md`, `LucidPro.md`, `LucidDirect.md` vs `LiveTrading.md` |
| 2 | **LucidDaily consistency: 40% or 50%.** The Customization article offers "40% (standard)" or "50% (add-on)". The Evaluation table lists 50% for every account size with no 40% option, and the Consistency article states flatly "you must have Consistency Percentage of 50% or less" and never mentions 40%. | `LucidDaily.md`, within one file |
| 3 | **LucidDaily has two settings, three settings, four configurations or eight.** The Customization article says "Two settings can be adjusted", then lists three (Daily Loss Limit, Evaluation Drawdown, Consistency), then says "These settings create **eight** unique LucidDaily account configurations", then the Available Account Configurations section says "LucidDaily offers **four** possible combinations" and lists four. Three binary settings give eight. | `LucidDaily.md`, within one article |
| 4 | **Scaling DLL is defined against two different quantities.** The LucidPro and LucidDirect funded account tables carry a column headed "Scaling DLL — **60% of Peak EOD Balance**". The LucidScale formula in the Daily Loss Limit articles is "Highest end-of-day account **profit** × 60%". On a $50,000 account those differ by roughly $30,000. The formula is correct; the table header is not. | `LucidPro.md`, `LucidDirect.md` |
| 5 | **LucidDirect 25K Initial Trail Balance.** The Daily Loss Limit table gives "None"; the Drawdown table gives "$26,100" for the same account. | `LucidDirect.md`, within one file |
| 6 | **Platform availability.** The Supported Platforms article summary says "All platforms work across **LucidFlex and LucidPro** accounts", while the body says "All listed platforms work with **all** Lucid account types." LucidDirect and LucidDaily are not addressed in the summary. | `GeneralInfo.md` |
| 7 | **Resets for a product with no evaluation.** The fees article says "LucidPro Evaluation **and LucidDirect** accounts are purchased by paying a one-time fee... you will need to purchase a reset if you wish to restart your **evaluation** account." LucidDirect has no evaluation phase. What a LucidDirect reset restarts is not stated. | `FeesPaymentsPayouts.md` vs `LucidDirect.md` |
| 8 | **Three move-to-live cap structures described for the same transition.** LucidPro Live (Legacy) uses per-account caps of $15,000–$30,000 plus escrow. LucidDirect Live (Legacy) uses per-account caps of $4,000–$16,000 plus escrow, and its own legacy sub-section uses $2,500/$5,000/$15,000. LucidFlex Live (Legacy) uses $4,000–$16,000, and its legacy sub-section uses "a **$5,000** move to live cap for each account **regardless of account size**". LucidPro's legacy sub-section uses "a **$150,000 total** live funding cap across all active accounts". Four different mechanisms. | `LucidPro.md`, `LucidDirect.md`, `LucidFlex.md` |

---

## 4. Missing data

**Product coverage gaps**

- **LucidDirect Live (Legacy) omits the $100,000 account size** from all three of its
  tables: Max Moved Live, Max Deposited Day 1, and the legacy transition table. LucidDirect
  is sold in $100,000. The equivalent LucidFlex article does include the 100K row
  ($12,000 moved live, $3,600 day one).
- **LucidDirect payout maximums stop at "Payouts 4-5"**, with no row for a sixth payout,
  while the LucidDirect Live article refers to "their sixth and final LucidDirect payout".
- **LucidDaily is absent from the trading-hours rules.** Allowed Trading Times covers
  "LucidPro, LucidFlex and LucidDirect Accounts" and "LucidLive Accounts" only.
- **LucidDaily and LucidFlex are absent from the account-limit rules.** Maximum Number of
  Accounts names only evaluation accounts, funded accounts, LucidDirect, LucidPro and
  LucidLive.
- **LucidPro $25K has no Daily Loss Limit** per the evaluation and DLL tables, yet the
  LucidPro Customization article presents DLL On/Off as a purchase choice and ties On
  Demand Payouts to DLL On. LucidDirect explicitly resolves the same situation for its
  25K ("no Daily Loss Limit, so their payouts follow the regular end-of-day schedule").
  LucidPro does not.
- **LucidPro Customization does not carry the hedging exclusion.** LucidFlex and
  LucidDaily both state that "Accounts with a Hedging Violation are not eligible for
  intraday payouts". LucidPro offers On Demand Payouts but does not mention it.

**Undocumented products and tiers**

- **LucidMaxx** is referenced three times as a materially better tier (daily uncapped
  payouts, instant live capital, a static rather than end-of-day live balance, a live
  balance above $0 that is withdrawable from day one). Every reference says "refer to the
  LucidMaxx documentation". That documentation is not in this folder.
- **LucidBlack** is named once, as the product that now holds the Live Bonus feature
  exclusively. It is not documented anywhere.

**Missing entirely**

- What happens when a **funded** account breaches. The Inactivity Policy covers resets for
  breached *evaluations* only. Whether a breached funded account can be repurchased or
  reset is never addressed.
- KYC and payout verification requirements and timing.
- Tax documentation (1099 or equivalent) and who issues it.
- Minimum age.
- Any U.S. state restrictions (only a country-level restricted list is given).
- The commission basis for the move-to-live calculation and whether live commissions
  differ from the simulated schedule.

---

## 5. Ambiguities worth resolving before a tradeoff

- **Which live structure applies to a new purchase today.** `LiveTrading.md` contains both
  a "Legacy Live Structure" and a "New Live Structure". Separately, each product file
  contains its own "X Live (Legacy)" article carrying the cutoff "accounts purchased/reset
  on 2/27/26 and prior". `LucidDaily.md` contains a "LucidDaily Live" article with no
  cutoff and a fourth set of rules. Nothing states the precedence.
- **The Live Bonus is described two ways.** The Legacy Live Structure pays a one-time bonus
  for finishing one session with live profits at or above the starting live drawdown
  (targets $1,100 / $2,100 / $3,100 / $4,600). The New Live Structure pays a repeatable
  bonus requiring both a profit target of $2,000 / $4,000 / $6,000 / $9,000 **and** 20
  trading days. The bonus amounts are identical ($1,000 / $2,000 / $3,000 / $4,500) but
  the targets differ by roughly a factor of two and the qualifying conditions are not
  comparable. The New Live article summary calls the bonus "monthly"; the body never does.
- **LucidFlex scaling direction.** The scaling plan says contract limits "move up and down"
  with profits and that "your scaling tier may adjust downward" after a payout, so the
  plan is not cumulative. The table's top tier for each account size is followed by blank
  cells rather than an open-ended "and above" row, leaving the limit above the top
  threshold undefined.
- **Undated cutoffs.** `LucidDirect.md` refers to "accounts purchased as of **1/18** at 3
  PM EST", "traders mid onboarding as of **1/18**" and "move to live email on **1/31** or
  earlier" with no year.
- **Timezone usage.** Trading hours are given in EST (4:45 PM EST close, 6:00 PM EST
  reopen) while payout windows are given in ET (6:00 PM to 3:45 PM ET). The 3:45 PM ET
  intraday payout cutoff appears only in the customization articles, not in Allowed
  Trading Times.
- **The 3:45 PM ET On Demand Payout cutoff is 60 minutes before the 4:45 PM close.** What
  happens to a position held between those times on an account that has already requested
  an intraday payout is not stated beyond "trading is paused until the end of the trading
  day".

---

## 6. Data quality issues

- **Commission article title is typo'd**: "pproved Products and Commissions" (missing the
  leading A).
- **Commissions are quoted per side.** Lucid publishes per-side rates; most other firms
  publish round-trip. Any comparison must double Lucid's figures first. ES at $1.75 per
  side is $3.50 round trip.
- **SIL (Micro Silver) is priced at $1.60 per side**, which is double MGC (Micro Gold,
  $0.80) and 70% of full-size Silver (SI, $2.30). For a contract one fifth the size of SI,
  this is out of line with every other micro in the table and should be verified.
- **Restricted-country list formatting**: "Papua" and "New Guinea" are split across two
  lines, as is "Congo Republic (Brazzaville)" / "Congo (Kinshasa)".
- **Marketing strings captured as content**: "$500,000,000 paid to traders" appears as a
  body line in `GeneralInfo.md`, `LucidFlex.md` and `LiveTrading.md`. "Did this answer your
  question? Disappointed Reaction😞Neutral Reaction😐" appears in `LucidFlex.md` and
  `Rules_n_guidelines.md`.
- All embedded screenshots and images are absent.

---

## 7. Verified figures

These were checked for internal consistency and hold up.

### Four product lines

| Product | Evaluation | Funded drawdown | Consistency | Notable |
|---|---|---|---|---|
| LucidPro | Yes, profit target | EOD | 40% on funded payouts (35% pre 11/28/2025) | DLL On/Off chosen at purchase; LucidScale DLL |
| LucidFlex | Yes, profit target | EOD | 40% or 50% in evaluation only, none when funded | Funded contract scaling; no buffer |
| LucidDirect | No, straight to funded | EOD | 20% on funded payouts | No evaluation; larger drawdowns at 100K/150K |
| LucidDaily | Yes, profit target | **Intraday** | 50% in evaluation only, none when funded | Daily payouts; auto-move-live on max daily profit |

### Evaluation parameters (identical across Pro, Flex and Daily)

| Account | Profit target | Max Loss Limit | Max size |
|---|---|---|---|
| $25,000 | $1,250 | $1,000 | 2 mini / 20 micro |
| $50,000 | $3,000 | $2,000 | 4 mini / 40 micro |
| $100,000 | $6,000 | $3,000 | 6 mini / 60 micro |
| $150,000 | $9,000 | $4,500 | 10 mini / 100 micro |

### Drawdown mechanics

| Account | MLL (Pro/Flex/Daily) | MLL (Direct) | Initial Trail Balance | Locked MLL |
|---|---|---|---|---|
| $25,000 | $1,000 | $1,000 | $26,100 | $25,100 |
| $50,000 | $2,000 | $2,000 | $52,100 | $50,100 |
| $100,000 | $3,000 | $3,500 | $103,100 (Direct: $103,600) | $100,100 |
| $150,000 | $4,500 | $5,000 | $154,600 (Direct: $155,100) | $150,100 |

Initial Trail Balance equals starting balance + MLL + $100 in every case. Once the account
closes above it, the MLL locks at starting balance + $100 and stops moving.

### LucidPro payout thresholds

All four columns are internally consistent. Buffer = starting balance + MLL + $100;
minimum balance for a $500 payout = buffer + $500; minimum balance for the maximum payout
= buffer + maximum.

| Account | Buffer | Min balance for $500 | Max payout 1 | Max payout 2+ | Min profit goal |
|---|---|---|---|---|---|
| $25,000 | $26,100 | $26,600 | $1,000 | $1,500 | $250 |
| $50,000 | $52,100 | $52,600 | $2,000 | $2,500 | $500 |
| $100,000 | $103,100 | $103,600 | $2,500 | $3,000 | $750 |
| $150,000 | $154,600 | $155,100 | $3,000 | $3,500 | $1,000 |

Note that on the $25,000 account the minimum profit goal ($250) is below the minimum
payout request ($500), so the goal is never the binding constraint there.

### Mechanics confirmed across documents

- **All drawdowns are end-of-day except LucidDaily funded accounts, which are intraday.**
  LucidDaily evaluations can be bought either way, and the intraday option is cheaper.
- **All Daily Loss Limits are soft breaches.** Hitting one locks the account out until the
  next session but does not fail it. Only the Max Loss Limit is a hard breach.
- **The LucidScale DLL only ratchets up.** Highest end-of-day profit × 60%, never decreases
  even if the account draws down. Applies to LucidPro and LucidDirect funded accounts once
  above the Initial Trail Balance. LucidDaily funded accounts keep a fixed DLL instead.
- **Profit split is 90/10 on every funded product.** Accounts purchased or reset before
  11/28/2025 at 3:00 PM EST keep 100% on the first $10,000.
- **LucidDaily has a maximum daily profit** of $6,000 / $8,000 / $10,000 / $12,000 by
  account size. Meeting or exceeding it triggers an automatic move to live. On that move,
  the buffer funds the live drawdown and is not withdrawable, and simulated profit above
  the buffer is capped at **$15,000 in total** regardless of account size or how many
  accounts are held.
- **Account limits**: 10 evaluation accounts per household, 5 funded accounts per
  household, 10 combined across evaluation and funded, 5 LucidLive accounts.
- **Positions must be flat by 4:45 PM EST.** Holding past this does not fail the account;
  Lucid closes it automatically. Markets reopen 6:00 PM EST Sunday to Thursday.
- **News trading is prohibited on LucidDaily funded accounts and is a hard breach**
  (US + High impact only, flat from one minute before to one minute after). It is
  permitted on Flex, Pro and Direct.
- **Microscalping threshold**: flagged if more than 50% of profit comes from trades held
  5 seconds or less.
- **Hedging is prohibited across accounts, across users and across firms**, including
  mini-against-micro and correlated products. Long/short the same contract in minis and
  micros is allowed within a single account only.
- **Automated strategies and trade copiers are permitted.** Flipping to meet trading-day
  requirements is explicitly allowed.
- **Inactivity**: an account with no net profit or loss of at least $1 within 30 calendar
  days is deleted. Breached evaluations are deleted after 30 days if not reset.
- **Payouts**: no fixed window, approved funds leave the account within minutes and are
  disbursed within 2 business days. Plaid (US instant), WorkMarket by ADP (US and
  international, bank or PayPal), or crypto (international, BTC/ETH/LTC/USDT/USDC).
- **Once live, no household member may trade simulated accounts.** All simulated accounts
  are closed on the move to live; evaluations held in reserve are closed, with the
  evaluation cost refunded only if the account has at least 50% of its drawdown remaining.
- **Cooldown after blowing a live account** is 2 weeks, longer at the risk team's
  discretion.

---

## 8. Next steps

1. Obtain the price list: evaluation price per product and size, LucidDirect price per
   size, reset price, the DLL On/Off delta, the 50% consistency add-on, and the LucidDaily
   drawdown-type delta.
2. Resolve whether the move to live occurs after payout 5 or payout 6.
3. Confirm the LucidDaily evaluation consistency requirement is 40%/50% selectable or a
   fixed 50%.
4. Obtain the LucidDirect $100,000 move-to-live and day-one figures.
5. Confirm which live structure applies to an account purchased today.
6. Obtain the LucidMaxx documentation, since it governs the best-case outcome of the
   program.
7. Confirm LucidDaily trading hours and whether the 4:45 PM EST flat rule applies.
8. Delete `LucidPro copy.md`.
