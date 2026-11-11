# Tradeify Data Health

Status of the Tradeify source material in this folder, for the purpose of comparing
funding options for daytrading.

Files reviewed:

- `Accounts_n_Rules.md`
- `Payouts_n_billing.md`
- `Getting_Started.md`
- `TradingPlatforms_n_products.md`
- `tradovate.md`
- `rithmic.md`
- `wealthCarts.md`

---

## 1. Overall state

This is the most complete of the three providers. Pricing, commissions, drawdown
mechanics, payout policies, contract scaling, product lists and conduct rules are all
present with concrete figures. Unlike the Apex material it describes currently purchasable
products, and unlike the Lucid material it includes a full price list.

The significant gaps are at the two ends of the journey: the **Tradeify Elite Program**
(the live-capital stage, referenced roughly eight times and never captured) and the
**Funded Reset price**. There is also a recurring undated cutoff, "the new dashboard
launch", used to split old and new parameters in at least four places.

---

## 2. Missing articles

Three collection indexes in this folder list more articles than were captured.

| Collection | Listed | Captured | Missing |
|---|---|---|---|
| Accounts & Rules | 20 | 18 | "Account Types", "Forge" (2 articles) |
| Getting Started | 14 | 13 | "How to Select the Correct Trading Contract" |
| Payouts & Billing | 8 | 8 | — |

Referenced throughout but not present in any file:

- **Tradeify Elite Program** — the live stage. The 80/20 split, daily payouts and the
  3-payouts-or-10-payouts eligibility threshold are mentioned in passing, but nothing
  about live drawdown, live contract limits, live payout mechanics, capital allocation or
  what happens on a live breach.
- **KYC and AML Policy** — required before the first payout, and before purchase on the
  Select 300K, and before activation for residents of ten named countries.
- **Drawdown Widget** — the article explaining how to see your real-time distance to the
  drawdown floor, which matters because the dashboard figure only updates once per day.
- **Sim and Live Account Restrictions**
- **Premier Trading League (PTL) Full Competition Guide**

---

## 3. Internal contradictions

| # | Contradiction | Where |
|---|---|---|
| 1 | **Select evaluation contract limits.** The Select Evaluation article states "25K Account Evaluation — Maximum Contracts: 1 mini / 10 micro". The Select Flex and Daily Payout Policies article states "During evaluation, you have access to the full contract limits (**2/20**, 4/40, 8/80, or 12/120 depending on account size)". The 2/20 figure is the 25K *funded* maximum, not the evaluation limit. | `Accounts_n_Rules.md` vs `Payouts_n_billing.md` |
| 2 | **Select evaluations have no Daily Loss Limit, except the 300K.** The Select Evaluation article, the SELECT vs Growth comparison, the Pricing Reference and the Essential Rules all state Select evaluations have no DLL. The 300K article states "The evaluation carries a **$4,000** daily loss limit." | `Accounts_n_Rules.md`, within one file |
| 3 | **Activation is instant, except on two of the three brokers.** "Activation is instant and there are no activation fees" is stated unconditionally in at least four places. The same article then says "Instant account activation after passing an evaluation is currently only available on the **Tradovate** platform." Rithmic and WealthCharts users are not told what to expect instead. | `Accounts_n_Rules.md`, within one article |
| 4 | **Select funded scaling.** Essential Trading Rules Overview states "Growth and Lightning use their maximum position size from day one; **Select funded accounts scale up** as the account grows", then immediately states "**Full limits available immediately — No need to build up gradually**" as a general rule. | `Getting_Started.md`, within one section |
| 5 | **Evaluations have no time limit, but accounts expire.** "There is no time limit to complete a Growth or Select Evaluation" is stated twice. Elsewhere: "your account remains active until you either pass, fail, or **the account expires**" and "Expired accounts cannot be reinstated". Expiry is never defined. The only time-based closure described is the weekly inactivity rule. | `Getting_Started.md` |
| 6 | **The Pricing Reference contradicts its own fee list.** It states "No hidden fees. The only costs are: (1) the account purchase price, (2) trading commissions, and (3) optional reset fees." Its own earlier sections describe the $300/month professional data fee, Tradovate L2 and EUREX add-ons, and TradingView subscriptions. It also omits the Funded Reset fee entirely. | `Accounts_n_Rules.md`, within one article |
| 7 | **Two definitions of the session boundary.** The trading day is defined as 6:00 PM ET to **5:00 PM ET** the next day in four places. One FAQ in the same article says "A Tradeify trading session runs from 6:00 PM ET to **4:45 PM ET** the next calendar day". | `Accounts_n_Rules.md`, within one article |
| 8 | **Select 300K availability.** The Select Evaluation article lists five sizes including $300,000, then its Getting Started steps say "Choose your account size (25K, 50K, 100K, **or 150K**)". | `Accounts_n_Rules.md`, within one article |
| 9 | **Stale collection description.** The Accounts & Rules collection is described as "Tradeify's challenge accounts including **Advanced**, Growth, and **Straight to Sim Funded** options". The current names are Select, Growth and Lightning. "Advanced" and "Straight to Sim Funded" appear nowhere else. | `Accounts_n_Rules.md` |

