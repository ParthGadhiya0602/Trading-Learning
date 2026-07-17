# Week 8 — Risk & Position Sizing

> **◀ Previous:** [Week 7 — Your First Paper Trades](./week-07-first-paper-trades.md) &nbsp;|&nbsp; **Course Home:** [Lessons Index](./README.md) &nbsp;|&nbsp; **Next ▶:** [Week 9 — Intensive Paper Trading](./week-09-intensive-paper-trading.md)

> ⚠️ **Educational content only — not financial advice.** Nothing in this lesson is a trade recommendation or suggestion. All examples and numbers are illustrative and hypothetical. Always consult a registered financial advisor before trading or investing. Trade and invest at your own risk — no responsibility is accepted for any loss, damage, or incorrect/invalid trades.

_This week you learn the one skill that keeps traders alive: deciding exactly how much you can lose — down to the rupee — before you ever think about how much you might win._

## Why This Week Matters

For seven weeks you have studied entries: candlesticks, levels, supply and demand zones, indicators, the opening range breakout. All of that answers the question _"where do I get in?"_ But entries are the part of trading you have the **least** control over. You cannot force Reliance to go up because you bought it. You cannot make Bank Nifty respect your level. The market decides whether a trade works.

Here is the pivot that separates people who last from people who blow up: **you control your loss; the market controls your profit.** You cannot dictate the reward, but you can decide, in advance and with total precision, that a given trade will never cost you more than ₹1,000. Making that decision — and then buying exactly the right quantity so it holds true — is _position sizing_. It is the single most important mechanical skill in this course, and it is pure arithmetic. No prediction required.

Why now, at Week 8? Because you have started paper-trading (Week 7) and you are about to intensify it (Week 9). If you build the habit of sizing every trade _before_ you touch the buy button now — while it is paper money — it becomes automatic long before real money is on the line in Week 12. Traders who skip this step spend their first real month learning it the expensive way.

## Concept 1 — Risk-First Thinking

Most beginners think in this order: _"I like this setup → how much can I make → let me buy as much as I can afford."_ A professional reverses every step: _"How much can I lose if I'm wrong → therefore how big a position → only then, is the reward worth that risk?"_

### The mechanism: why loss is the controllable variable

When you enter a long trade — say you buy SBIN at ₹600 — you are matched against a seller in the order book at that price. From that instant, price is a live auction between everyone who wants to buy and everyone who wants to sell. You are one small voice in that auction; you cannot move it. What you _can_ do is pre-place a resting sell order (your stop-loss) at, say, ₹594. If enough sellers push the price down to ₹594, your stop fires, you are out, and your loss is locked at ₹6 per share — a number you chose. The market never asked your permission to fall, but you decided in advance how much of that fall you would sit through.

Notice the asymmetry. Your **downside is a decision** (where you put the stop). Your **upside is a hope** (where the market happens to travel). Risk-first thinking simply means you engineer the thing you control and stop pretending you control the thing you don't.

### "Risk" is not the money you deploy

This trips up every beginner, so nail it now. If you buy 100 shares of SBIN at ₹600, you _deploy_ ₹60,000. But if your stop is at ₹594, you _risk_ only ₹6 × 100 = ₹600. Deployed capital and risked capital are completely different numbers. Sizing is about controlling the **risked** amount — the money that actually disappears if the stop hits — not the amount parked in the position.

## Concept 2 — The 1–2% Rule (and the real reason for it)

The rule: **never risk more than 1–2% of your trading capital on a single trade.** On a ₹1,00,000 paper account, that is ₹1,000–₹2,000 of _risk_ per trade — the maximum you allow yourself to lose if stopped out.

Beginners hear this and think it is about being timid. It is not. It is about **surviving a losing streak long enough for your edge to show up.** Even good intraday traders lose 40–50% of their trades. Losses do not arrive politely spaced out; they cluster. You will, at some point, lose five, six, seven trades in a row — not because your method broke, but because that is how randomness feels up close. The 1–2% rule is sized so that a normal cluster of losses is an annoyance, not a catastrophe.

