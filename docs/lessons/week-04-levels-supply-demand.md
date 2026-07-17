# Week 4 — Support, Resistance, Supply & Demand

> **◀ Previous:** [Week 3 — Candlestick Patterns That Matter](./week-03-candlestick-patterns.md) &nbsp;|&nbsp; **Course Home:** [Lessons Index](./README.md) &nbsp;|&nbsp; **Next ▶:** [Week 5 — The Four Indicators You Need](./week-05-indicators.md)

*Goal: learn to read the price map — the horizontal zones where intraday moves stall, reverse, and accelerate — and understand the order-flow mechanics that create them.*

## Why This Week Matters

In Weeks 1–3 you learned what a candle is, how to read a chart, and how the trading day is structured (the 9:15 AM open, the mid-session drift, the ~3:20 PM auto square-off for intraday positions). You can now describe *what happened*. This week you begin to anticipate *where it might happen next*.

Almost every intraday decision — where to enter, where to place your stop-loss, where to book profit — is answered by one question: **at what price does the balance of buyers and sellers change?** Those prices are not random. They cluster at levels the market remembers, at levels where large unfilled orders sit, and at levels where trapped traders are desperate to get out at breakeven. Support, resistance, supply and demand are four names for the same underlying truth: **price moves between zones where order flow flips**.

Get this week right and everything downstream — breakout trading, VWAP, moving-average pullbacks, options strikes — becomes easier, because you will always be trading *at a level that means something*, never in the empty middle of a range where anything can happen. This is education, not advice; you are still paper-trading, and you will not touch real money until Week 12.

## Concept 1: Why Levels Form (the mechanism, not the folklore)

A price level "works" only because of what humans and institutions *did* at that price before. Three forces create memory in the market.

### Unfilled orders (the biggest reason)

Imagine a large institution — a mutual fund, an FII (Foreign Institutional Investor), a prop desk — wants to buy ₹500 crore of Reliance. It cannot buy that in one click; a market order that size would sweep the order book and push the price up against itself. So it places **limit buy orders** (orders to buy only at or below a chosen price) stacked around, say, ₹2,900. Price drops to ₹2,900, some of those orders fill, buying pressure appears, price bounces. But the institution did not get its *entire* size filled — the bounce happened before all its orders executed. Those **leftover unfilled orders still sit at ₹2,900.** The next time price returns, they fill again and price bounces again. That is support: a price with resting demand that has not been fully consumed.

### Memory and self-fulfilling behaviour

Once traders *see* a bounce at ₹2,900 on the chart, thousands of them mark it. Next time price approaches, they place buys there too. The level now works partly because everyone expects it to work. This is real, but it is the weaker force — crowd memory evaporates once the resting orders behind it are gone.

### Breakeven psychology (trapped traders)

Suppose price fell hard from ₹2,950 to ₹2,880. Everyone who bought around ₹2,950 is now sitting in a loss, feeling stupid. Their dominant wish is to "get out at what I paid." When price crawls back up toward ₹2,950, those trapped buyers dump their shares to escape at breakeven. That wave of selling is fresh supply — it caps price and creates resistance *exactly where the earlier buyers got stuck.* This is why old tops act as ceilings: they are populated by people praying to be made whole.

## Concept 2: Support and Resistance Are Zones, Not Lines

Beginners draw a single hair-thin line and then feel betrayed when price pokes ₹4 through it. The market does not respect your pixel. Orders are stacked across a *band* of prices, and different traders drew their line off slightly different candles. So treat every level as a **zone** — a rectangle with a top and a bottom.

Definitions:
- **Support** — a zone below current price where buying has repeatedly overwhelmed selling, so price tends to stop falling and bounce.
- **Resistance** — a zone above current price where selling has repeatedly overwhelmed buying, so price tends to stop rising and turn down.

How wide is the zone? Draw it from the **open/close cluster to the wick extreme** of the candles that formed the turn. On Nifty (index) a zone might be 15–25 points wide; on Bank Nifty, being more volatile, 40–70 points; on a stock like SBIN, ₹2–4. Intraday you will typically read zones off the **5-minute chart**, cross-checked against the 15-minute.

