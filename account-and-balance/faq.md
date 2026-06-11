---
icon: circle-question
description: Quick answers about Yellow.pro balances, transfers, and locked funds.
---

# Account & Balance — FAQ

<details>

<summary>What is the difference between Account Balance (Yellow Wallet) and Trading Account (Spot Account)?</summary>

For Google Sign-in users, Account Balance (`Yellow Wallet`) is where deposits first arrive. Funds cannot be used for trading until transferred to the Trading Account (`Spot Account`). External wallet users do not have Account Balance — deposits go directly to the Trading Account. See [Understanding Your Balances](understanding-your-balances.md).

</details>

<details>

<summary>What is the difference between Spot balance and Perpetual balance?</summary>

Spot and Perpetual balances are completely separate. The Trading Account (`Spot Account`) is used for Spot trading, while the Perpetual Account is used only for perpetual futures positions. Funds do not transfer automatically between them — you must transfer manually via the Transfer feature.

</details>

<details>

<summary>Why do Google Sign-in users need to manually transfer funds but external wallet users don't?</summary>

Google Sign-in users have an additional Account Balance (`Yellow Wallet`) layer where deposits arrive first. External wallet users' deposits go directly to the Trading Account (`Spot Account`), so no extra step is needed. See [Understanding Your Balances](understanding-your-balances.md).

</details>

<details>

<summary>Can I withdraw directly from the Perpetual Account?</summary>

No. Funds in the Perpetual Account must be transferred back to the Trading Account (`Spot Account`) first, then (for Google Sign-in users) to Account Balance (`Yellow Wallet`) before withdrawal. See [How to Transfer Funds Between Accounts](transfer-funds-between-accounts.md).

</details>

<details>

<summary>What is the difference between blockchain-based transfers and internal transfers?</summary>

Account Balance ↔ Trading Account transfers are blockchain-based and may take time depending on network congestion. Trading Account ↔ Perpetual Account transfers are internal platform transfers and should be instant. See [Understanding Transfers on Yellow.pro](understanding-transfers.md).

</details>

<details>

<summary>Why is my Account Balance ↔ Trading Account transfer taking so long?</summary>

These are blockchain-based transfers subject to network congestion. They normally complete within a few minutes but can take significantly longer during high network activity. See [Understanding Transfers on Yellow.pro](understanding-transfers.md) if your transfer is still pending after 1 hour.

</details>

<details>

<summary>How do I transfer funds from the Perpetual Account to the Trading Account (Spot Account)?</summary>

Open the Perpetuals page (`yellow.pro/assets/perps`), click **Transfer**, and confirm the transfer from Perpetual Account to Trading Account (`Spot Account`). This is instant. See [How to Transfer Funds Between Accounts](transfer-funds-between-accounts.md).

</details>

<details>

<summary>How do I transfer funds from the Trading Account (Spot Account) to Account Balance (Yellow Wallet)?</summary>

Open the Assets page (`yellow.pro/assets`), click **Transfer**, and select Trading Account (`Spot Account`) → Account Balance (`Yellow Wallet`). This is blockchain-based and may take time. See [How to Transfer Funds Between Accounts](transfer-funds-between-accounts.md).

</details>

<details>

<summary>Can I track my transfer status?</summary>

Yes. Check the Transfer page (`yellow.pro/assets/deposit/transfer`) for recent transfers, or transaction history (`yellow.pro/assets/history`) for the complete history. Blockchain-based transfers show a TxID once submitted. See [Understanding Transfers on Yellow.pro](understanding-transfers.md).

</details>

<details>

<summary>Why is my transferable balance lower than my total balance?</summary>

Part of your balance is likely locked in open Spot orders or active perpetual positions. Only the available balance can be transferred or withdrawn. Close the related orders or positions to release the funds. See [Why Funds May Not Be Transferable](why-funds-not-transferable.md).

</details>

<details>

<summary>Why are my funds locked or showing as not transferable?</summary>

Funds may be locked if they are used as margin for perpetual positions, locked in open Spot orders, still processing during a blockchain transfer, or in the wrong account type for what you're trying to do. See [Why Funds May Not Be Transferable](why-funds-not-transferable.md) for solutions.

</details>

<details>

<summary>My funds are in Account Balance (Yellow Wallet) but I can't withdraw — why?</summary>

For Google Sign-in users, ensure the funds are not locked in open orders or positions, and check that the withdrawal amount meets the minimum requirement for that asset. See [Why Funds May Not Be Transferable](why-funds-not-transferable.md).

</details>

<details>

<summary>How does the complete fund flow work?</summary>

**Google Sign-in users**

* Deposits: External wallet → Account Balance (`Yellow Wallet`) → Trading Account (`Spot Account`) → Perpetual Account
* Withdrawals: Perpetual Account → Trading Account (`Spot Account`) → Account Balance (`Yellow Wallet`) → External wallet

**External wallet users**

* Deposits: External wallet → Trading Account (`Spot Account`) → Perpetual Account
* Withdrawals: Perpetual Account → Trading Account (`Spot Account`) → External wallet

See [Understanding Your Balances](understanding-your-balances.md) for the detailed flow.

</details>

<details>

<summary>Do Account Balance ↔ Trading Account transfers have fees?</summary>

These are blockchain-based transfers, so network fees may apply — but they are sometimes sponsored by Yellow. You'll see whether a fee applies on the Transfer page.

</details>

<details>

<summary>What information should I provide when reporting a transfer issue?</summary>

Provide your wallet address, the asset and amount involved, a screenshot of the transfer status or issue, and the TxID if it's visible. This helps the support team investigate faster. See [Contact Support](../community-and-resources/contact-support.md).

</details>
