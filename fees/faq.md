---
description: Quick answers about trading fees, VIP tiers, $YELLOW, funding, and network fees.
---

# Fees — FAQ

## Trading Fees

<details>

<summary>What are the trading fees on Yellow.pro for Spot and Perpetuals?</summary>

Trading fees depend on your VIP tier and whether your order is maker or taker. Base tier is Spot 0.08% maker / 0.10% taker and Perp 0.01% maker / 0.04% taker. See [VIP Tiers & Fee Discounts](vip-tiers.md) for the complete schedule.

</details>

<details>

<summary>What is the difference between a maker fee and a taker fee?</summary>

Maker orders add liquidity and have lower fees; taker orders consume liquidity and have higher fees. Market orders are usually taker; limit orders can be either. See [Trading Fees (Maker & Taker)](trading-fees.md).

</details>

<details>

<summary>Why was a fee charged on my trade, and how is it calculated?</summary>

Fees are charged whenever an order is successfully filled: `Fee = Fill Value × Fee Rate` (Fill Value = Price × Size). Cancelled or unfilled orders generate no fees. See [Trading Fees (Maker & Taker)](trading-fees.md).

</details>

<details>

<summary>What currency are trading fees charged in?</summary>

In the quote currency of each pair — e.g. trading USDT pairs charges fees in USDT.

</details>

<details>

<summary>How do I check and reduce my trading fees?</summary>

View fees in your trade history (`yellow.pro/spot/orders?tab=trades` or `/perps/orders?tab=trades`). To reduce them, increase your VIP tier through trading volume or by holding $YELLOW. See [VIP Tiers & Fee Discounts](vip-tiers.md).

</details>

## VIP Tiers & $YELLOW

<details>

<summary>What is a VIP tier and how often does it update?</summary>

Your VIP tier determines your trading fees — higher tiers pay less. It's evaluated automatically and continuously as your trading activity or $YELLOW balance changes, and you're always placed in the highest tier you qualify for. See [VIP Tiers & Fee Discounts](vip-tiers.md).

</details>

<details>

<summary>How do I qualify for higher VIP tiers?</summary>

Meet any one requirement: 30-day Spot volume, 30-day Perpetual volume, or a 24-hour average $YELLOW balance in your Trading Account (`Spot Account`). VIP 1 needs 100K USDT Spot volume, 1M USDT Perp volume, or 10,000 $YELLOW. See [VIP Tiers & Fee Discounts](vip-tiers.md).

</details>

<details>

<summary>How do I use $YELLOW to get a fee discount?</summary>

Hold a 24-hour average of $YELLOW in your Trading Account (`Spot Account`) to qualify for higher VIP tiers. Only Trading Account balance counts — not Account Balance (`Yellow Wallet`) or external wallets. There's no separate discount for paying fees with $YELLOW. See [$YELLOW Token & Fee Discounts](yellow-token-fee-discount.md).

</details>

<details>

<summary>Where can I get $YELLOW tokens?</summary>

$YELLOW is currently available directly on Yellow.pro for trading and holding. Additional exchange listings may be added in the future. See [$YELLOW Token & Fee Discounts](yellow-token-fee-discount.md).

</details>

## Funding Fees

<details>

<summary>What is a funding fee and when is it charged?</summary>

Funding fees are payments exchanged between long and short traders every 8 hours on Perpetual markets (positive rate: longs pay shorts; negative: shorts pay longs). They only apply if you hold an open position at the funding timestamp. See [Funding Fees Explained](funding-fees-explained.md).

</details>

<details>

<summary>Are funding fees different from trading fees?</summary>

Yes. Trading fees are charged when orders fill; funding fees are exchanged every 8 hours between traders for open Perpetual positions and are not collected by Yellow.pro. See [Funding Fees Explained](funding-fees-explained.md).

</details>

## Network Fees

<details>

<summary>What are withdrawal network fees and how much are they?</summary>

They're Ethereum blockchain transaction fees required to process withdrawals on-chain — not Yellow.pro fees. They vary with network congestion, and Yellow.pro shows the estimate before you confirm. See [Withdrawal Network Fees Explained](withdrawal-network-fees.md).

</details>

<details>

<summary>Why did my received amount differ from my withdrawal amount?</summary>

The network fee is deducted from your withdrawal — e.g. a 100 USDT withdrawal with a 1 USDT fee results in 99 USDT received. See [Withdrawal Network Fees Explained](withdrawal-network-fees.md).

</details>

## Fee Split

<details>

<summary>How is my trading fee used, and does the split increase my fees?</summary>

Your fee is divided internally — 85% toward $YELLOW buybacks and 15% toward platform operations (standard split); referred users have allocations that include referral commissions and rewards. The split does **not** increase your fee — the amount you pay is unchanged. See [Fee Split Explained](fee-split.md).

</details>

<details>

<summary>Are there any other fees besides trading and funding fees?</summary>

Besides trading fees, Spot has no additional fees. Perpetual traders also pay funding fees (every 8 hours). Network fees apply to deposits and withdrawals.

</details>
