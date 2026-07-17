# Week 11 — Review & Refine

> **◀ Previous:** [Week 10 — Psychology & Your Trading Plan](./week-10-psychology-and-plan.md) &nbsp;|&nbsp; **Course Home:** [Lessons Index](./README.md) &nbsp;|&nbsp; **Next ▶:** [Week 12 — Go Live: Small & Real](./week-12-go-live.md)

> ⚠️ **Educational content only — not financial advice.** Nothing in this lesson is a trade recommendation or suggestion. All examples and numbers are illustrative and hypothetical. Always consult a registered financial advisor before trading or investing. Trade and invest at your own risk — no responsibility is accepted for any loss, damage, or incorrect/invalid trades.

_This week you stop hunting new setups and become a forensic auditor of your own trading, turning ten weeks of journal entries into a small, evidence-based edge and a process you can repeat under pressure._

## Why This Week Matters

For ten weeks you have been adding: candlestick anatomy, supply and demand zones, EMAs and VWAP, the opening-range breakout, position sizing, a written plan. That was the accumulation phase. Week 11 is the opposite discipline — **subtraction**. The single most valuable move a developing trader makes is not learning one more pattern; it is discovering which of the patterns they already trade actually make money, and deleting the rest.

Here is the deeper reason this matters. Every setup you trade is a small bet that a certain kind of situation — a certain arrangement of buyers and sellers in the order book — resolves in your favour more often than random, or resolves bigger when it wins. You _believe_ each of your setups has this property. But belief is cheap. Your journal is the only place where that belief gets tested against reality. When you segment ten weeks of trades, you almost always find the same thing: your total profit came from one or two setups in one or two hours of the day, and everything else was noise that ranged from break-even to quietly destructive. You were, without knowing it, running a profitable business and an unprofitable business at the same time, out of the same account.

The goal of the whole course now changes shape. Until Week 10 the target was "learn the tools." From here the target is **a consistent process, executed with discipline, whose expectancy is positive**. Profit is downstream of process. If you aim at profit directly you will chase, revenge-trade, and over-size. If you aim at process, profit arrives as a by-product. Week 11 is where you define that process using data instead of hope — so that in Week 12, when you go live, you are executing a measured edge, not a feeling.

## Concept 1 — Why the Journal *Is* the Edge

A beginner thinks an edge lives in a chart pattern. It does not. An edge lives in the _statistics of your own execution_ of that pattern. Two traders can take the identical opening-range breakout on Bank Nifty and one makes money over a year while the other loses — same setup, different entries, exits, sizing, and discipline. The edge is the whole behaviour, and the only record of the whole behaviour is the journal.

### What "edge" actually means mechanically

When you take a demand-zone bounce on Reliance, you are betting that at a price level where large buyers previously absorbed all the selling, they will step in again before sellers can push price lower. If they do, price lifts and your stop below the zone is never hit. The setup "works" when that institutional demand is real and still present. Your journal, over 30 or 40 trades, measures how often that bet paid and how much it paid versus how much it cost when it failed. That measured ratio — not the theory behind the zone — is your edge.

So the journal is not admin. It is the instrument that _detects_ the edge, the way a thermometer detects a fever. Without it you are guessing. With it you can say, in numbers, "this specific bet, in this specific window, has paid me positively across a real sample." That sentence is the whole game.

### The minimum columns for every trade

Rebuild your journal (spreadsheet, not notebook — you cannot sort a notebook) with at least these fields:

- **Date & weekday** (Mon–Fri) — for day-of-week and time analysis.
- **Instrument** — Nifty, Bank Nifty, Reliance, HDFC Bank, ICICI Bank, SBIN, Infosys.
- **Direction** — Long or Short.
- **Setup name** — one of a _fixed, small list_ ("ORB", "demand-bounce", "VWAP-reclaim"). No free text.
- **Entry time window** — 9:15–9:45, 9:45–11:00, 11:00–13:00, 13:00–15:20 IST.
- **Result in R** (defined next).
- **Rules followed? Y/N** — the honesty column.
- **One-line note** — what you saw, and if you broke a rule, *why*.

## Concept 2 — Score in R, Not Rupees

You cannot compare a 12-point Nifty scalp to a 250-point Bank Nifty swing in rupees — the instruments move on different scales. So you normalise everything to **R**.

