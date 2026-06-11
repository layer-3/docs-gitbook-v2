---
description: >-
  Going long or short on Yellow.pro perpetuals, and using two-way (hedge) mode
  to hold both directions on the same pair at once.
---

# Long, Short & Hedge Mode

In perpetual trading you can profit in both rising and falling markets by choosing your **position direction** — and, with hedge mode, hold both directions on the same pair at once.

## Going Long

When you **go long**, you're betting the price will **increase**. You profit if it rises and lose if it falls.

> **Example:** open a long on ETH-USDT at 2,000 with 10x leverage; ETH rises to 2,200 → your position gains 200 USDT per ETH, amplified by leverage relative to the margin used.

Simplified: `PnL = (Exit Price − Entry Price) × Position Size`. If the price falls far enough, the position is liquidated.

## Going Short

When you **go short**, you're betting the price will **decrease**. You profit if it falls and lose if it rises.

> **Example:** open a short on ETH-USDT at 2,000 with 10x leverage; ETH drops to 1,800 → your position gains 200 USDT per ETH.

Simplified: `PnL = (Entry Price − Exit Price) × Position Size`. Losses on a short are theoretically unlimited if the price keeps rising, so risk management is especially important.

| | Long | Short |
| --- | --- | --- |
| Market view | Bullish (price up) | Bearish (price down) |
| Profit when | Price rises | Price falls |
| Loss when | Price falls | Price rises |
| Max loss | Position size (100%) | Unlimited (price can rise infinitely) |

## One-Way vs Two-Way (Hedge) Mode

By default, Yellow.pro operates in **One-Way Mode**: you hold only one direction per market, and opening the opposite side reduces or closes your existing position.

**Two-Way Mode (Hedge Mode)** lets you hold a **long and a short on the same pair simultaneously**, independently of each other.

| | One-Way Mode | Two-Way Mode |
| --- | --- | --- |
| Long + short on same pair | Not allowed | Allowed |
| Opening opposite side | Reduces/closes existing position | Creates a new independent position |
| Complexity | Lower | Higher |
| Best for | Directional traders | Hedging strategies |

### When to use hedge mode

* **Hedging a long** — open a short to offset a temporary decline without closing your long.
* **Strategy separation** — run a longer-term long and a short-term short, tracked separately.
* **Reducing directional bias** — test both sides and close whichever proves wrong.

{% hint style="info" %}
Each direction is an independent position with its own entry price, size, and PnL. In cross margin, both draw from the same balance. Hedge mode does **not** eliminate risk — both positions can lose in a choppy market. You cannot switch modes while you have open positions; close them first.
{% endhint %}

## Related Articles

* [Margin & Leverage](margin-and-leverage.md)
* [Understanding PnL](pnl.md)
* [Risk & Liquidation](risk-and-liquidation/README.md)
