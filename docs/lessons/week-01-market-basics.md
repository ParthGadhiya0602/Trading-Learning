# Week 1 — How the Market Actually Works

> **◀ Previous:** [Roadmap Overview](../roadmap.md) &nbsp;|&nbsp; **Course Home:** [Lessons Index](./README.md) &nbsp;|&nbsp; **Next ▶:** [Week 2 — Candlestick Anatomy](./week-02-candlestick-anatomy.md)

> ⚠️ **Educational content only — not financial advice.** Nothing in this lesson is a trade recommendation or suggestion. All examples and numbers are illustrative and hypothetical. Always consult a registered financial advisor before trading or investing. Trade and invest at your own risk — no responsibility is accepted for any loss, damage, or incorrect/invalid trades.

*Goal: understand the plumbing of the Indian stock market — who trades with whom, how a price is really made, and what happens to your order after you click "Buy" — before you ever place one.*

## Why This Week Matters

Most beginners jump straight to candlestick patterns and indicators, then lose money because they never understood the machine underneath. A chart is just a picture of something deeper: thousands of buy and sell orders colliding inside a computer, matched in milliseconds, settled through regulated intermediaries. If you don't understand that machine, every later concept — support, breakouts, stop-losses, slippage — will feel like magic incantations instead of logical consequences.

Intraday trading (buying and selling the *same* security within one trading day) is especially unforgiving. You are competing against professionals, algorithms, and institutions who understand the plumbing cold. This week you build that foundation: what an exchange is, what an index is, who protects you, how your account works, what order types actually do, and — most importantly — how a single price emerges from an "order book." Get this right and the other 11 weeks click into place. This is education, not financial advice; you will not risk one rupee of real money until Week 12.

## Concept 1 — The Exchange Is an Electronic Order-Matching Machine

India has two main stock exchanges: the **NSE** (National Stock Exchange) and the **BSE** (Bombay Stock Exchange). For intraday index trading — Nifty and Bank Nifty — the NSE is where almost all the action lives. Forget the old image of men in coloured jackets shouting on a floor. Since the 1990s, the NSE has been a fully **electronic, order-driven exchange**: a giant computer program called the **matching engine** that receives orders from all over the country and pairs buyers with sellers automatically.

"Order-driven" means the price is set by the orders that ordinary participants submit — not by a middleman quoting you a price. This is different from a "quote-driven" market (like some bond or forex desks) where a dealer stands in the middle. On the NSE, when you want to buy 10 shares of Reliance, your order is thrown into a shared pool. If someone else's sell order matches yours, a trade happens. Nobody decides the price for you; the price is simply where a willing buyer and a willing seller meet.

### The order book: the single most important object in trading

Every stock has an **order book** — a live, sorted list of all the unfilled buy orders and sell orders waiting for a match. Buy orders are called **bids**. Sell orders are called **asks** (or **offers**). The book is sorted by price: the highest bid and the lowest ask sit at the top, closest to being matched.

- The **best bid** is the highest price anyone is currently willing to pay.
- The **best ask** is the lowest price anyone is currently willing to sell at.
- The gap between them is the **spread**.

The **last traded price (LTP)** you see quoted is just the price of the *most recent* completed trade — it's history, a fraction of a second old. The bid and ask tell you what can happen *next*.

## Concept 2 — Reading Market Depth (the Bid-Ask Ladder)

Your broker's terminal shows a "market depth" or "5-level" window: the top five bids and top five asks, each with a quantity. This is a window into the order book. Learning to read it is a genuine edge most beginners never develop.

Bid-ask ladder for a hypothetical stock (illustrative only):

```
        MARKET DEPTH  —  "XYZ Ltd"   LTP: 100.20
  ================================================
        BID SIDE (buyers)  |  ASK SIDE (sellers)
  ------------------------------------------------
   Qty        Price         |  Price        Qty
  ------------------------------------------------
   1,200  ->  100.15        |  100.25  <-   800    best ask
     900  ->  100.10        |  100.30  <-   500
   2,500  ->  100.05        |  100.35  <- 1,100
     600  ->  100.00        |  100.40  <-   700
   1,000  ->   99.95        |  100.45  <-   950
  ------------------------------------------------
              ^                    ^
         best bid 100.15      spread = 100.25 - 100.15 = 0.10
  ================================================
   Total bid qty ~6,200      Total ask qty ~4,050
```

