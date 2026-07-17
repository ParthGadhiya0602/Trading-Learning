# Supply & Demand for Intraday Trading

_How to find the exact price zones where intraday moves begin - and trade from them._

Support & resistance tells you _roughly_ where price reacted before. **Supply & demand** tells you _why_ it reacted and gives you a tighter, higher-probability zone to trade from. For NSE intraday (Nifty, Bank Nifty, and liquid stocks), this is one of the most practical edges a beginner can learn.

> ⚠️ Education only, not financial advice. Zones improve _probability_, never certainty. Every trade still needs a stop-loss and correct position size.

---

## 1. The core idea

Big institutions (banks, funds) can't buy or sell their huge quantity in one click without moving the price against themselves. So they leave **unfilled orders** sitting at specific price levels. When price returns to those levels, the leftover orders fire and push price away again.

- **Demand zone** = a price area where strong _buying_ appeared. Price is likely to bounce **up** from it. (Think: a floor with hidden buy orders.)
- **Supply zone** = a price area where strong _selling_ appeared. Price is likely to drop **down** from it. (Think: a ceiling with hidden sell orders.)

The tell-tale sign of a zone: **a small consolidation (a "base") followed by a big, fast candle away from it.** That explosive move is the footprint of institutional orders.

---

## 2. How a zone is built: Base + Departure

Every zone has two parts:

1. **Base** - one to a few small candles where price pauses (buyers and sellers balanced).
2. **Departure** - a strong, big-bodied candle (or two) leaving the base quickly.

```
DEMAND ZONE (buy zone)              SUPPLY ZONE (sell zone)

        ┌─┐ big green departure       ▲ price came up into zone
        │ │                           │
        │ │                        ┌──┴──┐  base (small candles)
   ┌──┐ │ │                        │     │  ← draw zone here
   │  │─┘ │  base (small candles)  └──┬──┘
   └──┘   │  ← draw zone here          │
          │                            │
     price drops back to base,    ┌─┐  │ big red departure
     buyers fire → bounce up      │ │──┘
                                  │ │
                                  ▼ price drops away
```

**Four combinations** (the "curves"):

- **Rally–Base–Rally (RBR)** → demand zone (uptrend continuation)
- **Drop–Base–Rally (DBR)** → demand zone (reversal up)
- **Drop–Base–Drop (DBD)** → supply zone (downtrend continuation)
- **Rally–Base–Drop (RBD)** → supply zone (reversal down)

---

## 3. How to draw the zone (be precise)

1. Find the **base** (the small candles before the big move).
2. Draw a rectangle covering the base's **body-to-wick range**:
   - Demand zone: from the **lowest low** of the base up to the **open of the first big-body candle** (or the base's body top).
   - Supply zone: from the **highest high** of the base down to the base's body bottom.
3. Extend the rectangle to the right - that's your live zone.

Keep zones **tight**. A fresh, narrow zone that produced an explosive move is far better than a wide, vague one.

---

## 4. Fresh vs. tested zones

- **Fresh (untested) zone** = price hasn't returned since it formed → strongest. Most orders still unfilled.
- **Tested once** = weaker, but can still work.
- **Tested 2+ times** = usually exhausted; skip it. The orders are mostly filled.

For intraday, prefer zones formed **today** (or at the previous day's key turning points).

---

## 5. Trading a zone intraday (Bank Nifty example)

_Hypothetical numbers for illustration._

Suppose on the 5-min chart, Bank Nifty rallies, pauses in a tight base around **48,180–48,220**, then rockets up 250 points. That base is a **demand zone (RBR)**.

Later in the session price drifts back down into **48,180–48,220**.

- **Entry:** as price enters the zone and a bullish candle (e.g. a hammer or bullish engulfing) forms → go **long** near 48,210.
- **Stop-loss:** just **below** the zone, say 48,150 (below the base's low). Risk ≈ 60 points.
- **Target:** the next supply zone or a 1.5–2× multiple of risk → e.g. +120 points to 48,330. That's a **1:2 reward:risk**.
- **Position size:** shares/lots so that the 60-point risk = only 1–2% of your capital.

If price slices _through_ the zone without reacting, the zone failed - your stop takes you out small. That's the system working.

```
   supply zone (target) ─────────────────  48,330
                                   ↑
                              price bounces
   demand zone  ░░░░░░░░░░░░░░░░░░░░░░░░░░  48,220
                ░ ENTER here on bullish candle ░  48,210
                ░░░░░░░░░░░░░░░░░░░░░░░░░░  48,180
   STOP-LOSS ──────────────────────────────  48,150
```

---

## 6. Stacking confluence (this is what raises your win rate)

A zone alone is decent. A zone **plus** other signals is a high-quality trade. Look for:

- Zone aligns with a **candlestick reversal pattern** (hammer, engulfing, pin bar) _inside_ the zone.
- Zone sits near **VWAP** (fair value magnet) or a key **EMA** (20/50).
- Zone matches **yesterday's high/low** or a round number (e.g. Nifty 24,000).
- **Volume** spikes on the reaction candle.
- Overall **trend** agrees (buy demand zones in an uptrend, sell supply zones in a downtrend).

The more of these that line up, the better.

---

## 7. Common beginner mistakes

- Drawing zones **too wide** or after the fact (hindsight bias).
- Trading **tested-out** zones with no orders left.
- Ignoring the **trend** - buying a demand zone while the day is strongly bearish.
- **No stop-loss** below/above the zone. A zone is a probability, not a wall.
- Chasing price _after_ it has already left the zone instead of waiting for the return.

---

## Key Takeaways

- Supply/demand zones mark where institutions left unfilled orders - price tends to react there.
- A valid zone = a small **base** followed by a big **departure** candle.
- **Fresh** zones are strongest; skip zones tested 2+ times.
- Enter on a confirming candle _inside_ the zone; stop just beyond it; target ≥ 1:2.
- **Confluence** (candlestick + VWAP/EMA + volume + trend) is what turns a zone into a trade.

## Practice This Week

1. On the Nifty & Bank Nifty 5-min chart, mark **3 fresh demand and 3 fresh supply zones** each day (base + departure).
2. Note which zones price **returned to** and how it reacted - screenshot them.
3. Paper-trade **one** zone bounce with a written entry, stop, and 1:2 target.
4. For every zone trade, list which **confluence factors** were present.
