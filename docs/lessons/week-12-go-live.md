# Week 12 — Go Live: Small & Real

> **◀ Previous:** [Week 11 — Review & Refine](./week-11-review-and-refine.md) &nbsp;|&nbsp; **Course Home:** [Lessons Index](./README.md) &nbsp;|&nbsp; **Next ▶:** [Course Complete — Lessons Index](./README.md)

_This week you cross the line from paper to real money — using the smallest size possible — so that emotion, not method, is the only new variable, and you learn exactly how NSE costs eat into every trade._

## Why This Week Matters

For eleven weeks you have done everything except the one thing that actually defines a trader: risking your own rupees. You have read candles, drawn supply and demand zones, timed the opening range, sized positions on paper, and kept a journal. Your method is built. This week nothing about that method changes. One thing — and only one thing — changes: the money is now real, and real money produces real emotion.

That single change is bigger than it sounds. On paper, a stop-loss is a number you type without a flinch. With real money, that same number is a small physical event — a tightening in your chest, a whisper that says "give it one more tick." The entire purpose of Week 12 is to introduce that emotion in the smallest, safest dose possible, prove you can still follow your rules while feeling it, and understand the second silent enemy that paper trading never showed you: **transaction costs**.

Two forces decide whether a beginner survives going live: **psychology** (can you keep behaving like your paper self?) and **cost arithmetic** (does the trade even make money after the exchange, the government, and your broker take their cut?). This week we go deep on both, then place a real trade — tiny, disciplined, and journaled.

## Concept 1 — The Paper-to-Real Psychology Gap

### What actually changes in your brain

Paper trading is a flight simulator. It teaches the controls perfectly but withholds the one input that breaks people: consequence. The moment real money is on the line, your brain routes the decision through a different, older system. Two well-documented biases switch on hard:

- **Loss aversion** — a loss feels roughly twice as painful as an equal gain feels good. On paper a ₹300 loss is a shrug. With real money it stings enough that you start *avoiding* the stop-loss (moving it away, "just this once") to dodge the pain — which is precisely how a small planned loss becomes a large unplanned one.
- **The disposition effect** — the urge to snatch small profits quickly (to lock in the good feeling) while letting losers run (to postpone the bad feeling). This inverts your edge: it cuts winners short and lets losers grow, the exact opposite of "cut losses, let winners run."

None of this appears on paper because there is no consequence to trigger it. So paper competence is necessary but **not sufficient**. You are not fully trained until you have felt the emotion and followed the rules anyway.

### Why tiny size is the master dial

Here is the key mechanism most beginners never grasp: **emotion scales with the money at risk, not with the trade itself.** A trade where a bad outcome costs you ₹150 produces almost no fear. The same setup where a bad outcome costs ₹15,000 produces panic — hesitation, revenge, freezing. The chart is identical; only the emotional volume knob moved.

So size is the dial you use to keep emotion low enough that your rules survive contact with real money. This week you turn that dial almost all the way down. You will trade the **smallest possible size** — an amount where losing the full stop is genuinely a non-event. The goal is to make the *behaviour* real (clicking buy, setting a stop, walking away) while keeping the *stakes* trivial. Over months, as discipline proves itself, you raise the dial one notch at a time — never faster than your composure allows.

Caption: the same setup, felt two ways — and the one dial that controls it.

```
 PAPER TRADE                 REAL TRADE (same setup, real ₹)
 ------------                ------------------------------
 signal -> click now         signal -> ..hesitate.. -> click late
 stop hit -> "meh, next"     stop hit -> "one more tick, maybe.."
 no bodily response          heart rate up, palms, urge to override
 rules easy to follow        rules FIGHT your emotions

  The dial that shrinks the gap:  >>> SIZE <<<
   big size  = big emotion  = rules break
   tiny size = small emotion = rules survive first contact
```

## Concept 2 — The Full Anatomy of an NSE Intraday Cost

On paper, a ₹500 favourable move was a clean ₹500. In reality, a chain of charges is skimmed off *every* buy and *every* sell. For the small trades you will place this week, these charges are large **as a percentage** of the move — large enough to turn a "correct" trade into a net loss. You cannot manage what you don't understand, so here is every line, what it is, and who collects it. (All rates below are **illustrative** — brokers and exchanges revise them; confirm your broker's live tariff.)

