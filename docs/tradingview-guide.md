# TradingView for Indian Intraday - Complete Practical Guide

_How to actually use TradingView to find, plan, and manage intraday trades on the NSE._

TradingView is where you'll spend most of your screen time: charting, marking zones, scanning for candidates, and paper trading. This guide walks the free tier first (enough to learn on) and notes where paid tiers help.

> ⚠️ Education only. TradingView's paper trading is for practice; real orders route through your broker (Zerodha, etc.).

---

## 1. Setup

1. Create a **free account** at tradingview.com.
2. Search symbols with the exchange prefix:
   - Index: `NSE:NIFTY`, `NSE:BANKNIFTY`, `NSE:CNXFINANCE` (FinNifty)
   - Stocks: `NSE:RELIANCE`, `NSE:HDFCBANK`, `NSE:INFY`, etc.
3. **Data note:** free NSE data is delayed ~15 min. For live intraday you need either TradingView's real-time NSE data add-on **or** connect a supported Indian broker (some brokers stream live data into TradingView). Zerodha users often chart in TradingView and execute in Kite.

---

## 2. Chart basics

- **Timeframe** (top-left): use **5-min** as your intraday workhorse; **15-min** for structure/zones; **1-min** only for fine entries. **Daily** to mark big levels before the open.
- **Chart type:** set to **Candles** (candlestick). Avoid line charts for intraday.
- **Crosshair & data window:** hover any candle to read exact OHLC.
- **Right-click → Settings:** customize candle colors, so bullish/bearish read instantly.

---

## 3. Drawing tools (left toolbar) - your zone kit

These are the tools you'll use every single day:

- **Rectangle** → draw **supply & demand zones** and the **opening range**. This is your most-used tool.
- **Horizontal Line / Horizontal Ray** → yesterday's high/low, round numbers, VWAP-anchored levels.
- **Trend Line** → trendlines and channels.
- **Fib Retracement** → optional, for pullback levels.
- **Long/Short Position tool** → drag to visualize **entry, stop-loss, and target** and see the exact risk:reward ratio before you commit. Fantastic for enforcing 1:2.
- **Measure (Shift+click-drag)** → quickly see points/% and candle count between two prices.

Tip: press the **magnet icon** to snap drawings to exact highs/lows/opens.

---

## 4. Indicators (the "Indicators" button, top)

Add only what you need - search and click to add:

- **Moving Average Exponential** → add three: EMA **9**, **20**, **50** (set the "Length" in each).
- **VWAP** (search "VWAP") → the intraday fair-value line; resets daily automatically.
- **RSI** → default 14; watch overbought/oversold _with caution_ in trends.
- **Volume** → usually on by default; confirms breakouts and zone reactions.

Free tier allows a **limited number of indicators per chart** (a handful) - these four/five fit comfortably. Save them as a **template** (see §8) so every chart loads them.

---

## 5. Watchlist - what to track intraday

Create a watchlist (right panel) with:

- `NSE:NIFTY`, `NSE:BANKNIFTY`, `NSE:CNXFINANCE`
- 5–10 liquid stocks you understand (RELIANCE, HDFCBANK, ICICIBANK, INFY, TCS, SBIN, TATAMOTORS…)

Right-click the watchlist to add columns (Change %, Volume) so you can spot what's moving.

---

## 6. Finding trade candidates - the Screener

**TradingView Stock Screener** (menu → Screeners → Stock Screener) filters the whole market to a short list. Useful intraday filters:

- **Exchange = NSE**, and set a **minimum average volume** (liquidity is non-negotiable for intraday).
- **Change % from open** or **gap %** → find the day's movers.
- **Relative Volume** high → unusual activity worth watching.
- **Price range** you can afford (per-share price affects position sizing).

Also use the built-in **"Hotlists"** (top gainers/losers, most active) for a quick daily shortlist. Then chart each candidate and only trade the ones showing a clean zone or setup.

---

## 7. Alerts - stop staring at the screen

Right-click a price / zone / drawing → **Add Alert**. Set alerts on:

- The **edges of your demand/supply zones** ("alert me when Bank Nifty reaches 48,220").
- Yesterday's high/low or the opening-range boundary.

When it fires, _then_ you look and decide. This prevents boredom trades. (Free tier = limited active alerts; paid = many more.)

---

## 8. Save your setup (templates & layouts)

- After adding indicators + colors, click the indicators template dropdown → **Save As** a template (e.g. "Intraday 5m"). Apply it to any chart instantly.
- **Save the whole chart layout** (top-right save icon). Paid tiers allow **multiple saved layouts** and **multi-chart layouts** (e.g. Nifty 5-min + 15-min + Bank Nifty side by side).

---

## 9. Bar Replay - the best learning feature (use this a lot)

**Bar Replay** (top toolbar, the ⏮ icon) lets you rewind the chart to any past day and step forward candle-by-candle, as if trading live.

Use it to:

- **Backtest ORB and supply/demand** on dozens of past days quickly.
- Practise _deciding in real time_ without knowing the future.
- Build screen-time and pattern recognition fast.

This is how you get months of "reps" in days. (Intraday bar-replay depth is fuller on paid tiers, but you can practise plenty on free.)

---

## 10. Paper Trading - trade with fake money

Bottom panel → **Trading** tab → select **Paper Trading**. This gives you a simulated account to place buy/sell/stop/target orders on the chart. Use it for **all of weeks 1–11**:

- Place the entry, attach a **stop-loss and target** (bracket-style).
- Track your simulated P&L and order history.
- Treat it exactly like real money - same rules, same sizing.

---

## 11. Extras worth knowing

- **Economic calendar** (menu) - know when RBI policy, budget, or major results hit; volatility spikes then.
- **Mobile app** - good for alerts and watching, weak for precise drawing; do serious analysis on desktop.
- **Ideas / community scripts** - treat with skepticism; learn the core tools before adding others' indicators.

---

## A simple daily TradingView workflow

1. **Pre-market:** open Nifty & Bank Nifty daily + 5-min. Mark yesterday's high/low and fresh **supply/demand zones** with the Rectangle tool. Set **alerts** on zone edges.
2. **Screener/hotlists:** shortlist 3–5 liquid movers; chart each; keep only clean setups.
3. **9:15–9:30:** draw the **opening range** rectangle; wait.
4. **On alert:** check for a confirming candle _at_ the zone + VWAP/EMA confluence.
5. **Before entry:** use the **Long/Short Position tool** to lock entry, stop, target at ≥ 1:2.
6. **Execute** on Paper Trading (or your broker once live).
7. **After close:** screenshot each trade for your journal; use **Bar Replay** to review or practise more.

---

## Key Takeaways

- Set candles + 5-min timeframe; add EMA (9/20/50), VWAP, RSI, Volume and save as a template.
- The **Rectangle** and **Long/Short Position** tools are your daily workhorses (zones + risk:reward).
- Use the **Screener/Hotlists** to find liquid movers, then chart-confirm before trading.
- **Alerts** on zones stop you from overtrading out of boredom.
- **Bar Replay** = fast, safe reps; **Paper Trading** = practise real execution with fake money.

## Practice This Week

1. Build your watchlist and save an **"Intraday 5m" indicator template**.
2. Mark zones + set **3 alerts** on Nifty/Bank Nifty before the open, three days running.
3. Do **5 Bar Replay** sessions on past days, trading only ORB or a supply/demand bounce.
4. Place **3 Paper Trades** using the Long/Short Position tool to enforce a 1:2 target.
