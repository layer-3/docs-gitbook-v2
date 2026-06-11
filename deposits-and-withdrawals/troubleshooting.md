---
description: >-
  Identify and resolve common deposit and withdrawal issues before contacting
  support.
---

# Deposit & Withdrawal Troubleshooting

Use this guide to diagnose common deposit and withdrawal issues. For network, asset, limit, and irreversibility rules, see [Supported Networks, Assets & Limits](supported-networks-assets-limits.md).

{% tabs %}
{% tab title="Deposits" %}
<details>

<summary>Balance hasn't updated after a deposit</summary>

* **External wallet, ERC-20 token:** make sure you completed **both** the Approval and the Deposit transaction. Approval only grants permission — if the Deposit step wasn't confirmed, funds stay in your wallet. Return to the Deposit page and check whether the button shows **Deposit**.
* **Google Sign-in:** deposits first appear in **Account Balance (`Yellow Wallet`)**, not the Trading Account. Open the Assets page; if the funds are there, transfer them to the Trading Account (`Spot Account`) before trading.

</details>

<details>

<summary>Funds are in Account Balance instead of Trading Account</summary>

This is expected for Google Sign-in users — deposits arrive in Account Balance (`Yellow Wallet`) first. Open the Assets page, click **Transfer**, and move funds from Account Balance → Trading Account (`Spot Account`). See [How to Transfer Funds Between Accounts](../account-and-balance/transfer-funds-between-accounts.md).

</details>

<details>

<summary>Deposit has been pending for a long time</summary>

During congestion, deposits can take longer. Check status on a blockchain explorer (`etherscan.io`) using your deposit address or sending wallet address, or on the Deposit History page (`yellow.pro/assets/history`). Deposits need 15 confirmations. If it still hasn't reflected after the expected time, contact support with your transaction hash, wallet address, token, and amount.

</details>

<details>

<summary>Funds sent to the wrong network or address</summary>

Deposits sent on an unsupported network or to an incorrect address cannot be credited or recovered. Only Ethereum is supported. Always copy the deposit address directly from the Deposit page and confirm the network before sending.

</details>

<details>

<summary>Transaction failed</summary>

The funds were not transferred and remain in your wallet. Retry from the Deposit page. For ETH, no Approval is required — just retry the Deposit transaction.

</details>

</details>
{% endtab %}

{% tab title="Withdrawals" %}
<details>

<summary>Withdrawal cannot be initiated</summary>

Possible causes: funds aren't in the correct account (External → Trading Account; Google → Account Balance), available balance is reduced by open orders or positions, required transfers aren't complete, or the amount is below the minimum. Verify fund location, close restricting orders/positions, complete required transfers, and check the [minimum amounts](supported-networks-assets-limits.md).

</details>

<details>

<summary>Funds not showing as withdrawable / insufficient balance</summary>

Your available balance is likely reduced by funds locked in open orders or active perpetual positions, funds not yet in the correct account, or funds still processing during a transfer. Close or adjust trading activity and confirm fund location for your account type.

</details>

<details>

<summary>Withdrawal pending or delayed</summary>

Usually Ethereum network congestion or normal confirmation time (minutes, up to ~1 hour). Check status with your TxID at `yellow.pro/assets/history`. If not completed after 1 hour, contact support with your TxID.

</details>

<details>

<summary>Completed on-chain but not received</summary>

The transaction may still be processing on the receiving side, or the receiving platform has its own delays. Check your TxID at `yellow.pro/assets/history`, wait for confirmations, and contact the receiving wallet or exchange with your TxID.

</details>

<details>

<summary>Wrong network, wrong address, or unsupported platform</summary>

Blockchain transactions are irreversible. Funds sent to an incorrect address or unsupported network may not be recoverable — especially if the receiving platform doesn't support smart wallet abstraction. Contact the receiving platform with your TxID. Yellow.pro supports Ethereum only.

</details>

<details>

<summary>Received less than expected</summary>

The Ethereum network fee is deducted from the withdrawal amount. Compare the withdrawal amount, network fee, and final received amount in your history. Fees are shown before you confirm.

</details>

</details>
{% endtab %}
{% endtabs %}

## Contacting Support

When reporting a deposit or withdrawal issue, include your Yellow.pro wallet address, external wallet address (if applicable), transaction hash (TxID), token and network, amount, and a brief description (a screenshot helps). This lets the team investigate faster. See [Contact Support](../community-and-resources/contact-support.md).