### The product code comes first: MIS vs CNC

Before costs, one setting decides everything. When you place an equity order your broker asks for a **product type**:

- **MIS (Margin Intraday Square-off)** — an intraday product. You get leverage, you pay *intraday* charges, and the position is **auto-squared-off by your broker around 3:20 PM IST** if you haven't closed it. This is what you use this week.
- **CNC (Cash and Carry)** — a delivery product. Shares move into your demat account, you can hold overnight, but you pay *delivery* charges (higher STT, plus DP charges on the sell) and get no intraday leverage.

Choosing CNC by accident on an intended intraday trade is a classic, expensive beginner error — you take delivery, pay delivery costs, and tie up capital. Always confirm **MIS** for intraday.

### The charges, one by one

- **Brokerage — flat vs percentage.** Most discount brokers charge **₹20 per executed order, or 0.03% of turnover, whichever is lower**, on equity intraday. "Per order" means buy and sell are two separate charges — so a round trip is up to **₹40**. On a large trade the 0.03% cap keeps it at ₹20; on a small trade the flat ₹20 dominates. This is the single biggest reason tiny trades bleed: ₹40 is a huge fraction of a ₹100 gross profit.
- **STT (Securities Transaction Tax) — the government's cut.** On equity **intraday**, STT is **0.025%, charged on the SELL side only**. Remember that direction: you are taxed when you exit. (On delivery it is 0.1% on *both* sides — far heavier, another reason not to slip into CNC.)
- **Exchange transaction charge.** The NSE's fee for matching your order — roughly **0.00297%** of turnover on both buy and sell. Small, but always present.
- **GST — tax on the middlemen's fees.** **18%**, charged not on your turnover but on **(brokerage + exchange transaction charge + SEBI fee)**. It is a tax on the services you consumed, so it rides on top of those service charges.
- **SEBI turnover fee.** The regulator's fee: **₹10 per crore** of turnover (0.0001%). Tiny in rupees, but it exists and it feeds the GST base.
- **Stamp duty — the state's cut, BUY side only.** **0.003%** on the buy side for equity intraday. Note the asymmetry: STT hits your sell, stamp duty hits your buy.
- **DP charges — DELIVERY only, NOT intraday.** Depository Participant charges (~₹13–16 + GST **per scrip, per day**) are levied when shares leave your demat on a **delivery sell**. Pure intraday (MIS) never triggers them — but the moment you accidentally take delivery, they appear. Know they exist so an accidental overnight hold doesn't surprise you.

Caption: which side each charge lands on — memorise the asymmetry.

```
        BUY leg                         SELL leg
   ---------------------          ---------------------
   Brokerage      (flat)          Brokerage      (flat)
   Stamp duty     0.003%          STT            0.025% <- only here
   Exch txn       0.00297%        Exch txn       0.00297%
   SEBI fee       tiny            SEBI fee       tiny
        |                              |
        +----> GST 18% on (brokerage + exch txn + SEBI), both legs
   (DP charges: appear ONLY if this becomes a DELIVERY sell)
```

## Concept 3 — The Breakeven Move: Why Small Trades Lose Even When You're Right

Because those charges are mostly **fixed or turnover-based**, they behave like a wall your trade must clear *before you earn a single rupee*. That wall is the **breakeven move** — the price distance you need just to get back to zero.

Two facts make this brutal for beginners:

1. **You pay costs whether you win or lose.** Costs are not deducted from profit; they are deducted from the transaction. A losing trade costs you the stop distance *plus* the full round-trip charges. A winning trade earns the target distance *minus* the same charges.
2. **Costs therefore degrade your reward-to-risk ratio.** A setup you planned as a clean 1:2 on paper is worse than 1:2 in reality, because the same ~₹75 leaks out of both the win and the loss. The smaller your absolute rupee move, the more that fixed leak dominates — until, for a tiny scalp, the trade is a guaranteed loser no matter how right your direction was.

The defence is not to avoid costs (impossible) but to **only take trades whose expected move dwarfs the cost wall**, and to **never over-trade**, because every extra round trip is another ₹40–₹75 leak. Fewer, larger, higher-conviction trades beat many tiny ones — the arithmetic guarantees it.

