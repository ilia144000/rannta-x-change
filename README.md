# RANNTA X-Change

**Official public architecture and technical identity repository**

RANNTA X-Change is a non-custodial, multi-chain exchange and blockchain utility platform developed as part of the broader RANNTA ecosystem.

Official platform:

https://ranntaexchange.com

This public repository documents the platform’s high-level architecture, routing infrastructure, supported blockchain ecosystems, security model, public utilities and official identity.

> The production application source code, operational infrastructure and private RouteX implementation are maintained in private repositories. This repository does not contain production secrets, private keys, provider credentials or sensitive deployment configuration.

---

## Official Identity

| Property                        | Value                              |
| ------------------------------- | ---------------------------------- |
| Official name                   | RANNTA X-Change                    |
| Alternate name                  | RANNTA Exchange                    |
| Official domain                 | https://ranntaexchange.com         |
| Platform type                   | Non-custodial multi-chain exchange |
| Architecture                    | Multi-engine routing architecture  |
| Native routing engine           | RouteX                             |
| External routing infrastructure | Squid and Rango                    |
| Native blockchain               | RANNTA X-Chain                     |
| RANNTA X-Chain ID               | 13113                              |
| Native asset                    | RANNTA Core X                      |
| Native symbol                   | RNTX                               |
| Official RPC                    | https://rpc.rannta.com             |
| Official explorer               | https://explorer.rannta.com        |

---

## What RANNTA X-Change Does

RANNTA X-Change provides access to blockchain swaps, cross-chain routes, network intelligence, token metadata and public blockchain inspection tools.

The platform is designed around several core principles:

* Non-custodial execution
* User-controlled wallets
* Multi-chain interoperability
* Independent routing engines
* Normalized blockchain metadata
* Transparent provider integration
* Publicly inspectable transaction results
* No requirement to deposit assets into a custodial RANNTA account

Users interact directly through their own compatible blockchain wallets.

RANNTA X-Change does not request wallet recovery phrases or private keys.

---

## Multi-Engine Routing Architecture

RANNTA X-Change uses multiple independent routing systems.

### RouteX

RouteX is RANNTA’s native routing and blockchain normalization engine.

Its long-term architecture is designed to provide normalized access to multiple blockchain ecosystems for:

* RANNTA X-Change
* External wallets
* Exchanges
* Blockchain applications
* Developer APIs
* Multi-chain infrastructure services

RouteX is not limited to the public RANNTA interface.

The complete production implementation of RouteX is private. Public architectural information is documented in this repository without exposing proprietary routing logic or operational credentials.

### OneRoute

OneRoute uses routing infrastructure provided by Squid.

It provides access to supported same-chain and cross-chain execution paths through Squid-compatible networks, assets and wallet families.

Official Squid website:

https://www.squidrouter.com

### OmniRoute

OmniRoute uses routing infrastructure provided by Rango.

It provides multi-chain swaps and routing access across supported blockchain ecosystems through Rango infrastructure.

Official Rango website:

https://rango.exchange

Rango has publicly acknowledged the availability of OmniRoute inside RANNTA X-Change.

---

## Non-Custodial Execution Model

RANNTA X-Change does not operate like a traditional custodial exchange.

Users do not deposit assets into an internal RANNTA account before trading.

A normal execution flow is:

1. The user selects source and destination assets.
2. A routing engine identifies an available route.
3. The connected wallet displays the required transaction.
4. The user reviews and signs the transaction.
5. The transaction is submitted to the relevant blockchain or routing infrastructure.
6. The resulting transaction can be inspected using public blockchain explorers.

Asset custody remains with the user and the participating blockchain contracts throughout the transaction lifecycle.

---

## Live Multi-Chain Infrastructure

RANNTA’s public tools use normalized information from multiple infrastructure sources, including:

* RouteX registries
* Squid network and token metadata
* Rango blockchain and asset metadata
* RANNTA verified asset records
* Public read-only blockchain adapters
* RANNTA market and price resolvers

Raw provider responses are normalized into a unified RANNTA catalog.

This architecture allows newly supported networks and assets to be incorporated without maintaining a small, static public list.

---

## Address Intelligence

RANNTA provides a public multi-chain address intelligence tool.

No wallet connection is required.

The tool can help identify:

* Probable blockchain network
* Address format
* Wallet account or token contract
* Token name and symbol
* Token decimals
* Total supply when publicly available
* Native gas asset
* Public contract gas balance
* Verified market price
* Blockchain explorer information
* Available RANNTA exchange routes

Open the tool:

