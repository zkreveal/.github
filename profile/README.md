# zkReveal

**zkReveal builds on-chain receipt and settlement infrastructure for digital sellers.**

The current focus is **Reveal Receipt Mode** — a minimal USDC-based primitive for seller-issued checkout flows, payment links, bots, and private digital commerce.

Instead of trying to verify delivery on-chain, Receipt Mode focuses on a simpler, practical promise:

> A buyer pays, settlement happens immediately, and an on-chain receipt is created.

That receipt becomes the source of truth for seller systems, bots, dashboards, and indexers.

Receipt Mode is a **payment and receipt layer**, not an escrow or delivery-verification system.

---

## What we build

zkReveal provides infrastructure for:

- seller-issued payment links
- crypto checkout for digital products
- on-chain proof-of-payment receipts
- Telegram-native commerce flows
- private access and credential sales
- gated content and memberships
- composable settlement primitives for apps and marketplaces

The v1 contract is intentionally minimal:
sellers create listings → buyers purchase → receipts are emitted → fulfillment happens off-chain.

---

## Current focus

We are currently focused on:

- **Reveal Receipt Mode** as the first production primitive
- Solidity + Foundry smart contracts
- Arbitrum-based deployment
- USDC settlement
- seller-scoped purchase references
- EIP-712 signed quotes for dynamic checkout
- event-driven, indexer-friendly design
- lightweight seller flows (bots, dashboards, payment links)

This is the first layer — not the final system.

---

## How Receipt Mode works

At a high level:

1. Seller creates a listing (opaque metadata).
2. Seller/backend generates a purchase reference.
3. Buyer pays in USDC.
4. Contract records an on-chain receipt.
5. Seller systems observe the event and fulfill off-chain.

For real-world checkout flows, **signed quotes** are used.

Signed quotes bind:

- buyer
- seller
- listing
- amount
- purchase reference
- metadata hash
- settlement token
- expiry
- chain + contract

This enables:

- private payment links
- Telegram bot flows
- dynamic pricing
- integrator fees
- seller-controlled checkout logic

---

## What Receipt Mode does NOT do

Receipt Mode does not attempt to verify:

- delivery
- content correctness
- access provisioning
- refunds or disputes
- product quality

It does one thing:

> record payment and settlement on-chain.

Everything else happens off-chain.

This is an intentional design choice.

---

## Design philosophy

We believe digital commerce infrastructure should be:

- **minimal** — focused primitives, not bloated systems
- **composable** — usable inside apps, bots, APIs, and marketplaces
- **honest** — clear trust boundaries instead of fake decentralization
- **seller-first** — built for real sellers and real flows
- **event-driven** — easy to integrate via indexers and listeners
- **extensible** — evolve through new primitives, not complex upgrades

---

## Repositories

- **contracts** — Solidity + Foundry implementation of Reveal Receipt Mode

Additional repos (SDKs, bots, apps, tooling) will follow.

---

## Status

zkReveal is in an early-stage, infrastructure-first phase.

Current capabilities:

- immediate USDC settlement
- seller-owned listings
- seller-scoped purchase references
- EIP-712 signed receipt quotes
- on-chain receipt records
- off-chain fulfillment

It is **not** a marketplace, escrow protocol, or dispute system.

---

## Future direction

zkReveal may expand toward:

- encrypted delivery flows
- buyer-verifiable reveal mechanisms
- escrow-based settlement modes
- Telegram-native commerce systems
- SDKs for apps and marketplaces
- cross-chain payment entry
- stronger fulfillment guarantees

But only after the core primitive proves itself.

---

## Vision

zkReveal aims to become a foundational layer for digital commerce:

- creators selling private content
- sellers delivering credentials and access
- apps monetizing gated resources
- communities selling memberships
- marketplaces embedding crypto-native checkout
- agents purchasing digital resources

The first step is simple:

> reliable on-chain receipts for digital payments.

---

## Contact

Open an issue in the relevant repository or reach out through project channels as they become available.

---

## License

Each repository contains its own license.