Caption: SBIN intraday, 100 shares bought at ₹800; round-trip cost ≈ ₹76.

```
 Round-trip cost ≈ ₹76  ->  breakeven move = ₹76 / 100 sh = ₹0.76/sh

  entry
    |
    v
 ₹800.00      ₹800.76                        ₹808.00
    |------------|----------------------------|-------> price
   BUY       BREAKEVEN                     target(+₹8)
 (costs due)  (gross = costs,             net +₹724 after
              you keep ₹0)                 ~₹76 costs
  <-- NET LOSS ZONE -->|<------ NET PROFIT ZONE ------->

  A +₹0.60/share move (looks like a win!) = ₹60 gross
  but ₹60 - ₹76 costs = -₹16 NET.  Right direction, real loss.
```

## Concept 4 — Choosing Capital You Can Truly Afford to Lose

Go-live capital is not "money I hope to grow." It is **money whose complete disappearance changes nothing about your life.** Test it with one honest question: *if this entire amount vanished tomorrow, would my rent, food, EMIs, or family be affected in any way?* If the answer is anything but a flat no, the amount is too large.

- **Only 100% discretionary money.** No borrowed funds, no credit-card float, no money earmarked for anything, and absolutely no "I'll make it back" money. Borrowed money adds a repayment clock, and a clock destroys the calm that discipline needs.
- **Small enough that a bad week is a non-event.** For a true beginner this is a modest figure — think a few thousand rupees, not lakhs. It needs to be *real* enough to trigger genuine emotion (that is the training), yet *small* enough that losing it is boring.
- **Ring-fenced.** Keep this "learning capital" mentally and, ideally, physically separate from savings. It has one job: to teach you, at real emotional cost, whether you can follow your rules.

Your **1–2% per-trade risk rule** now applies to this small pot, and your **daily loss limit** still stands: if you hit it, you are done for the day, no exceptions.

## Concept 5 — The Go-Live Rulebook (Deliberately Restrictive)

This week's rules are stricter than any week before, on purpose. Restriction removes the freedom to make emotional mistakes while you are most vulnerable.

1. **Trade the minimum size.** The smallest quantity that still forms a real trade — e.g. a handful of shares of a liquid stock (SBIN, ICICI Bank, HDFC Bank) sized so your stop risks only 1–2% of your tiny capital. **Trade only the instrument you actually paper-traded.** If you never paper-traded index options, this is not the week to start.
2. **One trade per day. Maximum.** Not one *good* trade — one trade, full stop. When it is done (win, loss, or scratch), you close the terminal for the day. This caps both cost leakage and the number of chances your emotions get to sabotage you.
3. **Rules identical to paper.** Same setup, same zone logic, same entry trigger, same stop-loss placement, same target, same time-of-day filter. If it would not have been a paper trade, it is not a real trade.
4. **A stop-loss order on every single trade, placed before or immediately at entry.** Reward:risk ≥ 1:2 *on paper*, sized so the move comfortably clears the cost wall. No mental stops — a real, resting stop-loss order in the terminal.
5. **Journal it, with two new columns: _costs paid_ and _net P&L_.** Same journal as paper, plus the truth about what you actually kept.

### Go-live readiness checklist

Do not place a real order until you can tick every box honestly:

```
[ ] 20+ paper trades logged with a written journal
[ ] Paper results look consistent, not lucky (rules-followed %)
[ ] A one-page written rulebook exists: entry, stop, target, size
[ ] Account funded ONLY with money I can truly afford to lose
[ ] I know my broker's EXACT intraday charges (I looked them up)
[ ] I can state my breakeven move in ₹ for my chosen instrument
[ ] Product set to MIS; I've located the stop-loss order type
[ ] Max 1 trade/day at minimum size — agreed with myself in writing
[ ] Daily loss limit set: "if I lose today, I stop for the day"
```

If any box is blank, stay on paper one more week. There is no prize for rushing, and the market will still be here.

## Concept 6 — Scaling Up (Slowly) and When to Retreat to Paper

### Size follows evidence, never feelings

