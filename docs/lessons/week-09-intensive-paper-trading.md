# Week 9 — Intensive Paper Trading

> **◀ Previous:** [Week 8 — Risk & Position Sizing](./week-08-risk-and-position-sizing.md) &nbsp;|&nbsp; **Course Home:** [Lessons Index](./README.md) &nbsp;|&nbsp; **Next ▶:** [Week 10 — Psychology & Your Trading Plan](./week-10-psychology-and-plan.md)

*Goal: Build a real sample of paper trades, add a disciplined second setup, and learn to judge your trading by expectancy and process rather than by any single win or loss.*

## Why This Week Matters

By now you can read a candle, mark a level, size a position, and place a stop. You have one setup you understand — a breakout or pullback you learned in earlier weeks. That is a foundation, not a business. A trading method only proves itself over *many* trades, because any short run is dominated by luck. This week you stop treating each trade as a verdict on your skill and start treating your trading as a **statistical process** that produces a distribution of outcomes.

Intraday trading on the NSE is a game of small, repeated edges. The market opens at 9:15 AM and closes at 3:30 PM IST; intraday (MIS) positions are auto-squared-off by your broker around 3:20 PM if you have not already exited. Inside those six hours, a good trader might take one to three high-quality setups. Over a week that is maybe five to fifteen trades — still far too few to trust. The whole point of Week 9 is to grind out enough repetitions, under strict rules, that you can compute honest numbers about yourself: win rate, average win, average loss, and the single figure that ties them together — **expectancy**.

You will also add a **second setup** so your sample builds faster and you learn to handle two patterns without letting them blur into "I traded because something moved." And you will confront the emotional trap that ruins most beginners in week nine of their real journey: the urge to rip up a working method after three or four losses in a row.

Everything here is education using paper (simulated) money. No real capital until Week 12. Nothing below predicts prices or promises profit.

## Concept 1 — Sample Size: Why 1 or 5 Trades Tell You Nothing

Imagine a slightly biased coin that lands heads 55% of the time. If you flip it five times you could easily get one head or five heads. Nothing about those five flips reveals the 55% edge. You would need dozens or hundreds of flips before the observed frequency settles near the true 55%. Trades work the same way. Your setup has some *true* win rate you cannot see directly; each trade is one noisy flip.

### The mechanism: outcome vs. process

Every trade has two layers. The **process** is your decision — did the setup meet all your rules, was the stop placed correctly, was the size right? The **outcome** is what price did afterward. These are only loosely linked in the short run. A perfect-process trade can lose because a large seller happened to dump shares one minute after you entered. A rule-breaking gamble can win because the market lurched your way. Over one trade, outcome tells you almost nothing about process. Over 100 trades, outcomes start to reflect process, because luck averages out.

### Why beginners misread small samples

The market feels intensely personal, so a beginner reads two losses as "my method is broken" and two wins as "I've cracked it." Both conclusions are noise. A useful rule of thumb for a learner: **treat fewer than 20 trades as anecdote, 20–50 as a rough signal, and 100+ as something you can actually reason about.** This week you are trying to accumulate trades toward that first meaningful bucket — deliberately, not by over-trading.

```
Caption: Same 55%-edge method, three different 8-trade streaks.
Each streak is "true" but tells a totally different story.

Streak A:  W W L W W W L W    -> 6/8 = 75% "I'm a genius"
Streak B:  L L W L W L L W    -> 3/8 = 37% "My method is broken"
Streak C:  W L W L L W L W    -> 4/8 = 50% "Meh, coin flip?"

  All three came from the SAME 55% process.
  Short samples LIE. Only many trades reveal the edge.
```

## Concept 2 — Adding a Second Setup: The VWAP Bounce

A single setup fires only a few times a week. Adding a second, *different* setup lets you gather trades faster without lowering standards — provided the second one has rules as strict as the first. This week's addition is the **VWAP bounce**.

### What VWAP is and why institutions care

VWAP stands for **Volume-Weighted Average Price**. It is the average price at which the instrument has traded so far today, weighted by volume at each price. It resets every morning at 9:15. Because it reflects the *volume-weighted* consensus, large institutions use it as a benchmark: a fund buying a big block wants to accumulate *below* VWAP so its average fill beats the day's typical price. That behaviour is the mechanism behind the setup. When price on an uptrending day pulls back down to VWAP, institutional buy programs often step in around it, because buying at or under VWAP is "a good fill." Their buying can push price back up — a bounce.