Diagram — support and resistance as zones, with two bounces each:

```
 Price
  ^
  |    ####### RESISTANCE ZONE #######   <- selling band
  |   /\        /\            /\
  |  /  \      /  \          /  \
  | /    \    /    \        /    \
  |/      \  /      \      /      \
  |        \/        \    /        (price oscillates
  |                   \  /          between the zones)
  |    ~~~~~~~ SUPPORT ZONE ~~~~~~~   <- buying band
  |        ^bounce      ^bounce
  +------------------------------------> Time
```

Notice price *enters* each zone and reacts *within* it — it does not reverse on a single exact number. Your job is to expect a reaction inside the band, not at one price.

## Concept 3: Trendlines and Market Structure

Horizontal zones tell you *where*. Market structure tells you *which direction* to trust between them.

### Reading structure: HH/HL vs LH/LL

Price moves in swings — a push up (a swing high), a pullback (a swing low), another push. Label each swing point:

- **Uptrend** = a sequence of **Higher Highs (HH)** and **Higher Lows (HL)**. Each rally exceeds the last peak; each dip stops above the last dip. Buyers are in control; you favour long (buy) setups and treat support zones as buy areas.
- **Downtrend** = **Lower Highs (LH)** and **Lower Lows (LL)**. Sellers control; favour short (sell) setups and treat resistance as sell areas.

Diagram — an intraday uptrend in Higher Highs / Higher Lows:

```
 Price
  ^                              HH
  |                     HH      /\
  |            HH      /\      /  \
  |   HH      /\      /  \    /
  |  /\      /  \    /    \  /
  | /  \    /    \HL/      \/HL
  |/    \HL/      \/
  |      \/       (each low HL sits ABOVE the prior low
  |               each high HH sits ABOVE the prior high)
  +------------------------------------> Time
       trendline drawn UNDER the rising HLs
```

The rising **trendline** is drawn connecting the Higher Lows. It is a *diagonal* dynamic support — as long as pullbacks respect it, the uptrend is intact.

### Break of Structure (BOS)

The trend is a story that stays true until it breaks. In an uptrend, the first time price makes a **Lower Low** — dropping below the most recent Higher Low — that is a **break of structure**. The character of the market has changed; buyers failed to defend their line. You stop trusting long setups until a new structure forms. BOS is your objective "the trend may be over" signal, far more reliable than a gut feeling that "it looks toppy."

## Concept 4: Role Reversal (the flip) and its mechanism

Here is one of the most useful ideas in trading: **once a support zone is decisively broken, it becomes resistance — and vice versa.** Old floor becomes new ceiling. This is called a role reversal or a "flip," and it happens for a concrete order-flow reason, not magic.

Walk through the mechanism. Price sat on support at ₹1,000 (say, ICICI Bank). Buyers there kept it up. Then heavy selling *breaks* through ₹1,000 and price falls to ₹985. Two things are now true:
1. The resting buy orders that made ₹1,000 support have been **consumed** — they filled as price fell through. The demand that defended the level is gone.
2. Everyone who bought at ₹1,000 believing it was support is now **trapped in a loss.** Their breakeven wish sits at ₹1,000.

When price rallies back to ₹1,000, those trapped buyers sell to escape, *and* short-sellers who like the new downtrend add fresh sells. Both waves hit at ₹1,000. The old support is now a wall of supply — resistance. The level kept its importance but flipped its role.

Diagram — role reversal: broken support becomes resistance:

```
 Price
  ^
  |                    rally back tests old floor
  |   \               /\  <- REJECTED here (now resistance)
  |    \    OLD      /  \
  | ----\--SUPPORT--/----\------  <- the flip level (₹1,000)
  |      \  (₹1000)      \
  |       \  break        \  new
  |        \  down         \ downtrend
  |         \/              \/
  |        breaks           LL
  +------------------------------------> Time
      support HELD... then BROKE... then CAPPED as resistance
```

The flip gives you a high-quality trade: after the break, you wait for price to retest the old level from the other side and enter in the new direction, with a tight stop just beyond it.

## Concept 5: Supply and Demand Zones in Depth