Two green days are not evidence — they are noise. You increase size only against a documented track record:

- Trade **minimum size for at least a month, or ~20 real trades**, whichever is longer.
- Review the journal for the metric that matters most: **rules-followed percentage, independent of P&L.** If you followed your rules on >90% of trades, you have proven the behaviour. If you were profitable but broke rules, you got *lucky* and must fix that before sizing up.
- Only then step size up **one small notch** (e.g. 5 shares → 10), and hold there for another full block of trades before the next step.
- **Any rule-break, or a losing streak that rattles you, means step back down a rung.** Discipline must scale before size does.

Caption: the scaling ladder — each rung earned, any slip drops you down.

```
 SIZE
  ^
 4x|                                    . . . (only ever
  |                               _____/       on evidence)
 3x|                        _____/  ~20 more rule-following
  |                  _____/         trades at each rung
 2x|            ____/  <- step up ONLY after ~20 trades AND
  |       ____/          >90% rule-adherence at 1x
 1x|_____/  (minimum size: >=1 month / ~20 real trades)
  |________________________________________________> TIME
     any rule-break or losing streak  -->  step DOWN a rung
```

### When to stop and go back to paper

Going live is not a one-way door. Return to paper — with no shame — whenever:

- You break your own rules two or more times in a short span (moving stops, revenge trading, over-trading past one/day).
- You hit your daily or weekly loss limit and notice you *want* to keep trading anyway.
- Life stress (money worries, sleep loss, big personal events) is bleeding into your decisions.
- You realise your paper edge was thinner than you thought once costs were included.

Paper is your recalibration tool for life, not just a phase-one exercise. Dropping back to it is a sign of discipline, not failure.

## Worked Examples

> Both examples use **hypothetical, illustrative** numbers and rates to show the mechanics. They are not predictions and not advice. Verify all live rates and lot sizes with your broker/exchange.

### Example 1 — SBIN equity intraday (the honest round trip)

Monday, 9:50 AM IST. Your paper rulebook says: buy SBIN on a pullback into a demand zone with a 5-min higher-low confirmation. You take the minimum real size — **100 shares** — under **MIS**.

- **Entry:** ₹800.00. **Stop-loss order:** ₹796.00 (risk ₹4/share = ₹400 gross). **Target:** ₹808.00 (reward ₹8/share = ₹800 gross). Nominal reward:risk = 1:2.

The trade works; you exit at ₹808.00. Now the real accounting:

```
 SBIN 100 sh, buy ₹800 -> sell ₹808   (MIS intraday, HYPOTHETICAL)
 Gross P&L   100 x ₹8                        = +₹800.00
 --------------------------------------------------------
 Brokerage   ₹20 buy + ₹20 sell              =  -₹40.00
 STT 0.025% on SELL turnover (₹80,800)       =  -₹20.20
 Exch txn ~0.00297% on ₹160,800 turnover     =   -₹4.78
 SEBI ₹10/crore on ₹160,800                  =   -₹0.16
 Stamp 0.003% on BUY turnover (₹80,000)      =   -₹2.40
 GST 18% on (40 + 4.78 + 0.16)               =   -₹8.09
 --------------------------------------------------------
 Total costs                                 ≈  -₹75.63
 NET P&L                                     ≈ +₹724.37
```

You earned ₹800 in the market and kept ~₹724 — costs took ~9.5% of a healthy move. Fine. **Now watch what a scalp does.** Same 100 shares, but you snatch a quick +₹0.60/share:

- Gross = 100 × ₹0.60 = **+₹60.00**. Costs ≈ **₹75.41**. **Net = −₹15.41.**

You were *right about the direction* and still **lost money**. The breakeven move here is ₹75.63 ÷ 100 ≈ **₹0.76/share** — below that, being correct is not enough. And note the R:R damage on the winning trade: on paper it was 1:2 (₹800 vs ₹400), but net it is ₹724 vs a net loss of ₹475 (₹400 stop + ₹75 costs) ≈ **1.53** — costs quietly shaved your edge.

### Example 2 — Bank Nifty options (why F&O costs bite differently)

