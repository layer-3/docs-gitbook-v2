---
icon: book-open
description: Definitions of key terms used across Yellow.pro.
---

# Glossary of Terms

Key terms used throughout Yellow.pro and this documentation.

<details>

<summary>Account Balance (Yellow Wallet)</summary>

For Google Sign-in users, the main balance where deposits first arrive and from which withdrawals are made. Funds must be transferred to the Trading Account before trading. Also accessible on Yellow.com. External wallet users do not use Account Balance. See [Understanding Your Balances](../account-and-balance/understanding-your-balances.md).

</details>

<details>

<summary>ADL (Auto-Deleveraging)</summary>

The mechanism that settles liquidations on Yellow.pro: a liquidated position is matched against opposing traders, whose positions are partially closed. Priority is highest for the most profitable, highest-leverage positions on the opposite side. See [Cross-Margin Risk & ADL](../perpetual-trading/risk-and-liquidation/cross-margin-risk-and-adl.md).

</details>

<details>

<summary>Available Balance</summary>

Funds you can use right now — for new orders or withdrawals. Equals total balance minus funds locked **In Orders** or committed as position margin.

</details>

<details>

<summary>Bankruptcy Price</summary>

The mark price at which your account equity reaches zero. It sits just beyond your liquidation price, and is the price your position is force-settled at during liquidation. See [Liquidation & Mark Price](../perpetual-trading/risk-and-liquidation/liquidation-and-mark-price.md).

</details>

<details>

<summary>Base / Quote Currency</summary>

In a pair like `ETH-USDT`, the **base** currency is the asset being bought or sold (ETH) and the **quote** currency is what you pay or receive (USDT).

</details>

<details>

<summary>Cross Margin</summary>

The margin mode used on Yellow.pro perpetuals, where your entire available balance is shared collateral for all open positions. See [Margin & Leverage](../perpetual-trading/margin-and-leverage.md).

</details>

<details>

<summary>Funding Fee</summary>

A payment exchanged between long and short perpetual traders (usually every 8 hours) to keep the contract price near the market price. Not collected by Yellow.pro. See [Funding Fees Explained](../fees/funding-fees-explained.md).

</details>

<details>

<summary>Leverage</summary>

A multiplier that lets you open a position larger than your margin (e.g. 10x). Amplifies both gains and losses. See [Margin & Leverage](../perpetual-trading/margin-and-leverage.md).

</details>

<details>

<summary>Limit Order</summary>

An order to buy or sell at a specified price or better. Fills only at that price or better, and may not fill at all. See [Order Types](../spot-trading/order-types.md).

</details>

<details>

<summary>Liquidation</summary>

The automatic closure of a position when your account can no longer meet maintenance margin (margin ratio reaches 100%). See [Liquidation & Mark Price](../perpetual-trading/risk-and-liquidation/liquidation-and-mark-price.md).

</details>

<details>

<summary>Liquidation Price</summary>

The estimated mark price at which your account would be liquidated — where your equity falls to the maintenance margin level. In cross margin it moves with your PnL, positions, and balance. See [Liquidation & Mark Price](../perpetual-trading/risk-and-liquidation/liquidation-and-mark-price.md).

</details>

<details>

<summary>Maintenance Margin</summary>

The minimum margin required to keep a position open. If your effective margin falls below it, liquidation is triggered. On current markets the maintenance margin rate is a flat 0.5% of position notional.

</details>

<details>

<summary>Maker / Taker</summary>

A **maker** order adds liquidity by resting in the order book; a **taker** order removes liquidity by filling immediately. Maker fees are lower. See [Trading Fees](../fees/trading-fees.md).

</details>

<details>

<summary>Margin Ratio</summary>

A real-time indicator of how close your account is to liquidation. At 100%, liquidation is triggered. See [Margin & Leverage](../perpetual-trading/margin-and-leverage.md).

</details>

<details>

<summary>Market Order</summary>

An order that executes immediately at the best available price. Subject to slippage. See [Order Types](../spot-trading/order-types.md).

</details>

<details>

<summary>Mark Price</summary>

A fair-value price derived from external reference data, used to calculate unrealized PnL and liquidation — instead of the last traded price — to reduce manipulation. See [Liquidation & Mark Price](../perpetual-trading/risk-and-liquidation/liquidation-and-mark-price.md).

</details>

<details>

<summary>Network Fee</summary>

A blockchain transaction fee (currently Ethereum) for processing deposits and withdrawals on-chain. Set by the network, not Yellow.pro. See [Withdrawal Network Fees Explained](../fees/withdrawal-network-fees.md).

</details>

<details>

<summary>Perpetual Account</summary>

A separate balance used only for perpetual futures positions. Funds must be transferred here before opening perpetual positions, and cannot be withdrawn directly. See [Understanding Your Balances](../account-and-balance/understanding-your-balances.md).

</details>

<details>

<summary>Perpetual Contract</summary>

A derivative that tracks an asset's price with no expiry date. You never own the underlying asset. See [What is Perpetual Trading?](../perpetual-trading/what-is-perpetual-trading.md).

</details>

<details>

<summary>PnL (Realized / Unrealized)</summary>

Profit and Loss. **Unrealized** PnL is the current gain/loss on an open position (changes with the mark price); **Realized** PnL is locked in when you close. See [Understanding PnL](../perpetual-trading/pnl.md).

</details>

<details>

<summary>Position (Long / Short)</summary>

Going **long** profits when the price rises; going **short** profits when it falls. See [Long, Short & Hedge Mode](../perpetual-trading/long-short-hedge-mode.md).

</details>

<details>

<summary>In Orders</summary>

The balance state for funds locked by active open orders (and, on Spot, by a withdrawal that's still processing). They return to Available when the order is filled or cancelled. On Perpetuals, funds can be In Orders too, but there is no withdrawal step.

</details>

<details>

<summary>Spot Trading</summary>

The direct exchange of one asset for another at the current market price — you own the asset you buy. See [What is Spot Trading?](../spot-trading/what-is-spot-trading.md).

</details>

<details>

<summary>Stop Limit / Stop Market</summary>

Conditional orders that activate at a trigger price, then submit a limit order (stop limit) or a market order (stop market). See [Order Types](../spot-trading/order-types.md).

</details>

<details>

<summary>Tick Size / Step Size</summary>

**Tick size** is the smallest allowed price increment; **step size** is the smallest allowed quantity increment for a market. Orders that don't align are rejected.

</details>

<details>

<summary>Trading Account (Spot Account)</summary>

The balance where Spot trading takes place. For external wallet users, deposits arrive here directly. See [Understanding Your Balances](../account-and-balance/understanding-your-balances.md).

</details>

<details>

<summary>Two-Way Mode (Hedge Mode)</summary>

A position mode that lets you hold a long and a short on the same pair simultaneously. The default is One-Way Mode. See [Long, Short & Hedge Mode](../perpetual-trading/long-short-hedge-mode.md).

</details>

<details>

<summary>VIP Tier</summary>

Your fee level, set automatically by 30-day trading volume or your $YELLOW balance. Higher tiers pay lower maker/taker fees. See [VIP Tiers & Fee Discounts](../fees/vip-tiers.md).

</details>

<details>

<summary>$YELLOW</summary>

Yellow.pro's native token. Holding a 24-hour average in your Trading Account qualifies you for higher VIP tiers and lower fees. See [$YELLOW Token & Fee Discounts](../fees/yellow-token-fee-discount.md).

</details>
