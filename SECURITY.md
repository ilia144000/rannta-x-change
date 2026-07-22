# Security Policy

## RANNTA X-Change Security Model

RANNTA X-Change is designed as a non-custodial blockchain interface.

Users retain control of their wallets and approve transactions through their selected wallet applications.

RANNTA X-Change does not request or store:

* Wallet recovery phrases
* Private keys
* Wallet passwords
* Custodial user balances

## Transaction Authorization

A valid blockchain transaction requires explicit authorization through the user’s wallet.

Users should verify:

* Source network
* Destination network
* Source asset
* Destination asset
* Recipient address
* Token approval amount
* Smart-contract address
* Estimated output
* Fees
* Wallet signature request

Connecting a wallet does not itself transfer assets.

Asset movement requires a blockchain transaction or token approval explicitly confirmed by the user.

## External Infrastructure

RANNTA X-Change may use independent routing and execution infrastructure, including:

* RouteX
* Squid
* Rango
* Decentralized exchanges
* Bridges
* Public blockchain RPC providers
* Blockchain wallet connectors

Each provider and blockchain protocol may have its own security assumptions and smart-contract risks.

## Reporting a Vulnerability

Do not disclose security vulnerabilities through public GitHub issues.

Send security reports privately to:

[security@rannta.com](mailto:security@rannta.com)

Include:

* Affected URL or component
* Technical description
* Reproduction steps
* Potential impact
* Screenshots or transaction hashes when relevant
* Suggested mitigation when available

Do not include private keys, recovery phrases or sensitive wallet credentials in a report.

## Official Domains

The official RANNTA infrastructure includes:

* https://ranntaexchange.com
* https://rannta.com
* https://ranntaverse.app
* https://rpc.rannta.com
* https://explorer.rannta.com

Users should verify the domain before connecting a wallet or signing a transaction.
