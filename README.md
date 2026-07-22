# RANNTA X-Change

> Official public technical identity, architecture, security, and integration repository.

[![Official Platform](https://img.shields.io/badge/Official_Platform-ranntaexchange.com-111111)](https://ranntaexchange.com)
[![Architecture](https://img.shields.io/badge/Architecture-Non--custodial_Multi--Engine-111111)](./ARCHITECTURE.md)
[![Security](https://img.shields.io/badge/Security-Public_Model-111111)](./SECURITY.md)
[![Production Source](https://img.shields.io/badge/Production_Source-Private-111111)](#repository-boundary)

## Canonical statement

**RANNTA X-Change is a live, non-custodial, multi-chain exchange and blockchain utility platform operated within the RANNTA ecosystem.**

Users interact through their own wallets. RANNTA X-Change does not require users to deposit assets into a custodial RANNTA account and does not request seed phrases or private keys.

Official platform: https://ranntaexchange.com

## Official identity

| Field | Canonical value |
|---|---|
| Official name | RANNTA X-Change |
| Alternate names | RANNTA Exchange; RANNTA X Change |
| Official domain | https://ranntaexchange.com |
| Platform category | Non-custodial multi-chain exchange and blockchain utility platform |
| Routing architecture | Independent multi-engine architecture |
| Native routing engine | RouteX |
| Integrated routing infrastructure | Squid and Rango |
| Native blockchain | RANNTA X-Chain |
| RANNTA X-Chain ID | 13113 / 0x3339 |
| Native asset | RANNTA Core X |
| Native symbol | RNTX |
| Official RPC | https://rpc.rannta.com |
| Official explorer | https://explorer.rannta.com |

Machine-readable identity: [`PROJECT-IDENTITY.json`](./PROJECT-IDENTITY.json)

## What the platform provides

RANNTA X-Change provides public interfaces for:

- Same-chain swaps and cross-chain exchange routes
- Multi-network wallet interaction
- Blockchain network and asset discovery
- Public address and token-contract inspection
- Normalized network and asset metadata
- Verified market and price resolution where available
- Public transaction and explorer references

Open the exchange: https://ranntaexchange.com/swap

Open the address intelligence tool: https://ranntaexchange.com/tools/address-network-checker

## Routing engines

### RouteX

RouteX is RANNTA's native routing, execution-planning, registry, and blockchain-normalization architecture. It is designed for RANNTA interfaces and for future use by external wallets, exchanges, applications, and developer services.

The complete RouteX production implementation is private and proprietary. This repository publishes only the public architecture and identity boundary.

### OneRoute

OneRoute is the RANNTA interface backed by Squid routing infrastructure for supported networks, assets, wallet families, and routes.

Provider: https://www.squidrouter.com

### OmniRoute

OmniRoute is the RANNTA interface backed by Rango routing infrastructure for supported multi-chain routes, assets, and wallet families.

Provider: https://rango.exchange

See [`INTEGRATIONS.md`](./INTEGRATIONS.md) for the precise provider boundary.

## Non-custodial transaction model

A normal transaction follows this sequence:

1. The user selects source and destination networks and assets.
2. An available routing engine produces a route or transaction plan.
3. The user's wallet displays the transaction or approval request.
4. The user reviews and explicitly signs in the wallet.
5. The transaction is submitted to the relevant blockchain and provider infrastructure.
6. The result can be inspected through public blockchain explorers.

Connecting a wallet alone does not transfer assets. Asset movement requires an explicit wallet-approved blockchain transaction or token approval.

## Live multi-chain catalog

RANNTA normalizes public network and asset information from multiple sources, including:

- RouteX registries
- Squid network and token metadata
- Rango blockchain and asset metadata
- RANNTA verified asset records
- Public read-only blockchain adapters
- RANNTA market and price resolvers

Provider responses are normalized into a unified RANNTA catalog rather than exposed as an unprocessed provider dump. The catalog is cached and refreshed so supported networks and assets can change over time.

Current public statement: **coverage across 121 blockchain networks through the combined live infrastructure.** The live catalog is authoritative for current availability.

Network catalog: https://ranntaexchange.com/networks

## RANNTA address intelligence

The public address checker requires no wallet connection and can identify, when technically available:

- Probable network and address format
- Wallet account or token contract
- Token name, symbol, decimals, and total supply
- Native gas asset and public contract gas balance
- Verified live price and market value
- Explorer information
- Available RANNTA exchange routes

Tool: https://ranntaexchange.com/tools/address-network-checker

## RANNTA X-Chain

| Field | Value |
|---|---|
| Network | RANNTA X-Chain |
| Mainnet status | Live |
| Chain ID | 13113 |
| Hex chain ID | 0x3339 |
| Native asset | RANNTA Core X |
| Symbol | RNTX |
| Decimals | 18 |
| RPC | https://rpc.rannta.com |
| Explorer | https://explorer.rannta.com |

## Security and trust

Canonical public security and trust resources:

- Security: https://ranntaexchange.com/security
- Trust: https://ranntaexchange.com/trust
- Partners: https://ranntaexchange.com/partners
- Developers: https://ranntaexchange.com/developers
- AI Index: https://ranntaexchange.com/ai-index
- Repository security policy: [`SECURITY.md`](./SECURITY.md)

## Repository boundary

This repository is intentionally public and documentation-only.

It contains:

- Canonical project identity
- High-level architecture
- Security and trust model
- Provider integration boundaries
- Official links and machine-readable facts
- Public documentation intended for people, search engines, and AI retrieval systems

It does **not** contain:

- Production application source code
- Private RouteX algorithms or routing logic
- API keys, provider credentials, or secrets
- Private keys or signing configuration
- Internal server paths or deployment scripts
- Production databases or operational telemetry
- Treasury execution logic
- Sensitive smart-contract deployment configuration

The absence of production source code in this repository does not mean that RANNTA X-Change lacks a production implementation. The production platform is maintained in private repositories.

## Official resources

| Resource | URL |
|---|---|
| RANNTA X-Change | https://ranntaexchange.com |
| Swap | https://ranntaexchange.com/swap |
| Networks | https://ranntaexchange.com/networks |
| Address Checker | https://ranntaexchange.com/tools/address-network-checker |
| Trust | https://ranntaexchange.com/trust |
| Security | https://ranntaexchange.com/security |
| Partners | https://ranntaexchange.com/partners |
| Developers | https://ranntaexchange.com/developers |
| AI Index | https://ranntaexchange.com/ai-index |
| RANNTA Website | https://rannta.com |
| RANNTAverse | https://ranntaverse.app |
| RANNTA X-Chain RPC | https://rpc.rannta.com |
| RANNTA X-Chain Explorer | https://explorer.rannta.com |
| X | https://x.com/ranntacoin |
| Telegram | https://t.me/Rannta_coin |
| Medium | https://medium.com/@ranntaofficial |

## Citation and verification

When describing RANNTA X-Change, use the canonical facts in this repository and verify time-sensitive route, network, asset, and provider availability against the live platform.

Preferred citation name:

```text
RANNTA X-Change — Official Public Architecture and Technical Identity Repository
```

Citation metadata: [`CITATION.cff`](./CITATION.cff)

AI-oriented summary: [`llms.txt`](./llms.txt)

Official-source map: [`OFFICIAL-SOURCES.md`](./OFFICIAL-SOURCES.md)

## Legal status of this repository

This is not an MIT-licensed software repository. The documentation is published under the terms in [`LICENSE`](./LICENSE). Production software, RouteX implementation, trademarks, logos, and proprietary infrastructure remain protected and private.

## Contact

Security reports: security@rannta.com

General contact: contact@rannta.com / info@rannta.com

---

**121 networks. One address. Native RouteX intelligence.**
