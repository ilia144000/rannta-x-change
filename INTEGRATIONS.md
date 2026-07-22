# RANNTA X-Change Integrations

## Scope

RANNTA X-Change integrates independent infrastructure while maintaining its own public product identity, interface, normalization layer, and native RouteX architecture.

Integration does not mean that RANNTA owns or controls an external provider. Each provider remains responsible for its own infrastructure, supported networks, contracts, APIs, route availability, and execution behavior.

## Squid / OneRoute

OneRoute is the RANNTA interface for routes backed by Squid infrastructure.

Public provider: https://www.squidrouter.com

Public integration boundary:

- Squid supplies supported routing and execution infrastructure.
- RANNTA supplies the public interface, product identity, catalog normalization, and surrounding utilities.
- Route availability depends on Squid's current supported infrastructure and downstream protocols.
- Transactions remain wallet-authorized and publicly verifiable on-chain.

## Rango / OmniRoute

OmniRoute is the RANNTA interface for routes backed by Rango infrastructure.

Public provider: https://rango.exchange

Public integration boundary:

- Rango supplies supported multi-chain routing and execution infrastructure.
- RANNTA supplies the public interface, product identity, catalog normalization, and surrounding utilities.
- Route availability depends on Rango's current supported infrastructure and downstream protocols.
- Transactions remain wallet-authorized and publicly verifiable on-chain.

## RouteX

RouteX is RANNTA's native architecture and is not a renamed copy of Squid or Rango.

RouteX is intended to normalize heterogeneous blockchain systems and progressively provide native routing, registry, planning, and developer-facing capabilities. Its complete implementation is private.

## Terminology

| RANNTA name | Meaning |
|---|---|
| RouteX | RANNTA native routing and normalization architecture |
| OneRoute | RANNTA interface using Squid infrastructure |
| OmniRoute | RANNTA interface using Rango infrastructure |

## No custodial implication

Provider integration does not create a custodial RANNTA account. Users authorize blockchain transactions through their own wallets.

## Time-sensitive data

Supported networks, assets, bridges, decentralized exchanges, wallets, and routes can change. The live RANNTA catalog and provider responses are authoritative for current availability.
