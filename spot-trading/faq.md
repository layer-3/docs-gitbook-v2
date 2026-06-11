---
icon: circle-question
description: Quick answers to common spot trading questions on Yellow.pro.
---

# Spot Trading — FAQ

<details>

<summary>What is the difference between a market order and a limit order?</summary>

A **market order** executes immediately at the best price currently available — you don't choose a specific price. A **limit order** lets you specify the exact price at which you want to buy or sell, and only fills at that price or better; if no matching liquidity exists, it stays open until filled or cancelled.

Market orders prioritise speed; limit orders prioritise price control. See [Order Types](order-types.md).

</details>

<details>

<summary>What is a stop limit order and how do I use it?</summary>

A stop limit order activates only when the market reaches your **trigger price**, then places a **limit order** at your defined limit price. Set the trigger price (when it activates) and the limit price (the price of the resulting order). Because a limit order is placed after the trigger, there's no guarantee of execution if the market moves quickly past your limit price. See [Order Types](order-types.md).

</details>

<details>

<summary>What is a stop market order and how does it differ from stop limit?</summary>

A stop market order also activates at a trigger price, but submits a **market order** immediately upon activation instead of a limit order. Use stop **market** when you want to ensure execution after the trigger; use stop **limit** when you want to control the worst price you'll accept. See [Order Types](order-types.md).

</details>

<details>

<summary>Why did my limit order execute immediately instead of waiting?</summary>

A limit order fills immediately if your price matches or beats existing orders in the book. For example, a buy limit at 2,050 USDT with sell orders available at 2,040 fills right away at the better price — you took liquidity (acted as a taker). The limit price is the *worst* price you'll accept, not a guarantee the order will wait. This is expected behaviour.

</details>

<details>

<summary>Why was my order not executed?</summary>

Common reasons: the market never reached your limit price; insufficient liquidity at your price; the order was cancelled (including by IOC/FOK time-in-force settings); or it was rejected in validation. Check your Order History for the status and reason. See [Managing Orders](managing-orders.md).

</details>

<details>

<summary>Why are my funds locked while I have an open order?</summary>

When you place an order, Yellow reserves the funds needed to fill it — buy orders reserve the quote currency (e.g. USDT), sell orders reserve the base currency (e.g. BTC or ETH). They show as **Reserved** and return to **Available** when the order is filled, cancelled, or rejected. This stops you from spending the same funds on multiple orders at once.

</details>

<details>

<summary>Why did my trade execute at a different price than expected?</summary>

This typically happens with **market orders**: if your order is large or liquidity is thin, it fills across multiple price levels, producing an average price different from what was shown — this is **price slippage**, more pronounced in less liquid markets. For limit orders this is unusual; review your fill history and contact support if you suspect an error.

</details>

<details>

<summary>What is the difference between Open Orders, Order History, and Trade History?</summary>

**Open Orders** — currently active orders waiting to be filled or cancelled. **Order History** — a log of all orders placed (filled, partially filled, cancelled, or rejected). **Trade History** — a record of every actual fill. An order can appear in Order History with no Trade History entry if it was cancelled or rejected before filling. See [Managing Orders](managing-orders.md).

</details>

<details>

<summary>Why was my order rejected?</summary>

Orders are rejected when they fail validation — common causes include price not aligned with tick size, size not aligned with step size, below minimum order size or value, insufficient available balance, invalid trigger settings, or a temporarily unavailable market. The rejection reason appears in Order History. See [Managing Orders](managing-orders.md).

</details>

<details>

<summary>What is the difference between a maker and a taker?</summary>

A **maker** places an order that rests in the book and adds liquidity (typically a limit order that doesn't fill immediately). A **taker** matches an existing order immediately and takes liquidity (always the case for market orders, and for limit orders that cross the spread). See [Fees](../fees/trading-fees.md) for how this affects your rate.

</details>