### Strict rules for the VWAP bounce (long side)

1. **Context first.** Only take longs when the day is trending up: price is above a rising VWAP and making higher highs since the open. VWAP bounces fail badly in choppy, sideways sessions.
2. **The touch.** Wait for price to pull back *to* VWAP (or just touch it), not to be far above it.
3. **The trigger.** Enter only on a confirming candle — e.g., a 5-minute candle that touches VWAP and closes back *above* it with a real body, ideally on rising volume. No confirmation, no trade.
4. **Stop.** Just below the low of the confirmation candle (or a few points under VWAP). If price closes decisively below VWAP, the premise is dead — exit.
5. **Target.** The prior intraday high, or a fixed reward:risk of at least 1:2. (Mirror all of this for shorts on downtrending days below a falling VWAP.)

```
Caption: VWAP bounce (long). Price pulls back to a rising VWAP,
prints a confirmation candle, and resumes up.

 price
   |            prior high (target) - - - - - - - - o
   |         /\                                    /
   |        /  \        confirmation candle       /
   |       /    \      closes back above VWAP    /
   |      /      \       [#]                     /
   | .......\......\...[#]...................... VWAP (rising)
   |  ......  \    (touch)  ^ entry
   |             \         |  stop just below
   |              \________| candle low
   +-------------------------------------------------> time
        9:30      9:55        10:20
```

### Keeping the two setups from overlapping

The danger of two setups is that in the heat of the session you retro-fit whichever label makes a random move look tradeable. Prevent this with a hard rule: **before entry, you must name the setup out loud and it must satisfy that setup's full checklist — nothing borrowed from the other.** A breakout is a breakout only if it broke the level you pre-marked; a VWAP bounce is valid only with the VWAP touch *and* the confirmation candle. If a move could be "either," you skip it — ambiguity is a no-trade. In your journal, tag every trade with exactly one setup name. If you find trades tagged "both" or "kind of," that is a discipline leak, not a new pattern.

## Concept 3 — The Three Numbers: Win Rate, Average Win, Average Loss

To judge a method you need three statistics, and the smart way to express two of them is in **R**, your risk unit.

### R: the great equalizer

**R = the amount you risk on a trade** — the distance from entry to stop, times your position size, i.e. your planned loss if the stop hits. If you buy Reliance at ₹1,400 with a stop at ₹1,390, your risk per share is ₹10; if you hold 50 shares, 1R = ₹500. Expressing results in R instead of rupees lets you compare a small Reliance trade with a large Bank Nifty trade on the same scale. A trade that made twice your risk is +2R whether that was ₹1,000 or ₹10,000.

- **Win rate** = wins ÷ total trades (e.g., 8 wins in 20 = 40%).
- **Average win (avgWin)** = mean R gained on winning trades (e.g., +2.2R).
- **Average loss (avgLoss)** = mean R lost on losing trades (e.g., −1.0R; if you always exit at your stop it is −1.0R, but slippage and early exits make it realistic to measure).

Beginners obsess over win rate alone. Win rate without the average win and loss is meaningless: a 70% win rate that books tiny +0.3R wins and takes −2R losses is a losing method. The three numbers only make sense together — which is exactly what the next concept combines.

## Concept 4 — Expectancy: The One Number That Matters

**Expectancy** is the average profit or loss you can expect *per trade*, measured in R, once luck washes out. The formula:

```
Caption: The expectancy formula (all terms in R).

  E = (win% x avgWin) - (loss% x avgLoss)

    win%    = fraction of trades that win      (e.g. 0.40)
    loss%   = fraction that lose  = 1 - win%   (e.g. 0.60)
    avgWin  = average R gained on winners      (e.g. 2.2R)
    avgLoss = average R lost on losers         (e.g. 1.0R)
```

### Worked: a 40% win rate that still prints money

Plug in a 40% win rate, average win of +2.2R, average loss of 1.0R:

```
Caption: Expectancy worked, showing 40% wins can be profitable.

  E = (0.40 x 2.2) - (0.60 x 1.0)
    = 0.88        -  0.60
    = +0.28 R  per trade
```

