# Week 2 — Candlestick Anatomy

> **◀ Previous:** [Week 1 — How the Market Actually Works](./week-01-market-basics.md) &nbsp;|&nbsp; **Course Home:** [Lessons Index](./README.md) &nbsp;|&nbsp; **Next ▶:** [Week 3 — Candlestick Patterns That Matter](./week-03-candlestick-patterns.md)

_Goal: learn to read a single candlestick fluently in real time — what each part means, why it forms the way it does, and why the 5-minute candle becomes your intraday home base._

## Why This Week Matters

Last week you watched Nifty and Bank Nifty move up and down on a live screen. It probably looked like chaos — numbers ticking, colours flickering. This week you learn the alphabet that chaos is written in.

Everything in intraday trading — the levels you will draw in Week 4, the opening-range breakout you will trade in Week 6, the entries and stops you will risk paper money on in Week 7 — is ultimately a decision made by reading candles. A candlestick is not decoration. It is a compressed record of a battle: over some fixed slice of time, buyers and sellers fought, and the candle is the scoreboard. Four numbers, one shape, one story.

If you cannot read one candle cleanly, no pattern, indicator, or strategy built on top of candles will make sense — you will just be memorising shapes. So this week is slow and deliberate on purpose. By Friday you should be able to glance at any 5-minute candle on Bank Nifty and narrate, in one sentence, who won that five minutes and where price got rejected. That fluency is the foundation the next ten weeks stand on.

## Concept 1 — OHLC and How a Candle Forms in Real Time

Every candle covers a **fixed slice of time** and records exactly four prices:

- **Open (O)** — the price at the very first tick of that slice.
- **High (H)** — the highest price touched anywhere inside the slice.
- **Low (L)** — the lowest price touched anywhere inside the slice.
- **Close (C)** — the price at the very last tick of that slice.

The word "tick" means a single change in the traded price. On a liquid instrument like Bank Nifty, ticks arrive many times per second as trades execute.

### The four numbers are not created at the same time

This is the single most important idea beginners skip, so watch a 5-minute candle build live and you will see it happen:

1. **The Open locks first and never moves.** At 10:00:00 AM IST, the first trade of the new 5-minute slice prints — say Nifty trades at 23,450. That is the Open. It is frozen for the entire candle. Nothing that happens for the next five minutes can change it.
2. **The High and Low breathe outward.** For the next five minutes, every time price trades higher than the highest it has been so far, the High extends up. Every time it trades lower than the lowest so far, the Low extends down. They only ever move _away_ from each other — the High can rise and the Low can fall, but neither ever retreats. The candle's total height (High minus Low) can only grow, never shrink, as the slice progresses.
3. **The Close is whatever price is trading at the instant the slice ends.** At 10:04:59, whatever the last trade is becomes the Close, and the candle is finalised — it never changes again. A brand-new candle opens at 10:05:00.

So while a candle is _live_, only the Close is uncertain, and it is dancing around in real time. This is why experienced traders say "wait for the candle to close" — until the slice ends, the shape you see can still transform completely.

Diagram — how a single 5-minute candle builds, tick by tick:

```
 10:00:00        10:01           10:03          10:04:59
 open locks      pushes up       gets sold      closes
   |               |  H            |  H            |  H
   O ●            O ● ↑          O ●   ↑         O ●
                                   ↓ C             |
                                                  ● C  (final)
                                   |  L            |  L
 "Open fixed"   "High extends"  "Low extends,   "Close locks;
                                 close falls"    candle done"
```

## Concept 2 — Body vs Wicks: Reading the Battle

Once a candle closes, its shape has two parts.

The **body** is the thick block — the distance between the Open and the Close. The **wicks** (also called shadows or tails) are the thin lines poking out above and below the body — they reach up to the High and down to the Low.

- The **upper wick** measures how far price pushed _above the body_ and then got forced back down before the close. Buyers reached up there; sellers slapped them back.
- The **lower wick** measures how far price fell _below the body_ and then got bought back up before the close. Sellers pushed down there; buyers absorbed them.

Fully labelled bullish and bearish candles:

```
   BULLISH (green)              BEARISH (red)
        │  ← High                   │  ← High
        │  upper wick               │  upper wick
      ┌───┐ ← Close               ┌───┐ ← Open
      │   │                       │   │
      │   │  body                 │   │  body
      │   │                       │   │
      └───┘ ← Open                └───┘ ← Close
        │  lower wick               │  lower wick
        │  ← Low                    │  ← Low

 Close ABOVE Open = buyers    Close BELOW Open = sellers
 won the slice.               won the slice.
```

Notice the crucial asymmetry: **on a green candle the Open is at the bottom of the body and the Close at the top; on a red candle it flips** — Open at the top, Close at the bottom. Colour alone tells you the direction; you read the exact Open and Close from which end of the body they sit on.

### The mechanism: what wicks actually are in the order book

Think about _why_ a wick forms. Underneath every candle is an **order book** — a live ladder of buy orders (bids) stacked below the current price and sell orders (asks/offers) stacked above it. Price moves up when buyers are aggressive enough to consume all the sell orders at one level and reach for the next. It moves down when sellers consume all the buy orders at a level.

A long upper wick means: aggressive buyers ate through the offers and pushed price up — but at the higher prices, a wall of sellers appeared (big offers, and buyers running out of appetite), those sellers overwhelmed the buyers, and price got pushed back down before the slice closed. The wick is the _footprint of a failed push_. That is why a long wick is called **rejection** — the market visited that price and rejected it.

Order-book sketch behind a long upper wick (rejection at the top):

```
 PRICE      ORDERS RESTING              WHAT HAPPENED
 23,510   ████████ big offers  ← sellers waiting here → wick top
 23,505   ██ thin offers       ← buyers ate through these ↑
 23,500   █ (open level)       ← price started here, O
 ...
 23,495   ██████ bids          ← price closed back down here, C

 Buyers pushed to 23,510, hit a wall of sellers,
 got forced back to 23,495 by the close = long upper wick.
```

## Concept 3 — Body Size and Wick Shapes: the Full Spectrum

The _proportions_ of body to wick are the real information. Learn to read the spectrum.

- **Big body, tiny wicks** — one side dominated with conviction and held control right into the close. A long green body on Reliance says buyers pushed steadily and closed near the high: strong, committed demand.
- **Small body, long wicks on both sides (a "spinning top")** — a fight with no winner. Price ranged widely but closed near where it opened. This is **indecision**, and it shows up at the start of ranges and often just before a reversal or a pause.
- **A candle with almost no body at all (a "doji")** — Open and Close are nearly identical. Perfect balance; the market is undecided.
- **Long wick on one side only** — directional rejection. A long _lower_ wick with the body up top means sellers tried to push down and got firmly rejected by buyers (bullish hint). A long _upper_ wick with the body down low means buyers tried to push up and got rejected by sellers (bearish hint).
- **Marubozu** — a big body with _no wicks at all_ (or almost none). The name is Japanese for "bald head." A green marubozu means price opened at the low, went straight up, and closed at the high — one side controlled every single tick of the slice. It is the strongest single-candle statement of conviction there is.

The candle-shape spectrum and what each tells you:

```
 MARUBOZU   BIG BODY   SMALL BODY  SPINNING    LONG-LOWER   DOJI
 (no wick)  small wick  small wick    TOP         WICK
   ┌─┐        │           │           │            │          │
   │ │       ┌─┐         ┌─┐         ┌─┐          ┌─┐        ─┼─
   │ │       │ │         └─┘        ┌┴─┴┐         └─┘         │
   │ │       │ │          │         └───┘          │          │
   └─┘       └─┘          │           │            │          │
                          │                        │
 total      strong      mild       indecision   rejection   perfect
 control    conviction  lean       (no winner)  of lows     balance
```

## Concept 4 — Timeframes: the Same Move Looks Different

The **timeframe** sets how much time each candle covers. On NSE intraday you will mostly meet 1-minute, 5-minute, 15-minute, 60-minute, and the daily candle. The critical insight: **the same price move looks completely different depending on the timeframe you view it through**, because a higher timeframe candle is simply a bundle of lower timeframe candles compressed into one.

Concretely: one 5-minute candle is made of five 1-minute candles. Its Open is the first 1-min Open, its Close is the fifth 1-min Close, its High is the highest High across all five, and its Low is the lowest Low across all five. Zoom out and detail collapses into a single shape.

The same 15-minute swing shown on three timeframes:

```
  1-MINUTE (15 candles)        5-MINUTE (3 candles)     15-MIN (1)
  lots of noise & wicks        cleaner structure        one shape
   │ │  ┌┐ │                         │                      │
   ┌┐└┐┌┘└┐┌┐  ┌┐               ┌─┐  │   ┌─┐              ┌───┐
   ││ └┘  └┘└┐┌┘└┐              │ │ ┌┴┐  │ │              │   │
   └┘        └┘  │              └─┘ │ │  └─┘              │   │
                 │                  └─┘                   └───┘

  Same 15 minutes of price. The 1-min shows every wobble;
  the 5-min keeps the shape; the 15-min is one clean candle.
```

### Why 5-minute is the intraday workhorse

- **1-minute** is fast and noisy. Every tiny wobble becomes a candle, and most of those wicks are meaningless flickers. It overwhelms beginners and produces dozens of fake signals. It is useful later for precise entries, not for learning to read.
- **5-minute** is the sweet spot. It has enough detail to show real structure, but it filters out the panic-inducing noise — a burst of ticks on 1-min becomes one tidy 5-min candle. A full session (9:15 AM to 3:30 PM IST) is exactly **75 five-minute candles**, which fits readably on one screen. This is your home timeframe for the entire roadmap.
- **15-minute** is slower and cleaner. Use it for **context** — the day's overall bias and the big levels — before you zoom into the 5-min to act.
- **60-minute and daily** give you the multi-day backdrop: is this instrument in an uptrend or downtrend over the past weeks? Glance, don't live-watch.

The professional habit you are building: **read the 15-min for bias, act on the 5-min.** Never let the 1-min's noise make your decisions this year.

## Concept 5 — Context: a Green Candle Can Still Be Bearish

A beginner sees green and thinks "up, good." But a candle's meaning depends entirely on **where it sits** relative to the candles around it and the levels on the chart. Colour is a fact; meaning is context.

Consider a green candle — Close above Open, buyers technically won that slice. But suppose it printed with a tiny body and a huge upper wick, right at a price where Nifty was rejected twice yesterday. Buyers pushed up into that ceiling and got swatted down; they closed green only because they closed a hair above the open, but the _story_ is sellers defending a level. That "green" candle is a warning, not a green light.

The reverse is true too: a small red candle after a strong run up, with a long lower wick, often means sellers barely managed to nudge price down and buyers immediately bought the dip — that red candle can be quietly bullish.

The lesson: never read a candle in isolation once you have context. Ask three questions every time — (1) What is the body/wick telling me about this slice? (2) Where is this candle sitting (near a level, mid-air, after a big move)? (3) What did the candles just before it do?

## Concept 6 — Reading a Sequence as Momentum, and Pairing Volume

One candle is a word. A _sequence_ of candles is a sentence — and the sentence tells you about **momentum**, the tendency of price to keep moving in one direction.

- **Several green candles with rising or steady bodies, each closing near its high, each opening near the previous close** = strong upward momentum. Buyers keep control slice after slice.
- **Bodies shrinking while the trend continues** = momentum fading. The move is running out of fuel even though price still drifts up. Often precedes a pause or reversal.
- **A sudden big opposite-colour body that engulfs the prior candle** = a potential shift in who is in control. (You will name these formally as patterns next week.)

### Volume: the conviction meter

**Volume** is the number of shares or contracts traded during the candle's time slice, shown as a bar under the chart. It measures _participation_ — how much real money was behind the move. Volume is the truth-serum for candle size.

- A **big body on big volume** is trustworthy: many participants agreed and committed. A green marubozu on Reliance with volume far above the recent average means real institutional demand, not a fluke.
- A **big body on thin volume** is suspect: price moved a lot but few people traded, so it can reverse just as easily. Common in the sleepy midday lull (roughly 12:00–1:30 PM IST).
- A **breakout candle on surging volume** carries far more weight than the same candle on quiet volume — this is the core of why breakouts are traded with a volume filter (Week 6).

Rule of thumb to internalise this week: **size shows what price did; volume shows whether to believe it.**

## Worked Examples

### Example 1 — A rejection candle on Bank Nifty (hypothetical)

It is 9:45 AM IST. You are watching **Bank Nifty** on the 5-minute chart. The 9:45 candle closes with:

- Open: 51,000
- High: 51,090
- Low: 50,985
- Close: 50,955