**1R = the amount you risked on that trade**, i.e. the distance from your entry to your initial stop-loss, expressed in money. If you entered Bank Nifty and your stop was ₹1,500 away in account terms, then 1R = ₹1,500 *for that trade*. A trade that made ₹3,000 is +2R. A trade that hit its stop is −1R. A trade you bailed early for a small gain is +0.4R.

The power of R is that it makes every trade the same "size" for analysis, no matter the instrument or the day's volatility. It also forces you to record your stop *before* you know the outcome, which quietly enforces the discipline of always having a stop.

```
Caption: One trade measured in R (Bank Nifty long, hypothetical)

   Price
    ^
    |                                  ┌──── TARGET  +2R  (₹3,000)
    |                                 /
    |            ENTRY ●─────────────/
    |          (48,200)              |
    |                                | 1R = ₹1,500 = 40 pts risk
    |            STOP  ○─────────────┘
    |          (48,160)
    +---------------------------------------------> time
     Outcome recorded as a multiple of that 1R, never as raw ₹.
```

## Concept 3 — The Six Metrics That Matter (and How to Compute Them)

You do not need fancy analytics. Six numbers, computed from the R column, tell you almost everything.

### 1. Win rate

`Win rate = winning trades ÷ total trades`. How *often* you win. On its own it means little — a 40% win rate can be highly profitable and an 80% win rate can lose money. Never optimise for this number alone; it is the classic beginner trap.

### 2. Average R won and average R lost

Average of the R values of your winners, and (separately) of your losers. This is how *big* you win versus how *big* you lose. If your average winner is +2.4R and your average loser is −1.0R, your winners are more than twice your losers — the sign of good exits and honoured stops.

### 3. Expectancy — the one number that tells the truth

Expectancy blends "how often" and "how big" into your **average profit per trade, in R**:

```
Expectancy (R) = (Win% × Avg Win R) − (Loss% × Avg Loss R)
```

If expectancy is positive, every time you take a trade you are, on average, adding money — even though any single trade is uncertain. This is the number you protect. A casino does not win every spin; it wins because expectancy per spin is tilted its way and it spins many times. You are the casino only if your expectancy is positive and you take enough trades to let it express.

### 4. Profit factor (the concept)

`Profit factor = total R won ÷ total R lost` (using absolute value of losses). It answers: for every ₹1 I lost, how many ₹ did I make? A profit factor of 1.0 is break-even. Above ~1.5 is healthy for a beginner. It is a fast gut-check that agrees with expectancy but is easier to eyeball.

### 5. Maximum drawdown

The largest peak-to-trough drop in your running R total. If your equity curve climbed to +14R, then sagged to +6R before recovering, your max drawdown was **8R**. This measures pain, not profit — it tells you the worst losing stretch you have to be able to sit through without abandoning the plan. A strategy with great expectancy but a 20R drawdown may be psychologically un-tradeable for you.

### 6. Rule-adherence %

`Rule-adherence = trades where Rules-followed = Y ÷ total trades`. The most honest mirror in trading. Discipline is not a feeling; it is a percentage. Beginners routinely find their rule-break trades hold their largest losses. Adherence turns "be disciplined" into a measurable target you can raise week over week.

## Concept 4 — Segment to Find Where the Edge *Really* Lives

A single blended expectancy hides the truth. Your job is to slice the same 30–40 trades along four axes and find the pockets where your money was actually made.

### By setup

Total the R for each named setup. It is normal to find one setup is +11R and another is −5R. The −5R setup is not "unlucky" — it is a business you should close.

### By time-of-day

Sum R by entry window. The 9:15–9:45 open is violent: spreads are wide, the order book is thin, and price whips as overnight orders clear. Many beginners bleed here. The 9:45–11:00 window is often calmer and trend-friendlier. You are looking for the hour where *your* setups resolve cleanly.

```
Caption: Performance by hour of day — total R per entry window
         (hypothetical 30-trade sample)

  +R
  8 |                        ████
  6 |                        ████
  4 |                        ████        ████
  2 |            ████        ████        ████
  0 |──────────  ████  ────  ████  ────  ████  ──────
 -2 |   ▓▓▓▓     ████        ████        ████
 -4 |   ▓▓▓▓
    +----------+---------+---------+---------+--------
      9:15-9:45 9:45-11:00 11:00-13:00 13:00-15:20
        -4R       +3R        +8R         +4R
      (chop, avoid)         (your edge lives here)
```

### By instrument

Bank Nifty moves faster and wider than Nifty; single stocks like SBIN or Infosys respond to their own news. You may find your reading of Bank Nifty is sharp and your stock trades are random. Concentrate where you are demonstrably good.

