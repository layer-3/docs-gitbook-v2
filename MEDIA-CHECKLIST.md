---
hidden: true
description: >-
  Internal working guide — media (images, diagrams, video) to add across the
  docs. Hidden from the published navigation.
layout:
  width: wide
---

# Media Checklist (internal)

A working guide for the team capturing and adding media to the docs. Hidden from public readers (`hidden: true`), but visible in the GitBook editor. Tick the **Status** column (`☐` → `✅`) as each asset lands.

{% hint style="warning" %}
**All media must be captured on the platform's _white (light) theme._** Switch the app to the light theme before taking any screenshot, GIF, or recording, so every image in the docs stays visually consistent. Re-shoot anything captured on the dark theme.
{% endhint %}

## Capture standards

* **Theme:** white / light theme only (see above).
* **No private data:** use test accounts; blur or use placeholder wallet addresses, balances, and emails.
* **Consistent frame:** same browser zoom (100%) and a consistent window width across a flow; capture at 2× / retina where possible for crisp output.
* **Tight crop:** crop to the relevant UI — avoid full-desktop screenshots with unrelated chrome.
* **Annotations:** when adding callouts/arrows, keep them a consistent style; name the file with the `-annotated` suffix.

## How to add an asset

1. Capture it following the standards above.
2. Name it per the **Naming convention** below.
3. Save it to `.gitbook/assets/`.
4. Reference it on the target page with a relative path and meaningful alt text — `![Alt text](../.gitbook/assets/name.png)` (use `../../` from a nested page).
5. Change the asset's **Status** in the table below to `✅`.

## Naming convention

```
<area>-<subject>[-<detail>].<ext>
```

* **lowercase kebab-case**, no spaces or underscores.
* **area prefix:** `home`, `start` (getting-started), `connect`, `account`, `deposit`, `withdraw`, `transfer`, `spot`, `perp`, `fees`, `api`.
* **suffixes:** `-diagram`, `-annotated`, or a state word (`-filled`, `-rejected`).

| Media type            | Format          | Use for                                  |
| --------------------- | --------------- | ---------------------------------------- |
| UI screenshot         | `.png`          | Captures of the interface                |
| Diagram / illustration| `.svg`          | Anything drawn (crisp at any zoom, tiny) |
| Short loop            | `.gif` (≤ 4s)   | Tiny silent loops only                   |
| Long walkthrough      | video `{% embed %}` | End-to-end flows (host on Loom/YouTube) |

***

## Priority 1 — Deposit, withdraw & transfer flows

Capture these **first**. Each path needs **end-to-end** coverage — a short video/GIF of the whole flow plus the key stills. The account types differ:

* **EOA (external wallet):** funds are tradable directly — no Yellow Wallet step.
* **Google / Gmail login:** deposits land in the **Yellow Wallet** (Account Balance) and must be **transferred to the Trading (Spot) Account** before trading; withdrawals reverse it (Trading Account → Yellow Wallet → withdraw).

| Status | Path | Asset | Format | What it shows | Target page |
| --- | --- | --- | --- | --- | --- |
| ☐ | Deposit · EOA | `deposit-eoa-flow.gif` | gif → video | Connect wallet → deposit form → on-chain send → funds tradable | `deposits-and-withdrawals/how-to-deposit.md` |
| ☐ | Deposit · EOA | `deposit-eoa-form.png` | png | Deposit address / form for an external-wallet user | `deposits-and-withdrawals/how-to-deposit.md` |
| ☐ | Deposit · Gmail | `deposit-gmail-flow.gif` | gif → video | Deposit to Yellow Wallet → transfer to Trading Account → ready to trade | `deposits-and-withdrawals/how-to-deposit.md` |
| ☐ | Deposit · Gmail | `deposit-gmail-address.png` | png | Deposit address / screen (Yellow Wallet) | `deposits-and-withdrawals/how-to-deposit.md` |
| ☐ | Deposit · Gmail | `transfer-yellow-to-spot.png` | png | Transfer modal: Yellow Wallet → Trading (Spot) Account | `account-and-balance/transfer-funds-between-accounts.md` |
| ✅ | Withdraw · EOA | `withdraw-eoa-flow.gif` | gif | Withdraw form → network + fee → confirm → on-chain (relocated from a mislabeled "spot interface" asset) | `deposits-and-withdrawals/how-to-withdraw.md` |
| ☐ | Withdraw · EOA | `withdraw-eoa-form.png` | png | Withdrawal form (address, network, fee) | `deposits-and-withdrawals/how-to-withdraw.md` |
| ☐ | Withdraw · Gmail | `withdraw-gmail-flow.gif` | gif → video | Transfer Trading Account → Yellow Wallet → withdraw → confirm | `deposits-and-withdrawals/how-to-withdraw.md` |
| ☐ | Withdraw · Gmail | `transfer-spot-to-yellow.png` | png | Transfer modal: Trading (Spot) Account → Yellow Wallet | `account-and-balance/transfer-funds-between-accounts.md` |
| ☐ | Withdraw · Gmail | `withdraw-gmail-form.png` | png | Withdrawal form (Yellow Wallet) | `deposits-and-withdrawals/how-to-withdraw.md` |
| ☐ | Transfer · Spot ↔ Perp | `transfer-spot-to-perp-flow.gif` | gif → video | Full transfer flow both ways (Spot → Perpetual and back), confirm, updated balance | `account-and-balance/transfer-funds-between-accounts.md` |