### Why the exact number matters so much

The damage from risk-per-trade is not linear — it compounds. We will prove this with hard numbers in Concept 6, but hold the intuition now: at 2% risk, a brutal six-loss streak costs you about 11% of your account. At 10% risk, the _same_ streak takes nearly _half_ of it. The difference between "recoverable dip" and "career-ending hole" is a single dial: how much you risk per trade. Beginners set that dial with their emotions ("I'm sure about this one"). Professionals set it with a rule and never touch it.

Start the week at **1% (₹1,000)**. It is deliberately conservative. You are learning; your job is to make many small, correct decisions, not big ones.

## Concept 3 — The R-Multiple Framework: Think in R, Not Rupees

Here is a mental upgrade that changes everything. Stop measuring trades in rupees. Measure them in **R**.

**R is the amount you risk on a trade.** That is the whole definition. If you decide a trade risks ₹1,000, then for that trade, 1R = ₹1,000. Every outcome is now expressed as a multiple of R:

- Stopped out for your full planned loss → **−1R**
- Target hit at twice your risk → **+2R**
- Closed early for a small gain of half your risk → **+0.5R**

Why bother? Because rupee amounts change with account size and stop distance, but **R normalizes everything onto one ruler.** A ₹1,000 loss on a tight SBIN stop and a ₹1,000 loss on a wide Bank Nifty stop are _the same event_: −1R. This lets you compare trades, tally results, and reason about your system without the numbers shifting under you.

Diagram — the R-multiple ruler (one trade, risk = 1R):

```
        LOSS  |         RISK-FREE         |   PROFIT
              |                           |
   -2R   -1R  |  0R                      +1R        +2R      +3R
    |     |   |   |                       |          |        |
 ---+-----●---+---+-----------------------+----------●--------+---
         STOP    ENTRY                            TARGET
      (max loss)              (breakeven)      (1:2 reward)
              |                          |
   Everything left of ENTRY is what you   Everything right is
   PRE-DECIDED you could lose (= -1R).     hope, measured in R.
```

_Caption: A single trade laid on the R ruler. You place the stop at −1R and the target at +2R before entry. Outcomes are read as multiples of R, not rupees._

From now on, when you journal a trade, write "+2R" or "−1R", not just the rupee figure. You are training yourself to see the _structure_ of the trade, independent of its size.

## Concept 4 — The Position Size Formula

This is the most important formula in the course. Memorize it:

```
        Money Risked (your R in rupees)
Qty  =  ───────────────────────────────
          Entry Price  −  Stop Price
```

The denominator — entry minus stop — is your **risk per share** (or per point, for an index). Divide your total rupee risk by it and you get exactly the quantity that makes a stop-out cost precisely 1R. The formula does the discipline _for_ you: give it a wide stop and it hands you a small position; give it a tight stop and it hands you a bigger one. Either way, the loss is pinned at your chosen R.

Diagram — the formula worked, and why the position resizes to the stop:

```
  Capital ₹1,00,000   |   Risk 1% = ₹1,000  = 1R
  ─────────────────────────────────────────────────────
                        risk/share        Qty = 1000 / risk
  Entry 600, Stop 594     ₹6      →        166 shares
  Entry 600, Stop 590     ₹10     →        100 shares
  Entry 600, Stop 580     ₹20     →         50 shares
  ─────────────────────────────────────────────────────
  Wider stop  ─────────►  bigger risk/share ─────► FEWER shares
  Every row loses EXACTLY ₹1,000 if the stop is hit.
```

_Caption: Same ₹1,000 risk, three different stops. The formula shrinks the position as the stop widens so the rupee loss never changes. You size to the stop — never to your excitement._

### Converting index points to rupees via lot size

