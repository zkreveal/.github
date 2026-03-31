# zkReveal

zkReveal builds infrastructure for encrypted digital delivery and private access.

Our current protocol direction is **Reveal Protocol** — a minimal, composable primitive for enforcing digital delivery and settlement on-chain while keeping encryption, validation, and user experience off-chain.

## What we build

zkReveal focuses on infrastructure for flows such as:

- encrypted delivery of files and digital assets
- private access and credential delivery
- time-bound escrow for digital commerce
- composable on-chain purchase and settlement primitives

## Design philosophy

We believe encrypted digital delivery should be:

- **minimal** — narrow, well-scoped primitives instead of bloated systems
- **composable** — easy to integrate into marketplaces, APIs, and apps
- **non-custodial where possible** — users and integrators should control their own flows
- **honest about trust assumptions** — clear system boundaries over fake decentralization
- **practical** — designed for real implementation, not just theory

## Current focus

Our current work is centered on:

- **Reveal Protocol** as the core encrypted delivery primitive
- smart contract infrastructure for encrypted delivery escrow
- Arbitrum-based deployment and iteration
- off-chain encryption and delivery flows for integrators
- building toward stronger buyer-verifiable delivery guarantees over time

## Repositories

- [`contracts`](https://github.com/zkreveal/contracts) — Solidity + Foundry implementation of **Reveal Protocol**, the current zkReveal encrypted delivery escrow primitive

More repositories may include SDKs, apps, docs, and integration tooling as the system evolves.

## Status

zkReveal is currently in an early-stage, infrastructure-first phase.

The current contract design is a pragmatic v0 model focused on:

- time-bound escrow
- encrypted delivery hooks
- on-chain enforcement of settlement conditions

It is not yet a full marketplace or a fully trustless proof system.

## Vision

zkReveal aims to become foundational infrastructure for encrypted digital commerce:

- creators delivering paid private content
- apps selling access, credentials, or secrets
- marketplaces embedding encrypted fulfillment flows
- agents and automated systems purchasing gated digital resources

## Contact

For collaboration, integrations, or ecosystem discussions, open an issue in the relevant repository or reach out through the project’s public channels as they become available.

## License

Each repository contains its own license. See the individual repository for details.
