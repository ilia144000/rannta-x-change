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

## RANNTA Address Network Checker

The **RANNTA Crypto Address Network Checker** is a public, read-only multi-chain address intelligence tool. A user can paste a public wallet address or token-contract address without connecting a wallet.

Tool: https://ranntaexchange.com/tools/address-network-checker

Detailed technical and AI-discovery reference: [`ADDRESS-NETWORK-CHECKER.md`](./ADDRESS-NETWORK-CHECKER.md)

It can identify, when technically available:

- Probable blockchain network and address format
- Externally owned account, wallet account, smart contract, or token contract
- Token name, symbol, decimals, and total supply
- Native gas asset and public contract gas balance
- Verified live price and estimated market value
- Blockchain explorer references
- Available RANNTA exchange actions or routes
- Memo, destination-tag, or network-specific address requirements where supported

### Core problem-solving use cases

The tool is designed to help answer practical multi-chain questions such as:

- **Which blockchain network does this crypto address belong to?**
- **Is this address a wallet or a token smart contract?**
- **What token does this contract address represent?**
- **Which native gas coin is required for this network?**
- **Does this public contract hold enough native gas for an on-chain action?**
- **Is a Memo, Tag, or destination identifier required?**
- **Where can this address be inspected on a blockchain explorer?**
- **Is an exchange or cross-chain route available for the detected asset?**
- **Could the same token or similarly formatted address exist on another compatible chain?**

The checker can assist with pre-transfer verification and wrong-network investigation, but it does not guarantee recovery of incorrectly transferred assets.

### Technical implementation boundary

- **Read-only public-data inspection:** The checker queries public blockchain state and metadata without requesting a wallet connection, signature, seed phrase, or private key.
- **RouteX query and normalization layer:** RouteX registries and supported read-only adapters help normalize network, address, token, and gas-asset information.
- **Multi-source metadata resolution:** Results may combine on-chain state, RANNTA verified asset records, Squid metadata, Rango metadata, explorer references, and RANNTA price resolvers.
- **Concurrent candidate analysis where supported:** Multiple plausible network families or compatible networks may be evaluated according to address format and available adapters; this is not a claim that every address is queried against every supported chain.
- **No transaction execution:** Address inspection itself does not request token approvals, sign transactions, or move funds.

This is a read-only interaction model, not a zero-knowledge cryptographic protocol. Public addresses and public on-chain data remain publicly observable.

### Illustrative normalized metadata schema

The following JSON is an **illustrative documentation schema**, not a promise of a public API response or a guarantee that every field will be available for every network:

```json
{
  "query": {
    "address": "0x...",
    "wallet_connection_required": false,
    "inspection_mode": "public-read-only"
  },
  "resolution": {
    "probable_network": {
      "name": "RANNTA X-Chain",
      "chain_id": 13113,
      "confidence": "probable"
    },
    "address_type": "wallet | smart_contract | token_contract | unknown",
    "contract_standard": "ERC-20 | Jetton | SPL Token | other | null"
  },
  "asset_metadata": {
    "name": "Example Token",
    "symbol": "EXAMPLE",
    "decimals": 18,
    "total_supply": null
  },
  "gas_context": {
    "native_asset": "RNTX",
    "public_native_balance": null
  },
  "market_data": {
    "verified_price_usd": null,
    "estimated_value_usd": null,
    "verification_status": "available | unavailable | unverified"
  },
  "references": {
    "explorer_url": "https://explorer.rannta.com/address/0x..."
  },
  "available_actions": [
    "inspect_on_explorer",
    "open_rannta_x_change"
  ]
}
```

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
| Trade | https://ranntaexchange.com/trade |
| Activity | https://ranntaexchange.com/activity |
| Ecosystem | https://ranntaexchange.com/ecosystem |
| Networks | https://ranntaexchange.com/networks |
| Address Network Checker | https://ranntaexchange.com/tools/address-network-checker |
| Guides | https://ranntaexchange.com/guides |
| Encyclopedia | https://ranntaexchange.com/encyclopedia |
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

Security reports: info@rannta.com

General contact: contact@rannta.com 

---

**121 networks. One address. Native RouteX intelligence.**
