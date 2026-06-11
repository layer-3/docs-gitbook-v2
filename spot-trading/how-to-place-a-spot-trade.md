---
description: A step-by-step guide to placing and cancelling a spot trade on Yellow.pro.
---

# How to Place a Spot Trade

## Before You Start

Make sure you have:

* connected your wallet and logged in to [Yellow.pro](https://yellow.pro)
* deposited funds into your account
* sufficient **Available** balance in the relevant currency

> If your balance shows as **Reserved**, those funds are locked in open orders. Cancel an open order to release them.

{% stepper %}
{% step %}
### Select a market

On the left panel of the trading interface, browse or search for the market you want to trade (for example, `ETH-USDT`). The order book, chart, and order form load for that market.
{% endstep %}

{% step %}
### Choose your order type

In the order form, select your order type:

* **Market order** — executes immediately at the best available price. No price input needed.
* **Limit order** — executes at your specified price or better. Requires a price input.
* **Stop Limit / Stop Market** — conditional orders that activate when a trigger price is reached.

Not sure which to choose? See [Order Types](order-types.md).
{% endstep %}

{% step %}
### Set the side: Buy or Sell

* **Buy ETH-USDT** → you spend USDT to receive ETH.
* **Sell ETH-USDT** → you spend ETH to receive USDT.
{% endstep %}

{% step %}
### Enter price and amount

* **Market order:** enter only the **Amount**; the platform uses the best available price.
* **Limit order:** enter both the **Price** and the **Amount**.

The form shows an estimated **total value** before you confirm.

> Ensure your price respects the market's **tick size** and your amount respects the **step size**, or the order will be rejected.
{% endstep %}

{% step %}
### Review and submit

Double-check the market, side, order type, price (if applicable), amount, and estimated fee, then click **Buy** or **Sell**.
{% endstep %}

{% step %}
### Monitor your order

After submission:

* your order appears in **Open Orders** at the bottom of the screen
* if it fills immediately, your balance updates and the trade appears in **Trade History**
* if it's a limit order waiting to be filled, it stays in **Open Orders** until matched or cancelled
{% endstep %}
{% endstepper %}

## Cancelling an Open Order

1. Go to the **Open Orders** tab at the bottom of the screen.
2. Find the order you want to cancel.
3. Click the **Cancel** (X) button next to it.

Funds reserved for the cancelled order return to your **Available** balance immediately.

## Tips for New Traders

* Start with small amounts while you get familiar with the interface.
* Use limit orders when you care about the exact execution price.
* Always verify your order details before confirming — there is no undo after submission (though you can cancel a limit order if it hasn't filled yet).
* Check market parameters (tick size, minimum size) if your order is being rejected.

## Related Articles

* [Order Types](order-types.md)
* [Managing Orders](managing-orders.md)