### By direction (long vs short)

Very common asymmetry: beginners are better on the long side because rising markets feel intuitive, while shorts require selling something you don't own into strength, which feels unnatural and is often mistimed. If your shorts are −6R and longs are +9R, that is a data-driven instruction: trade long-only until your short data improves.

```
Caption: Performance-by-setup table (hypothetical 30 trades)

 Setup           Trades  Win%   Avg+R  Avg−R  TotalR  Verdict
 --------------  ------  -----  -----  -----  ------  --------
 ORB (9:45-11)      10    50%   +2.4   -1.0   +7.0    KEEP ✓
 Demand-bounce       8    50%   +2.2   -1.0   +4.8    KEEP ✓
 VWAP-reclaim        6    33%   +1.8   -1.0   -0.4    WATCH
 Gut-feel breakout   6    17%   +1.5   -1.4   -5.6    CUT ✗
 --------------  ------  -----  -----  -----  ------  --------
 TOTAL              30    40%   +2.2   -1.1   +5.8
```

## Concept 5 — Cutting Losers and Scaling Winners *Without* Curve-Fitting

Here is the trap that ruins the review. You slice your data so finely that you "discover" an edge that is really just noise. You find that all four of your Tuesday Bank Nifty longs entered between 10:03 and 10:18 won, and you conclude "my edge is Tuesday Bank Nifty longs at 10:10 AM." That is **curve-fitting**: sculpting a rule to fit a handful of past data points that will not repeat. Four trades is not evidence; it is an anecdote.

### The sample-size discipline

Trust segments only when the sub-sample is large enough to mean something. Rough beginner guidance:

- **Fewer than ~5 trades in a bucket:** ignore entirely. No conclusion.
- **~5–10 trades:** a hint. Note it, keep collecting, do not restructure your plan around it.
- **~20+ trades:** worth acting on, and even then hold it loosely.

Cut a setup only when it is *both* negative *and* backed by enough trades, or when it is negative *and* every losing trade shows a rule break (that's an execution problem, not an edge problem — fixable, don't delete the setup yet).

### Scale winners the boring way

"Scaling a winner" does not mean betting 5% on your best setup tomorrow. It means, over time and only once the sample is convincing, allowing your strongest setup a slightly larger share of your risk budget — for example moving your best setup from 1% to 1.5% risk while keeping everything ≤2%. You never abandon the per-trade risk cap, the mandatory stop-loss, or the ≥1:2 reward-to-risk floor. Scaling is a gentle tilt toward proven strength, not a licence to gamble.

The safest, most honest "refinement" is almost always **removing** trades (drop the CUT setup, avoid the 9:15–9:45 window) rather than **adding** cleverness. Removing your worst bucket mechanically raises your overall expectancy without any curve-fitting risk at all.

## Concept 6 — Consistency of Process Is the Real Week-11 Goal

It is tempting to define success this week as "I found I'm profitable." But your paper sample is small and one good run can flatter you. The durable goal is narrower and tougher: **a written process you can execute the same way every day**, whose expectancy is positive on the trades where you actually followed it.

That last clause is everything. Compute expectancy twice — once on all trades, once on rules-followed-only trades. The gap between them is the price of your indiscipline. If all-trades expectancy is +0.25R and rules-followed expectancy is +0.70R, then your edge is real and your enemy is *you*, not the market. That is fixable in Week 12 by simply doing what you already know you should. Consistency means shrinking that gap toward zero.

## Worked Examples

> All numbers below are **hypothetical and illustrative**, chosen to show the method. Your own journal numbers are the only ones that matter. This is education, not a prediction or a promise of profit.

### Example 1 — A Full 30-Trade Review, Start to Finish

Assume paper capital of ₹1,00,000 and a base risk of 1% (so 1R ≈ ₹1,000). Over Weeks 5–10 you logged 30 trades. After tabulating the R column and summing, you get the setup table shown earlier: total **+5.8R** across 30 trades.

**Step 1 — Blended metrics.**

- Win rate = 12 wins ÷ 30 = **40%** (loss rate 60%).
- Avg win = **+2.2R**, avg loss = **−1.1R**.
- Expectancy = (0.40 × 2.2) − (0.60 × 1.1) = 0.88 − 0.66 = **+0.22R per trade**.
- Total won = 12 × 2.2 = 26.4R; total lost = 18 × 1.1 = 19.8R. Profit factor = 26.4 ÷ 19.8 = **1.33**.