Index derivatives (Nifty and Bank Nifty futures/options) do not trade in single units — they trade in **lots**, a fixed bundle of units set by the exchange. You cannot buy "one Bank Nifty"; you buy one lot. So for the index the formula's denominator is measured in **index points**, and you must first convert points to rupees using the lot size:

```
Rupees risked per lot  =  (Entry points − Stop points)  ×  Lot size
Lots  =  Money Risked  ÷  Rupees risked per lot   (then ROUND DOWN)
```

> Lot sizes are revised periodically by NSE/SEBI — always check the current contract before trading. The numbers below are **illustrative** so you can learn the mechanics.

The critical wrinkle: lots are whole numbers. If the maths says 1.4 lots, you trade **1** lot (round down — never round up past your risk). This coarse granularity is why index trading usually needs more capital than single-stock trading: one lot can already exceed a small account's 1% risk budget. We work a full example below.

## Concept 5 — Stop-Loss Types

Every trade needs a stop placed _before_ entry. Three common ways to decide where it goes.

### Fixed stop (points or percentage)

A set distance: "stop 15 points below entry" or "stop 0.5% below entry." Simple and mechanical — good training wheels. Its weakness: it ignores the chart. A fixed stop can land in the middle of ordinary noise and get picked off by random wiggles that mean nothing.

### Structure / zone-based stop

Placed just beyond a _real_ chart level — below a swing low or demand zone for a long, above a swing high or supply zone for a short. This is the method you built toward in Week 4. Its logic: the stop sits where the market would genuinely prove your idea _wrong_, not at an arbitrary distance.

Diagram — a structure-based stop on a long:

```
   Target 48,240  ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─  +2R
                                      ▲
   Entry  48,000  ──────●─────────────┘     go long here
                        │
   Demand zone   ░░░░░░░░░░░░░░░░░░░░░░  47,900–47,960
   Stop   47,880  ──────✕───────────────    just BELOW the zone
                        └── −1R: the level failed, idea is wrong
```

_Caption: The stop sits under the demand zone — the price at which the reason for the trade no longer holds. Distance is dictated by the chart, and the formula sizes the position to it._

### ATR concept (a preview)

ATR — Average True Range — is an indicator that measures how much an instrument typically moves in a given period (its "normal" range). The idea, which you will use more later: set your stop as a multiple of ATR (e.g. 1.5 × ATR below entry) so your stop is **calibrated to current volatility**. On a wild day the stop is naturally wider; on a quiet day, tighter. This stops you from using a 10-point stop on a day Bank Nifty is swinging 300 points. For now, just understand the principle — volatility should inform stop distance.

## Concept 6 — Reward:Risk, Win-Rate, and Why Small Risk Survives

### The R:R filter

Before entering, measure the distance to a _logical_ target versus the distance to your stop. Demand **reward:risk ≥ 1:2** — risk 1R to make at least 2R. This one filter is why you can be wrong most of the time and still grow.

### How win-rate interacts with R:R — an expectancy preview

**Expectancy** is the average result you can expect per trade, in R:

```
Expectancy (R) = (Win% × avg win in R) − (Loss% × avg loss in R)
```

With a 1:2 system (wins = +2R, losses = −1R) and a modest **40% win rate**:

```
  = (0.40 × 2R) − (0.60 × 1R)
  = 0.80R      −   0.60R
  = +0.20R  per trade
```

Positive. Over 100 trades that is roughly +20R of expected gain — at a win rate where you lose _more often than you win_. This is the mathematical engine behind "cut losses short, let winners run": a strong R:R lets a mediocre win-rate still compound upward. Flip it: a 1:1 system needs to win **more than half** the time just to break even after costs. R:R does the heavy lifting so your entry timing doesn't have to be perfect.

### The drawdown maths — why 2% survives and 10% doesn't

Losing streaks are certain. Watch what an identical six-loss streak does at 2% risk versus a reckless 10%, both starting from ₹1,00,000:

