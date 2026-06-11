---
description: Quick answers to common deposit and withdrawal questions on Yellow.pro.
---

# Deposits & Withdrawals — FAQ

## Deposits

<details>

<summary>What assets and networks does Yellow.pro support for deposits?</summary>

Deposits are supported on the **Ethereum network only**. Supported assets: ETH, WBTC, USDT, BNB, WSOL, and YELLOW. See [Supported Networks, Assets & Limits](supported-networks-assets-limits.md) for confirmations and tracking.

</details>

<details>

<summary>Why do Google Sign-in users have a different deposit flow than external wallet users?</summary>

Google Sign-in users operate through a Yellow Wallet, so deposits first arrive in Account Balance (`Yellow Wallet`) before being moved to the Trading Account (`Spot Account`). External wallet users skip this — deposits go directly to the Trading Account. See [How to Deposit](how-to-deposit.md).

</details>

<details>

<summary>Can I deposit directly into my Perpetual Account?</summary>

No. Deposits go first to Account Balance (Google) or the Trading Account (external wallet). Perpetual trading requires a separate, instant transfer from Trading Account → Perpetual Account.

</details>

<details>

<summary>What's the difference between Approval and Deposit transactions?</summary>

For ERC-20 tokens, **Approval** grants Yellow.pro permission to access your token (no funds move), while **Deposit** actually transfers the funds. Both are required to complete the deposit. Native ETH deposits only need the Deposit step. See [How to Deposit](how-to-deposit.md).

</details>

<details>

<summary>How long does a deposit take?</summary>

Usually minutes, but up to 1 hour during congestion. Deposits require 15 blockchain confirmations before being credited. See [Deposit & Withdrawal Troubleshooting](troubleshooting.md).

</details>

<details>

<summary>I completed a deposit but my balance hasn't updated — what should I do?</summary>

External wallet users: verify you completed the Deposit transaction (not just Approval). Google users: check whether funds are in Account Balance and transfer them to the Trading Account. See [Deposit & Withdrawal Troubleshooting](troubleshooting.md).

</details>

<details>

<summary>Can I recover funds sent to the wrong network or address?</summary>

No. Once confirmed on-chain, a transaction cannot be reversed. Only the Ethereum network is supported — always verify the address and network before sending.

</details>

## Withdrawals

<details>

<summary>Why can't I withdraw directly from my Trading Account?</summary>

It depends on your account type. External wallet users withdraw directly from the Trading Account (`Spot Account`); Google account users must first move funds to Account Balance (`Yellow Wallet`). See [How to Withdraw](how-to-withdraw.md).

</details>

<details>

<summary>How do I move funds from Perpetual → Spot → Account Balance before withdrawing?</summary>

For Google users: (1) transfer Perpetual → Spot (instant), (2) transfer Spot → Account Balance (on-chain, may take time), (3) withdraw from Account Balance. See [How to Withdraw](how-to-withdraw.md).

</details>

<details>

<summary>Why is my withdrawal showing insufficient balance even though I have funds?</summary>

Funds may be locked in open orders or active positions, or not in the correct account for your account type. See [Deposit & Withdrawal Troubleshooting](troubleshooting.md).

</details>

<details>

<summary>What is the minimum withdrawal amount?</summary>

Each asset has its own minimum (e.g. USDT 5, ETH 0.005). There's no maximum. See the table in [Supported Networks, Assets & Limits](supported-networks-assets-limits.md).

</details>

<details>

<summary>My withdrawal is completed on-chain but I haven't received it — what do I do?</summary>

It may still be processing on the receiving platform. Check your TxID at `yellow.pro/assets/history`, then contact the receiving wallet or exchange with your TxID. See [Deposit & Withdrawal Troubleshooting](troubleshooting.md).

</details>

<details>

<summary>I withdrew to the wrong network or wrong address — what happens?</summary>

Blockchain transactions are irreversible. If sent to an incorrect address or unsupported network, recovery may not be possible. Contact the receiving platform with your TxID. See [Deposit & Withdrawal Troubleshooting](troubleshooting.md).

</details>

<details>

<summary>Are there withdrawal fees?</summary>

Network fees are charged by the blockchain (not Yellow.pro) and deducted from your withdrawal amount. The estimate is shown before you confirm. See [Supported Networks, Assets & Limits](supported-networks-assets-limits.md).

</details>

<details>

<summary>Why does a Google withdrawal depend on smart wallet detection?</summary>

Your Account Balance (`Yellow Wallet`) uses smart wallet abstraction, and some platforms don't automatically detect smart wallet balances. Verify the receiving platform supports Ethereum smart contracts before withdrawing. See [How to Withdraw](how-to-withdraw.md).

</details>

<details>

<summary>What details should I provide when reporting a deposit or withdrawal issue?</summary>

Include your wallet address, transaction hash (TxID), asset and amount, network, and a brief description (a screenshot helps). See [Contact Support](../community-and-resources/contact-support.md).

</details>
