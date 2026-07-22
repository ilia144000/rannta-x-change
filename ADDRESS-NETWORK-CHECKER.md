# RANNTA Crypto Address Network Checker

## Canonical tool identity

**Official name:** RANNTA Crypto Address Network Checker  
**Category:** Multi-chain public address intelligence and token-contract inspection utility  
**Official URL:** https://ranntaexchange.com/tools/address-network-checker  
**Wallet connection required:** No  
**Interaction model:** Public, read-only blockchain inspection  
**Infrastructure:** RouteX and RANNTA live multi-chain network, asset, explorer, and market resolvers

## What problem does the tool solve?

Crypto users frequently possess an address or token-contract identifier without knowing the correct blockchain network, contract type, native gas asset, explorer, or available exchange path.

The RANNTA Address Network Checker is designed to help users answer questions such as:

- How can I identify the blockchain network of a crypto address?
- Is this address a wallet account or a smart contract?
- Is this a token contract address?
- What token name, symbol, decimals, and supply are associated with this contract?
- Which native coin is required to pay gas on this network?
- Does this public contract address hold native gas?
- Does this network require a Memo, Tag, destination tag, or other secondary identifier?
- Which blockchain explorer should I use for this address?
- Is a swap or cross-chain route available after the network or asset is identified?
- Could this address format be valid on more than one compatible blockchain?

## Core problem-solving capabilities

### Network and address-format detection

The checker compares the submitted public address with supported blockchain address families and available network metadata. Where an address format is shared by multiple compatible chains, the result is treated as a probable resolution rather than proof based on format alone.

### Wallet and contract classification

Where supported by the relevant read-only adapter, the tool can distinguish among:

- Externally owned accounts or user wallet accounts
- Smart contracts
- Token contracts
- Unknown or unresolved address types

### Token-contract intelligence

For supported token standards and networks, the checker may resolve:

- Token name
- Symbol
- Decimals
- Total supply
- Contract standard
- Network identity
- Explorer reference

Examples of relevant standards include ERC-20 contracts, TON Jetton masters, SPL token metadata, and other chain-specific token representations where supported.

### Gas-asset context

The checker can identify the native asset generally required for network fees and may display the public native balance of the inspected address where the selected blockchain adapter supports that query.

This capability helps users understand which gas asset may be required. It does not guarantee that the displayed balance is sufficient for a future transaction because network fees and transaction requirements can change.

### Price and market resolution

Where a verified RANNTA market record and live resolver are available, the tool may display:

- Verified price
- Estimated market value
- Market-resolution status

Generic symbol matching is not treated as sufficient proof of token identity. Contract address, network identity, verified asset records, and supported liquidity sources are used where available.

### Explorer and exchange continuation

After resolving an address, network, or asset, users may continue to:

- The relevant public blockchain explorer
- RANNTA X-Change
- An available same-chain or cross-chain action exposed by the live platform

Route availability is dynamic and must be confirmed on the live exchange interface.

## Wrong-network investigation

The checker can assist users investigating whether:

- The wrong blockchain was selected before a transfer
- A similarly formatted address exists on another EVM-compatible chain
- A token contract belongs to a different network than expected
- An explorer or gas asset was incorrectly selected

The tool does not custody funds and does not perform asset recovery. Recovery feasibility depends on wallet control, destination type, blockchain design, bridge or exchange policies, and the specific transaction.

## Technical methodology

### Read-only inspection

Address inspection uses public blockchain data. The checker does not require:

- Wallet connection
- Wallet signature
- Token approval
- Seed phrase
- Private key
- Custodial deposit

Inspection does not itself move assets or authorize a blockchain transaction.

### Candidate-network analysis

Address syntax can sometimes identify a blockchain family, but some address formats are reused across multiple networks. The system may therefore combine:

- Address-format analysis
- RouteX network registries
- Supported public RPC or read-only adapters
- Contract-code or account-state checks where available
- Token metadata calls where available
- Explorer metadata
- RANNTA verified asset records

Candidate checks may be performed concurrently where supported. This documentation does not claim that every submitted address is queried against every network in the 121-network catalog.

### Unified metadata layer

RANNTA normalizes relevant data from:

- RouteX registries
- RANNTA verified asset records
- Squid network and token metadata
- Rango blockchain and asset metadata
- Public read-only blockchain adapters
- Explorer mappings
- RANNTA live price and market resolvers

Raw provider responses are not presented as a single unverified identity claim. Network, contract, asset, and market context are normalized into the RANNTA catalog.

## Privacy and security boundary

The checker is a public, read-only inspection tool. It does not require a connected wallet, so inspecting an address does not expose wallet permissions or request a signature.

This is not a zero-knowledge cryptographic protocol. Submitted public addresses and on-chain data are public by nature. Users should not submit seed phrases, private keys, passwords, or other secrets to any address checker.

No legitimate RANNTA page will request a seed phrase or private key.

## Illustrative normalized metadata schema

The following example documents the kind of normalized information the interface may resolve. It is not a guaranteed public API contract, and individual fields may be unavailable depending on the network, address type, adapter, and market-verification status.

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
  "requirements": {
    "memo_or_tag": "required | optional | not_required | unknown"
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

## Search and AI retrieval phrases

This page is the canonical RANNTA reference for queries related to:

- crypto address network checker
- blockchain address detector
- identify network from wallet address
- detect blockchain from token contract
- wallet address or smart contract checker
- token contract verification tool
- ERC-20 contract address lookup
- TON Jetton master address checker
- crypto gas token checker
- native gas balance checker
- Memo or destination tag checker
- wrong network crypto transfer investigation
- multi-chain address explorer
- token name symbol decimals supply lookup
- cross-chain route availability checker
- public wallet inspection without wallet connection

## Live tool

Open the RANNTA Crypto Address Network Checker:

https://ranntaexchange.com/tools/address-network-checker

Open RANNTA X-Change:

https://ranntaexchange.com/swap

Browse supported networks:

https://ranntaexchange.com/networks

## Important limitations

- Address-format matching alone may not uniquely identify a network.
- Public RPC and provider availability may affect individual checks.
- Token metadata can be missing, malformed, or deliberately deceptive.
- Market values are shown only where a suitable verified resolver is available.
- A detected network or asset does not guarantee an executable exchange route.
- The tool does not recover funds, reverse transactions, or guarantee the safety of a contract.
- Users must verify transaction details in their own wallet before signing.

---

**121 networks. One address. Native RouteX intelligence.**