Supply and demand is a more precise, more mechanical way of finding levels. Instead of connecting old wick-tops by eye, you find the exact candles where a large imbalance of orders launched price away. The logic: **big players leave a footprint, and price often returns to that footprint to fill their remaining orders.**

### Base + departure: the anatomy of a zone

Every real zone has two parts:
1. **The base** — one or a few small, tight, sideways candles. This is where the big order sat *accumulating* (buying quietly) or *distributing* (selling quietly). Small candles = balance, orders resting.
2. **The departure** — one or more big, strong candles that rocket away from the base. This is the *imbalance* — demand so far exceeded supply (or vice versa) that price had to run to find the other side.

The base is the zone you draw. The strong departure is your *proof* that serious unfilled orders live there. No strong departure = no real zone, just noise.

### The four curves

Every zone is one of four shapes, named by what comes in and what goes out (R = Rally/up, D = Drop/down, B = Base):

```
DEMAND zones (expect price to bounce UP):
  RBR  Rally - Base - Rally    (up, pause, up again = continuation)
  DBR  Drop - Base - Rally     (down, pause, reverse up = reversal)

SUPPLY zones (expect price to drop DOWN):
  DBD  Drop - Base - Drop      (down, pause, down again = continuation)
  RBD  Rally - Base - Drop     (up, pause, reverse down = reversal)
```

- **RBR** and **DBR** are **demand** zones — the departure was *upward*, so buyers dominate there. You look to buy on a return.
- **DBD** and **RBD** are **supply** zones — the departure was *downward*, so sellers dominate. You look to sell on a return.

Reversal zones (DBR, RBD) mark tops and bottoms; continuation zones (RBR, DBD) mark pauses inside a trend and are excellent for joining a move.

### Drawing a tight zone precisely

Precision matters because it defines your risk. For a **demand** zone:
- **Top of zone (proximal line)** = the highest *body/open* among the base candles (the level price first reaches on the way back).
- **Bottom of zone (distal line)** = the lowest *wick* of the base (the deepest point orders could sit).

For a **supply** zone, mirror it: bottom = lowest body of the base, top = highest wick. A good intraday zone is *tight* — the smaller the base, the sharper your entry and the smaller your stop.

### Fresh vs tested — and why tested zones weaken

This is the single most important nuance beginners miss. A **fresh** zone has never been retested since it formed — all the institutional unfilled orders are still sitting there. A **tested** zone has already been revisited once; on that visit, a chunk of the resting orders **got consumed** to produce the bounce. Each subsequent test eats more of the remaining orders. So a fresh zone is strongest, the first test is reliable, and by the third or fourth touch the zone is often hollowed out — the orders are gone, and price slices through. **Prefer fresh zones. Every test weakens a level; it does not strengthen it.** (This is the exact opposite of the naive belief that "the more times a level is tested, the stronger it is.")

### Zones nest across timeframes

A demand zone you spot on the 5-minute chart often sits inside a larger demand zone on the 15-minute or 60-minute chart. When they align — a fresh 5-min demand sitting on a fresh 15-min demand — you have a **confluence**, the highest-probability spot on the chart. Bigger-timeframe zones hold more institutional size and matter more; when a small-timeframe zone contradicts a big one, trust the big one.

### Why zones beat plain lines for intraday timing

Plain S/R tells you a general area. A supply/demand zone gives you a **precise proximal edge to enter at and a precise distal edge to hide your stop behind**, which produces a *smaller, better-defined risk* and therefore a better reward-to-risk ratio. Intraday you have minutes, not days — the tight zone lets you enter fast and know instantly (if the distal breaks) that you were wrong.

## Worked Examples

*All numbers below are hypothetical and illustrative — chosen to teach the mechanics, not to predict any real price.*

### Example 1 — Fresh RBR demand zone on Bank Nifty (continuation long)

Setup: It is 10:20 AM IST. Bank Nifty (an index; traded intraday via futures/options in lots — you are paper-trading the index level) is in a clear 5-min uptrend, printing Higher Highs and Higher Lows.