Positive expectancy of **+0.28R per trade** means that, on average, every trade you take is *worth* about a quarter of your risk unit — even though you lose 60% of the time. Over 100 trades, +0.28R × 100 = +28R of expected gain. If 1R = ₹500, that is roughly ₹14,000 of expected profit across 100 trades, before costs. The losses do not upset you emotionally once you internalize this, because losing 60% of the time is *the plan*, not a failure.

This is the single most liberating idea in trading: **you do not need to be right often; you need to be right big and wrong small.** Cutting losses at −1R and letting winners run to +2R or +3R is what makes a low win rate profitable. The flip side is a warning — a method with a great feeling win rate can have *negative* expectancy if the losses are fat.

### The breakeven relationship

For any win rate there is a minimum reward:risk (R:R) you must achieve just to break even (E = 0). Rearranging the formula with avgLoss = 1R, breakeven avgWin = loss% ÷ win%.

```
Caption: Win-rate vs R:R breakeven table (avgLoss = 1R).
"Need" = avgWin in R required just to break even.
Anything ABOVE that line = positive expectancy.

  Win%  | Breakeven avgWin | Comfortable target
 -------+------------------+--------------------
  30%   |   2.33 R         |  aim >= 3.0 R
  40%   |   1.50 R         |  aim >= 2.0 R
  50%   |   1.00 R         |  aim >= 1.5 R
  60%   |   0.67 R         |  aim >= 1.2 R
  70%   |   0.43 R         |  aim >= 1.0 R

  Read: at 40% wins you only need > 1.5R avg win to be
  profitable. Our 2.2R example clears it easily.
```

This table is why the course insists on **reward:risk ≥ 1:2**. At 1:2 you break even at a 33.3% win rate; anything above that and you are ahead. It gives you a wide margin for the noise of a real sample.

## Concept 5 — Variance: Judge the Process, Not the Outcome

Even a +0.28R method does not deliver +0.28R every trade. It delivers a *distribution*: a scatter of −1R losses, some +2R and +3R winners, an occasional scratch. **Variance** is the spread of that distribution. High variance means long winning and losing streaks are normal even when the underlying edge is real and unchanged.

```
Caption: Distribution of R outcomes over 20 trades of a
positive-expectancy method. Each # is one trade.

  -2R  #
  -1R  # # # # # # # #     <- most losses cluster at the stop
   0R  #                     (a scratch/early exit)
  +1R  # #
  +2R  # # # #
  +3R  # # #
  +4R  #
       |----|----|----|
        losses    winners

  8 losses, 1 scratch, 11 winners of varying size.
  Sum ~ +5.6R over 20 trades = ~ +0.28R each. The EDGE
  lives in the shape, not in any single bar.
```

Because of variance, the correct question after any trade is never "did it win?" but "did I follow my process?" Score each trade **A/B/C on execution** independent of profit: A = every rule followed, B = minor deviation, C = broke a rule. A losing A-trade is a *good* trade; a winning C-trade is a *bad* trade that got lucky and will cost you later. If you reward process, expectancy takes care of the rupees over the sample.

## Concept 6 — The Losing-Streak Trap: Don't Over-Tinker

Here is the exact sequence that destroys beginners. A method with a genuine +0.28R edge throws four losses in a row — completely normal at a 40% win rate (roughly a 1-in-8 event, so it happens most weeks). The beginner panics: "It's not working." They widen the stop, then move the target closer, then add an indicator, then skip the next valid signal out of fear. They have now changed the method mid-sample, so their statistics are worthless, and the changes usually make expectancy *worse* because they were driven by pain, not evidence.

### The mechanism of the mistake

Each tweak resets your sample size to zero — you can no longer say what your win rate or average win is, because you keep measuring a moving target. And loss-driven changes systematically shrink winners (fear of giving back gains) and enlarge losers (hope that price comes back), inverting the very ratio that makes a low win rate profitable.

### The fix

Freeze your rules for a defined block — this whole week, no changes. Write your setup checklists down *before* Monday and treat them as law. Only after you have a meaningful sample (aim for 20+ trades, ideally more) do you review the data and adjust *one* variable at a time, with a reason grounded in the journal, not in the last loss. Add a **daily loss limit** — e.g., stop trading for the day after −2R or −3R total — so a bad streak can never spiral into a blow-up. The limit protects the sample and your psychology; it is a circuit breaker, not an admission of defeat.

## Worked Examples