---

## 4. Missing data

**Prices**

- **Funded Reset price.** The whole product is described without a figure. The only
  pricing statement is "The second use costs 10% more than the first." It is also absent
  from the Pricing Reference, which presents itself as comprehensive.
- **Select 300K reset** is listed as "Not available", which is consistent, but the 300K is
  also absent from the 50% Consistency Add-on pricing table while being marked "Not
  available" there too — consistent, but the 300K is then never given an add-on status in
  the Select Evaluation article.
- **Select Flex payout caps with the 50% Consistency Add-on omit the 25K row.** Caps are
  given for 50K ($2,000), 100K ($3,000) and 150K ($4,000). The add-on is sold on the 25K
  (priced at $135 in the pricing table), so a 25K add-on cap should exist.

**Commissions**

Four supported products are listed in the fee schedule as **"Not listed in fee schedule"**:
NKD (Nikkei 225), FVS (VSTOXX), FXXP (STOXX Europe 600) and FGBX (Euro-Buxl). These are
tradable products with no published commission.

EUREX commissions are quoted in EUR while accounts are denominated in USD. The products
article confirms EUREX contracts are "traded in euros but settled in USD" but gives no
conversion rate, timing or spread.

**Tables with missing rows**

- The Growth payout article's **pre-September-12-2025 minimum balance table omits the
  $25,000 row** (it covers 50K, 100K, 150K only).
- The Growth **legacy payout tier table omits the $25,000 column** for the same reason.

**Undefined terms**

- **"V1" and "V2"** are used throughout the Select Flex and Daily article to distinguish
  two versions of the 300K ($5,100 vs $6,100 buffer, $3,500 vs $4,000 daily cap). The 300K
  article documents V2 only and never defines V1 or says who holds one.
- **"The new dashboard launch"** is used as a parameter cutoff in at least four places —
  Select 50K profit target ($2,500 vs $3,000), Lightning 150K risk parameters, Lightning
  general parameters, and the Lightning article's opening warning — with **no date given**.
- **"Before March 31st"** is given as the cutoff for the $3,750 Lightning 150K DLL, with
  no year.

**Missing entirely**

- The entire Elite Live stage (see section 2).
- Tax treatment beyond "Rise sends the 1099".
- Any U.S. state restrictions.
- Minimum age.

---

## 5. Ambiguities worth resolving before a tradeoff

- **Three different Lightning 150K parameter sets exist.** Current: DLL $3,000, drawdown
  $5,250. Pre-dashboard-launch: DLL $3,750, drawdown $6,000. Pre-March-31st: DLL $3,750.
  Which applies to a purchase made today is clear (current), but the overlap makes the
  article hard to read without error.
- **Growth minimum balances follow no stated formula.** $26,500 / $53,000 / $104,500 /
  $156,500 are presented as a table with no derivation. They are neither 6% of account size
  nor drawdown-plus-buffer, unlike every other threshold in the Tradeify documentation.
  Worth confirming they are current.
- **Scaling triggers are labelled "Equity" but mean "profit".** The Select scaling table
  headers read "Scaling Trigger 1 ($1,500 Equity)"; the worked examples clarify this means
  $1,500 of profit, i.e. a $51,500 balance on a 50K account.
