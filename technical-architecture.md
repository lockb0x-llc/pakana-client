Pakana Technical Architecture Document

Last updated: April 14, 2025

# 1. Overview

Pakana is a decentralized, programmable escrow and asset ownership platform built on Stellar, Soroban, and IPFS. It uses an ASP.NET Core Razor/Blazor frontend with a proprietary backend API stack (Pakana API, lockb0x API) to deliver secure, auditable workflows for rights assignment, lien waivers, payments, and metadata storage.

# 2. Core Components

Pakana is composed of the following primary subsystems:

- • ASP.NET Core Razor/Blazor frontend (open-source UI library)

- • Stellar Razor Components (drop-in UI abstractions for Stellar actions)

- • Stellar Identity Framework (role-based, multi-signature account identity extension)

- • Pakana API (Org/Project/Deliverable management, identity delegation, workflow automation)

- • lockb0x API (ZK-rollup, IPFS/IPNS metadata encryption and storage)

- • Stellar blockchain (account orchestration, multisig, lbx token escrow)

- • Soroban smart contracts (programmable ownership, escrow control, keeper failsafe logic)

- • Optional: Plaid financial API integration (for fiat anchoring & linked bank logic)

# 3. Data Model

Pakana organizes data hierarchically: Organizations own Projects; Projects create Deliverables; Deliverables are signed, managed, and tracked by assigned users. Each Deliverable has metadata, waiver state, and payment information linked to Stellar accounts.

# 4. Blockchain Integration

Pakana integrates with the Stellar blockchain using the Horizon SDK and custom Soroban contracts.
- Each Deliverable creates a multi-signature escrow account.
- lbx tokens represent funds or asset value.
- lockb0x stores signed waivers, hash-linked to Stellar memo fields.
- Soroban contracts enforce: milestone completion, payment conditions, and keeper logic.

# 5. Smart Contract Architecture

Soroban contracts include:

- • Mint Lock: Token issuance for unique IP/lien rights

- • Timelock: Schedule-controlled disbursements

- • Custom Account: Multi-party control and fallback logic

- • Keeper: Failsafe for dispute resolution or lost access

- • Events: Transparent metadata hash logging and emission

# 6. Identity & Security

Users are authenticated via OAuth and assigned roles (Org Manager, Project Manager, Clerk). Keys are managed client-side using AES-GCM encryption and never stored unencrypted. All signed transactions are generated in-browser or via wallet integrations.

# 7. Deployment Architecture

Pakana is hosted on Azure with:
- Azure App Services for Razor App
- Azure Functions for lockb0x + API endpoints
- Azure PostgreSQL for metadata persistence
- IPFS daemon clusters and private pinning services
- Optional: Azure Front Door CDN + DNS for high availability
- KeyVault + App Configuration for secret and environment control

# 8. Extensibility

The front-end is modular and open-source. Third parties can:
- Extend Razor components
- Use Pakana APIs with scoped OAuth keys
- Fork and customize workflows or Soroban contract logic
- Integrate with external identity, payments, or legal systems