What this tells you:

- **Spread = ₹0.10.** To buy *right now* you'd pay 100.25 (hit the ask); to sell *right now* you'd get 100.15 (hit the bid). You lose the spread instantly on a round trip — this is your first, unavoidable cost.
- **Depth** = how much quantity is stacked at each level. There are 6,200 shares wanting to buy vs 4,050 wanting to sell in the visible window. That imbalance is a *hint* (not a guarantee) of near-term buying pressure.
- **Liquidity** = how easy it is to trade a large size without moving the price. A deep book (big quantities at every level, tight spread) is liquid. Reliance, HDFC Bank, and the index derivatives are extremely liquid; a small-cap stock might have a ₹2 spread and thin depth, which is dangerous for intraday.

### Why liquidity is a survival issue for intraday

Intraday traders enter and exit many times a day. Every entry and exit pays the spread and risks **slippage** (getting a worse price than you expected). In an illiquid stock the spread alone can eat your whole profit target. This is *why* beginners are steered toward Nifty, Bank Nifty, and large-cap stocks: the machine gives you fair, tight, deep prices.

## Concept 3 — Price-Time Priority: How the Matching Engine Decides

When two orders could match, which one wins? The NSE uses **price-time priority**:

1. **Price first** — a better-priced order always takes precedence. A buyer bidding 100.20 gets filled before a buyer bidding 100.15.
2. **Time second** — among orders at the *same* price, the one that arrived *first* is filled first (first-in, first-out queue).

Order matching flow — a single buy order arriving (illustrative):

```
  You send: BUY 1,000 @ MARKET
        |
        v
  +----------------------------+
  |   MATCHING ENGINE          |
  |   scans ASK side, cheapest |
  |   price first              |
  +----------------------------+
        |
        v
  Step 1: fill 800 @ 100.25   (best ask fully consumed)
  Step 2: fill 200 @ 100.30   (next level, partial)
        |
        v
  Result: 1,000 shares bought
          avg price = (800*100.25 + 200*100.30)/1000
                    = 100.26
  New best ask becomes 100.30 (300 left) then 100.35 ...
```

Notice two crucial things. First, a **market order "walks the book"**: it keeps consuming the cheapest available asks until it's filled, so a large order gets a *worse average price* the deeper it digs. That extra cost is called **impact cost** — the price impact *your own* order causes. Second, after your trade, the book has changed: the 100.25 level is gone. You literally moved the market, even if only by a paisa.

This mechanism is the entire reason charts move. A green candle is just buyers aggressively consuming asks, pushing the best ask higher. A red candle is sellers hitting bids downward. Price is a footprint of who was more aggressive.

## Concept 4 — Order Types and Exactly What Each One Does

An order type is an *instruction* to the matching engine. Using the wrong one is one of the fastest ways beginners lose money.

### Market order
"Fill me immediately at whatever price the book offers." It **guarantees execution but not price**. In liquid instruments during normal hours this is fine; in thin books or at volatile moments it can slip badly (see impact cost above). Never fire a market order at 9:15:00 into a gapping open.

### Limit order
"Fill me only at my price *or better*." A BUY limit at 100.15 will only buy at 100.15 or lower. It **guarantees price but not execution** — if the market never comes to your price, you don't get filled. This is the default professional tool because it controls cost. The trade-off: you might miss the move while waiting.

### Stop-loss order (SL-M, stop-loss market)
A *dormant* order that activates only when price crosses a **trigger**. You set it to protect a position. Example: you're long at 100.20 and place a stop-loss with trigger 99.50. Nothing sits in the visible book. If the LTP falls to 99.50, the engine *then* releases a market order to sell, exiting your position. It's your automatic seatbelt.

### Stop-limit order (SL, stop-loss limit)
Same trigger idea, but when it activates it releases a *limit* order instead of a market order. You set both a trigger and a limit price (e.g. trigger 99.50, limit 99.40). Advantage: you won't get an absurd fill in a flash crash. Danger: if price gaps straight through your limit, the order **doesn't fill and you're still in a losing trade**. Beginners must understand this trade-off — a stop-limit can fail to protect you exactly when you need it most.

Where these orders sit relative to price (long trade, illustrative):

