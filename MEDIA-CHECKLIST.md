---
hidden: true
description: >-
  Internal working notes — media (images, diagrams, video) to add across the
  docs. Not part of the published navigation.
---

# Media Checklist (internal)

Working notes for media to add/improve across the docs. **Hidden from the published TOC** (`hidden: true` + not listed in `SUMMARY.md`). Safe to edit freely.

## Naming convention

```
<area>-<subject>[-<detail>].<ext>
```

* **lowercase kebab-case**, no spaces or underscores
* **area prefix:** `home`, `start` (getting-started), `connect`, `account`, `deposit`, `withdraw`, `transfer`, `spot`, `perp`, `fees`, `api`
* **extension by type:**
  * `.png` — UI screenshots
  * `.svg` — conceptual diagrams / illustrations (prefer for anything drawn — crisp + tiny)
  * `.gif` — short silent loops, **≤4s only**
  * **video** — no file; `{% embed %}` a Loom/YouTube URL (use for long flows)
* **suffixes:** `-diagram`, `-annotated`, or a state word (`-rejected`, `-filled`)
* **store in** `.gitbook/assets/`; reference with relative paths (`../.gitbook/assets/…`, `../../` from nested pages) and meaningful alt text

## P1 — high value

* [ ] `start-how-it-works-diagram.svg` — 📊 — fund flow wallet → deposit → Account Balance → Trading Account → trade — `getting-started/how-yellow-works.md`
* [ ] `account-balances-panel.png` — 📷 — balances UI: Available vs Reserved, both account types — `account-and-balance/understanding-your-balances.md`
* [ ] `account-types-diagram.svg` — 📊 — Account Balance vs Trading Account — `account-and-balance/understanding-your-balances.md`
* [ ] `perp-leverage-margin-selector.png` — 📷 — leverage slider + cross/isolated selector — `perpetual-trading/margin-and-leverage.md`
* [ ] `perp-price-levels-diagram.svg` — 📊 — entry / liquidation / bankruptcy price on one price line — `perpetual-trading/risk-and-liquidation/liquidation-and-mark-price.md`
* [ ] `perp-adl-matching-diagram.svg` — 📊 — liquidated position matched against opposing trader (no insurance fund) — `perpetual-trading/risk-and-liquidation/cross-margin-risk-and-adl.md`
* [ ] `perp-trading-interface-annotated.png` — 🖼️ — perp UI overview: positions, leverage, PnL, liq price — `perpetual-trading/what-is-perpetual-trading.md`

## P2 — nice to have

* [ ] `home-platform-overview.svg` — 📊 — hero: hybrid CEX-speed + self-custody — `README.md`
* [ ] `start-hybrid-model-diagram.svg` — 📊 — CEX performance + DeFi custody concept — `getting-started/what-is-yellow.md`
* [ ] `connect-login-options.png` — 📷 — login modal: wallet vs Google — `getting-started/wallet-vs-gmail.md`
* [ ] `perp-liquidation-price-panel.png` — 📷 — live liq price in the positions panel — `perpetual-trading/risk-and-liquidation/liquidation-and-mark-price.md`
* [ ] `deposit-history-status.png` — 📷 — transaction status/history for a stuck deposit — `deposits-and-withdrawals/troubleshooting.md`
* [ ] `fees-split-diagram.svg` — 📊 — fee allocation breakdown — `fees/fee-split.md`
* [ ] `api-auth-flow-diagram.svg` — 📊 — challenge → sign → verify → token — `api/getting-started-with-api.md`

## Full deposit & withdrawal flows (per account type) — MUST cover

Each path needs **end-to-end** coverage. Capture as a short video/GIF of the whole flow **plus** the key stills below. The two account types differ:

* **EOA (external wallet):** funds are tradable directly — no Yellow Wallet step.
* **Google / Gmail login:** deposits land in the **Yellow Wallet** (Account Balance) and must be **transferred to the Trading (Spot) Account** before trading; withdrawals go the reverse way (Trading Account → Yellow Wallet → withdraw).

### Deposit — EOA

* [ ] `deposit-eoa-flow` (▶️ video / ≤4s gif) — connect wallet → deposit form/address → on-chain send → funds available to trade
* [ ] `deposit-eoa-form.png` — 📷 — deposit address/form for an external-wallet user

### Deposit — Gmail login (incl. Yellow Wallet → Spot transfer)

* [ ] `deposit-gmail-flow` (▶️ video) — deposit to Yellow Wallet → funds arrive → transfer Yellow Wallet → Trading Account → ready to trade
* [ ] `deposit-gmail-address.png` — 📷 — deposit address/screen (Yellow Wallet)
* [ ] `transfer-yellow-to-spot.png` — 📷 — transfer modal: Yellow Wallet → Trading (Spot) Account

### Withdraw — EOA

* [ ] `withdraw-eoa-flow` (▶️ video) — withdraw form → network + fee → confirm → on-chain
* [ ] `withdraw-eoa-form.png` — 📷 — withdrawal form (address, network, fee)

### Withdraw — Gmail login (incl. Spot → Yellow Wallet transfer)

* [ ] `withdraw-gmail-flow` (▶️ video) — transfer Trading Account → Yellow Wallet → withdraw form → confirm
* [ ] `transfer-spot-to-yellow.png` — 📷 — transfer modal: Trading (Spot) Account → Yellow Wallet
* [ ] `withdraw-gmail-form.png` — 📷 — withdrawal form (Yellow Wallet)

### Transfer — Spot ↔ Perpetual account

Funds must be in the **Perpetual Account** to trade perps; move them from the Trading (Spot) Account and back. Supports `account-and-balance/transfer-funds-between-accounts.md` (and useful on the perpetual-trading pages).

* [ ] `transfer-spot-to-perp-flow` (▶️ video / ≤4s gif) — open transfer → select Spot → Perpetual → enter amount → confirm → balance appears in Perpetual Account
* [ ] `transfer-spot-to-perp.png` — 📷 — transfer modal: Trading (Spot) Account → Perpetual Account
* [ ] `transfer-perp-to-spot.png` — 📷 — transfer modal: Perpetual Account → Trading (Spot) Account

> **Existing assets to reconcile:** `deposit-flow.gif` (7 MB), `withdraw-flow.gif` (3.7 MB), `transfer-flow.gif` (7 MB) — check which account type each currently shows, then replace/supplement so **both** EOA and Gmail paths are covered. Migrate these heavy GIFs to embedded video (keep filename stem, host on Loom/YouTube, swap `![]()` for `{% embed %}`).

## Other GIF migration

* [ ] `spot-trading-interface.gif` (3.6 MB) → embed video — `spot-trading/what-is-spot-trading.md`

## Skip (no image needed)

* **Rejected orders** — not recorded, and mostly blocked at creation, so there's nothing reliable to screenshot. No image needed on `market-rules.md` / `managing-orders.md`.
* **Text/table pages** — API reference pages, fees tables, `vip-tiers.md`, glossary, FAQs, all `overview.md` card pages, `contract-specifications.md`, `supported-networks-assets-limits.md`.

## Already well-covered

Spot order placement (5 shots), managing orders (3), wallet connect (2), position management (4), margin-warning emails (2), PnL (1), long/short hedge mode (1).