Suppose (only if you had genuinely paper-traded this) you buy **1 lot of a Bank Nifty call option**, premium ₹200, and sell at ₹230. Bank Nifty options carry a **lot size** (illustrative 15 here — exchanges revise index lot sizes periodically, so confirm the current figure). Note F&O differs: **options STT is 0.1% on the SELL side of premium**, brokerage is a flat ₹20/order, and exchange charges on options premium are higher.

```
 BANK NIFTY 1-lot option, buy ₹200 -> sell ₹230  (HYPOTHETICAL)
 lot = 15* shares of premium   (*verify current lot size)
 Gross P&L   (230-200) x 15                   = +₹450.00
 --------------------------------------------------------
 Brokerage   ₹20 buy + ₹20 sell               =  -₹40.00
 STT 0.1% on SELL premium (₹3,450)            =   -₹3.45
 Exch txn ~0.03503% on ₹6,450 premium         =   -₹2.26
 SEBI ₹10/crore on ₹6,450                     =   -₹0.01
 Stamp 0.003% on BUY premium (₹3,000)         =   -₹0.09
 GST 18% on (40 + 2.26 + 0.01)                =   -₹7.61
 --------------------------------------------------------
 Total costs                                  ≈  -₹53.42
 NET P&L                                      ≈ +₹396.58
```

The lesson: on a small options trade the **flat ₹40 brokerage dominates** — it alone is ~9% of a ₹450 gross win, and on a ₹30 premium scalp (₹30 × 15 = ₹450... vs a ₹2 move = ₹30 gross) it would swamp the profit entirely. Every instrument has its own cost shape; you must know yours before you trade it live.

## Common Mistakes (and the fix)

1. **Sizing up the moment it's "real" because paper felt easy.**
   *Why beginners do it:* paper success breeds overconfidence, and small size feels "not worth it."
   *The fix:* the whole point of Week 12 is emotional training, not income. Trade minimum size precisely *because* it feels trivial — that's what keeps your rules intact. Income comes months later, after discipline is proven.

2. **Ignoring costs and scalping for tiny moves.**
   *Why beginners do it:* they only ever saw gross P&L on paper, so a "+₹60" looks like a win.
   *The fix:* compute your breakeven move once and pin it to your screen. Never take a trade whose realistic target doesn't clear the cost wall several times over. Fewer, larger trades beat many tiny ones.

3. **Moving or cancelling the stop-loss when the position turns red.**
   *Why beginners do it:* loss aversion — the real pain of a real loss makes "just give it room" feel reasonable.
   *The fix:* place a **resting stop-loss order** in the terminal at entry, and forbid yourself from touching it. If you can't leave it alone, your size is too big — cut it. A stop you widen is not a stop.

4. **Accidentally trading CNC (delivery) instead of MIS, or forgetting to square off.**
   *Why beginners do it:* unfamiliar terminal, wrong default product, or freezing near close.
   *The fix:* verify **MIS** on every order this week, and set a personal alarm for **3:00 PM** to close manually — don't rely on the ~3:20 PM broker auto-square-off (which may add an auto-square-off penalty of ~₹50 and fills you at a worse price). Delivery slippage means higher STT, DP charges, and tied-up capital.

5. **Over-trading to "make back" a loss or a cost.**
   *Why beginners do it:* the sting of the first real loss triggers revenge trading.
   *The fix:* the hard **one-trade-per-day** cap exists exactly for this moment. When the trade is closed, the terminal closes too. Tomorrow is a fresh, single chance.

## Nuances & Edge Cases

