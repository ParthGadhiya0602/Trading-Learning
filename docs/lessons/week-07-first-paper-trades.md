# Week 7 — Your First Paper Trades

> **◀ Previous:** [Week 6 — Pick ONE Setup: Opening Range Breakout](./week-06-orb-and-setups.md) &nbsp;|&nbsp; **Course Home:** [Lessons Index](./README.md) &nbsp;|&nbsp; **Next ▶:** [Week 8 — Risk & Position Sizing](./week-08-risk-and-position-sizing.md)

> ⚠️ **Educational content only — not financial advice.** Nothing in this lesson is a trade recommendation or suggestion. All examples and numbers are illustrative and hypothetical. Always consult a registered financial advisor before trading or investing. Trade and invest at your own risk — no responsibility is accepted for any loss, damage, or incorrect/invalid trades.

_Goal: run a complete, honest trade lifecycle — from watchlist to journal entry — on a demo platform, so the process becomes muscle memory before real money is ever at risk._

## Why This Week Matters

For six weeks you have been learning to _read_ the market: candles, structure, trend, support and resistance, VWAP, the opening range. Reading is passive. Trading is a physical act — you must click buttons, type numbers into an order ticket, and then sit with the discomfort of an open position while price moves against you. These are two completely different skills, and most beginners discover the hard way that "I saw the setup" and "I executed the setup correctly" are worlds apart.

This week you close that gap. You will place your first _paper trades_ — trades with fake money on a demo platform that behaves exactly like the real one. The point is not to make imaginary profit (imaginary profit is worthless). The point is to build a **repeatable process**: a checklist you run before every trade, an order structure that protects you automatically, and a journal that turns each trade into data you can learn from.

In intraday trading, your edge is not a magic indicator. Your edge is _consistency of process under pressure_. A trader who follows the same disciplined loop 200 times will beat a genius who improvises 200 times. Paper trading is where you install that loop. When you reach Week 12 and switch to real capital, nothing about your _behaviour_ should change — only the money becomes real. That is the whole reason this week exists.

## Concept 1 — The Full Trade Lifecycle

A trade is not a single event ("I bought Reliance"). It is a **lifecycle** with distinct stages, and each stage has its own decisions. Most losses happen because a beginner skips a stage — they find a setup and jump straight to clicking buy, with no plan for where they are wrong or where they will take profit.

Here is the complete loop you will run every single day.

Caption: The intraday trade lifecycle — a closed loop, journal feeds back into watchlist.

```
   ┌─────────────────────────────────────────────────────────┐
   │                                                          v
┌──────────┐   ┌──────────┐   ┌──────────┐   ┌──────────┐  ┌──────────┐
│ 1. WATCH │-> │ 2. PLAN  │-> │ 3. ENTER │-> │ 4. MANAGE│->│ 5. EXIT  │
│  LIST    │   │ setup +  │   │ order    │   │ trail /  │  │ SL, tgt, │
│ (pre-mkt)│   │ SL + tgt │   │ ticket   │   │ hold     │  │ or time  │
└──────────┘   └──────────┘   └──────────┘   └──────────┘  └────┬─────┘
                                                                 │
                            ┌────────────────────────────────────┘
                            v
                       ┌──────────┐
                       │ 6. JOURNAL│  <- the stage beginners skip,
                       │  + review │     and the only one that
                       └──────────┘     makes you better
```

**Stage 1 — Watchlist (before 9:15 AM).** You pick 3–5 instruments to watch. As a beginner, keep it tiny: Nifty, Bank Nifty, and two liquid stocks such as Reliance and HDFC Bank. You note their previous-day high/low, any big overnight news, and where price closed.

**Stage 2 — Plan.** _Before_ the market opens, and before you touch an order, you write down: which setup you are hunting (this week, only ONE setup), the exact trigger price, the stop-loss level, and the target. If you cannot write these three numbers, you do not have a trade.

**Stage 3 — Enter.** You place the order ticket only when price actually reaches your trigger. Not before ("it looks like it will"), not after chasing.

**Stage 4 — Manage.** The position is live. You either leave it completely alone until it hits SL or target (recommended for beginners), or you trail your stop as price moves in your favour.

**Stage 5 — Exit.** The trade closes: your stop-loss fires, your target fills, or the clock forces you out (\~3:20 PM for intraday — more on that below).

**Stage 6 — Journal.** You record what happened and why. This is the stage that converts random clicking into a learnable skill.

## Concept 2 — The Order Ticket: What Every Field Actually Does

