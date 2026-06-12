---
icon: circle-xmark
description: >-
  How to close a perpetual position fully or partially on Yellow.pro, and what
  happens to your margin and realized PnL.
---

# Closing a Position (Full or Partial)

Closing a position locks in your **Realized PnL** and releases its margin back to your Available Balance. There are two ways to close: a one-click market close, or a controlled close through the order form.

## Quick Close (the ✕ button)

Clicking the **✕** next to a position in the **Positions** panel places an immediate **market order** to close the **entire** position — there are no order-type or amount options. It fills against the best available prices straight away; if there isn't enough liquidity to match it, it fills **partially** and the remainder **expires**. It's the fastest way out, with the least control — use it when you just need to exit.

![Closing a position with the ✕ button in the Positions panel](../../.gitbook/assets/perp-close-position.png)

## Controlled Close (order form → Close tab)

For full control — including partial closes and specific exit prices — close through the order form instead of the ✕ button:

1. Switch the order form to the **Close** tab.
2. Choose the order type: **Market**, **Limit**, or **Stop**.
3. Enter the **amount** to close — your full size, or less for a partial close.
4. Confirm.

A **Limit** close lets you exit at a specific price or better (e.g. a take-profit level); a **Stop** close triggers at a price you set. A **partial** close leaves the rest of the position open at the original entry price, with margin adjusting proportionally. Resting limit or stop closes wait in **Open Orders** until they fill or you cancel them.

![Closing through the order form's Close tab](../../.gitbook/assets/perp-close-partial.png)

> **Example:** you hold 2 ETH long and close 1 ETH → your position becomes 1 ETH long, and half the margin is released.

{% hint style="info" %}
Take Profit / Stop Loss orders must currently be set manually — they are not automatically linked to a position.
{% endhint %}

## After Closing

* **Realized PnL** is credited or debited from your balance (trading fees are deducted).
* The position leaves the Positions panel and the closed trade appears in **Trade History**.
* In cross margin, closing one position can affect the others — always check your remaining balance.

**Tip:** use the **✕ quick close** (market) to exit fast — e.g. to avoid liquidation; use a **Limit close** in the Close tab when you have a target price and aren't in a rush.

## Related Articles

* [Adjusting Margin & Leverage](adjusting-margin-and-leverage.md)
* [Understanding PnL](../pnl.md)