- **Costs are charged on losers too.** A losing trade isn't just the stop distance — it's the stop distance *plus* the full round trip. Ten small losing trades in a day can cost you ₹700+ in charges alone before any market loss. This is the strongest possible argument for the one-trade-a-day rule.
- **The ITM-option-at-expiry STT trap.** If you ever hold an *in-the-money* option to expiry, STT is levied on the **intrinsic value at a much higher rate** (historically ~0.125%), which can be enormous relative to your premium. Beginners have been shocked by charges exceeding their "profit." Rule: square off before expiry; never let ITM options sit.
- **Slippage is a hidden cost paper never charged you.** Paper fills you at the exact price you clicked. Real markets fill you at the *available* price — in fast moves or thin stocks your buy fills a little higher and your sell a little lower. Trade liquid names (index majors, large-cap stocks) to keep slippage small, and prefer limit orders where sensible.
- **Auto-square-off is a backstop, not a plan.** The ~3:20 PM broker square-off exists so you don't accidentally carry MIS overnight, but relying on it means a market-order exit at whatever price exists then, plus a possible penalty. Always plan your own exit.
- **Your first real green trade is more dangerous than your first red one.** A win releases a dopamine hit that whispers "do it again, bigger." The disciplined response to a win is identical to a loss: close the terminal, journal it, done for the day.
- **SEBI regulates all of this.** The exchanges (NSE/BSE), the depositories, and your broker all operate under SEBI rules; the charges above are largely mandated pass-throughs (STT/stamp duty are government taxes), which is why no broker can make them disappear — only brokerage itself is competitive.

## Day-by-Day (Mon–Fri)

- **Monday — Cost audit (no trade).** Log into your broker. Find the exact charges/brokerage page and any built-in brokerage calculator. Recompute Example 1 using *your* broker's real rates. Write down, on paper, your **breakeven move in ₹** for the one instrument you'll trade. *Observation target:* what fraction of a ₹100 gross profit your costs consume.
- **Tuesday — Fund & configure (no trade).** Transfer only lose-able capital. Build your watchlist (Nifty, Bank Nifty, Reliance, HDFC Bank, ICICI Bank, SBIN, Infosys). Locate the **MIS** product toggle and the **stop-loss order** type. Do a dry run: build an order, confirm the product is MIS, then **cancel before it executes**. *Observation target:* the exact click-path to place a stop-loss without hesitation.
- **Wednesday — First real trade.** Watch 9:15–9:45 AM IST; let the opening range settle. Take **one** minimum-size trade that exactly matches a paper setup. Set the resting stop and the target *before* entry. Then stop for the day and journal gross, costs, and net. *Observation target:* what your body did when the position first went against you.
- **Thursday — Second real trade + compare.** One trade only. Afterward, compare gross vs net P&L against Wednesday. Did costs surprise you? Did you leave the stop untouched? *Observation target:* whether your real behaviour matched your paper behaviour tick for tick.
- **Friday — Week and course review.** A no-trade day is a valid, disciplined outcome if no clean setup appears. Review every real trade: rules-followed %, total costs paid, and honest emotional notes. Write your decision: hold at minimum size, or (only against evidence) plan the first tiny step up. *Observation target:* your rules-followed percentage, independent of profit.

## Key Takeaways

- Going live changes **only the emotion**, never the method — keep your behaviour identical to your paper self.
- **Tiny size is the master dial**: it keeps emotion low enough that your rules survive real money. Size for training, not income.
- **Costs are charged on every leg, win or lose** — brokerage (flat), STT (sell side, intraday equity), exchange txn, GST on the fees, SEBI fee, stamp duty (buy side); DP only on delivery. Know your **breakeven move** before you trade.
- Small, tiny-target trades can be **net losers even when you're right** — take fewer, larger, higher-conviction trades and never over-trade.
- Fund only with **money you can truly afford to lose**, keep the 1–2%-per-trade and daily-loss-limit rules, and cap yourself at **one trade per day**.
- **Scale up only against documented consistency** (>90% rules-followed over ~20 trades), one notch at a time — and drop back to paper without shame whenever discipline slips.

## This Week's Milestone

You have placed at least **one real, minimum-size NSE intraday trade** under MIS, with a resting stop-loss set before entry, following your written rulebook exactly — and you have journaled its **net-of-cost** P&L alongside the gross. Proving you can risk real rupees with the same discipline you showed on paper is the finish line of this 12-week roadmap, and the true starting line of your trading life.

_This lesson is educational only and not financial advice. All prices, rates, and lot sizes are hypothetical and illustrative; verify current figures with your broker and the exchange. Markets carry real risk of loss — never trade money you cannot afford to lose._

---

> **◀ Previous:** [Week 11 — Review & Refine](./week-11-review-and-refine.md) &nbsp;|&nbsp; **Course Home:** [Lessons Index](./README.md) &nbsp;|&nbsp; **Next ▶:** [Course Complete — Lessons Index](./README.md)