```
  price
   ^
   |   103.00  ---- TARGET (limit sell, take profit)  R:R rewards
   |                                                   |
   |   100.20  ==== ENTRY (bought here)                | risk
   |                                                   |
   |    99.50  ---- STOP-LOSS trigger (protective exit)v
   |
   +---------------------------------------------> time

   Risk  = 100.20 - 99.50 = 0.70 per share
   Reward= 103.00 - 100.20 = 2.80 per share
   Reward : Risk = 2.80 : 0.70 = 4 : 1   (aim >= 2:1)
```

**Rule from day one:** every position gets a stop-loss the moment you enter. No exceptions. We will formalise position sizing in Week 8, but the discipline starts now.

## Concept 5 — What an Index Really Is (Nifty 50 and Bank Nifty)

You cannot buy "the Nifty" as a share — it's a *number*, a summary of a basket of stocks. The **Nifty 50** tracks 50 of the largest, most-traded companies on the NSE. **Bank Nifty** tracks 12 major banking stocks. They exist so you can measure "the market" (or "the banking sector") with a single figure.

### Free-float market-cap weighting (conceptually)

The index is a weighted average, not a simple average. Each company's weight is based on its **free-float market capitalisation** — the market value of only the shares actually available for public trading (excluding promoter/government locked-in holdings). Bigger, more-tradable companies pull the index more.

Conceptually:

```
  Index level = Base value * ( current total free-float mkt cap )
                             ------------------------------------
                             ( free-float mkt cap in base period )

  Weight of a stock ~  its free-float market cap
                       --------------------------------
                       sum of all constituents' free-float caps
```

Practical consequence for a trader: because weighting is by size, a few giants dominate. In Bank Nifty, the largest banks (e.g. HDFC Bank, ICICI Bank) move the index far more than the smallest constituent. When you watch Bank Nifty, you're really watching the heavyweight banks. That's *why* traders keep an eye on HDFC Bank and ICICI Bank ticks to anticipate Bank Nifty — the index is a mirror of its biggest members.