*All numbers are hypothetical and for illustration only — not predictions.*

### Example 1 — VWAP bounce on Bank Nifty (long)

Setup context: Tuesday, Bank Nifty has opened firm and by 10:00 AM is trending up, trading above a rising VWAP, having made higher highs. This is a valid *up-trend context* for a long VWAP bounce.

- **10:18 AM** — Bank Nifty (illustrative index level) pulls back from a high near 52,180 down toward VWAP at 52,050.
- **10:25 AM** — The 5-minute candle dips to 52,035 (a clean VWAP touch) but closes back at 52,075 with a solid body and rising volume. Confirmation.
- **Entry** 52,080. **Stop** just below the candle low at 52,020 → risk = 60 points = 1R.
- **Target** the prior high area at 52,180 → reward = 100 points. R:R ≈ 1:1.66. You demand ≥1:2, so you extend the target only if structure supports it; here the prior swing high above at 52,220 gives 140 points → R:R ≈ 1:2.3. Acceptable.
- **10:52 AM** — Price tags 52,225. You exit. Result: **+2.3R.** Tag it VWAP-bounce, execution grade A.

Tick-by-tick reasoning: the edge came from *waiting* for the close-back-above-VWAP candle. Had you bought the instant price touched VWAP at 10:20, you'd have had no confirmation and a worse stop. Note lot sizes exist for index derivatives, so real Bank Nifty exposure trades in fixed lots — but on paper you can model the point move directly as R.

### Example 2 — Breakout on Reliance vs. a tempting non-setup

- **9:47 AM, Thursday** — Reliance has built a tight range between ₹1,395 and ₹1,402 for 25 minutes (your pre-marked resistance is ₹1,402).
- **9:52 AM** — A 5-minute candle closes at ₹1,405, breaking ₹1,402 on volume noticeably above the morning average. Valid breakout.
- **Entry** ₹1,405. **Stop** back inside the range at ₹1,398 → risk ₹7 = 1R. Size: risking 1% of a ₹1,00,000 paper account = ₹1,000, so ~142 shares.
- **Target** measured move: range height ₹7 projected twice = ₹1,419, giving R:R ≈ 1:2.
- **10:30 AM** — Reliance reaches ₹1,420; you exit. Result: **+2R.** Tag it breakout, grade A.

Now the discipline test. At **11:10 AM**, ICICI Bank spikes ₹4 in two minutes but there was no level you had pre-marked and no VWAP touch. It "feels" like it's breaking out. **You do not trade it** — it matches neither checklist. Logging this as a *correct skip* is as valuable as a winning trade, because it proves you can tell a setup from a random move. That is the skill that keeps expectancy positive.

## Common Mistakes (and the fix)

1. **Quitting the method after a losing streak.** *Why:* losses feel like proof of failure. *Fix:* expect streaks — four losses at 40% wins is routine; freeze rules for the full week and judge only after 20+ trades.
2. **Over-trading to "make it back."** *Why:* the sample-building goal gets twisted into a volume race, and revenge-trading after a loss. *Fix:* cap trades per day (e.g., max 3) and enforce a daily loss limit of −2R to −3R. More trades only help if each still meets the full checklist.
3. **Chasing win rate instead of expectancy.** *Why:* being "right" feels good, so beginners take quick +0.5R profits and hold losers hoping to be right. *Fix:* let winners run to ≥2R, cut losers at −1R exactly; track expectancy, not win %.
4. **Blurring the two setups.** *Why:* in the moment, any move can be rationalized into a pattern. *Fix:* name the setup before entry, satisfy its full checklist, tag exactly one setup per trade; ambiguous = no trade.
5. **Not logging skips and process grades.** *Why:* only wins/losses feel worth recording. *Fix:* log every valid signal you took *and* every correct skip, with an A/B/C execution grade, so you measure discipline, not just money.

## Nuances & Edge Cases

