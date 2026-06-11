---
icon: coins
description: >-
  How Yellow.pro's balance areas work — Account Balance, Trading Account, and
  Perpetual Account — and how funds flow between them.
---

# Understanding Your Balances

Yellow.pro uses different balance areas depending on how your account was created and what trading activity you're doing. Understanding these balances helps avoid confusion when depositing, transferring, and withdrawing funds.

## Account Types Determine Your Balance Structure

Your account type affects which balances you use:

* **Google Sign-in users** use three balances: Account Balance (`Yellow Wallet`), Trading Account (`Spot Account`), and Perpetual Account.
* **External wallet users** use only two balances: Trading Account (`Spot Account`) and Perpetual Account. They do not use Account Balance.

## Account Balance (`Yellow Wallet`)

**What it is:** For Google Sign-in users only. This is your smart contract wallet linked to your account. Deposits first arrive here before becoming available for trading.

**What you can do with it:**

* Receive incoming deposits
* Hold funds before moving them to your Trading Account (`Spot Account`)
* Process withdrawals (funds must be here before you can withdraw)

{% hint style="warning" %}
Funds in Account Balance (`Yellow Wallet`) cannot be used directly for trading. They must first be transferred to your Trading Account (`Spot Account`).
{% endhint %}

## Trading Account (`Spot Account`)

**What it is:** The balance where trading takes place. For Google Sign-in users, funds arrive here only after transferring from Account Balance (`Yellow Wallet`). For external wallet users, deposits arrive directly here.

**What you can do with it:**

* Place trades on Spot markets
* Transfer funds to the Perpetual Account for perpetual trading
* Withdraw directly (external wallet users only)
* Transfer back to Account Balance (`Yellow Wallet`) before withdrawal (Google Sign-in users only)

## Perpetual Account

**What it is:** A separate balance used only for perpetual futures trading. Funds must be transferred here manually before they can be used for perpetual positions.

**What you can do with it:**

* Open and maintain perpetual trading positions
* Hold margin for active positions

{% hint style="warning" %}
Funds in the Perpetual Account cannot be withdrawn directly. They must be transferred back to the Trading Account (`Spot Account`) first, then to Account Balance (`Yellow Wallet`) before withdrawal.
{% endhint %}

## How Funds Flow Through Your Balances

{% tabs %}
{% tab title="Google Sign-in" %}
**Deposits**

`External wallet or exchange → Account Balance (Yellow Wallet) → Trading Account (Spot Account) → Perpetual Account`

**Withdrawals**

`Perpetual Account → Trading Account (Spot Account) → Account Balance (Yellow Wallet) → Your external wallet`
{% endtab %}

{% tab title="External Wallet" %}
**Deposits**

`External wallet → Trading Account (Spot Account) → Perpetual Account`

**Withdrawals**

`Perpetual Account → Trading Account (Spot Account) → External wallet`
{% endtab %}
{% endtabs %}

## Understanding Transfer Types

Yellow.pro supports two different types of transfers. Which type applies depends on which balances are involved.

### Blockchain-based transfers (not instant)

**Account Balance ↔ Trading Account** transfers are processed through the blockchain and are not instant. These transfers:

* generate a blockchain transaction with a TxID
* take time to process depending on network congestion
* may include a network fee (sometimes sponsored by Yellow — you'll see this on the Transfer page)
* show as "Pending" until completed, then "Completed"
* can be tracked in your transaction history at `yellow.pro/assets/history`

### Internal transfers (instant)

**Trading Account (`Spot Account`) ↔ Perpetual Account** transfers are internal platform transfers and normally reflect instantly. These transfers:

* do not generate blockchain transactions
* complete immediately after confirmation
* have no network fees
* should not show as "Pending"

If a Trading Account ↔ Perpetual Account transfer doesn't complete instantly, refresh the page, disconnect and reconnect your wallet, then retry. If the issue persists, [contact support](../community-and-resources/contact-support.md).

## Quick Comparison: Google Sign-in vs External Wallet

| Feature | Google Sign-in Users | External Wallet Users |
| --- | --- | --- |
| Account Balance (`Yellow Wallet`) used? | Yes (required) | No |
| Deposits arrive in | Account Balance (`Yellow Wallet`) | Trading Account (`Spot Account`) |
| Extra transfer needed before trading? | Yes (Account Balance → Trading Account) | No |
| Withdrawal process | Must transfer to Account Balance first | Direct from Trading Account |
| Account Balance ↔ Trading Account transfers | Blockchain-based, not instant | Not applicable |
| Trading Account ↔ Perpetual Account transfers | Instant, internal | Instant, internal |
| Can withdraw directly from Perpetual Account? | No | No |

## Important Things to Know

* Funds locked in open orders or active positions may not be available for transfer until those orders or positions are closed.
* Transfers between Account Balance and Trading Account should be treated like standard blockchain transactions in terms of timing.
* Trading Account ↔ Perpetual Account transfers are internal and normally instant for both account types.
* Network fees for Account Balance ↔ Trading Account transfers may apply — check the Transfer page to see if a fee applies.
* Blockchain transactions cannot be reversed once completed.

## Related Articles

* [Understanding Transfers on Yellow.pro](understanding-transfers.md)
* [How to Transfer Funds Between Accounts](transfer-funds-between-accounts.md)
* [Why Funds May Not Be Transferable](why-funds-not-transferable.md)