When you click "Buy" on Zerodha Kite (or the paper-trading panel in TradingView), a small window opens called the **order ticket** or **order window**. Beginners find it intimidating because it has many fields. Let us dissect it, because typing the wrong thing here is how people lose money by _accident_ rather than by a bad idea.

Caption: A simplified Zerodha-style order ticket, field by field.

```
┌───────────────────────────────────────────────────┐
│  BUY   RELIANCE                               NSE │
│  ┌──────────┬──────────┬──────────┐               │
│  │  MIS     │  CNC      │  ...     │  <- Product  │
│  └──────────┴──────────┴──────────┘               │
│  Qty [   10 ]        Price [ 2955.00 ]            │
│  ┌────────┬────────┬───────────┐                  │
│  │ MARKET │ LIMIT  │ SL / SL-M │  <- Order type   │
│  └────────┴────────┴───────────┘                  │
│  Trigger [        ]   (only for SL orders)        │
│  ─────────────────────────────────────────        │
│  [ ] Bracket:  Target[ 15 ] Stoploss[ 8 ]         │
│                                                   │
│           [   SWIPE / CLICK TO BUY   ]            │
└───────────────────────────────────────────────────┘
```

**Product — MIS vs CNC.** This is the most important field for an intraday trader. **MIS (Margin Intraday Squareoff)** means the position _must_ close the same day; the broker gives you extra leverage but will auto-square-off your position around **3:20 PM** if you haven't closed it yourself. **CNC (Cash and Carry)** is for delivery — the shares sit in your account overnight. For intraday practice you almost always use MIS. Index options/futures use **NRML** or MIS. Picking CNC by mistake means no auto-square-off and (for real accounts) needing full cash.

**Quantity.** For stocks, any whole number of shares. For index derivatives (Nifty, Bank Nifty futures/options) you cannot buy an arbitrary amount — they trade in fixed **lot sizes**, and you trade whole lots only. Lot sizes are set by the exchange and change periodically, so always confirm the current lot size on the platform rather than memorising a number.

**Order type — MARKET vs LIMIT vs SL.**

- A **MARKET** order says "fill me right now at whatever the best available price is." It fills instantly but you accept **slippage** — the price you get may be worse than the last-traded price you saw.
- A **LIMIT** order says "fill me only at this price or better." No slippage, but it may never fill if price runs away.
- A **stop-loss order (SL / SL-M)** is an order that sits dormant until price hits a **trigger**, then activates. This is how you place your protective exit.

**Trigger price.** Only used for SL orders — the price that "arms" the order.

## Concept 3 — The Bracket Order: Your Automatic Safety Net

The single most useful structure for a beginner is the **bracket order (BO)**. A bracket order is not one order — it is three orders bundled together and placed simultaneously:

1. Your **entry** (buy or sell).
2. A **stop-loss**, placed automatically the moment the entry fills.
3. A **target** (profit-booking limit), also placed automatically.

They are called a "bracket" because your entry is bracketed on both sides — a floor below (stop) and a ceiling above (target). Critically, the two exits are **OCO — One Cancels the Other**: the instant one of them fills, the platform cancels the other. You can never be left with a naked, unprotected position.

Caption: Bracket order structure for a long (buy) trade.

```
   PRICE
     ^
     │   ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─   TARGET  ₹2970  (+₹15)  ── profit exit
     │
     │        ▲  price moves up
     │        │
     │   ═════╪═════════════════   ENTRY   ₹2955  ── order fills here
     │        │
     │        ▼  price moves down
     │
     │   ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─   STOPLOSS ₹2947  (−₹8)   ── loss exit
     │
     └───────────────────────────────────────────> TIME

   Risk  = 2955 − 2947 = ₹8   per share
   Reward= 2970 − 2955 = ₹15  per share
   R:R   = 15 : 8  ≈  1 : 1.9   (aim for >= 1:2)
```

Why this matters for discipline: the bracket order forces you to decide your stop and target _before_ you enter, at the calm moment, not in the panic of a moving position. It also removes the beginner's deadliest habit — moving or deleting the stop-loss because "it'll come back." With a bracket order, your risk is fixed the instant you enter.

### GTT — a different tool, not for intraday

You will see **GTT (Good Till Triggered)** on Kite. A GTT lets you set a trigger that stays alive for many days (up to a year) waiting for a price. It is a _delivery/swing_ tool — GTT triggers place **CNC** orders and are not meant for MIS intraday setups. Know what it is so you don't reach for it by mistake; you will not use it in this course's intraday work.

## Concept 4 — Manual vs Auto Exit, and the 3:20 PM Deadline

There are three ways a trade ends, and you must respect all three.