Let's decode it tick by tick. The Open locked at 51,000. Over the five minutes, buyers pushed price up and the High extended to 51,090 — that's 90 points above the open. But sellers appeared up there, overwhelmed the buyers, and drove price all the way back down; the Low reached 50,985 and the candle closed at 50,955, _below_ the open.

- Body = 51,000 → 50,955 = a **red** body of 45 points (Open at top, Close at bottom).
- Upper wick = 51,090 − 51,000 = **90 points** — very long.
- Lower wick = 50,955 − 50,985 = 30 points.

```
       │   ← High 51,090
       │   long upper wick (90 pts)
     ┌───┐ ← Open 51,000
     └───┘ ← Close 50,955
       │   ← Low 50,985
```

Story: buyers tried hard and got crushed. The long upper wick is **rejection at the highs**. Now add context — suppose 51,090 is exactly where Bank Nifty stalled and reversed yesterday afternoon. That makes this a level being _defended by sellers_ two days running. If the next 5-min candle is also red and closes lower, that is a momentum sentence forming: sellers in control. You are not trading this yet — you are learning to _hear_ it. (Note: illustrative numbers, not a forecast.)

### Example 2 — Comparing timeframes on Reliance (hypothetical)

It is 11:00 AM IST. **Reliance** makes a clean 15-minute push from ₹2,900 up to ₹2,918, then drifts back to ₹2,912 by 11:15.

On the **1-minute** chart, those 15 minutes are fifteen separate candles: a couple of green pushes, a red pullback to ₹2,906, another green leg to ₹2,918, then a fade — a jagged, wick-heavy mess that could scare you out of a good move.

On the **5-minute** chart, the same span is three candles: a strong green body 2,900→2,910, a green body 2,910→2,918 with a small upper wick, and a small red body 2,918→2,912 with an upper wick. Clean, readable: a two-candle rally, then a pullback with rejection at the top.

On the **15-minute** chart, it is **one** candle: Open 2,900, High 2,918, Close 2,912 — a green body with a modest upper wick. One shape.

```
  1-MIN: ┌┐└┐┌┐ ┌┐┌┐└┐  (jagged, 15 candles — noise)
  5-MIN: ┌─┐ ┌─┐ ┌┐      (3 candles — a rally + pullback)
 15-MIN: ┌───┐            (1 candle — green, upper wick)
```

Same money, same fifteen minutes — three different pictures. The 1-min would have you panicking on the pullback to 2,906; the 5-min lets you see it was a healthy pause inside an up-move; the 15-min confirms the bias is up. This is exactly why you read bias on the higher timeframe and act on the 5-min. Now pair volume: if the two green 5-min candles printed on volume well above Reliance's morning average and the red pullback came on thin volume, that says buyers committed and sellers barely showed up — a strong, believable move. (Illustrative only.)

## Common Mistakes (and the fix)

1. **Reading a candle before it closes.** Beginners see a live candle turn into a big green body and jump in — then it closes as a red rejection because the Close swung in the last thirty seconds. _Why they do it:_ the live candle looks decided. _Fix:_ until the 5-min slice ends, only the Close is uncertain, and it can flip the whole shape. Wait for the close before you judge a candle.

2. **Treating colour as the whole story.** "Green = buy, red = sell." _Why:_ it's the most visible feature. _Fix:_ a green candle at a resistance level with a huge upper wick is a _warning_, not a green light. Always read body-vs-wick and context, not just colour.

3. **Living on the 1-minute chart.** Beginners crave action and drop to 1-min, then get shaken out by noise and fake wicks. _Why:_ it feels faster and more exciting. _Fix:_ commit to 5-min as home base. One 1-min flicker is meaningless; the 5-min filters it into signal.

4. **Ignoring volume entirely.** Judging a big body as "strong" without checking if anyone traded it. _Why:_ volume bars are easy to overlook. _Fix:_ every time you call a candle "strong," glance at its volume bar. Big body + thin volume = don't trust it, especially at midday.

5. **Confusing Open/Close position between green and red candles.** Beginners assume the top of the body is always the Close. _Why:_ they learned it on a green candle. _Fix:_ remember the flip — green has Close on top, red has Open on top. The colour tells you which.

## Nuances & Edge Cases