Tick-by-tick reasoning:
- From 9:45–10:00 price rallied from 48,200 to 48,500 (a strong **Rally**).
- From 10:00–10:15 it went sideways in a tight band 48,470–48,500, three small candles (a **Base** — big buyer resting orders accumulating).
- At 10:15 a large green candle blasts from 48,490 to 48,720 (the **Departure Rally**). That is an **RBR** demand zone. The strong departure proves unfilled buy orders remain in the base.
- I draw the zone: proximal (top) = 48,500 (highest base body), distal (bottom) = 48,470 (lowest base wick). Zone width = 30 points.
- At 10:35 price pulls back and re-enters the zone, touching 48,505. It is **fresh** (first test) and it is a *continuation* zone in an uptrend — high probability.
- **Entry:** buy limit at 48,500 (the proximal edge).
- **Stop-loss:** 48,455, just below the distal line (a few points buffer). Risk = 45 points.
- **Target:** reward:risk of at least 1:2 → 90+ points → 48,590, and the prior swing high at 48,720 as a second target. I risk only 1–2% of my paper capital on this trade, sized so 45 points of loss = that 1–2%.
- Outcome logic: buyers' resting orders fill, price lifts off 48,500, I trail my stop under each new Higher Low. If instead price closes a 5-min candle below 48,455, the zone failed (orders were weaker than they looked) — I am out for a small, pre-defined loss. That is a good trade *whether or not it wins*, because the process was correct.

### Example 2 — RBD supply zone flip on Reliance (reversal short)

Setup: 11:10 AM IST, Reliance. Price had been climbing all morning but momentum is fading.

- 10:40–10:55: price rallies to 2,948 (**Rally**).
- 10:55–11:05: two small doji-like candles stall at 2,945–2,950 (**Base** — sellers quietly distributing).
- 11:05: a big red candle drops from 2,946 to 2,910 (**Departure Drop**). That is an **RBD** supply zone — a reversal top. Proximal (bottom, for supply we enter at the lower edge on the way up... note for supply the proximal is the *bottom* of the base that price reaches first from below) — here I mark proximal = 2,945, distal (top) = 2,950. Zone = 5 points wide (tight — good).
- Meanwhile price also just made a **Lower Low** at 2,910, breaking the morning's rising structure → a **Break of Structure**. Trend character has flipped from up to down. Now I *want* short setups.
- 11:25: price retraces up and re-enters the supply zone at 2,946 — a **fresh** RBD test, in confluence with the BOS.
- **Entry:** sell (short) at 2,945.
- **Stop-loss:** 2,954, just above the distal high. Risk = ₹9.
- **Target:** ≥1:2 → ₹18+ → 2,927, with the recent swing low 2,910 as second target.
- Mechanism recap: the trapped buyers from 2,948 plus fresh short-sellers hit price at the zone, resting sell orders overwhelm buying, price rolls over. If a 5-min candle closes above 2,954, the supply is exhausted and I exit small.

## Common Mistakes (and the fix)

**1. Drawing levels as exact lines.** Beginners mark 48,500.00 and get stopped out by a 3-point wick. *Why:* charts look precise, so people assume the market is. *Fix:* always draw a zone (a rectangle) and expect a reaction *within* it, with your stop a small buffer beyond the far edge.

**2. Believing more touches = stronger level.** Beginners pile in on the fourth bounce, then get crushed. *Why:* it feels intuitive that a "proven" level is safer. *Fix:* the opposite is true — each touch *consumes* resting orders. Favour fresh zones and first tests; be sceptical after three touches.

**3. Trading levels in the empty middle.** Beginners buy or sell anywhere. *Why:* impatience and fear of missing out. *Fix:* only take trades *at* a meaningful zone or after a clean break-and-retest (flip). In the middle of a range, anything can happen and your risk is undefined.

**4. Ignoring the higher-timeframe context.** Beginners short a 5-min supply zone that sits right on top of a massive 15-min demand zone — and get run over. *Why:* they zoom in and forget the bigger picture. *Fix:* mark 15-min and 60-min zones first, then trade the 5-min *in agreement* with them. Big timeframe wins ties.

**5. No stop, or a stop inside the zone.** Beginners place the stop where price naturally wiggles and get shaken out, or skip the stop entirely. *Why:* they fear taking the loss. *Fix:* the stop belongs *beyond the distal line*, and you risk only 1–2% per trade. A stop is the price at which your idea was proven wrong, not a suggestion.