- **VWAP is unreliable in the first ~15 minutes** because too little volume has traded to make it meaningful; the opening auction and early spread distort it. Give it until ~9:30–9:45 before trusting VWAP bounces.
- **Range-bound days kill the VWAP bounce.** The setup needs a trend and a rising (or falling) VWAP. On a flat VWAP with price oscillating across it, "bounces" are just chop — skip the setup entirely that day.
- **Auto square-off skews late trades.** MIS positions get squared off around 3:20 PM. A trade entered at 3:05 has almost no room to reach a 2R target, and a forced exit is not a clean −1R or +2R — it's whatever price is at 3:20. Avoid initiating new setups in the last ~20 minutes; they pollute your statistics.
- **Scratches are data, not nothing.** An early exit at 0R (you left because the premise changed before the stop) belongs in the log. A method with many disciplined scratches often has a better *real* avgLoss than −1R.
- **Correlation between Nifty and Bank Nifty.** They move together; a long VWAP bounce on Bank Nifty and a long breakout on Nifty at the same time are not two independent trades — they are one bet sized double. Count correlated positions as shared risk against your daily loss limit.
- **Paper fills are too generous.** Real fills suffer slippage and you skip STT/brokerage this week — so treat this week's rupee results as slightly optimistic. The *shape* of your distribution and your discipline matter more than the exact profit.

## Day-by-Day (Mon–Fri)

- **Monday — Freeze the rules.** Write both checklists (your existing setup + the VWAP bounce) on one page: context, trigger, stop, target, R:R ≥ 1:2. Watch the open. *Observation target:* mark VWAP on your chart and note every time price touched it and whether it bounced or broke.
- **Tuesday — Trade setup #1 only.** Take only your original setup, max 3 trades, daily loss limit −2R. Log each with entry/stop/target, R result, setup tag, and A/B/C grade. *Observation target:* did any losing trade earn an A? Note it — that's a good trade.
- **Wednesday — Trade the VWAP bounce only.** Restrict yourself to the new setup so you learn its feel in isolation. *Observation target:* count how many VWAP touches gave a valid *confirmation candle* vs. how many you'd have jumped on too early.
- **Thursday — Both setups live.** Name the setup out loud before every entry. *Observation target:* log at least one *correct skip* — a move that tempted you but matched neither checklist.
- **Friday — Compute your stats.** Fill the weekly template below from your journal. *Observation target:* your expectancy number and whether your average win cleared the breakeven line for your win rate.

### Weekly stats template

```
Caption: Fill this from your journal every Friday.

  WEEK 9 PAPER-TRADING STATS
  --------------------------------------------------
  Total trades ............... ____
  Wins ....... ____   Losses ....... ____  Scratches __
  Win% = wins / total ........ ____ %
  avgWin (mean R of winners) . ____ R
  avgLoss (mean R of losers) . ____ R
  Largest win / largest loss . ____R / ____R
  Correct skips logged ....... ____
  Execution grades  A:__  B:__  C:__
  --------------------------------------------------
  Expectancy E = (win% x avgWin) - (loss% x avgLoss)
  E = (____ x ____) - (____ x ____) = ______ R / trade
  --------------------------------------------------
  Rule breaks this week (C-grades) & fix for each:
  1) ______________________________________________
  2) ______________________________________________
```

## Key Takeaways

- A handful of trades is noise; only 20+ (ideally 100+) trades reveal whether your method has an edge. Build the sample deliberately.
- Express everything in **R**. Track win rate, average win, and average loss together — never win rate alone.
- **Expectancy E = (win% × avgWin) − (loss% × avgLoss)** is the one number that matters. A 40% win rate is comfortably profitable at +2.2R average wins (+0.28R/trade).
- Reward:risk ≥ 1:2 breaks even at just a 33% win rate, giving you a wide margin against variance.
- Judge the **process, not the outcome**: grade every trade A/B/C on rule-following; a losing A-trade beats a winning C-trade.
- Never re-engineer a method mid-losing-streak. Freeze rules, enforce a daily loss limit, and change one thing only after the data — not the pain — tells you to.

## This Week's Milestone

You have a completed weekly stats sheet built from **at least 15 logged paper trades across both setups**, every trade tagged with one setup name and an A/B/C execution grade, at least one correct skip recorded — and you can state your expectancy in R and explain, using the breakeven table, whether your average win clears the line for your win rate. Proving you can compute and interpret your own edge is the point; the profit figure is secondary.

---

> **◀ Previous:** [Week 8 — Risk & Position Sizing](./week-08-risk-and-position-sizing.md) &nbsp;|&nbsp; **Course Home:** [Lessons Index](./README.md) &nbsp;|&nbsp; **Next ▶:** [Week 10 — Psychology & Your Trading Plan](./week-10-psychology-and-plan.md)
