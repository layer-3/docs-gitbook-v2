---
icon: fire
description: >-
  What triggers liquidation on Yellow.pro, the liquidation process and price,
  and why the mark price (not the last traded price) determines it.
---

# Liquidation & Mark Price

## What is Liquidation?

**Liquidation** is the automatic closure of one or more open positions when your account no longer has sufficient margin to support them. It prevents your balance from going negative. You lose the margin allocated to the affected position(s), but never owe more than you deposited.

## When Does Liquidation Happen?

Liquidation triggers when your **Margin Ratio reaches 100%** — your account equity has dropped to the maintenance margin level:

`Margin Ratio = Maintenance Margin Required / Account Equity`

In **cross margin mode** (used on Yellow.pro), this is calculated across **all** your open positions together, not per individual position.

The **Maintenance Margin Rate (MMR)** is the fraction of position notional you must keep as a buffer. On current markets (BTC and ETH perpetuals) the MMR is a flat **0.5%**:

`Maintenance Margin Required = Position Notional × 0.5%`

{% hint style="info" %}
To protect you from brief price wicks, liquidation is evaluated on the **worst-case mark price** seen in each scan window — the lowest price for longs and the highest for shorts — not on a single instantaneous tick.
{% endhint %}

## The Liquidation Process

1. **Detection** — the system continuously monitors your account's margin ratio.
2. **Trigger** — when the ratio hits 100%, the liquidation engine takes over your account.
3. **Netting** — if you hold both a long and a short in the same market, they are closed against each other first to reduce exposure.
4. **Takeover & settlement** — your remaining position(s) are taken over and matched against opposing traders through [auto-deleveraging (ADL)](cross-margin-risk-and-adl.md), settled at your **Liquidation Price** (or the **Bankruptcy Price** as a fallback — both explained below).
5. **Record** — the liquidation is logged in your Trade History.

![A liquidation entry in trade history](../../.gitbook/assets/perp-liquidation-history.png)

## Liquidation Price

Your **Liquidation Price** is the estimated Mark Price at which your account would be liquidated — the price at which your equity falls to the maintenance margin level. It's shown in the positions panel. In cross margin it is **not fixed**: it moves with your unrealized PnL, positions you open or close, and deposits or withdrawals.

For a single position with balance `B`, the simplified formula is:

```
Long:  Liquidation Price = (Amount × Entry − B) / (Amount × (1 − MMR))
Short: Liquidation Price = (Amount × Entry + B) / (Amount × (1 + MMR))
```

In practice the engine also folds in the unrealized PnL and maintenance margin of your *other* open positions, since cross margin shares one collateral pool. You don't need to compute this by hand — the platform displays your live liquidation price — but the formula shows what moves it.

<details>

<summary>Worked example</summary>

You open a long of **0.1 BTC at 50,000**, with a balance of **1,000 USDT** and no other positions. At MMR = 0.5%:

`(0.1 × 50,000 − 1,000) / (0.1 × (1 − 0.005)) = 4,000 / 0.0995 ≈ 40,201`

Your liquidation price is about **40,201**. Adding margin lowers it; opening more positions or taking losses elsewhere raises it.

</details>

## Bankruptcy Price

The **Bankruptcy Price** is the Mark Price at which your account equity reaches **zero**. It sits *beyond* your liquidation price (lower for a long, higher for a short) — liquidation is triggered first, leaving a thin buffer before bankruptcy.

```
Long:  Bankruptcy Price = Entry − (Account Equity / Position Size)
Short: Bankruptcy Price = Entry + (Account Equity / Position Size)
```

A liquidation normally settles at your liquidation price. The bankruptcy price is the **fallback** used when the liquidation price can't be applied — it's the worst-case floor for what a position can settle at. Any value between your liquidation price and bankruptcy price is consumed by the liquidation; whatever remains (often little or nothing) stays in your balance.

## Mark Price vs Last Traded Price

Yellow.pro shows two prices, and the difference matters:

* **Last Traded Price** — the price of the most recent trade. It can be briefly distorted by large orders or thin liquidity.
* **Mark Price** — a calculated fair-value price derived from external reference data that smooths out temporary anomalies.

**Liquidation and unrealized PnL are based on the Mark Price**, not the last traded price.

{% hint style="info" %}
This protects you both ways: a temporary spike in the last traded price that doesn't move the Mark Price will **not** liquidate you — but a drop in the Mark Price that isn't visible on the chart **can**. Always watch the Mark Price in your positions panel.
{% endhint %}

## How to Avoid Liquidation

* Set **stop-loss orders** to exit before the liquidation threshold (not guaranteed).
* **Add margin** (deposit funds) to increase your buffer.
* **Reduce position size or leverage** to lower the maintenance margin required.
* **Monitor your margin ratio** and act early. Make sure [margin warning emails](margin-warnings-and-risk-management.md) are enabled.

## Related Articles

* [Cross-Margin Risk & ADL](cross-margin-risk-and-adl.md)
* [Margin Warnings & Risk Management](margin-warnings-and-risk-management.md)
* [Margin & Leverage](../margin-and-leverage.md)