- **The daily gap and the first candle.** The 9:15 AM candle's Open is often _not_ equal to yesterday's Close — NSE has an opening auction (the pre-open session, 9:00–9:15 AM) that sets the opening price based on overnight news and global cues. So the first 5-min candle can open with a "gap." Don't read that gap as intra-slice buying; it happened before the session.

- **Wicks depend on where the highs and lows occurred in time, which the candle hides.** A candle with equal upper and lower wicks doesn't tell you the _order_ — did price spike up then down, or down then up? The 5-min candle compresses that away. If the sequence matters, drop to 1-min briefly to see it, then come back.

- **Thin instruments make ugly, misleading wicks.** A single large order in an illiquid stock can create a huge wick that means nothing about a real battle — it's just one trade in a thin book. Index instruments (Nifty, Bank Nifty) and large caps (Reliance, HDFC Bank, ICICI Bank, SBIN, Infosys) are liquid, so their wicks are more meaningful. Beware reading wick-drama on small, thinly traded names.

- **The close near 3:30 PM is distorted by square-off flows.** Because intraday (MIS) positions are auto-squared-off by brokers around **3:20 PM IST**, the last candles of the day carry a wave of exit orders that aren't fresh opinions on direction. Candles in the 3:15–3:30 window can look violent for mechanical reasons.

- **"Doji" and "spinning top" are context-dependent, not automatic signals.** A doji in the middle of a quiet range means nothing; the same doji after a long run into a key level can flag exhaustion. The shape is a hint; the location supplies the meaning.

## Day-by-Day (Mon–Fri)

- **Monday — Set up and freeze your workspace.** On TradingView or your broker (Zerodha Kite, Upstox), load **NIFTY** and **BANKNIFTY** as **Candlesticks** on the **5-minute** timeframe, timezone confirmed as **IST (UTC+5:30)**, no indicators, volume bars ON. Screenshot the layout. _Observation target:_ confirm the day has \~75 five-minute candles from 9:15 to 3:30.

- **Tuesday — Watch a candle build live.** From 9:15–9:35 AM, stare at ONE forming Bank Nifty 5-min candle at a time. Watch the Open lock, the High/Low extend, the Close dance until the slice ends. _Observation target:_ catch at least one candle whose colour flips in the final minute before close.

- **Wednesday — Timeframe comparison.** Put Reliance on 1-min, 5-min, and 15-min side by side and follow one 15-minute move across all three. _Observation target:_ write one sentence on how many candles the same move became on each, and how the noise changed.

- **Thursday — Wick and volume hunt.** On HDFC Bank and ICICI Bank 5-min, mark 3 long-upper-wick candles and 3 long-lower-wick candles. For each, note its volume bar relative to neighbours. _Observation target:_ find one long-wick candle on high volume and one on low volume, and say which you'd trust.

- **Friday — The battle drill.** Pick 10 random 5-min candles across SBIN and Infosys. For each, write the OHLC story in one sentence: who dragged the rope, who was holding it at the whistle, where price got rejected. _Observation target:_ narrate all 10 without hesitating.

## Key Takeaways

- A candle is a scoreboard for a fixed time slice: **Open locks first, High/Low extend outward, Close locks last** — and only the Close is uncertain while the candle is live.
- The **body** shows who won and how strongly; **wicks** show where price was rejected — a long upper wick is sellers defending highs, a long lower wick is buyers defending lows.
- The **same move looks different on every timeframe**; a higher timeframe candle is just a bundle of lower ones. Read **15-min for bias, act on 5-min**, ignore 1-min noise for now.
- **Colour is a fact, meaning is context** — a green candle at resistance with a huge upper wick is a warning, not a buy signal.
- **Volume is the conviction meter**: size shows what price did, volume shows whether to believe it.
- This is pure observation. **No real money until Week 12** — you are building the reading fluency everything else depends on.

## This Week's Milestone

You can point at any 5-minute candle on Nifty or Bank Nifty and, in one sentence and without hesitating, state its full OHLC story — who won the slice, how strongly, where price got rejected, and whether the volume backs it up.

---

> **◀ Previous:** [Week 1 — How the Market Actually Works](./week-01-market-basics.md) &nbsp;|&nbsp; **Course Home:** [Lessons Index](./README.md) &nbsp;|&nbsp; **Next ▶:** [Week 3 — Candlestick Patterns That Matter](./week-03-candlestick-patterns.md)