**Auto exit (your bracket's SL or target fires).** This is the goal — you defined the levels, the market did the rest, no emotion involved.

**Manual exit.** Sometimes you close a trade yourself before either level hits — for example, price stalls for 40 minutes and momentum has clearly died. This is legitimate but dangerous for beginners because it is where fear and boredom creep in. Rule for this week: only exit manually for a _pre-defined reason_ you wrote down, never because you "feel" something.

**Time-based / mandatory square-off (\~3:20 PM IST).** The NSE cash-equity session runs 9:15 AM to 3:30 PM. But **MIS intraday positions are auto-squared-off by your broker before the close — typically around 3:20 PM** (some brokers vary by segment). If you do nothing, the broker closes your position at market price and may charge a small penalty. Never let this happen by accident: plan to be flat by 3:15 PM. An open MIS trade at 3:19 PM is not a "position," it is a countdown.

### Trailing the stop

**Trailing** means moving your stop-loss in the direction of profit as price advances, locking in gains while giving the trade room to run. If you bought Reliance at ₹2955 with a stop at ₹2947 and price climbs to ₹2965, you might trail the stop up to ₹2957 — now the worst case is a small profit, not a loss. Kite's bracket order supports an automatic trailing-stop value. For your first paper week, keep it simple: use a fixed bracket (no trailing) so you can measure your setup cleanly. Add trailing next week once the basic loop is automatic.

## Concept 5 — Making Paper Trading Honest

Paper trading is only useful if it is _realistic_. A dishonest simulation teaches dishonest habits that will bankrupt a real account. Here are the rules that keep it honest.

**Trade real size.** Decide the capital you will _actually_ start with in Week 12 — say ₹50,000 — and trade that exact number on paper. Risking 1% (₹500) per trade _feels_ completely different from risking an abstract "10 lots." Small real size teaches the right emotions; huge fake size teaches recklessness.

**Assume slippage.** In real markets your market order fills a little worse than the price on screen. Simulate this: whenever you take an entry or exit at market, penalise yourself by a tick or two. If Nifty shows 24,500 and you buy at market, record your fill as 24,501 or 24,502. This single habit stops you from building a strategy that only "works" on frictionless fantasy prices.

**One setup only.** This week, pick a _single_ setup (the Opening Range Breakout is ideal — you learned it recently) and trade _only_ that. Trading five different ideas gives you five tiny, useless samples. Twenty repetitions of one setup gives you a signal you can actually read.

**Max 1–2 trades per day.** Overtrading is the number-one destroyer of beginners. A hard cap of two trades forces you to wait for _quality_. If both are gone by 10:30 AM, you are done — watch and learn, don't hunt.

**No rewinding.** The cardinal sin of paper trading is scrolling back on a chart and "trading" a move you already know happened. This is not practice; it is lying to yourself. Only trade **live**, in real time, deciding at the hard right edge of the chart where the future is genuinely unknown.

## Concept 6 — What to Record, and Why

Your journal is the machine that turns experience into skill. Each field exists for a reason — you are building a dataset about your own behaviour.

| Field                     | Example                  | Why it matters                |
| ------------------------- | ------------------------ | ----------------------------- |
| Date / time in / time out | 16-Jul, 9:52 / 10:31     | Reveals _when_ you trade well |
| Instrument                | Bank Nifty               | Which markets suit you        |
| Setup                     | ORB long                 | Proves you traded your plan   |
| Entry / SL / target       | 51,200 / 51,080 / 51,440 | The plan, in numbers          |
| Actual exit + reason      | 51,440, target hit       | Plan vs reality               |
| Risk (₹) and R-multiple   | ₹500 risk, +2.0R         | Normalises wins/losses        |
| Screenshot                | chart image              | Lets you re-examine the read  |
| Mistake / emotion note    | "entered 1 candle early" | The real lessons live here    |

The **R-multiple** is the most important number. **R** is the amount you risked (the distance from entry to stop, in rupees). If you risk ₹500 and make ₹1,000, that is **+2R**. Recording results in R instead of rupees lets you compare a Nifty trade to a Reliance trade fairly, and it keeps your focus on process, not the size of the rupee number. A trader who averages a positive R over many trades will grow; one who chases big rupee wins with sloppy risk will not.

## Worked Examples

_All numbers below are hypothetical and illustrative — chosen to show the mechanics, not to predict any real price._

### Example 1 — Bank Nifty, Opening Range Breakout (a winner)

**Watchlist (9:00 AM).** Bank Nifty closed strong yesterday near its high. You mark it as your primary.

**Plan (before entry).** Your setup: 15-minute Opening Range Breakout. The **opening range** is the high and low made between 9:15 and 9:30 AM. You will go long only if price breaks _above_ the range high with conviction. Risk cap: 1% of your ₹50,000 paper account = **₹500**.

**9:15–9:30 — the range forms.** Bank Nifty ranges between a high of **51,180** and a low of **51,020**.

**9:41 — trigger.** A strong 5-minute candle closes at **51,205**, above the range high, on rising volume. You enter long. Assuming one tick of slippage, you record your fill at **51,200** — wait, that is below the trigger; be honest: slippage makes a market buy _worse_, so you fill at **51,207**.

**Sizing.** You place your stop just below the breakout candle's structure, at **51,087** (a 120-point risk). Bank Nifty moves in ₹1 per point per unit. To keep loss near ₹500, your position size must be tiny — this is exactly the lesson: a 120-point stop is _large_, so you can only carry a small position. You set target at **51,447** (a 240-point reward) for a clean **1:2 R:R**.

Caption: Bank Nifty ORB long, entry-to-exit (hypothetical).

```
  51,447 ┄┄┄┄┄┄┄┄┄┄┄┄┄┄┄┄┄┄┄┄┄┄┄●  TARGET hit 10:38  (+2R)
                              ╱
                          ▁▂▄█
  51,180 ──range high──── █    (breakout candle 9:41)
         ▁▂█▄▂▁  ▁▂█        ↑ ENTRY 51,207
  51,020 ──range low─────
         └ opening range ┘
                              STOP 51,087 (never touched)
   9:15   9:30   9:45   10:00   10:15   10:30   10:38
```

**Manage & exit.** Price never revisits your stop. It grinds up and tags **51,447** at 10:38 AM. The bracket's target order fills; the stop is auto-cancelled (OCO). Result: **+2R, +₹1,000** on paper.

**Journal.** You note: "Waited for the candle to _close_ above the range — good discipline. Entry was clean. Could I have trailed for more? Maybe, but the plan was 1:2 and the plan won." You are done for the day — that was trade one, and it worked.

### Example 2 — Reliance, breakout that fails (a loser handled correctly)

The goal of this example is to show that a _losing_ trade can be a _good_ trade if the process was right.

**Plan.** Reliance has been rising all morning and is pressing against an intraday resistance at **₹2,955**. Your setup: buy the breakout above ₹2,955. Risk: **₹500**.

**11:12 — trigger.** A candle pushes to ₹2,957. You buy at market; with slippage your fill is **₹2,958**. You set your stop below the breakout base at **₹2,947** (₹11 risk per share) and target at **₹2,979** (₹21 reward, \~1:2). With ₹500 total risk and ₹11 per share, you size about **45 shares**.

Caption: Reliance failed breakout — stop does its job (hypothetical).

```
  2,979 ┄┄┄┄┄┄┄┄┄┄┄┄  TARGET (never reached)
  2,958 ═══●══════════  ENTRY 11:12
        ▄█ ▂          price pokes up then rolls over
  2,955 ──resistance──
              ▄▂▁
  2,947 ──────────●──  STOP hit 11:29  (−1R, −₹495)
              (bracket SL fires, target auto-cancels)
  11:12    11:18    11:24    11:29
```

**What happens.** The breakout has no follow-through — a "false breakout." Price ticks to ₹2,961, stalls, and sellers push it back. At 11:29 it trades through ₹2,947. Your bracket stop-loss fires (with a tick of slippage, fill ≈ ₹2,946). Loss: about **−₹495, −1R**. The target order auto-cancels.

**Journal.** "Setup was valid, entry followed the plan, stop was pre-set and I did NOT move it. Loss was capped at 1R exactly as designed. Nothing to fix — this is a cost of doing business." This is the mindset shift of the week: a trade that loses money while following the process is a **success of discipline**. The trades to fear are the ones where you widened the stop, prayed, and got saved — because that habit eventually destroys the account.

## Common Mistakes (and the fix)

**1. Placing the entry before defining the stop.** Beginners get excited by a moving candle and click buy, planning to "figure out the exit later." Later never comes calmly. **Fix:** use bracket orders so the SL and target are mandatory fields — you physically cannot enter without them.

**2. Choosing CNC instead of MIS (or vice-versa).** A misclick here changes everything: leverage, auto-square-off, and (in real accounts) the cash required. **Fix:** make "check product = MIS" the first line of your pre-trade checklist, and read it aloud every time until it is automatic.

**3. Moving the stop-loss away from price.** When the trade goes against them, beginners drag the stop further out to "give it room." This converts a small planned loss into a large unplanned one. **Fix:** treat the stop as a physical law. The only direction a stop may ever move is _toward_ profit (trailing), never away.

**4. Overtrading after a loss (revenge trading).** After a losing trade the urge to "win it back immediately" is enormous, and it leads to taking setups that aren't there. **Fix:** the hard cap of 1–2 trades/day and a **daily loss limit** — if you are down 2R (say ₹1,000) on the day, you stop, close the platform, and journal. No exceptions.

**5. Fake-realistic paper trading.** Trading huge fantasy size, ignoring slippage, or rewinding the chart. **Fix:** trade real size, add slippage on every fill, and only ever trade live at the right edge.

## Nuances & Edge Cases

- **Slippage is worst exactly when you need fills most.** During fast moves and at the open, the gap between screen price and fill price widens. A market order at 9:15:05 can fill surprisingly far from what you saw. This is why limit entries or waiting for the range to settle are gentler for beginners.
- **Stop-loss orders are not guaranteed at your price.** An SL-M (stop-loss market) order guarantees you _exit_ once triggered but not _at what price_ — in a gap or fast drop you can fill below your stop. Your "1R risk" is therefore a close estimate, not a hard ceiling. Respect that by keeping size modest.
- **Bracket-order availability varies.** Brokers periodically enable/disable BO and CO (cover order) product types. If BO isn't available, replicate it manually: enter, then _immediately_ place a separate SL order — never sit even 30 seconds unprotected.
- **The 3:20 square-off can move your P&L.** If your trade is still open near 3:20 PM, the auto-close happens at whatever the market is doing then — possibly a worse price than you'd choose. Being flat by 3:15 keeps _you_ in control of the exit.
- **Liquidity differs across your watchlist.** Nifty, Bank Nifty and large-caps like Reliance/HDFC Bank fill smoothly. Thinner stocks show wide bid-ask spreads, meaning your entry and exit both cost more. Stick to liquid names while learning.

## Day-by-Day (Mon–Fri)

- **Monday — Set up the tools.** Open a Zerodha Kite account in demo/observation mode or the TradingView paper-trading panel. Place ONE practice bracket order on Reliance with tiny size just to see all three legs (entry, SL, target) appear. _Observation target:_ watch the OCO behaviour — when one exit fills, confirm the other vanishes.
- **Tuesday — Build the checklist and watchlist.** Write your pre-trade checklist on paper (product = MIS, setup valid, SL set, R:R ≥ 1:2, within daily loss limit). Pre-market, build a 4-name watchlist with each instrument's previous-day high/low. _Observation target:_ mark the 9:15–9:30 opening range on Bank Nifty and note where it breaks.
- **Wednesday — First live paper trade.** Take exactly ONE ORB trade, live, with real size and simulated slippage. Whether it wins or loses does not matter. _Observation target:_ did you follow every checklist line, in order?
- **Thursday — Second paper trade + trailing observation.** Take up to two trades. On any winner, _watch_ (don't necessarily act) how a trailing stop would have behaved versus your fixed target. _Observation target:_ would trailing have helped or stopped you out early today?
- **Friday — Journal review.** Take zero or one trade; spend the hour reviewing the week's journal. Count your trades, tally R, and find the one recurring mistake. _Observation target:_ identify the single behaviour to fix next week (e.g., "I enter one candle too early").

## Key Takeaways

- A trade is a six-stage lifecycle; the stage beginners skip — **journaling** — is the only one that makes you better.
- **MIS = intraday with \~3:20 PM auto-square-off; CNC = delivery.** Check the product field first, every time.
- The **bracket order** (entry + auto SL + auto target, OCO) forces you to define risk before you enter and prevents naked positions.
- Honest paper trading means **real size, simulated slippage, one setup, ≤2 trades/day, and no rewinding.**
- Score every trade in **R-multiples**, not rupees — a disciplined −1R loss is a _good_ trade; a rescued trade with a moved stop is a bad one.
- Protect every trade with a stop, risk **1–2% per trade**, aim for **R:R ≥ 1:2**, and honour a hard **daily loss limit**.

## This Week's Milestone

By Friday you have a completed trade journal containing **at least three live paper trades** — each showing a pre-written plan (entry, stop, target), the actual outcome in R-multiples, a chart screenshot, and one honest note on process. The proof is not profit; it is that **every trade was bracketed, sized to ≤1–2% risk, and closed before 3:20 PM by rule rather than by accident.**

---

> **◀ Previous:** [Week 6 — Pick ONE Setup: Opening Range Breakout](./week-06-orb-and-setups.md) &nbsp;|&nbsp; **Course Home:** [Lessons Index](./README.md) &nbsp;|&nbsp; **Next ▶:** [Week 8 — Risk & Position Sizing](./week-08-risk-and-position-sizing.md)
