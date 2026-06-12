---
icon: ruler
description: >-
  Spot market trading rules — tick size, step size, minimum order size and
  value, price limits, and slippage tolerance — and why orders get rejected.
---

# Market Rules & Limits

Every spot order is validated against the rules of its market before it's accepted. If an order breaks any rule, it's **rejected** and the reason appears in your Order History. This page lists the rules and the current values for each spot market.

## Order Validation Rules

| Rule | What it means | Reject if… |
| --- | --- | --- |
| **Tick size** | The smallest allowed price increment. Your price must be an exact multiple of it. | Price is not a multiple of the tick size. |
| **Step size** | The smallest allowed amount increment. Your amount must be an exact multiple of it. | Amount is not a multiple of the step size. |
| **Minimum order size** | The smallest amount (in the base asset) you can trade. | Amount is below the minimum. |
| **Maximum order size** | The largest amount (in the base asset) per order. | Amount is above the maximum. |
| **Minimum notional** | The smallest order *value* (price × amount, in USDT). | Order value is below the minimum notional. |
| **Price limits** | The price must fall within the market's allowed range. | Price is below the minimum or above the maximum. |
| **Slippage tolerance** | Market orders are rejected if they would fill too far from the current price (protects you in thin liquidity). | A market order would fill beyond **5%** from the reference price. |
| **Available balance** | You must have enough unreserved balance to cover the order. | Available balance is insufficient. |

## Spot Market Specifications

{% hint style="info" %}
Prices and amounts accept up to 8 decimal places, but must still align to the **tick size** (price) and **step size** (amount) below.
{% endhint %}

| Market | Min order | Max order | Step size | Tick size | Price range (USDT) | Min notional |
| --- | --- | --- | --- | --- | --- | --- |
| **WBTCUSDT** | 0.0001 WBTC | 50,000 WBTC | 0.0001 | 0.01 | 50,000 – 1,000,000 | 1 USDT |
| **ETHUSDT** | 0.001 ETH | 50,000 ETH | 0.001 | 0.01 | 1,000 – 100,000 | 1 USDT |
| **YELLOWUSDT** | 1 YELLOW | 10,000,000 YELLOW | 1 | 0.0001 | 0.0001 – 100 | 5 USDT |

All spot markets currently apply a **5% market-order slippage tolerance**.

## Worked Examples

<details>

<summary>Price not aligned to tick size</summary>

You place a limit buy on **ETHUSDT** at **2,000.005**. The tick size is **0.01**, so the price must end at a multiple of 0.01 (e.g. `2,000.00` or `2,000.01`). The order is rejected. Round your price to the tick size and resubmit.

</details>

<details>

<summary>Amount below the minimum / not aligned to step size</summary>

You try to sell **0.0005 ETH**. The minimum order size on ETHUSDT is **0.001** and the step size is **0.001**, so `0.0005` is both too small and not a valid increment. Use `0.001`, `0.002`, and so on.

</details>

<details>

<summary>Order value below the minimum notional</summary>

You place a buy on **YELLOWUSDT** for **3 YELLOW** at **0.50 USDT** — an order value of `1.5 USDT`. The minimum notional is **5 USDT**, so the order is rejected. Increase the amount or price so the total value is at least 5 USDT.

</details>

## Related Articles

* [How to Place a Spot Trade](how-to-place-a-spot-trade.md)
* [Order Types](order-types.md)
* [Managing Orders](managing-orders.md)