You trade the index through **derivatives** (futures and options), which come in fixed **lot sizes** (you can't buy a single "unit" of Nifty; you trade one lot, a fixed quantity set by the exchange). We only note this now; derivatives mechanics come much later. For paper trading this week, you'll simply *observe* the index and its heavyweight stocks.

## Concept 6 — Long, Short, and How Shorting Is Even Possible Intraday

**Going long** = buying first, hoping to sell higher. Intuitive.

**Going short** = *selling first* (something you don't own), hoping to buy it back cheaper. Profit = sell high, buy low, in that order. Beginners find this baffling: how can you sell what you don't own?

Intraday, the mechanism is **intraday square-off within the same session**. When you short, your broker lets you sell now on the understanding that you *must* buy back (cover) before the market closes today. You never actually deliver shares; the two trades net off. Because the position is opened and closed the same day, no shares need to change hands in settlement — you only keep the profit or pay the loss on the price difference. This is only possible under an intraday product (see next concept), and it's why you *can't* casually hold a short "overnight" the way you shorted it intraday.

Shorting matters because markets often fall faster than they rise (fear moves quicker than greed). An intraday trader who can only go long is blind in one eye.

## Concept 7 — Your Accounts, Product Types (MIS vs CNC), Margin, and Settlement

To trade you need three linked things, usually bundled by one broker:

- **Trading account** — the interface that sends orders to the exchange.
- **Demat account** — an electronic locker (held at a depository, NSDL or CDSL) that stores shares you *own*.
- **Bank account** — where your money lives and settles.

### MIS vs CNC — the product tag that changes everything

When you place an equity order, you pick a **product type**:

- **CNC (Cash aNd Carry)** — delivery. You intend to *own* the shares; they land in your Demat. No extra intraday leverage; you pay the full value. Used by investors.
- **MIS (Margin Intraday Square-off)** — the intraday product. You get **leverage** (trade a larger position than your cash would allow) *because* you promise to close by day's end. This is the tag intraday traders use, and the one that enables intraday shorting.

### How intraday leverage/margin works

**Margin** is a good-faith deposit the broker/exchange requires to let you hold a position. With MIS, because the risk window is only a few hours and everything closes today, the required margin is a fraction of the full value — that fraction is your **leverage**. If a position needs ₹1,00,000 of value but only ₹20,000 of margin, you have 5x leverage.

Leverage is a magnifier in *both* directions. A 1% favourable move on 5x leverage is roughly a 5% gain on your margin; a 1% adverse move is roughly a 5% loss. This is precisely why we obsess over stop-losses and the 1–2% risk rule. Note that SEBI (the regulator) has tightened intraday leverage rules over the years so the eye-watering leverage of the past no longer exists — a good thing for beginners.

### The ~3:20 PM auto square-off

Because MIS positions *must* close today, your broker automatically **squares off** (force-closes) any open MIS position, typically around **3:20 PM** — before the 3:30 PM close. Two things follow. First, if you forget to exit, the broker exits for you at whatever the market gives, often with an extra charge. Second, you should plan to be flat well before 3:20; don't let the clock trade for you.

### Settlement and the T+1 concept

When you *do* take delivery (CNC), the trade settles on a schedule. India runs on **T+1 settlement**: trade day plus one business day. Buy shares today (T), and they arrive in your Demat, with cash debited, on the next business day (T+1). For pure intraday (MIS) you open and close within the day, so nothing hits your Demat — you just realise the net cash difference. Understanding T+1 matters so you know *why* intraday and delivery behave differently in your account.

## Concept 8 — SEBI: Who Protects You

**SEBI** (Securities and Exchange Board of India) is the statutory regulator of Indian securities markets. It licenses and supervises exchanges, brokers, and depositories; sets rules on margins, disclosures, and conduct; and runs investor-protection and grievance mechanisms. Practically, SEBI is *why* your broker must segregate your funds, *why* leverage is capped, and *why* there are circuit limits that pause trading when prices move violently. You don't interact with SEBI daily, but its rules shape every mechanic in this lesson. Trade only with a SEBI-registered broker — never an unregulated "tip" platform promising guaranteed returns.

## Concept 9 — The Sessions: Pre-Open and Normal, and Slippage

The trading day isn't one uniform block. It has structure.

### Pre-open session (order collection + equilibrium price)

Before continuous trading begins, the NSE runs a **pre-open session** (roughly 9:00–9:15 AM) to discover a fair opening price and absorb the overnight news rush. It has phases: an **order-collection** window where participants place/modify/cancel orders but *nothing is matched yet*; then the engine computes a single **equilibrium price** — the price at which the *maximum* quantity can be traded — and executes all crossable orders at that one uniform price; then a brief buffer before the normal session opens at 9:15 AM.

Why it exists: if the market simply flung open at 9:15 after overnight news, the first prices would be chaotic. The auction concentrates everyone's opening intentions into one calculated, fair price so continuous trading starts from a sensible level.

Session timeline (NSE equities, IST — illustrative):

```
  09:00 --------- 09:08 -- 09:12 -- 09:15 --------------- 15:20 -- 15:30
   |   PRE-OPEN             |        |    NORMAL SESSION     |       |
   |  order collection      |        |  continuous matching  |       |
   |  (no matching)         |        |  price-time priority  |       |
   |         equilibrium ---+        |                       |       |
   |         price calc &            |             MIS auto  |       |
   |         opening match           |             square-off|  MARKET
   |                                 |             (~15:20)   |  CLOSE
   v                                 v                        v       v
   [==== auction ====]               [==== you trade here ====][flat][done]
```

As a beginner you should generally **avoid trading the first few minutes** after 9:15 — it's the most violent, spread-widening part of the day. Watch it; don't touch it yet.

### Slippage and impact cost (the hidden taxes)

- **Slippage** = the difference between the price you *expected* and the price you *got*. Caused by the market moving in the instant between your decision and your fill, or by a market order walking the book. Worse when volatility is high or liquidity is low.
- **Impact cost** = the portion of slippage caused by *your own* order size pushing through multiple book levels (from Concept 3). Large order + thin book = large impact cost.

You cannot eliminate these, but you control them: trade liquid instruments, prefer limit orders when appropriate, avoid the chaotic open, and never size so big that you're a whale in a puddle.

## Worked Examples

### Example 1 — A market buy walking the book in Reliance (hypothetical)

*All numbers illustrative. Time 11:05 AM IST.* You want to buy 1,500 shares of **Reliance**. The ask side of the book reads:

```
  ASK (sellers)
  Price     Qty
  2,900.50   600
  2,901.00   500
  2,901.50   900
```

You send **BUY 1,500 @ MARKET**. Tick by tick, the engine walks the ask side cheapest-first:

- Fills 600 @ 2,900.50
- Fills 500 @ 2,901.00
- Fills 400 @ 2,901.50 (partial; 500 remain at that level)

Average fill price = (600×2900.50 + 500×2901.00 + 400×2901.50) / 1500 = **₹2,900.93**.

You *saw* 2,900.50 on screen but paid an average of 2,900.93 — that ~₹0.43 gap is **impact cost**, about ₹645 total on this order, purely from your size eating the book. Lesson: in a fast or thin moment, a market order costs more than the quoted price. A limit order at 2,900.50 would have filled only 600 shares — controlling price, sacrificing certainty.

### Example 2 — A protected long in a Bank Nifty heavyweight (hypothetical)

*All numbers illustrative and for observation, not a recommendation. Monday 10:30 AM IST.* You're paper-trading a long in **ICICI Bank** because you notice the bid side stacking (buyers pressing). The depth shows:

```
  BID (buyers)          ASK (sellers)
  Price     Qty         Price     Qty
  1,199.90  4,000       1,200.10  1,200
  1,199.80  3,500       1,200.20  1,000
  1,199.70  2,800       1,200.30    900
```

Bid quantity (10,300 in view) dwarfs ask quantity (3,100) — a hint of buying pressure. You go **long via a LIMIT buy at 1,200.10** (crossing to the best ask to ensure a fill). You get **1,200.10**.

Immediately you set your risk:

- **Stop-loss (SL-M)** trigger at **1,197.10** → risk = 3.00 per share.
- **Target (limit sell)** at **1,206.10** → reward = 6.00 per share.
- **Reward : Risk = 2 : 1.** Good.

Two scenarios unfold:

- *Buyers win:* aggressive buyers keep hitting the ask, price ticks 1,201 → 1,203 → 1,206.10, your target limit fills. Paper profit ₹6.00/share. You did nothing at the top — the order worked for you.
- *Sellers win:* a wave of sell orders hits the bids, price slides to 1,197.10, your stop trigger releases a market sell, you exit near 1,197. Paper loss ~₹3.00/share — exactly the risk you *chose in advance*.

The point of this exercise is not the profit. It's seeing that (a) the depth imbalance was your read, (b) the order types executed your plan mechanically, and (c) your loss was capped *because you defined it before entering*. This is the entire discipline of trading in miniature.

## Common Mistakes (and the fix)

1. **Firing market orders into the 9:15 open.** *Why beginners do it:* excitement, fear of missing the move. *What goes wrong:* spreads are widest and the book is thin, so slippage/impact cost are brutal. *Fix:* watch the first 15 minutes; don't trade them. Prefer limit orders; let the book settle.

2. **Trading illiquid stocks for the "big move."** *Why:* small caps swing more, seem like easy money. *What goes wrong:* wide spreads and thin depth mean you lose on entry and can't exit cleanly; your own order moves the price against you. *Fix:* in this course, stick to Nifty/Bank Nifty and large caps (Reliance, HDFC Bank, ICICI Bank, SBIN, Infosys).

3. **Entering without a stop-loss ("I'll watch it").** *Why:* overconfidence; a stop feels like admitting you might be wrong. *What goes wrong:* one fast adverse move and a small loss becomes an account-threatening one; MIS leverage magnifies it. *Fix:* place the stop-loss in the *same breath* as the entry. If you can't define your stop, you don't have a trade.

4. **Confusing MIS and CNC.** *Why:* the tags are unfamiliar. *What goes wrong:* buy CNC expecting intraday leverage and you tie up full cash and hold overnight by accident; or hold an MIS position past ~3:20 and get force-squared-off at a bad price with extra charges. *Fix:* intraday = MIS, and always know your product tag before confirming. Plan to be flat before 3:20 PM.

5. **Believing a stop-limit always protects you.** *Why:* it sounds strictly better than a stop-market. *What goes wrong:* in a fast gap the price jumps past your limit and the order never fills — you're still in the loss. *Fix:* understand the trade-off; for intraday protection in liquid instruments, a stop-loss *market* (SL-M) prioritises getting you out.

## Nuances & Edge Cases

- **LTP is stale.** The last traded price is the past. Decisions live at the bid and ask. A stock can show LTP 100.20 while the only thing you can actually buy at is 100.35 because the book thinned out. Always glance at the spread, not just the LTP.
- **The book is a hint, not a promise.** Large resting orders can be pulled (cancelled) in an instant, and some are placed to mislead. Depth imbalance suggests pressure; it doesn't guarantee direction. Never treat the book as certainty.
- **Circuit limits pause trading.** SEBI/exchange rules halt or band a security if it moves too violently (upper/lower circuit). If you see price "frozen," it may be at a circuit — you may not be able to exit at will. Another reason to avoid thin, jumpy names.
- **Index heavyweights lead the index.** Because of free-float weighting, watching the top 2–3 Bank Nifty constituents often previews the index's next tick better than watching the index number itself.
- **Auto square-off time can vary by broker/segment.** ~3:20 PM is typical for equity MIS, but confirm your broker's exact time. Treat it as a deadline you beat, not one you test.
- **Spread is your minimum cost, before any brokerage or taxes.** Even a "flat" trade that you enter and exit at the same LTP actually loses the spread. Costs like STT and brokerage stack on top (covered later). Frequent trading multiplies all of this.

## Day-by-Day (Mon–Fri)

- **Monday — Map the machine.** Open your broker's or a charting platform's market-depth window for **Reliance** and **HDFC Bank**. *Observation target:* write down the best bid, best ask, and spread at 9:30, 12:00, and 3:00 PM. Note how the spread and depth change through the day.
- **Tuesday — Watch the auction.** Observe the **pre-open session (9:00–9:15)**. *Observation target:* note the discovered opening price for Nifty and Bank Nifty and how the first 15 minutes after 9:15 behave (wide? violent?). Do not trade.
- **Wednesday — Order types on paper.** In a paper/demo account place (and cancel) one of each: market, limit, stop-loss (SL-M), stop-limit. *Observation target:* record which gave price certainty vs execution certainty, and note that limit orders below/above market just *sit* in the book.
- **Thursday — Index vs its heavyweights.** Put **Bank Nifty**, **HDFC Bank**, and **ICICI Bank** side by side. *Observation target:* for 30 minutes, note how the two banks' ticks lead or lag the index. Confirm with your own eyes that the giants move the index.
- **Friday — Simulate one full round trip.** On paper, go long a liquid stock (e.g. **SBIN** or **Infosys**) *with a predefined stop-loss and a 2:1 target set at entry.* *Observation target:* record entry, stop, target, actual fill prices, and whether you experienced any slippage. Ensure you are "flat" (no open position) before 3:20 PM.

## Key Takeaways

- The NSE is an electronic, **order-driven** exchange; price is where the best bid and best ask meet, matched by **price-time priority**.
- The **order book / market depth** shows bids, asks, spread, and depth — read it to gauge liquidity and pressure, but treat it as a hint, not a promise.
- **Order types** are instructions: market (execution certainty), limit (price certainty), stop-loss (protection), stop-limit (protection with a fill risk). Every trade gets a stop-loss, set at entry.
- **MIS** enables intraday leverage and shorting but forces an **auto square-off (~3:20 PM)**; **CNC** is delivery and settles **T+1**. **SEBI** regulates and protects the whole system.
- Indices like **Nifty 50 / Bank Nifty** are **free-float weighted** baskets; heavyweights dominate and lead the index.
- **Slippage** and **impact cost** are unavoidable frictions — minimise them with liquid instruments, appropriate order types, and by avoiding the chaotic open.

## This Week's Milestone

You can open a live market-depth window and, out loud, correctly narrate a single security: name the best bid, best ask, spread, and which side has more depth; explain what would happen if you sent a market buy (which asks it would consume and the likely impact cost); and state which product tag (MIS/CNC) you'd use for an intraday trade and when it would auto square-off. If you can do that from memory, without notes, Week 1 is complete.

---

> **◀ Previous:** [Roadmap Overview](../roadmap.md) &nbsp;|&nbsp; **Course Home:** [Lessons Index](./README.md) &nbsp;|&nbsp; **Next ▶:** [Week 2 — Candlestick Anatomy](./week-02-candlestick-anatomy.md)
