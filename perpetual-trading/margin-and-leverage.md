---
icon: gauge-high
description: >-
  How cross margin, leverage, initial and maintenance margin, and the margin
  ratio work for perpetual trading on Yellow.pro.
---

# Margin & Leverage

Yellow.pro uses **cross margin** for perpetual trading, combined with adjustable **leverage**. Understanding how they interact is key to managing risk.

## Cross Margin

In **cross margin** mode your **entire available Perpetual account balance** acts as collateral for all open positions — they share one margin pool. This is the margin mode used on Yellow.pro.

* A profitable position can provide buffer for a losing one.
* A single heavily losing position can draw from your whole balance.
* Liquidation triggers when your **total** account margin ratio hits the maintenance threshold — not per individual position.

> **Example:** a long BTC position up +200 USDT and a short BTC position down −150 USDT net to +50 USDT. Cross margin considers the whole account, so the losing leg isn't liquidated on its own.

| | Cross Margin | Isolated Margin |
| --- | --- | --- |
| Collateral | Full perpetual account balance | Fixed amount per position |
| Liquidation scope | All positions share risk | Each position risks only its margin |
| Max loss per position | Up to full account balance | Only the isolated margin |

{% hint style="info" %}
Yellow.pro currently uses **cross margin** as the primary mode. Isolated margin may be introduced in future updates.
{% endhint %}

## Leverage

**Leverage** is a multiplier that lets you open a position larger than your account balance: `Position Size = Margin × Leverage`. With 100 USDT and 10x leverage you control a 1,000 USDT position.

Leverage amplifies both gains **and** losses against the full position size:

| Leverage | Margin | Position Size | 5% gain | 5% loss |
| --- | --- | --- | --- | --- |
| 1x | 100 USDT | 100 USDT | +5 USDT | −5 USDT |
| 10x | 100 USDT | 1,000 USDT | +50 USDT | −50 USDT |
| 20x | 100 USDT | 2,000 USDT | +100 USDT | −100 USDT |

Higher leverage moves your **liquidation price closer** to entry and leaves less buffer for fluctuations. Beginners should start low (1x–5x).

## Initial vs Maintenance Margin

* **Initial Margin** — the minimum required to open a position: `Initial Margin = Position Size / Leverage`.
* **Maintenance Margin** — the minimum required to **keep** a position open. If your effective margin falls below it, liquidation is triggered. It's a fixed percentage of position size, lower than the initial margin.

## Margin Ratio

The **Margin Ratio** is a real-time indicator of how close you are to liquidation:

| Margin Ratio | Meaning |
| --- | --- |
| Low (e.g. <50%) | Well-funded, low risk |
| High (e.g. >80%) | Risk increasing — consider reducing positions |
| 100% | Liquidation triggered |

## How to Reduce Margin Risk

* **Add margin** — deposit more funds to increase your buffer.
* **Reduce position size** — close part of a position to lower required maintenance.
* **Lower leverage** — where supported, reduces liquidation risk.
* **Use stop-loss orders** — exit automatically before liquidation.

> You may receive an email warning when your margin ratio approaches critical levels. See [Margin Warnings & Risk Management](risk-and-liquidation/margin-warnings-and-risk-management.md).

## Related Articles

* [Long, Short & Hedge Mode](long-short-hedge-mode.md)
* [Risk & Liquidation](risk-and-liquidation/README.md)
* [Cross-Margin Risk & ADL](risk-and-liquidation/cross-margin-risk-and-adl.md)