- **Growth Funded payout requirement is labelled "Minimum Trading Days"** but specifies
  only a count of *profitable* days (5 days above $100/$150/$200/$250). No total trading
  day requirement is given.
- **The date boundary of September 1, 2026 is written two ways.** The payout policy article
  says caps apply to accounts purchased "**after** Sep 1st, 2026" and separately lists caps
  for accounts purchased "**before** Sep 1st, 2026", leaving September 1 itself unassigned.
  The Select Evaluation article resolves it as "on or after September 1, 2026".

---

## 6. Structural points that are correct but change the economics

These are not errors. They are consequences of the documented rules that are easy to miss
and that materially affect a comparison.

- **The drawdown is end-of-day for *updating* but real-time for *enforcement*.** The floor
  only moves up at the close, but it is checked continuously against net liquidation value
  including unrealised P&L. Touching it intraday fails the account permanently even if the
  day closes green. This is stated repeatedly and unambiguously, and it is stricter than
  "end-of-day drawdown" normally implies.
- **The dashboard drawdown figure updates once per day.** Every other metric is real-time.
  Real-time drawdown distance must be read from the platform (Tradovate "Dis Drawdown Net
  Liq" or NinjaTrader "Trailing Max Drawdown" column).
- **Evaluation profit does not carry over.** A funded account always starts at its base
  size regardless of where the evaluation ended.
- **Current Growth accounts are permanently capped per payout.** Payouts after the fourth
  stay at the fourth tier ($1,000 / $3,000 / $4,000 / $5,000). Pre-September-2025 accounts
  uncapped at payout 7 up to $25,000. The current structure has no uncapping mechanism.
- **Lightning profit goals are several times the payout caps.** A $150K Lightning account
  needs $9,000 of profit to unlock Payout 1, which is capped at $3,000.
- **The move to Elite Live is a one-way door that Tradeify controls.** "Tradeify reserves
  the right to move you to a Live Funded Account at any time after a successful payout",
  combined with "If your application for a Live Account is denied, you will not be
  permitted to return to the Simulated stage" and "you cannot have Sim and Live accounts
  active simultaneously".
- **The microscalping rule is a payout gate, not a breach.** On funded accounts only, over
  50% of trades *and* over 50% of profit must come from trades held longer than 10 seconds.
  Failing it blocks payout requests without failing the account.
- **Hedging detection is automated and cross-account.** The automatic breach requires all
  three of: opposing positions, held over 10 seconds, with over $150 of profit from the
  hedge. Cross-account and correlated-product hedging is reviewed manually instead, with no
  stated thresholds.
- **Brokers cannot be switched.** L2 and EUREX data are Tradovate-only, and moving to
  Tradovate requires buying a new account. No refunds on this basis.

---

## 7. Verified figures

### Pricing

| Account | Price | Reset |
|---|---|---|
| Growth 25K | $99 | $60 |
| Growth 50K | $145 | $95 |
| Growth 100K | $255 | $169 |
| Growth 150K | $369 | $229 |
| Select 25K (40%) | $109 | $75 |
| Select 50K (40%) | $165 | $109 |
| Select 100K (40%) | $265 | $169 |
| Select 150K (40%) | $369 | $239 |
| Select 300K | $570 | not available |
| Select 25K (50% add-on) | $135 | $90 |
| Select 50K (50% add-on) | $205 | $145 |
| Select 100K (50% add-on) | $329 | $230 |
| Select 150K (50% add-on) | $459 | $319 |
| Lightning 25K | $345 | not available |
| Lightning 50K | $492 | not available |
| Lightning 100K | $660 | not available |
| Lightning 150K | $796 | not available |

One-time purchases, no subscriptions, no activation fees. 5-account bundle gives 5% off
and stacks with promo codes, on Growth 25K/50K and Select 25K/50K only. All sales final.
The worked bundle example checks out: 5 × $109 = $545, less 5% = $517.75, less a 40% promo
= $310.65.

### Evaluation parameters

| Account | Profit target | Max drawdown (Growth) | Max drawdown (Select) | Growth DLL | Select DLL | Max size |
|---|---|---|---|---|---|---|
| $25K | $1,500 | $1,000 | $1,000 | $600 | None | 1 mini / 10 micro |
| $50K | $3,000 | $2,000 | $2,000 | $1,250 | None | 4 mini / 40 micro |
| $100K | $6,000 | $3,500 | $3,000 | $2,500 | None | 8 mini / 80 micro |
| $150K | $9,000 | $5,000 | $4,500 | $3,750 | None | 12 mini / 120 micro |
| $300K (Select) | $14,000 | — | $8,000 | — | $4,000 (see contradiction 2) | 16 mini / 160 micro |

Growth: 1 trading day minimum, no consistency rule. Select: 3 trading days minimum due to
40% consistency, or 2 days with the 50% add-on. No time limit on either.

### Drawdown lock trigger balances (funded accounts)

| Account | Growth | Lightning | Select Flex | Select Daily |
|---|---|---|---|---|
| 25K | $26,100 | $26,100 | $26,100 | $26,100 |
| 50K | $52,100 | $52,100 | $52,100 | $52,100 |
| 100K | $103,600 | $104,100 | $103,100 | $102,600 |
| 150K | $155,100 | $155,350 | $154,600 | $153,600 |

Each equals starting balance + that product's drawdown + $100. After locking, the floor is
fixed at starting balance + $100 and never moves again. Locking also triggers immediately
on a payout request, whichever comes first. Drawdown never locks on evaluation accounts.

### Funded drawdowns and daily loss limits

| Account | Growth DD / DLL | Lightning DD / DLL | Select Flex DD / DLL | Select Daily DD / DLL |
|---|---|---|---|---|
| 25K | $1,000 / $600 | $1,000 / none | $1,000 / none | $1,000 / $500 |
| 50K | $2,000 / $1,250 | $2,000 / $1,250 | $2,000 / none | $2,000 / $1,000 |
| 100K | $3,500 / $2,500 | $4,000 / $2,500 | $3,000 / none | $2,500 / $1,250 |
| 150K | $5,000 / $3,750 | $5,250 / $3,000 | $4,500 / none | $3,500 / $1,750 |

At 6% profit the DLL rises to equal the drawdown amount, effective the next session. On
pre-September-12-2025 accounts it is removed entirely at that point instead.

### Payout rules by product

| | Growth | Lightning | Select Flex | Select Daily |
|---|---|---|---|---|
| Consistency | 35% | 20% → 25% → 30% | none | none |
| Frequency gate | 5 days above $100/$150/$200/$250 | none | 5 winning days | daily |
| Balance gate | $26,500 / $53,000 / $104,500 / $156,500 | profit goal | none | buffer $1,100 / $2,100 / $2,600 / $3,600 |
| Minimum payout | $250 / $500 / $1,000 / $1,500 | $1,000 | $250 | $250 |
| Formula | capped amount | capped amount | 50% of total profit | 2× cycle profit |

Select Flex caps (purchased on or after Sep 1, 2026): $1,250 / $2,500 / $3,500 / $4,500.
Before that date: $1,250 / $3,000 / $4,000 / $5,000. 300K Flex: $10,000.

Select Daily caps (on or after Sep 1, 2026): $600 / $1,250 / $1,750 / $2,500. Before:
$600 / $1,000 / $1,500 / $2,500. 300K Daily: $4,000 with a 50% new-profit requirement.

Growth caps by payout number: 25K flat $1,000; 50K $1,500 / $2,000 / $2,500 / $3,000;
100K $2,000 / $2,500 / $3,000 / $4,000; 150K $2,500 / $3,000 / $4,000 / $5,000.

Lightning caps: 25K flat $1,000; 50K $2,000 for payouts 1-3 then $2,500; 100K $2,500 then
$3,000; 150K $3,000 then $3,500. Profit goals: Payout 1 $1,500 / $3,000 / $6,000 / $9,000,
Payout 2+ $1,000 / $2,000 / $3,500 / $4,500, resetting each cycle with no carry-over.

### Commissions (round trip, per contract)

ES, NQ, YM, RTY $5.76. EMD $5.66. MES, MNQ $1.82. CL $5.98. GC $6.20. Currencies $6.20
except 6S at $10.20. Lean Hogs $9.20, Live Cattle $11.20, Feeder Cattle $7.20. EUREX
priced in EUR: FDAX €5.94, FDXM €3.72, FESX €4.12, FDXS €1.42, FSXE €1.34, FGBS €7.70,
FGBM €5.70, FGBL €3.70.

Ten micros cost roughly three times one mini in commission ($18.20 vs $5.76 on the S&P).

### Mechanics confirmed across documents

- **Profit split 90/10 on all simulated funded accounts, 80/20 on Elite Live.**
- **Max 5 simulated funded accounts, per person and per household**, in any mix of Growth,
  Select and Lightning, with at most 3 of them being Select 300K.
- **Evaluation purchase limits**: Growth unlimited, Select 15 per rolling 30 days, Select
  300K 5 per rolling 30 days and excluded from the 15. Each Select evaluation can be reset
  up to 10 times per 30 days. Passed evaluations can be banked until a funded slot opens.
- **Flat by 4:45 PM ET**, 12:59 PM ET on holiday half-days. Positions left open are closed
  automatically without failing the account. No overnight, weekend or swing trading on any
  account type including Live.
- **A trading day is one trade placed between 6:00 PM ET and the next close.** Trades at
  10:00 AM and 7:00 PM on the same calendar day count as two trading days.
- **One trade per week minimum** on every evaluation and funded account, or it is closed
  after an email warning.
- **News trading is unrestricted** on all account types.
- **DCA, martingale, flipping, scalping, algorithmic trading and trade copying are all
  permitted.** Algorithms must be exclusively owned and provable on request; HFT bots are
  prohibited.
- **Hedging is prohibited within and across accounts**, by Product Group (Equity Index,
  Energy, Metals, Currencies, Interest Rates, Grains, Livestock, Volatility). Minis and
  micros may be held together in the same direction at 10 micros = 1 mini. Long Equity
  Index plus long Volatility counts as offsetting.
- **48 supported root symbols** across CME, CBOT, COMEX, NYMEX and EUREX. EUREX is
  Tradovate-only. No crypto, stocks, forex, options or single stock futures. Micro Silver
  (SIL) is explicitly not supported; MGC is the only supported micro metal.
- **Level 1 CME data is free on all brokers** provided the Non-Professional Agreement is
  signed; failure to sign risks a $300/month professional fee. L2 and EUREX are paid
  Tradovate-only add-ons billed by Tradovate.
- **Payouts** are processed within 24 hours of approval, up to 72 hours over a weekend or
  outside Mon-Fri 8:00 AM - 5:00 PM ET. Rise is primary (ACH or crypto), Plane is the
  fallback with up to 7 days. No PayPal. Rise issues the 1099. Only one payout request can
  be open per account at a time.
- **Elite Live eligibility**: 3 payouts on a single account, or 10 total payouts since the
  last live transition. These are minimum thresholds for consideration, not automatic
  qualification.
- **Restricted countries: 65**, listed by name. The alphabetical list matches the stated
  count. Based on residency, not travel location.
- **All sales final**, no refunds. Chargebacks freeze all accounts and trigger a permanent
  ban. Only the trader's own card may be used.

---

## 8. Files with no decision-relevant content

`TradingPlatforms_n_products.md`, `tradovate.md`, `rithmic.md` and `wealthCarts.md` are
platform setup, configuration and troubleshooting guides. They contain nothing that bears
on a funding tradeoff beyond what is already in the pricing and rules articles. The one
useful item buried in them is the Drawdown Widget reference in `tradovate.md`, which
matters because the dashboard drawdown figure is only updated daily.

Note the filename `wealthCarts.md` is misspelled, and the folder is named `Tradify` while
the firm is `Tradeify`.

---

## 9. Next steps

1. Obtain the Tradeify Elite Program article. It governs the live stage, the 80/20 split
   and the one-way transition, and is the single largest gap.
2. Obtain the Funded Reset price for Select 50K, 100K and 150K.
3. Confirm the Select 25K evaluation contract limit: 1 mini or 2 minis.
4. Confirm whether the Select 300K evaluation really has a $4,000 daily loss limit when no
   other Select evaluation has one.
5. Confirm what activation looks like on Rithmic and WealthCharts if instant activation is
   Tradovate-only.
6. Get the date of "the new dashboard launch" so legacy parameters can be ruled out.
7. Obtain commissions for NKD, FVS, FXXP and FGBX, or treat them as untradeable.
8. Obtain the Select Flex 25K payout cap under the 50% consistency add-on.
