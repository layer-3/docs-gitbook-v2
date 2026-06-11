---
description: >-
  How trading fees work on Yellow.pro for Spot and Perpetuals, and the
  difference between maker and taker orders.
---

# Trading Fees (Maker & Taker)

Yellow.pro charges a trading fee when your order is **filled** on a Spot or Perpetual market. The amount depends on your [VIP tier](vip-tiers.md) and whether your order acts as a maker or taker.

## How Trading Fees Are Calculated

`Fee = Fill Value × Fee Rate`, where `Fill Value = Price × Size`.

> **Example:** buy 1 ETH at 2,000 USDT with a 0.1% taker fee → Fill Value = 2,000 USDT, Fee = 2,000 × 0.001 = **2 USDT**.

Fees are charged in the **quote currency** of the pair (e.g. USDT for USDT pairs), and **only on filled orders** — cancelled or unfilled orders cost nothing, and partial fills are charged only on the filled portion.

## Maker vs Taker

Your rate depends on whether your order adds or removes liquidity:

* **Maker** — adds liquidity by resting in the order book (e.g. a limit buy below the market, or a limit sell above it). **Lower fee.**
* **Taker** — removes liquidity by filling immediately against existing orders (market orders, or limit orders that match an existing price). **Slightly higher fee.**

Order type doesn't always decide this: a limit order placed away from the market is usually a maker, but a limit order placed at a matching price fills instantly as a taker.

{% hint style="info" %}
At higher VIP tiers, some Perpetual markets offer **maker rebates** — you earn rewards instead of paying fees for providing liquidity. See [VIP Tiers & Fee Discounts](vip-tiers.md).
{% endhint %}

## Spot vs Perpetual

Spot trading has slightly higher fees than Perpetual trading. Your exact maker and taker rates on both markets are set by your **VIP tier** — see the full schedule in [VIP Tiers & Fee Discounts](vip-tiers.md).

## Important Things to Know

* **Funding fees are separate** — Perpetual traders also pay [funding fees](funding-fees-explained.md) (every 8 hours).
* **Your VIP tier updates automatically** as your trading activity or $YELLOW balance changes.
* **No separate $YELLOW discount** — your savings come from your VIP tier, not from paying fees with $YELLOW. See [$YELLOW Token & Fee Discounts](yellow-token-fee-discount.md).
* The fee you pay is divided internally afterwards — see [Fee Split Explained](fee-split.md).

## Where to Check Your Fees

View exact fees in your trade history — Spot at `yellow.pro/spot/orders?tab=trades`, Perpetual at `yellow.pro/perps/orders?tab=trades`. Each trade shows the fee type (maker or taker), the amount charged, and the executed price and size.

## Related Articles

* [VIP Tiers & Fee Discounts](vip-tiers.md)
* [Funding Fees Explained](funding-fees-explained.md)
* [Fee Split Explained](fee-split.md)