```
  After loss #     Risk 2%           Risk 10%
  ────────────     ──────────        ──────────
       1           ₹98,000           ₹90,000
       2           ₹96,040           ₹81,000
       3           ₹94,119           ₹72,900
       4           ₹92,237           ₹65,610
       5           ₹90,392           ₹59,049
       6           ₹88,584           ₹53,144
  ────────────     ──────────        ──────────
  Drawdown         ~11.4%            ~46.9%
  Gain to recover  ~12.9%            ~88.2%
```

_Caption: Two equity paths through the SAME six losses. At 2% you are dented; at 10% you are cut in half — and a half-sized account needs to nearly DOUBLE to get back to even._

The asymmetry of recovery is the killer. Lose 50% and you must make **100%** just to return to breakeven. Lose 11% and you need about 13%. The deeper you dig, the more disproportionately hard the climb out — which is why capping each trade's risk is not caution, it is survival engineering.

### Risk of ruin, intuitively

_Risk of ruin_ is the probability that a string of losses wipes you out (or drops you so low you can't recover). It rises sharply as (a) risk-per-trade goes up, (b) win-rate goes down, and (c) R:R gets worse. You don't need the formula this week — you need the intuition: **big bets plus an unavoidable losing streak equals ruin, no matter how good your entries are.** The 1–2% rule pushes your risk of ruin so low that a normal bad run simply cannot end you. That is its entire job.

### Never average down intraday

When a trade goes against you, the tempting move is to buy _more_ at the lower price to "lower your average" and recover faster on a bounce. Do not do this intraday. Averaging down **increases** your position exactly as the market tells you that you are wrong — it converts a planned −1R loss into a −2R or −3R disaster and destroys the whole point of position sizing. Your stop is your admission of being wrong; honour it. If you find yourself wanting to add to a loser, that is the signal to _reduce_, not add. Add only to _winners_, and only if your plan says so.

## Worked Examples

> All numbers below are **hypothetical and illustrative**, chosen for clean arithmetic — not predictions and not current quotes.

### Example 1 — Single stock: ICICI Bank long (structure stop)

- **Capital** ₹1,00,000. **Risk** 1% → **1R = ₹1,000**.
- 10:05 IST — ICICI Bank breaks above an intraday resistance and holds. Price **₹1,200**.
- Nearest demand/support sits at ₹1,192; you place the stop just under it at **₹1,190**.
- **Risk per share** = 1,200 − 1,190 = **₹10**.

```
Qty = 1,000 / 10 = 100 shares
```

- Deployed = 100 × ₹1,200 = ₹1,20,000 (fine in paper; real life uses intraday MIS margin).
- **If stopped** at ₹1,190: loss = 100 × ₹10 = **₹1,000 = −1R**. Exactly the plan.
- **Target at 1:2** = entry + 2 × risk = 1,200 + 20 = **₹1,220**. If hit: 100 × ₹20 = **₹2,000 = +2R**.
- 11:40 IST — price tags ₹1,220, target fills. Result logged as **+2R**, not "₹2,000". You now have a clean data point comparable to every other trade regardless of size.

Now stress-test the discipline: suppose the only sensible stop had been ₹1,180 (risk ₹20/share). The formula returns 1,000 / 20 = **50 shares** — half the size — and a stop-out still costs exactly ₹1,000. The wider the stop, the smaller the position. You never let a wide stop tempt you into over-risking.

### Example 2 — Index, lot-based: Bank Nifty long (points → rupees)

This shows the two things stock examples can't: converting **points to rupees via lot size**, and **rounding down to whole lots**.

- **Capital** ₹5,00,000. **Risk** 1% → **1R = ₹5,000**.
- **Illustrative Bank Nifty lot size = 35 units** (verify the live contract — it changes).
- 9:35 IST — Bank Nifty pulls back into a demand zone at 47,900–47,960 and prints a bullish reversal. You go long at **48,000**.
- Structure stop just below the zone at **47,880**.
- **Risk in points** = 48,000 − 47,880 = **120 points**.

Step 1 — convert points to rupees per lot:

```
Rupees risked per lot = 120 points × 35 = ₹4,200 per lot
```

Step 2 — how many lots fit inside 1R?

```
Lots = 5,000 / 4,200 = 1.19  →  ROUND DOWN  →  1 lot
```

- You trade **1 lot**. Real risk if stopped = 120 × 35 = **₹4,200**, which is ₹800 _under_ your ₹5,000 budget. Good — you are always at or below 1R, never over.
- **Target at 1:2** = 2 × 120 = 240 points → **48,240**. If hit, gain = 240 × 35 = **₹8,400 ≈ +1.68R** on the ₹5,000 unit (or +2R measured against the ₹4,200 you actually risked — journal it consistently one way).
- 10:50 IST — Bank Nifty reaches 48,240; target fills.

Teaching point: had you naively rounded 1.19 _up_ to 2 lots, a stop-out would cost 2 × ₹4,200 = **₹8,400 — a −1.68R loss on a trade you called 1R.** Rounding down is not optional. And notice the coarse granularity: with ₹5,00,000 you could take only 1 lot on a 120-point stop. Index trading needs real capital before the lot math gives you any flexibility — a big reason beginners paper-trade stocks first.

## Common Mistakes (and the fix)

**1. Sizing to excitement, not to the stop.** _Why beginners do it:_ a setup looks "obvious," so they buy as many shares as the account allows and place a stop wherever. _The fix:_ the position size is an **output** of the formula, never an input. Decide R and the stop first; let `Qty = R ÷ (entry − stop)` tell you the size. Confidence has no vote.

**2. Moving or widening the stop when price approaches it.** _Why:_ watching a stop about to hit hurts, and "it'll come back" feels safer than accepting the loss. _The fix:_ the stop is a pre-committed decision; the moment you widen it you have abandoned your R and turned a −1R into an unknown. Set it, then treat it as untouchable. If anything, you may _tighten_ to protect profit — never loosen.

**3. Ignoring lot size / rounding up on the index.** _Why:_ they apply the stock formula to Bank Nifty and forget one lot is 35 units, or they round 1.19 up to "just take 2." _The fix:_ always convert points → rupees with the current lot size, then round lots **down**. One lot that slightly under-risks beats two lots that blow past your R.

**4. Averaging down into a loser.** _Why:_ lowering the average price feels like a smart recovery. _The fix:_ it doubles your risk exactly when the market says you're wrong. Honour the stop; add only to winners. Wanting to add to a loser is your cue to _cut_, not build.

**5. Taking 1:1 (or worse) trades because they "look easy."** _Why:_ nearby targets fill more often, which feels good. _The fix:_ run the expectancy — a 1:1 system needs &gt;50% wins just to survive costs. Demand ≥ 1:2 and reject everything else. Learning to _pass_ on sub-1:2 setups is itself a core skill this week.

## Nuances & Edge Cases

- **Slippage and gaps mean −1R is a floor, not a guarantee.** Your stop is an _order_, not a force field. If price gaps or moves violently through your level (news, expiry, open), you can be filled _worse_ than your stop — a −1.3R instead of −1R. This is another argument _for_ small per-trade risk: it cushions the occasional overshoot.
- **Costs quietly erode small edges.** Brokerage, STT, exchange fees and GST are covered in depth later, but know now that they nibble every trade. A "1:2" that's really 1:1.7 after costs still works; a "1:1" often turns _negative_ after costs. R:R gives you a buffer against the drag.
- **Correlated positions stack risk.** Long Bank Nifty _and_ long HDFC Bank _and_ long ICICI Bank at once is not three 1R trades — banks move together, so it behaves closer to one 3R bet. Count correlated exposure as combined risk when you total your open R.
- **A daily loss limit sits above the per-trade rule.** Cap the _day_ too — e.g. stop trading after −3R in a session. This blocks the revenge-trading spiral where three quick losses tempt you into a reckless fourth. The per-trade rule protects the account from one trade; the daily limit protects it from one bad _mood_.
- **The \~3:20 PM auto square-off is a risk event.** Intraday (MIS) positions are auto-closed by your broker around 3:20 PM if you haven't exited. Late in the session your "stop" may effectively become "whatever the square-off gets" — factor the closing window into any trade you're still holding near 3:15.

## Day-by-Day (Mon–Fri)

- **Monday — Set your numbers.** Write down paper capital (₹1,00,000) and per-trade risk (1% = ₹1,000 = 1R). Pin it above your screen. This is fixed all week. _Observation target:_ during 9:15–3:30 IST, just watch how far Bank Nifty travels in single 5-min candles — feel how fast an over-sized position would move against you.
- **Tuesday — Drill the stock formula.** For 5 hypothetical entries on SBIN, Reliance and Infosys, compute `Qty = 1,000 ÷ (entry − stop)` by hand. _Observation target:_ confirm each stop-out equals ₹1,000; note how the share count changes as your stop distance changes.
- **Wednesday — Index lot maths.** For 3 hypothetical Bank Nifty and Nifty entries, convert points → rupees with the current lot size, then compute lots and **round down**. _Observation target:_ find one case where the correct answer is "position too big for 1R — skip or reduce," and record it.
- **Thursday — R:R filter + expectancy.** Take 6 paper setups; measure each one's distance to a logical target vs its stop. "Take" only those ≥ 1:2. _Observation target:_ count how many you had to reject, and write the expectancy of your chosen set assuming a 40% win rate.
- **Friday — Full paper trades in R.** Execute 3 complete paper trades: entry, formula-sized quantity, structure stop, ≥1:2 target — and **log every result as an R-multiple** (+2R, −1R…), not just rupees. _Observation target:_ verify you honoured exactly 1R of risk on all three, and that no stop was ever widened.

## Key Takeaways

- Decide your loss **before** entry. Risk 1–2% of capital per trade — start at 1%, never exceed 2%.
- `Qty = Money Risked ÷ (Entry − Stop)`. You size to the stop, never to your confidence. For the index, convert points → rupees via lot size and **round lots down**.
- Think in **R**, not rupees: −1R for a full stop, +2R for a 1:2 winner. R makes every trade comparable regardless of size.
- Demand reward:risk ≥ 1:2. With 1:2, even a 40% win rate has positive expectancy (+0.2R/trade).
- Losing streaks are certain. At 2% risk a six-loss run costs \~11%; at 10% it costs \~47% — and deep holes need disproportionately huge gains to climb out.
- Never average down intraday, cap your daily loss, and respect the \~3:20 PM square-off. Survival, not prediction, is the edge.

## This Week's Milestone

Given any NSE setup — "ICICI Bank at ₹1,200, stop ₹1,190" or "Bank Nifty at 48,000, stop 47,880, lot size 35" — you can state, within seconds and out loud, the exact quantity (or number of lots, rounded down) to trade so that being wrong costs no more than your fixed 1R, with a target placed at ≥ 1:2. Prove it Friday with **3 fully-sized, fully-logged paper trades, each result recorded as an R-multiple.**

_Education only — not financial advice. No method guarantees profit. Lot sizes are set by NSE/SEBI and change; verify the live contract. Use a stop-loss on every trade._

---

> **◀ Previous:** [Week 7 — Your First Paper Trades](./week-07-first-paper-trades.md) &nbsp;|&nbsp; **Course Home:** [Lessons Index](./README.md) &nbsp;|&nbsp; **Next ▶:** [Week 9 — Intensive Paper Trading](./week-09-intensive-paper-trading.md)
