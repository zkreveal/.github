# zkReveal

zkReveal builds on-chain receipt and settlement infrastructure for digital sellers.

The current focus is **Reveal Receipt Mode** — a minimal USDC-based primitive for seller-issued checkout flows, payment links, bots, and private digital commerce.

A buyer pays, settlement happens immediately, and an on-chain receipt is created.

That receipt becomes the source of truth for seller systems, Telegram bots, dashboards, apps, and indexers.

Receipt Mode is a **payment and receipt layer** — not a marketplace or escrow protocol.

---

## What zkReveal enables

zkReveal provides infrastructure for:

- seller-issued payment links
- crypto checkout for digital products
- on-chain proof-of-payment receipts
- Telegram-native commerce flows
- private access and credential sales
- gated content and memberships
- composable settlement primitives for apps and marketplaces

The v1 flow is intentionally simple:

```text
seller creates listing
→ seller/backend generates purchase reference
→ buyer pays in USDC
→ contract records receipt
→ seller system fulfills off-chain
```

---

## Current focus

We are currently building **Reveal Receipt Mode** as the first production primitive.

The current stack focuses on:

- Solidity + Foundry smart contracts
- Arbitrum-based deployment
- USDC settlement
- seller-owned listings
- seller-scoped purchase references
- EIP-712 signed quotes for dynamic checkout
- event-driven, indexer-friendly design
- lightweight seller flows through bots, dashboards, and payment links

This is the first layer — not the final system.

---

## Signed checkout quotes

For real-world checkout flows, Receipt Mode supports EIP-712 signed quotes.

Signed quotes bind:

- buyer
- seller
- listing
- amount
- purchase reference
- metadata hash
- settlement token
- expiry
- chain and contract

This enables:

- private payment links
- Telegram bot checkout
- dynamic pricing
- integrator fees
- seller-controlled checkout logic

---

## Scope

Reveal Receipt Mode records payment, settlement, and receipt creation on-chain.

Fulfillment happens off-chain through seller systems, bots, dashboards, APIs, or applications.

This keeps the v1 primitive simple, composable, and honest about its trust boundaries.

zkReveal does not try to force every part of digital commerce on-chain. Instead, it provides a reliable receipt layer that other systems can build on.

---

## Design philosophy

zkReveal is built around a few principles:

- **minimal** — focused primitives, not bloated systems
- **composable** — usable inside apps, bots, APIs, and marketplaces
- **honest** — clear trust boundaries instead of fake decentralization
- **seller-first** — built for real sellers and real checkout flows
- **event-driven** — easy to integrate through indexers and listeners
- **extensible** — new primitives over complex upgrades

---

## Repositories

- **contracts** — Solidity + Foundry implementation of Reveal Receipt Mode

Additional repositories for SDKs, bots, apps, and tooling may follow.

---

## Status

zkReveal is in an early-stage, infrastructure-first phase.

Current capabilities include:

- immediate USDC settlement
- seller-owned listings
- seller-scoped purchase references
- EIP-712 signed receipt quotes
- on-chain receipt records
- off-chain fulfillment

zkReveal is not currently a marketplace, escrow protocol, or dispute system.

---

## Future direction

After the core receipt primitive proves itself, zkReveal may expand toward:

- encrypted delivery flows
- buyer-verifiable reveal mechanisms
- escrow-based settlement modes
- Telegram-native commerce systems
- SDKs for apps and marketplaces
- cross-chain payment entry
- stronger fulfillment guarantees

The long-term goal is to become a foundational payment and receipt layer for digital commerce.

---

## Vision

zkReveal is designed for:

- creators selling private content
- sellers delivering credentials and access
- apps monetizing gated resources
- communities selling memberships
- marketplaces embedding crypto-native checkout
- agents purchasing digital resources

The first step is simple:

**reliable on-chain receipts for digital payments.**

---

## Contact

Open an issue in the relevant repository or reach out through project channels as they become available.

---

## License

Each repository contains its own license.
