# Week 6 — Pick ONE Setup: Opening Range Breakout

> **◀ Previous:** [Week 5 — The Four Indicators You Need](./week-05-indicators.md) &nbsp;|&nbsp; **Course Home:** [Lessons Index](./README.md) &nbsp;|&nbsp; **Next ▶:** [Week 7 — Your First Paper Trades](./week-07-first-paper-trades.md)

_This week you stop collecting strategies and commit to mastering one mechanical setup — the Opening Range Breakout (ORB) — until it is boringly automatic._

## Why This Week Matters

For five weeks you have been building the alphabet of price: candles (Weeks 2–3), levels and supply/demand zones (Week 4), and indicators like EMA and VWAP (Week 5). An alphabet is not a sentence. A **setup** is the sentence — a fixed, repeatable pattern of conditions that tells you _when to enter, where your stop goes, and where you take profit_, decided **before** the trade, not during it.

Here is the trap almost every beginner falls into: they learn ten setups shallowly, then in the heat of a live 9:15 AM open they freeze, second-guess, and end up trading on feeling. Feelings lose money. A professional intraday trader typically runs **one or two setups they know cold** — they have seen the pattern win, fail, and fake-out hundreds of times, so they can act without hesitation and, just as importantly, _sit on their hands_ when the setup is absent.

This week you commit to the **Opening Range Breakout**. It is the best first setup for a reason: it is objective (the rules leave almost nothing to opinion), it happens at a predictable time (right after the open), and it teaches the two skills every other setup also needs — reading a breakout versus a fakeout, and placing a stop at a structural point rather than a random number. Master ORB now and Weeks 7–12 (paper trading, sizing, psychology, going live) have something concrete to practise on.

Remember the frame for the whole course: **paper only until Week 12.** Nothing here is a prediction or a promise of profit. It is a training method built around one non-negotiable idea — you protect capital first and let profit be a by-product of discipline.

## Concept 1 — The Logic of the Opening Range

### What actually happens at 9:15 AM

The Indian cash market opens at 9:15 AM IST after a pre-open auction (9:00–9:15). But the open is not a fresh start — it is a _release of pressure_ that built up overnight. Consider everything that piled up while the market was closed:

- US markets closed, SGX/GIFT Nifty moved overnight, crude and the rupee shifted.
- Company news, global events, and results landed after 3:30 PM yesterday.
- Thousands of traders and institutions placed **orders overnight** — buy and sell limit orders sitting in the book, plus market orders queued to fire at 9:15.

At 9:15 all of that hits the order book at once. For the first few minutes, buyers and sellers are _discovering_ what price is fair given the overnight information. The **opening range (OR)** — the high and low made in the first 15 minutes (9:15–9:30) — is the visible footprint of that fight. The high is the level where sellers were strong enough to stop the advance; the low is where buyers were strong enough to stop the decline.

### Why the range edges become "battle lines"

Think about who is trapped at the edges. Someone who bought near the OR high and then watched price fall back into the range is now sitting at a small loss, _hoping_ to get out at break-even if price returns. Someone who sold near the OR low is in the mirror position. These trapped participants leave resting orders exactly at the range edges. That is why a **decisive push through the OR high** matters: it doesn't just clear the sellers who created that high, it can trigger stop-losses of the trapped shorts (who must buy to exit), which adds fuel to the move. A breakout is, mechanically, the moment one side runs out of resting orders and the other side's momentum takes over.

```
Caption: The opening range as the day's first battle line

Price
  |         sellers win here → OR HIGH
  |   ┌───────●─────────────────────────┐  ← resting SELL orders + trapped longs
  |   │        ↑        ↓                │
  |   │     buyers   sellers   (fight)   │   NO-MAN'S-LAND: do not trade inside
  |   │        ↓        ↑                │
  |   └───────●─────────────────────────┘  ← resting BUY orders + trapped shorts
  |         buyers win here → OR LOW
  +----|-----|------------------------------> Time (IST)
     9:15  9:30
```

## Concept 2 — The Setup Families (and why you master only ONE)