So you are net positive, but thinly. +0.22R per trade is a real but fragile edge.

**Step 2 — Segment.** The table exposes the culprit: "Gut-feel breakout" is **−5.6R** across 6 trades with a 17% win rate. That single setup is dragging the whole account. "VWAP-reclaim" is roughly break-even (−0.4R over 6). ORB and demand-bounce are both clearly positive (+7.0R and +4.8R).

**Step 3 — Cut, honestly.** The gut-feel setup is negative *and* — checking notes — 5 of its 6 trades were marked "Rules followed = N" (chased entries, no defined stop). That is both a bad edge and an execution problem. Cut it. VWAP-reclaim is only 6 trades and near zero: not enough data to keep *or* condemn, so mark it WATCH and keep collecting — do not build the plan around it.

**Step 4 — Recompute on the survivors (ORB + demand-bounce only, 18 trades).**

- Wins = 9, losses = 9 → win rate **50%**.
- Total R = +7.0 + 4.8 = **+11.8R** over 18 trades.
- Expectancy = 11.8 ÷ 18 = **+0.66R per trade** — three times the blended figure.

Simply *removing your worst business* nearly tripled your expected profit per trade, with zero curve-fitting. That is the entire lesson of Week 11 in one number.

**Step 5 — Rule adherence.** Across all 30 trades, 9 were "N" → adherence = 21/30 = **70%**, break rate 30%. Those 9 rule-breaks totalled −8.9R. Your disciplined self is dramatically more profitable than your impulsive self.

### Example 2 — Reading the Equity Curve and Its Drawdown

Take the ORB-plus-demand-bounce survivor set and plot the running R total trade by trade. An **equity curve** is just your cumulative R after each closed trade; it is the single best picture of whether a process is healthy.

```
Caption: Equity curve (cumulative R) with drawdown annotated
         18 surviving trades, hypothetical

 cumR
 +12 |                                        ●────●  peak +11.8
 +10 |                                   ●───/
  +8 |                    ●──●      ●───/   ▲
  +6 |               ●───/    \    /        │ recovery
  +4 |          ●───/          \  /         │
  +2 |     ●───/            ●───\/  ◄ trough │ MAX DRAWDOWN
   0 |●───/                 -0.8 below +6.something
     +----+----+----+----+----+----+----+----+----> trades
      1    3    5    7    9   11   13   15   17

 Peak before dip ≈ +7.6R ; trough ≈ +4.2R  =>  max drawdown ≈ 3.4R
```

Read it like this. The curve rises overall (good — positive expectancy is doing its job). Around trades 9–11 it drops from about +7.6R to about +4.2R — a losing cluster of roughly **3.4R drawdown**. That is your worst stretch. The practical question is: could you have kept trading your plan, unchanged, through those three red trades without panicking, widening stops, or quitting? In money that dip is about ₹3,400 on a ₹1,00,000 account — survivable and well within a sane daily-loss framework. Knowing your historical drawdown in advance is what lets you sit calmly through the next one instead of abandoning a winning process at its low point, which is exactly when beginners quit.

## Common Mistakes (and the fix)

**1. Worshipping win rate.** Beginners tune everything to win more often and feel good, taking tiny profits to lock in a "W." *Why they do it:* winning feels like being right, and being right is emotionally rewarding. *Fix:* optimise expectancy, not win rate. A 40% win rate with +2.2R winners beats a 70% win rate with +0.3R winners. Let winners run to target.

**2. Curve-fitting to a tiny sample.** Finding that "my three Wednesday Nifty shorts all won" and rebuilding the plan around Wednesdays. *Why:* the brain sees patterns in noise and craves a secret. *Fix:* require ~20+ trades before trusting a segment; treat 5–10 as a hint only; below 5, ignore.

**3. Reviewing in rupees, not R.** Concluding Bank Nifty is "better" because it made more ₹, when it simply moves in bigger points. *Why:* rupees are what we feel. *Fix:* normalise everything to R so a Nifty scalp and a Bank Nifty swing are directly comparable.

**4. Skipping the rule-adherence column, or lying in it.** Marking "Y" on a trade you know you fudged. *Why:* honesty about indiscipline stings. *Fix:* the "N" trades are the most valuable rows you own — they show exactly where your money leaks. Score them ruthlessly; the mirror only helps if it's clean.