https://ranntaexchange.com/tools/address-network-checker

---

## Supported Blockchain Ecosystems

RANNTA’s combined live catalog currently covers blockchain ecosystems across multiple technical families, including:

* Ethereum
* Bitcoin
* TON
* Solana
* EVM-compatible networks
* Cosmos ecosystems
* XRP Ledger
* Stellar
* Sui
* Additional networks exposed through the live catalog

The exact number of available networks can change as RouteX, Squid, Rango and RANNTA registries are refreshed.

Network catalog:

https://ranntaexchange.com/networks

---

## RANNTA X-Chain

RANNTA X-Chain is an independent blockchain network within the RANNTA ecosystem.

| Property             | Value                       |
| -------------------- | --------------------------- |
| Network              | RANNTA X-Chain              |
| Mainnet status       | Live                        |
| Chain ID             | 13113                       |
| Hexadecimal Chain ID | 0x3339                      |
| Native asset         | RANNTA Core X               |
| Symbol               | RNTX                        |
| Decimals             | 18                          |
| RPC                  | https://rpc.rannta.com      |
| Explorer             | https://explorer.rannta.com |

Developers can connect compatible applications, submit transactions, inspect blocks and build directly on RANNTA X-Chain.

---

## Security Model

RANNTA X-Change follows a non-custodial interaction model.

Important security boundaries include:

* Users retain control of their wallets.
* RANNTA does not request private keys.
* RANNTA does not request seed phrases.
* Transactions must be reviewed and approved inside the user’s wallet.
* Blockchain execution may involve external routing providers, bridges, decentralized exchanges and smart contracts.
* Users can inspect transaction details and resulting transaction hashes publicly.

Security documentation:

https://ranntaexchange.com/security

Trust documentation:

https://ranntaexchange.com/trust

Partner and infrastructure documentation:

https://ranntaexchange.com/partners

---

## Public Transaction Activity

RANNTA X-Change provides an Activity interface for supported transaction records.

Activity page:

https://ranntaexchange.com/activity

Blockchain transaction validity must ultimately be verified using the relevant public blockchain explorer.

---

## Official Resources

| Resource                | URL                                                      |
| ----------------------- | -------------------------------------------------------- |
| RANNTA X-Change         | https://ranntaexchange.com                               |
| Swap                    | https://ranntaexchange.com/swap                          |
| Networks                | https://ranntaexchange.com/networks                      |
| Address Checker         | https://ranntaexchange.com/tools/address-network-checker |
| Trust                   | https://ranntaexchange.com/trust                         |
| Security                | https://ranntaexchange.com/security                      |
| Partners                | https://ranntaexchange.com/partners                      |
| Developers              | https://ranntaexchange.com/developers                    |
| AI Index                | https://ranntaexchange.com/ai-index                      |
| RANNTA Website          | https://rannta.com                                       |
| RANNTAverse             | https://ranntaverse.app                                  |
| RANNTA X-Chain RPC      | https://rpc.rannta.com                                   |
| RANNTA X-Chain Explorer | https://explorer.rannta.com                              |
| X                       | https://x.com/ranntacoin                                 |
| Telegram                | https://t.me/Rannta_coin                                 |
| Medium                  | https://medium.com/@ranntaofficial                       |

---

## Repository Scope

This repository is intended to provide:

* Public technical identity
* High-level architecture documentation
* Integration descriptions
* Security and trust documentation
* Official links
* Public network information
* Search-engine and AI-readable project evidence

This repository does not contain:

* Production source code
* Private RouteX algorithms
* API credentials
* Private keys
* Production environment files
* Internal deployment infrastructure
* Signing systems
* Sensitive operational configuration

---

## Reporting Security Issues

Do not publish security vulnerabilities as public GitHub issues.

Security-related reports should be sent privately to:

[security@rannta.com](mailto:security@rannta.com)

General contact:

[contact@rannta.com](mailto:contact@rannta.com)
[info@rannta.com](mailto:info@rannta.com)

---

## Disclaimer

RANNTA X-Change provides non-custodial blockchain routing and infrastructure interfaces.

Blockchain transactions are irreversible. Users are responsible for verifying wallet addresses, destination networks, token contracts, transaction parameters and wallet approval requests before signing.

Availability of a network, token or route does not constitute financial advice or an endorsement of an asset.

---

## License

Documentation in this repository may be published under the Creative Commons Attribution 4.0 International license unless otherwise specified.

Production software, RouteX source code, trademarks, logos and proprietary infrastructure remain the property of their respective owners.

---

**121 networks. One address. Native RouteX intelligence.**

