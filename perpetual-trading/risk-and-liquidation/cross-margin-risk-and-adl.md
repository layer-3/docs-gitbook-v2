---
description: >-
  How cross margin aggregates risk across all your positions, and how
  auto-deleveraging (ADL) works as a last-resort backstop.
---

# Cross-Margin Risk & ADL

## How Cross Margin Aggregates Risk

Yellow.pro uses **cross margin**, so all positions share one pool of collateral — your total account balance. Liquidation is assessed on your **entire account**, not a single position:

`Account Equity = Total Balance + Total Unrealized PnL`
`Margin Ratio = Total Maintenance Margin Required / Account Equity`

Liquidation occurs when the total-account margin ratio reaches 100%.

> **Example:** a long ETH down −300 USDT and a short BTC up +100 USDT net to −200 USDT. If the ETH loss grows, the combined margin ratio can trigger liquidation — even though the BTC short is profitable.

### The cascade effect

In extreme conditions, one position's losses can threaten the whole account: the market moves sharply against position A → account equity drops → the account margin ratio rises → if it hits 100%, **all positions may be liquidated, including profitable ones.** This is the main risk of cross margin.

**Protective measures:** use a stop-loss on every position, size positions so no single trade dominates, keep free margin well above zero, and monitor your margin ratio in volatile markets.

## Auto-Deleveraging (ADL)

**ADL** is a last-resort risk mechanism used when a liquidated position cannot be covered by the platform's **insurance fund** (for example, when the market moves too fast to close it at the bankruptcy price). It should not occur under normal conditions.

### How ADL works

1. A position is liquidated and can't be fully covered by the insurance fund.
2. The ADL engine ranks traders on the **opposite side** by profit percentage and leverage (highest profit + highest leverage = highest priority).
3. Top-ranked traders' positions are automatically reduced by the amount needed to cover the shortfall.
4. Affected traders are notified and can re-enter the market immediately.

### The ADL indicator

Yellow.pro shows an **ADL indicator** (a series of bars/lights) next to your open positions — more bars lit means higher ADL priority. Priority rises with high profit and high leverage. To reduce it: take some profit (partially close) or reduce leverage.

{% hint style="info" %}
If you're ADL'd, the closed portion is settled at the **Mark Price** at the time — not a penalty price — and your realized PnL is credited. ADL is rare and typically only happens in severe crashes, very low liquidity, or black-swan events.
{% endhint %}

## Related Articles

* [Liquidation & Mark Price](liquidation-and-mark-price.md)
* [Margin Warnings & Risk Management](margin-warnings-and-risk-management.md)
* [Margin & Leverage](../margin-and-leverage.md)