{% hint style="info" %}
**Reconcile existing assets:** `deposit-flow.gif` (7 MB), `withdraw-flow.gif` (3.7 MB), `transfer-flow.gif` (7 MB) — check which account type each currently shows, then replace/supplement so **both** EOA and Gmail paths are covered. Migrate these heavy GIFs to embedded video (keep the filename stem, host on Loom/YouTube, swap `![]()` for `{% embed %}`).
{% endhint %}

## Priority 1 — Interface & UI screenshots

| Status | Asset | Format | What it shows | Target page |
| --- | --- | --- | --- | --- |
| ☐ | `spot-trading-interface.gif` | gif → video | Main spot trading interface overview — **still needed** (the prior file was actually an external-wallet withdraw flow, now relocated) | `spot-trading/what-is-spot-trading.md` |
| ☐ | `perp-trading-interface-annotated.png` | png (annotated) | Perp UI overview: positions, leverage, PnL, liquidation price | `perpetual-trading/what-is-perpetual-trading.md` |
| ☐ | `account-balances-panel.png` | png | Balances UI: Available vs In Orders, both account types | `account-and-balance/understanding-your-balances.md` |
| ☐ | `perp-leverage-margin-selector.png` | png | Leverage slider + cross / isolated selector | `perpetual-trading/margin-and-leverage.md` |
| ☐ | `connect-login-options.png` | png | Login modal: external wallet vs Google | `getting-started/wallet-vs-gmail.md` |
| ☐ | `perp-liquidation-price-panel.png` | png | Live liquidation price in the positions panel | `perpetual-trading/risk-and-liquidation/liquidation-and-mark-price.md` |
| ☐ | `deposit-history-status.png` | png | Transaction status / history view | `deposits-and-withdrawals/troubleshooting.md` |

## Later — Diagrams & illustrations

Lower priority — produce after the screenshots above. All `.svg`.

| Status | Asset | What it shows | Target page |
| --- | --- | --- | --- |
| ☐ | `start-how-it-works-diagram.svg` | Fund flow: wallet → deposit → Account Balance → Trading Account → trade | `getting-started/users-journey.md` |
| ☐ | `account-types-diagram.svg` | Account Balance vs Trading Account | `account-and-balance/understanding-your-balances.md` |
| ☐ | `perp-price-levels-diagram.svg` | Entry / liquidation / bankruptcy price on one price line | `perpetual-trading/risk-and-liquidation/liquidation-and-mark-price.md` |
| ☐ | `perp-adl-matching-diagram.svg` | Liquidated position matched against an opposing trader (no insurance fund) | `perpetual-trading/risk-and-liquidation/cross-margin-risk-and-adl.md` |
| ☐ | `home-platform-overview.svg` | Hero: hybrid CEX-speed + self-custody | `README.md` |
| ☐ | `start-hybrid-model-diagram.svg` | CEX performance + DeFi custody concept | `getting-started/what-is-yellow.md` |
| ☐ | `fees-split-diagram.svg` | Fee allocation breakdown | `fees/fee-split.md` |
| ☐ | `api-auth-flow-diagram.svg` | Challenge → sign → verify → token | `api/getting-started-with-api.md` |

***

## Skip — no image needed

* **Rejected orders** — not recorded, and mostly blocked at creation, so there's nothing reliable to screenshot. No image on `market-rules.md` / `managing-orders.md`.
* **Text / table pages** — API reference pages, fees tables, `vip-tiers.md`, glossary, FAQs, all `overview.md` card pages, `contract-specifications.md`, `supported-networks-assets-limits.md`.

## Already well-covered

Spot order placement (5 shots), managing orders (3), wallet connect (2), position management (4), margin-warning emails (2), PnL (1), long / short hedge mode (1).
