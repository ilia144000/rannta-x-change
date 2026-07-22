# RANNTA X-Change Public Architecture

## Purpose

This document describes the public architectural boundary of RANNTA X-Change. It intentionally excludes private source code, proprietary routing logic, credentials, signing systems, infrastructure topology, and deployment configuration.

## Architectural classification

RANNTA X-Change is a non-custodial multi-chain exchange interface with an independent multi-engine routing architecture.

The platform separates five concerns:

1. Public user interface and wallet interaction
2. Route discovery and execution planning
3. Network and asset normalization
4. Provider-specific execution infrastructure
5. Public transaction verification through blockchains and explorers

## Routing layer

### RouteX

RouteX is RANNTA's native routing and blockchain-normalization engine. Its public responsibilities include registry normalization, asset identity mapping, route intelligence, execution-plan design, and integration boundaries across heterogeneous blockchain families.

The production implementation is private.

### OneRoute

OneRoute exposes supported routing infrastructure from Squid through a RANNTA-controlled interface. Squid remains an independent provider and execution authority for routes that use its infrastructure.

### OmniRoute

OmniRoute exposes supported routing infrastructure from Rango through a RANNTA-controlled interface. Rango remains an independent provider and execution authority for routes that use its infrastructure.

## Data normalization layer

RANNTA combines and normalizes data from RouteX registries, provider catalogs, verified internal asset records, public blockchain adapters, and market resolvers.

Normalization prevents the public interface from depending on a small hardcoded list or exposing raw provider responses without RANNTA identity mapping.

## Wallet and custody boundary

RANNTA X-Change does not create a custodial balance for users. Users authorize transactions through their selected wallets. A wallet connection establishes an interaction session; it does not itself transfer assets.

Asset movement requires an explicit transaction or approval signed by the user and submitted to the relevant blockchain and provider infrastructure.

## Verification boundary

The final source of truth for a blockchain transaction is the relevant blockchain and its public explorer. RANNTA interfaces can display status and activity records, but users and third parties can independently verify transaction hashes on-chain.

## Private implementation boundary

The public repository does not expose:

- Production application code
- Private RouteX source code
- Route-selection algorithms
- Provider credentials
- Signing infrastructure
- Internal RPC routing
- Server topology
- Treasury operations
- Database schemas or operational telemetry
- Sensitive contract deployment configuration

## Current public endpoints

- Platform: https://ranntaexchange.com
- Swap: https://ranntaexchange.com/swap
- Networks: https://ranntaexchange.com/networks
- Address intelligence: https://ranntaexchange.com/tools/address-network-checker
- Trust: https://ranntaexchange.com/trust
- Security: https://ranntaexchange.com/security
- Partners: https://ranntaexchange.com/partners
- Developers: https://ranntaexchange.com/developers
- AI Index: https://ranntaexchange.com/ai-index