**5. Adding instead of subtracting.** Responding to a mediocre review by learning a new indicator or setup. *Why:* adding feels productive; cutting feels like loss. *Fix:* the highest-return action is almost always deleting your worst setup and worst hour, not bolting on complexity.

## Nuances & Edge Cases

- **Paper-trading flatters you.** Real fills slip, real spreads cost, and real emotions bite harder with money on the line. Your Week 12 live expectancy will likely be *lower* than your paper expectancy. Bank a margin of safety — a paper edge of +0.05R is not enough to survive the translation to live.
- **Small samples lie in both directions.** Just as a bad setup can look good over 5 lucky trades, a genuinely good setup can look bad over 5 unlucky ones. Do not delete a well-reasoned setup on a handful of losses if the losses obeyed your stop; that may just be normal variance within its drawdown.
- **Costs are not yet in your numbers.** Real trading carries brokerage, STT, exchange fees, and GST. A setup that is +0.15R gross might be break-even or negative net. In later weeks you fold costs into R; for now, know that a razor-thin edge probably isn't one.
- **Regime change.** An ORB edge measured in a trending stretch of the market may weaken in a choppy, range-bound month. Your edge is conditional on market conditions you don't fully control, which is why you keep journaling forever, not just this week.
- **MIS auto square-off distorts late trades.** Intraday (MIS) positions are auto-squared by your broker around ~3:20 PM IST. Trades entered near the close may have been exited by the system, not by your plan — flag those so they don't pollute your exit statistics.

## Day-by-Day (Mon–Fri)

- **Monday — Build clean data.** Copy every Week 5–10 trade into a spreadsheet with all the columns above. Convert each result to R. Add and fill the "Rules followed Y/N" column honestly. Do *no* analysis yet — today is data hygiene only. *Observation target:* how many total trades you actually have, and your rule-break count.
- **Tuesday — Segment.** Build the by-setup and by-time-of-day tables and sum R for each. Identify your single best setup, best hour, best instrument, and best direction — and the worst of each. *Observation target:* which one bucket holds most of your losses.
- **Wednesday — Compute the six metrics.** Win rate, avg win R, avg loss R, expectancy, profit factor, max drawdown, and rule-adherence %. Plot a simple cumulative-R equity curve by hand or in the sheet. *Observation target:* the size of your largest drawdown, in R and in ₹.
- **Thursday — The discipline gap.** Recompute expectancy twice: all trades vs rules-followed-only. Read every "N" note and write one sentence on the emotion behind each break (boredom, FOMO, revenge, fear). *Observation target:* the gap between your two expectancy numbers.
- **Friday — Trading Plan v2 + live rehearsal.** Write a one-page plan naming your one or two KEEP setups, best window, instrument(s), and direction, with risk ≤2% per trade, reward:risk ≥1:2, mandatory stop, and daily loss limit. Then watch the live market in your chosen window (9:45–11:00 IST) and *mark* — do not trade — each time your KEEP setup appears. *Observation target:* how often your setup genuinely triggers in one clean session.

## Key Takeaways

- Your edge does not live in a chart pattern — it lives in the measured statistics of your own execution, and the journal is the only instrument that detects it.
- **Expectancy per trade** is the one metric that fuses how often *and* how big you win; keep it positive and let it compound over many trades. Win rate alone is a trap.
- Segment by setup, hour, instrument, and direction — your profit almost always hides in one or two pockets while everything else is noise or leakage.
- Cut losers by *subtraction*, and demand a real sample (~20+ trades) before trusting any segment, so you refine your edge instead of curve-fitting to luck.
- The gap between your all-trades expectancy and your rules-followed expectancy is the exact, measurable cost of your indiscipline — and it is the most fixable thing you own.
- The true goal this week is a consistent, written process with positive expectancy on the trades you actually followed — profit is the by-product, never the target.

## This Week's Milestone

You have a one-page **Trading Plan v2** built entirely from your own data: it names your KEEP setup(s), best time window, instrument, and direction; it shows your six computed metrics; and it proves a *positive expectancy on your rules-followed trades* with a known, survivable maximum drawdown — leaving you ready to execute a measured edge, not a feeling, when you go live in Week 12.

---

> **◀ Previous:** [Week 10 — Psychology & Your Trading Plan](./week-10-psychology-and-plan.md) &nbsp;|&nbsp; **Course Home:** [Lessons Index](./README.md) &nbsp;|&nbsp; **Next ▶:** [Week 12 — Go Live: Small & Real](./week-12-go-live.md)
