---
icon: ruler
description: >-
  Perpetual contract specifications — tick size, step size, minimum order size
  and value, price band, max leverage, and maintenance margin — and why orders
  get rejected.
---

# Contract Specifications

Every perpetual order is validated against the contract's rules before it's accepted. If an order breaks any rule, it's **rejected** and the reason appears in your Order History. This page lists the rules and the current values for each perpetual contract.

## Order Validation Rules

| Rule | What it means | Reject if… |
| --- | --- | --- |
| **Tick size** | The smallest allowed price increment. Your price must be an exact multiple of it. | Price is not a multiple of the tick size. |
| **Step size** | The smallest allowed amount increment. Your amount must be an exact multiple of it. | Amount is not a multiple of the step size. |
| **Minimum order size** | The smallest amount (in the base asset) you can trade. | Amount is below the minimum. |
| **Maximum order size** | The largest amount (in the base asset) per order. | Amount is above the maximum. |
| **Minimum notional** | The smallest order *value* (price × amount, in USDT). | Order value is below the minimum notional. |
| **Price band** | A limit price must stay within a range around the reference (mark) price. | Price is below **50%** or above **150%** of the reference price. |
| **Maximum leverage** | The highest leverage allowed on the contract. | Selected leverage exceeds the maximum. |
| **Available margin** | You must have enough free margin to open or increase the position. | Available margin is insufficient. |

{% hint style="info" %}
The **price band** is why a limit order placed far from the current price can be rejected even when its price is otherwise valid. It prevents fat-finger orders and trades at unrealistic prices.
{% endhint %}

## Contract Specifications

| Contract | Min order | Max order | Step size | Tick size | Price band | Min notional | Max leverage | Maintenance margin |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **BTCUSDT-PERP** | 0.001 BTC | 1,000,000 BTC | 0.001 | 0.1 | 50% – 150% of reference | 1 USDT | 100× | 0.5% |
| **ETHUSDT-PERP** | 0.001 ETH | 1,000,000 ETH | 0.001 | 0.01 | 50% – 150% of reference | 1 USDT | 100× | 0.5% |

The **maintenance margin rate (MMR)** is the fraction of position notional you must keep to avoid liquidation. See [Margin & Leverage](margin-and-leverage.md) and [Liquidation & Mark Price](risk-and-liquidation/liquidation-and-mark-price.md) for how leverage and maintenance margin affect your positions.

## Worked Examples

<details>

<summary>Price not aligned to tick size</summary>

You place a limit order on **BTCUSDT-PERP** at **60,000.05**. The tick size is **0.1**, so the price must end at a multiple of 0.1 (e.g. `60,000.0` or `60,000.1`). The order is rejected. Round your price to the tick size and resubmit.

</details>

<details>

<summary>Limit price outside the price band</summary>

With BTC trading around **60,000**, you place a limit buy at **20,000** — below **50%** of the reference price (30,000). The order falls outside the price band and is rejected. Place the order within the allowed range around the current price.

</details>

<details>

<summary>Amount below the minimum / not aligned to step size</summary>

You try to open a **0.0005 BTC** position on BTCUSDT-PERP. The minimum order size is **0.001** and the step size is **0.001**, so `0.0005` is both too small and not a valid increment. Use `0.001`, `0.002`, and so on.

</details>

## Related Articles

* [Margin & Leverage](margin-and-leverage.md)
* [Liquidation & Mark Price](risk-and-liquidation/liquidation-and-mark-price.md)
* [FAQ](faq.md)
