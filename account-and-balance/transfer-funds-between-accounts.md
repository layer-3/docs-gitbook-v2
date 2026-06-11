---
icon: money-bill-transfer
description: >-
  How to move funds between Account Balance, Trading Account, and Perpetual
  Account, and which transfers apply to your account type.
---

# How to Transfer Funds Between Accounts

Yellow.pro lets you transfer funds between different account balances depending on your account type. This guide explains how to access transfers and which transfers apply to your account.

## Before You Start

* Google Sign-in users can transfer between Account Balance (`Yellow Wallet`), Trading Account (`Spot Account`), and Perpetual Account.
* External wallet users only transfer between Trading Account (`Spot Account`) and Perpetual Account.
* Transfers between Trading Account and Perpetual Account are instant.
* Transfers involving Account Balance are processed on the blockchain and may take time.
* Funds locked in open orders or active positions may not be available for transfer.

![Transferring funds between accounts on Yellow.pro](../.gitbook/assets/transfer-flow.gif)

{% tabs %}
{% tab title="Google Sign-in" %}
### Account Balance → Trading Account (`Spot Account`)

**When to use:** moving deposited funds from Account Balance into the Trading Account so you can trade on Spot markets.

1. Open the Assets page: `yellow.pro/assets`
2. Click **Transfer**.
3. Select the asset and amount.
4. Confirm the transfer.

The window shows **From:** Account Balance (`Yellow Wallet`) → **To:** Trading Account (`Spot Account`). This is a blockchain-based transfer and may take time depending on network conditions.

### Trading Account → Account Balance (`Yellow Wallet`)

**When to use:** moving funds back to Account Balance before withdrawing to your external wallet.

1. Open the Assets page: `yellow.pro/assets`
2. Click **Transfer**.
3. Select Account Balance as the destination.
4. Select the asset and amount.
5. Confirm the transfer.

This is also a blockchain-based transfer and may take time.

### Trading Account (`Spot Account`) ↔ Perpetual Account

**When to use:** moving funds between Spot trading and perpetual trading.

1. Open the Perpetuals page: `yellow.pro/assets/perps`
2. Click **Transfer**.
3. Select the asset and amount.
4. Confirm the transfer.

This is an internal platform transfer and normally reflects instantly.
{% endtab %}

{% tab title="External Wallet" %}
External wallet users do not use Account Balance (`Yellow Wallet`). The only available transfer is between Trading Account (`Spot Account`) and Perpetual Account.

1. Open the Perpetuals page: `yellow.pro/assets/perps`
2. Click **Transfer**.
3. Select the asset and amount.
4. Confirm the transfer.

This transfer is internal and normally completes instantly.
{% endtab %}
{% endtabs %}

## Transfer Processing Times

| Transfer type | How it works | Typical time |
| --- | --- | --- |
| Account Balance ↔ Trading Account | Blockchain-based | Varies with network congestion |
| Trading Account ↔ Perpetual Account | Internal transfer | Instant |

## Important Information

If a Trading Account ↔ Perpetual Account transfer doesn't complete instantly:

1. Refresh the page.
2. Disconnect and reconnect your wallet.
3. Retry the transfer.

If an Account Balance ↔ Trading Account transfer remains pending for an unusually long time, check the transfer status and TxID on the History page (`yellow.pro/assets/history`). See [Understanding Transfers on Yellow.pro](understanding-transfers.md) for troubleshooting.

## Related Articles

* [Understanding Your Balances](understanding-your-balances.md)
* [Understanding Transfers on Yellow.pro](understanding-transfers.md)
* [Why Funds May Not Be Transferable](why-funds-not-transferable.md)
