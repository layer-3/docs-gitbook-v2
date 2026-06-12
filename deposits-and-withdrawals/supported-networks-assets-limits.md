---
icon: network-wired
description: >-
  Supported network and assets, blockchain confirmations, minimum withdrawal
  amounts, network fees, and irreversibility rules for deposits and withdrawals.
---

# Supported Networks, Assets & Limits

This page covers everything that applies to both deposits and withdrawals: the supported network, assets, confirmation requirements, minimum withdrawal amounts, network fees, and the rules around irreversibility.

## Supported Network

**Ethereum is the only network currently supported** for deposits and withdrawals on Yellow.pro. All transactions are processed through the Ethereum blockchain.

{% hint style="danger" %}
Funds sent on any other network will not be credited and **cannot be recovered** by the platform. Always confirm the selected network matches your sending or receiving wallet before confirming.
{% endhint %}

## Supported Assets

| Asset | Name | Minimum Withdrawal |
| --- | --- | --- |
| ETH | Ether (native token) | 0.005 |
| WBTC | Wrapped Bitcoin | 0.00015 |
| USDT | Tether | 5 |
| YELLOW | Platform token | 1,000 |
| WSOL | Wrapped SOL | 0.1 |
| BNB | BNB | 0.015 |

When depositing, select the asset from the deposit form — the network is automatically set to Ethereum. Always confirm the asset and network before sending funds.

{% hint style="info" %}
You can deposit and withdraw all assets above, but not every asset has a spot trading pair yet. **WSOL** and **BNB** are currently deposit-and-withdraw only. See [Market Rules & Limits](../spot-trading/market-rules.md) for the markets available to trade.
{% endhint %}

## Blockchain Confirmations

Deposits require **15 blockchain confirmations** before being credited to your account. This helps ensure transaction security and finality on the Ethereum network. During periods of high network congestion, confirmations may take longer than usual.

## Minimum Withdrawal Amounts

Withdrawals below the minimum amount cannot be initiated. If your available balance is below the required minimum for an asset (see the table above), the withdrawal option remains unavailable until you have more funds. There is **no maximum** withdrawal limit.

## Network Fees

Blockchain network fees are required to process withdrawals on-chain.

* **Not charged by Yellow.pro** — they are Ethereum network transaction costs.
* **Who pays:** you — the fee is deducted from your withdrawal amount.
* **Who sets it:** the blockchain network (dynamic, based on congestion).
* **When shown:** the estimated fee appears on the Withdraw page before you confirm.

> **Example:** if you withdraw 100 USDT with a 1 USDT network fee, you receive 99 USDT.

## Withdrawals Are Final

Once a withdrawal is submitted on-chain, it **cannot be reversed, cancelled, or modified.** Funds sent to the wrong address, or to an unsupported blockchain, cannot be recovered by Yellow.pro. Always verify the recipient address and that the receiving platform supports the Ethereum network before confirming.

## Tracking Deposits & Withdrawals

Track transaction status and details in your history at `yellow.pro/assets/history` — including the TxID, asset and amount, network fee deducted, final received amount, and status. For deposits to a Google Sign-in Account Balance, you can also verify the on-chain transaction on a blockchain explorer such as `etherscan.io` using your deposit address.

## Related Articles

* [How to Deposit](how-to-deposit.md)
* [How to Withdraw](how-to-withdraw.md)
* [Deposit & Withdrawal Troubleshooting](troubleshooting.md)