You will _see_ four common intraday setups this week, but only _trade_ ORB. Knowing the others helps you understand what ORB is and isn't.

- **Opening Range Breakout (ORB).** Trade the confirmed break of the 9:15–9:30 high/low. Objective, time-boxed, beginner-friendly. **Your pick.**
- **EMA crossover.** Go long when a fast EMA (e.g. 9) crosses above a slow EMA (e.g. 21), short when below. Simple, but it _lags_ — in a sideways, choppy session it whipsaws you with false crosses.
- **VWAP bounce.** Price pulls back to the VWAP (the day's volume-weighted average price, the line institutions benchmark against) and resumes in the trend direction. Powerful, but it requires you to already _know_ the trend and read context.
- **Breakout-and-retest.** Price breaks a level, comes back to "kiss" it, then continues. High quality, but demands patience and experience to tell a healthy retest from a full reversal.

Why only one? Because skill compounds with **repetition of the same pattern.** If you spread ten trades across four setups, you get 2–3 samples each — not enough to learn anything. Put all ten into ORB and you start to feel the difference between a clean break and a trap. One setup mastered beats five half-known, every time.

## Concept 3 — Full ORB Mechanics

### Step 1: Define the range

After the 9:15–9:30 window, mark the **OR high** and **OR low** with two horizontal lines. (Some traders use a 5-minute or 30-minute range; you will standardise on the **15-minute** range this week so every trade is comparable.) The gap between the lines is **no-man's-land** — you never enter there, because inside the range neither side has won and you'd be trading noise.

### Step 2: Distinguish a valid breakout from a fakeout

This is the whole game. A **fakeout** (or "fake breakout") is when price pokes past the range edge, sucks in breakout traders, then snaps back inside — trapping them. A **valid breakout** has three confirming features:

1. **Close beyond, not just a wick.** Wait for a full 5-minute candle to _close_ above the OR high (or below the OR low). A long upper wick that closes back inside is rejection, not a breakout.
2. **Volume expansion.** The breakout candle's volume should be visibly larger than the prior few candles. A break on thin volume means few participants agree — those break most easily.
3. **Follow-through (optional but powerful): the retest holds.** After breaking, price often dips back to the broken edge. If that edge now acts as _support_ (for a long) and price bounces, the old resistance has become support — strong confirmation.

```
Caption: Fakeout vs true breakout at the OR high

  FAKEOUT (avoid)                    TRUE BREAKOUT (trade)
  OR High ───┐  ▲ wick pokes         OR High ───┐        ┌──▲ closes ABOVE
             │  │ above, then         close      │   ┌────┘   on BIG volume
             │  ▼ closes back IN      inside →   │───┘  ↑ candle body clears edge
  ───────────┴──── price falls        ───────────┴──────── price holds & runs
  vol: thin, no conviction            vol: SPIKE, conviction
```

### Step 3: Entry variants

- **Break entry (aggressive).** Enter as the next candle opens right after the confirming close beyond the range. You catch more of the move but risk more fakeouts.
- **Retest entry (conservative).** Wait for price to pull back to the broken edge and show it holds (a small bullish candle off the level for a long), then enter. Fewer trades, but far fewer traps and a _tighter stop_. As a beginner, prefer the retest entry — it forces patience.

```
Caption: Retest entry on an OR-high breakout

Price
  |                    ┌─● ENTRY (retest holds, buy here)
  |            ┌───────┘ │   stop just below the edge → tight risk
  | OR High ───┴─────────┴────────────  broken level now = SUPPORT
  |        ┌───┘   (price dips back to "kiss" the line, bounces)
  | OR Low ┘
  +------------------------------------------> Time
```

### Step 4: Stop placement

Your stop is where the setup is **proven wrong**, not a number that feels comfortable. For an ORB long:

- **Structural stop:** just below the **OR low** (the whole range failed). Wider, but the setup is only truly dead if price re-enters and crosses the range.
- **Tighter stop:** just below the **breakout candle's low** or below the **retested edge**. Smaller risk, but you can get shaken out by noise.

The retest entry lets you use the tight stop with confidence, because you have a clear invalidation point right below the level.

### Step 5: Targets

Three ways to define the target, from mechanical to discretionary:

1. **Range-height projection (measured move).** Take the range width (OR high − OR low) and project it from the breakout point. If the range is 140 points and you break the high at 48,120, the measured target is 48,120 + 140 = 48,260.
2. **Next zone.** Target the next supply zone above (for a long) or demand zone below (for a short) that you marked in Week 4.
3. **Fixed R-multiple.** Set the target at a fixed multiple of your risk (the stop distance). Insist on **reward:risk ≥ 1:2**. Book part of the position at the first target and trail the rest if the move is strong.

### Step 6: Time-of-day filter and avoiding dead days

- **Only take ORB entries roughly 9:30–10:30 AM.** The move born from the open is freshest then. Breakouts at noon are usually low-conviction; the auto square-off for intraday (MIS) positions kicks in around **3:20 PM**, and liquidity/volatility often thin out mid-session.
- **Skip low-volatility days.** If the opening range is unusually _tight_ (a tiny 15-min box) and volume is limp, breakouts fizzle — there is no fuel. Expiry days, big-event days (RBI policy, Budget, US Fed), and holiday-shortened sessions all distort the pattern. When in doubt, observe, don't trade.

## Concept 4 — Confluence: Stacking ORB with Zones and VWAP

A signal is stronger when independent tools agree. This is **confluence.**

- **Supply/demand.** Take the long only if the OR-high break has **open space** above — room to the next supply zone. If a heavy supply zone sits just 20–30 points overhead, price will likely stall right into it; skip the trade. A breakout _into a wall_ is a low-probability trade no matter how clean the candle looks.
- **VWAP.** For longs, you want price **above VWAP** — it means the average buyer today is in profit and the institutional benchmark is being respected on the upside. A breakout _above_ the OR high while price is _below_ VWAP is fighting the day's average and is weaker.

```
Caption: Confluence check before an ORB long

  Supply zone ////////////////  ← is there OPEN SPACE to here? (target room)
                    ↑ target
  OR High ─────────────────────  ← break trigger
  VWAP  ~~~~~~~~~~~~~~~~~~~~~~~~   ← price should be ABOVE this for a long
  OR Low ──────────────────────
  Demand zone \\\\\\\\\\\\\\\\\  ← support below = confidence for longs

  GO long only if:  break holds + volume + above VWAP + open space up.
```

## Worked Examples

_All numbers below are illustrative and hypothetical — chosen to show the method, not to predict any real price. Index point values and lot sizes are set by the exchange/SEBI and change over time; treat the per-point rupee figures as teaching values._

### Example 1 — Bank Nifty ORB long (clean, with a retest)

**Setup (a hypothetical Tuesday):**

- 9:15–9:30 forms the range: **OR High = 48,120**, **OR Low = 47,980**. Range width = **140 points.**
- VWAP at 9:35 sits near 48,050 — price is _above_ it. Good.
- The next supply zone you marked is around 48,400 — roughly 280 points of open space above the high. Plenty of room.

**Tick by tick:**

- **9:40** — a 5-min candle _closes at 48,150_, clearly above the OR high, on volume noticeably larger than the prior three candles. That is a confirmed break, not a wick.
- **9:45** — instead of chasing, you wait. Price dips back to **48,125**, right at the old OR high, and forms a small bullish candle — the edge is holding as support. **Retest entry: buy at 48,130.**
- **Stop:** just below the retested edge / breakout candle low at **48,070** → **risk = 60 points.**
- **Target (measured move):** 48,130 + 140 = **48,270**, which is also short of the 48,400 supply zone. Reward = 140 points. **Reward:Risk = 140 : 60 ≈ 1:2.3** ✅
- **Outcome (illustrative):** by 10:15 price tags 48,275. You book most of the position at target and trail the rest. Trade closed well before the 3:20 PM square-off.

**Position sizing (paper account ₹1,00,000, risking 1% = ₹1,000):**

- Suppose the instrument you paper-trade moves ₹15 per point per lot (illustrative).
- Risk per lot = 60 points × ₹15 = **₹900.** That fits inside your ₹1,000 limit → **1 lot is takeable.**
- Notice how the _retest_ gave a 60-point stop instead of the \~150-point structural stop. Tighter risk made the trade fit your rule — the entry technique directly enabled the size.

### Example 2 — Nifty ORB that fakes out and stops you small (this is the point)

**Setup (a hypothetical Thursday, quieter day):**

- 9:15–9:30 range on Nifty: **OR High = 24,510**, **OR Low = 24,450.** Range width = only **60 points** — a narrow, low-energy box. Volume is unremarkable. This is a yellow flag, but you decide to try a strict retest entry only.

**Tick by tick:**

- **9:50** — a 5-min candle closes at **24,522**, just above the OR high, but volume is _only average_ — no real spike. Because you require confirmation, you wait for a retest rather than chasing the break.
- **9:55** — price pulls back to 24,508 and gives a small bullish candle at the edge. **Retest entry: buy at 24,512.**
- **Stop:** below the edge at **24,488** → **risk = 24 points.**
- **10:05** — the break has no follow-through. A larger red candle pushes price back _inside_ the range and through your stop. **Stopped out at 24,488 → loss = 24 points.** This was a **fakeout**: thin volume, narrow range, no fuel.
- **Rupee impact (illustrative, ₹1,00,000 account, ₹15/point):** 24 points × ₹15 = **₹360 lost ≈ 0.36% of capital.** Well within the 1–2% rule.

**Why this is a _good_ losing trade:** you respected the setup, took a _small_ defined loss, and did not average down or move your stop. The fakeout warning signs (narrow range, weak volume) were there — next time you'd likely **skip** it entirely and keep even that ₹360. Small losses on fakeouts are the cost of doing business; blowing up on one revenge trade is what ends careers. Over many trades, if your winners average \~2R and you keep losers to \~1R, the math works even when you're wrong often.

## Common Mistakes (and the fix)

1. **Trading the wick, not the close.** Beginners jump in the instant price pokes past the OR high. _Why:_ fear of missing the move. _Fix:_ wait for a full 5-min candle to **close** beyond the range; a wick that closes back inside is rejection.

2. **Ignoring volume.** Taking every break regardless of participation. _Why:_ the candle alone looks convincing. _Fix:_ require **volume expansion** on the breakout candle. No volume, no conviction, no trade.

3. **Moving or widening the stop when price approaches it.** _Why:_ the hope that "it'll come back." _Fix:_ the stop is set at the invalidation point _before_ entry and is **never** widened. If it's hit, the setup is wrong — accept the small, planned loss.

4. **Chasing a breakout straight into a supply/demand wall.** _Why:_ excitement about the move, blindness to overhead resistance. _Fix:_ check for **open space** to the next zone first. No room, no trade — the reward side of your ratio isn't there.

5. **Over-trading after 10:30 AM.** _Why:_ boredom, wanting action. _Fix:_ enforce the **time filter**. The ORB edge lives in the first hour; late "breakouts" are usually chop that dies before the 3:20 PM square-off.

## Nuances & Edge Cases

- **Gap opens change the picture.** If the market gaps far up or down at 9:15 (a big overnight move), the opening range may form _after_ an exhausted push. A break in the gap's direction can immediately reverse (a "gap-and-fail"). On large gaps, be more conservative — favour retests and open-space checks.
- **A tight range isn't automatically bad — but weak volume is.** Sometimes a tight morning range _coils_ before a strong afternoon move. The disqualifier is the _combination_ of tight range **and** limp volume, which signals no participants are engaged.
- **Bank Nifty moves faster than Nifty.** Bank Nifty is more volatile (banks are heavy, rate-sensitive) so its opening ranges are wider in points and its breakouts are quicker and sharper. Your point-based stops and targets will naturally be larger on Bank Nifty than on Nifty — size accordingly so the _rupee_ risk stays 1–2%.
- **Both edges can break in one morning.** Price can break the OR high, fail, then break the OR low. This is a range-day tell. If your first ORB trade fakes out, be _very_ selective about a second entry the same morning — you may simply be in a choppy, rangebound session with no edge.
- **MIS vs CNC matters for square-off.** Intraday product types like MIS are auto squared-off by the broker around **3:20 PM**; a delivery product (CNC) is not, but you are not holding overnight this course. Plan every ORB trade to complete well within the session.
- **Expiry and event days distort everything.** Weekly/monthly F&O expiry, RBI policy, the Union Budget, and US Fed nights all inject unusual volatility and gappy behaviour. As a beginner, mark these on a calendar and **observe** rather than trade the ORB on them.

## Day-by-Day (Mon–Fri)

- **Monday — Rules & first observation.** Re-read this lesson. Write the full ORB checklist in your own words in your journal (range → close beyond → volume → open space → above/below VWAP → stop → 1:2 target → time filter). Watch 9:15–9:30 live and mark Bank Nifty's OR high/low. _Do not trade._ **Observation target:** did price break out or stay inside by 10:30?
- **Tuesday — Spot the confirmation.** Mark the OR. When a 5-min candle closes outside, judge it: was volume expanded? Did it close beyond or just wick? Note the exact hypothetical entry, stop, and measured target on paper. Screenshot the chart. **Observation target:** find one _valid_ break and one _fakeout_ in the same session if you can.
- **Wednesday — First full paper trade.** Paper-trade ONE Bank Nifty ORB end to end using a **retest entry**: entry, structural or tight stop, measured/next-zone target, and correct 1% position size. Log it whether it wins or stops out. **Observation target:** did your actual reward:risk land at ≥ 1:2?
- **Thursday — Add confluence.** Before 9:15, mark supply/demand zones and note VWAP. Take a paper ORB only if it breaks toward **open space** and sits on the right side of VWAP. Skip any break into a nearby wall and **write why you skipped.** **Observation target:** log at least one deliberate _skip_ and the reason.
- **Friday — Review & refine.** Tally the week's paper trades: wins/losses, the _actual_ R:R achieved, and any rule you broke. Note how many losses were small fakeouts (good discipline) versus rule violations (fix these). Refine exactly **one** rule if the data supports it. **Observation target:** a one-paragraph written verdict on your own discipline.

## Key Takeaways

- The **opening range (9:15–9:30)** is the visible footprint of overnight orders colliding at the open — its high and low are the day's first battle lines. Never trade inside it.
- A **valid breakout** = close beyond the edge **+ volume expansion** (bonus: a holding retest). A poke-and-return on thin volume is a **fakeout** — the trap you must learn to avoid.
- Prefer the **retest entry**: it forces patience, cuts fakeouts, and gives a tighter, well-defined stop right below the broken level.
- Every trade has a **stop at the invalidation point** (never widened), targets **reward:risk ≥ 1:2**, and risks only **1–2%** of capital — and a small fakeout loss is a _successful_ execution of the plan.
- **Confluence multiplies edge**: trade breakouts toward **open space**, on the right side of **VWAP**, and skip breaks straight into supply/demand walls or on dead, low-volatility days.
- Respect the clock: ORB entries **9:30–10:30 AM**, everything closed before the \~**3:20 PM** intraday square-off.

## This Week's Milestone

You have a written, mechanical ORB rulebook **and** a journal of at least **3 paper ORB trades on Bank Nifty or Nifty** — each with a marked opening range, a volume-confirmed (or explicitly rejected) entry, a stop at a structural/invalidation point, a documented ≥ 1:2 target, and a correct 1–2% position size — **plus at least one logged trade you deliberately skipped and the reason why.** The proof isn't a winning week; it's that every entry, exit, and skip can be traced back to a written rule.

---

> **◀ Previous:** [Week 5 — The Four Indicators You Need](./week-05-indicators.md) &nbsp;|&nbsp; **Course Home:** [Lessons Index](./README.md) &nbsp;|&nbsp; **Next ▶:** [Week 7 — Your First Paper Trades](./week-07-first-paper-trades.md)
