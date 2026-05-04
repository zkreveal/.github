# zkReveal

**zkReveal builds on-chain receipt and settlement infrastructure for digital sellers.**

The current project focus is **Reveal Receipt Mode** — a minimal USDC-based payment and receipt primitive for seller-issued checkout flows, private payment links, Telegram bots, gated access, and digital commerce.

Instead of trying to verify delivery on-chain, Receipt Mode focuses on a narrower v1 promise:

> A buyer pays, settlement happens immediately, and an on-chain receipt is created for seller systems, bots, dashboards, and indexers to verify.

Receipt Mode is a proof-of-payment and settlement primitive. It is not an escrow or delivery-verification system.

---

## What we build

zkReveal focuses on infrastructure for flows such as:

- seller-issued payment links
- USDC checkout for digital products
- on-chain proof-of-payment receipts
- Telegram bot commerce
- private access and credential sales
- gated communities and digital fulfillment
- composable purchase and settlement primitives
- future encrypted delivery and reveal workflows

The current v1 contract is intentionally small: sellers create listings, buyers purchase receipts, and seller systems fulfill off-chain after verifying the receipt.

---

## Current focus

Our current work is centered on:

- **Reveal Receipt Mode** as the first production primitive
- Solidity + Foundry smart contracts
- Arbitrum-based deployment and iteration
- USDC settlement
- seller-scoped purchase references
- seller-authorized signed quotes using EIP-712
- event/indexer-friendly receipt infrastructure
- Telegram bot and lightweight seller checkout flows

This is the practical first layer before expanding into stronger encrypted delivery, reveal, escrow, or dispute models.

---

## How Receipt Mode works

At a high level:

1. A seller creates a listing with opaque metadata.
2. The seller or backend creates a purchase reference.
3. A buyer pays in USDC.
4. The contract emits and stores an on-chain receipt.
5. Seller systems verify the receipt and fulfill off-chain.

For production checkout/payment-link flows, signed quotes are recommended.

Signed quotes bind:

- buyer
- listing
- seller
- amount
- purchase reference
- metadata hash
- settlement token
- expiry
- chain
- contract

This makes them suitable for Telegram bots, private checkout links, seller-issued orders, dynamic pricing, and integrator-fee flows.

---

## What Receipt Mode does not do

Receipt Mode does **not** verify:

- delivery
- content correctness
- access provisioning
- product quality
- refunds
- disputes
- whether the seller actually fulfilled the order

Seller systems, bots, dashboards, or off-chain workflows are responsible for fulfillment after seeing a valid receipt.

This is an intentional v1 design choice. zkReveal starts with a narrow, useful settlement primitive instead of pretending to solve every trust problem on-chain.

---

## Design philosophy

We believe digital commerce infrastructure should be:

- **minimal** — narrow, well-scoped primitives instead of bloated systems
- **composable** — easy to integrate into marketplaces, bots, APIs, and apps
- **honest about trust assumptions** — clear boundaries over fake decentralization
- **seller-friendly** — practical for real sellers, not only protocol theorists
- **indexer-friendly** — useful events and receipts for apps and dashboards
- **upgradeable by architecture, not admin magic** — simple v1 contracts with clear future paths

---

## Repositories

- **contracts** — Solidity + Foundry implementation of Reveal Receipt Mode

More repositories may include SDKs, bots, apps, docs, and integration tooling as the system evolves.

---

## Status

zkReveal is currently in an early-stage, infrastructure-first phase.

The current contract design is a pragmatic v1 focused on:

- immediate USDC settlement
- seller-owned listings
- seller-scoped purchase references
- EIP-712 signed receipt quotes
- on-chain purchase receipts
- off-chain fulfillment by seller systems

It is not yet a full marketplace, escrow protocol, dispute system, or fully trustless delivery-verification layer.

---

## Future direction

zkReveal may expand toward:

- encrypted delivery flows
- buyer-verifiable reveal workflows
- escrow-based settlement modes
- Telegram-native digital commerce
- SDKs for marketplaces and apps
- cross-chain payment entry
- stronger off-chain/on-chain fulfillment guarantees

The long-term vision is to become foundational infrastructure for digital commerce where payments, receipts, access, and fulfillment can be composed across apps.

---

## Vision

zkReveal aims to become a lightweight settlement and receipt layer for internet-native digital commerce:

- creators selling private content
- sellers delivering credentials or access
- apps monetizing gated resources
- Telegram communities selling memberships
- marketplaces embedding crypto-native checkout
- agents purchasing digital resources from other systems

The first step is simple:

> reliable on-chain receipts for seller-issued digital payments.

---

## Contact

For collaboration, integrations, or ecosystem discussions, open an issue in the relevant repository or reach out through the project’s public channels as they become available.

---

## License

Each repository contains its own license. See the individual repository for details.