## Nuances & Edge Cases

- **Round numbers act as psychological zones.** Nifty 24,000, Bank Nifty 50,000, Reliance ₹3,000 — humans cluster orders at round figures, so these behave like extra zones even without prior structure.
- **The opening 15 minutes distort levels.** The 9:15–9:30 auction is noisy; yesterday's close, today's open, and overnight gaps redraw the map. Let structure form before trusting intraday zones.
- **Zones expire intraday.** A demand zone from 9:30 may be irrelevant by 2:00 PM after a strong trend day has consumed everything. Freshness has a time dimension too.
- **A break needs conviction, not a wick.** A single wick poking through a level is often a liquidity grab (stop hunt), not a real break. Wait for a *candle body close* beyond the zone before calling it broken and expecting a flip.
- **MIS auto square-off skews late-day levels.** Because intraday (MIS) positions are force-closed by the broker around 3:20 PM, the last 30 minutes can see mechanical selling/buying unrelated to any zone. Don't over-interpret 3:00–3:20 reactions.
- **Zone within a strong trend > counter-trend zone.** A demand zone that asks you to buy against a powerful downtrend is fighting the tide. Prefer zones that let you trade *with* structure.

## Day-by-Day (Mon–Fri)

- **Monday — Horizontal zones.** On the Nifty 5-min chart, mark yesterday's high, yesterday's low, and today's obvious swing turns as *zones* (rectangles), not lines. *Observation target:* watch price interact with two of your zones today and note whether it reacted inside the band or ignored it.
- **Tuesday — Market structure.** On Bank Nifty 5-min, label every swing HH/HL/LH/LL for the whole session and draw the trendline. *Observation target:* identify the exact candle of the first Break of Structure and note the time it happened.
- **Wednesday — Role reversal.** Find one clean example where a support zone broke and later capped price as resistance (or vice versa) on any of Reliance, HDFC Bank, or SBIN. *Observation target:* screenshot the flip and write one sentence on the trapped-trader mechanism behind it.
- **Thursday — Supply & demand zones.** On ICICI Bank and Infosys 5-min, find and classify at least four zones as RBR, DBR, DBD, or RBD. Draw proximal and distal lines precisely. *Observation target:* mark which are fresh vs already tested.
- **Friday — Paper-trade two zone setups.** Take two hypothetical trades at *fresh* zones in agreement with structure. Log entry, stop (beyond distal), target (≥1:2), and the RBR/RBD/BOS reason. *Observation target:* record whether each held or broke, and why.

## Key Takeaways

- Levels form because of **unfilled institutional orders, crowd memory, and trapped-trader breakeven psychology** — not chart magic.
- Trade **zones (bands), never exact lines**, and place stops just beyond the far (distal) edge.
- **Market structure (HH/HL vs LH/LL) tells you direction**; a Break of Structure is your objective trend-change signal.
- A broken level **flips role** (support↔resistance) because its orders are consumed and its buyers are trapped.
- Supply/demand zones = **base + strong departure**, in four shapes (RBR, DBR = demand; DBD, RBD = supply); **fresh beats tested**, and higher-timeframe zones win.
- Every trade needs a stop-loss, risk of only 1–2%, and reward:risk ≥ 1:2 — process over outcome.

## This Week's Milestone

On a single 5-minute chart of Nifty or Bank Nifty, you can independently: (1) mark at least three zones as rectangles, (2) label the market structure and point to any Break of Structure, (3) classify each zone as RBR/DBR/DBD/RBD and mark it fresh or tested, and (4) draw one complete hypothetical trade — entry at the proximal edge, stop beyond the distal edge, target at ≥1:2 — with a written one-line reason grounded in order-flow mechanics. Do that unaided and Week 4 is done.

---

> **◀ Previous:** [Week 3 — Candlestick Patterns That Matter](./week-03-candlestick-patterns.md) &nbsp;|&nbsp; **Course Home:** [Lessons Index](./README.md) &nbsp;|&nbsp; **Next ▶:** [Week 5 — The Four Indicators You Need](./week-05-indicators.md)
