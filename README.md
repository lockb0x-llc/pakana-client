Pakana Client
Pakana Production Build — SCF Award Submission (Formatted for Web Form)

Overview

Pakana — a decentralized IP and asset ownership management platform that automates rights verification, contract signing, and conditional disbursements using Stellar. While Pakana leverages escrow and payment mechanisms, its true value lies in managing the creation, verification, and ownership transfer of intellectual property and real-world assets like construction liens, legal deliverables, and software project task or feature deliverables.

Pakana integrates our previously released open-source libraries (Stellar Razor Component Library, Stellar Identity Framework) and our proprietary lockb0x.io protocol, providing a secure metadata and data storage layer. It is purpose-built for legal professionals, property deverlopers, application developers, fiduciaries, and creatives who need provable, auditable flows for claim generation, settlement, and disbursement.



Once the inital software development is completed, for the production version of the Pakana platform, it will include:
- A decentralized IP and ownership flow platform built with .NET, Stellar, and IPFS
- Integration of previously released Razor Components and Stellar Identity Framework
- Integration of lockb0x.io — our enterprise-grade, ZK-rollup encrypted, IPFS-based metadata and decentralized document and media storage solution.
- Further integration with Plaid to mirror fiat bank account transactions to Stellar Ledger transactions and trigger fiat bank account transactions when approved on-chain.
- New Soroban smart contract functionality for automated rights management, verification, and programmable, contract-based disbursements
- A fully open-source Razor/Blazor client application extensible by third-party developers and compatible with public or private deployments
- A backend API and identity management system built on our proprietary Pakana and Lockb0x APIs

A litle more technical information:
Pakana tracks your deliverable from invitation to execution, storing cryptographic proof of contracts, waivers, and lien/copyright assignments, with automated payment triggers upon approval throughout your Organization's Project lifecycles. 
Pakana's design is predicated on the idea that tokens, escrow, and payments are downstream artifacts of the IP or Asset Creation Process that Pakana enables — ownership verification and transfer are the core result of implementing blockchain to upgrade these processes for the 21st Century, from invitation to execution. 
In short, Pakana give you the benefits of blockchain without the hassle and anxiety.

You can manage multiple Organizations and create mulitplt Projects under those Organizations, 

When live on Mainnet, Pakana will provide the follwoing features:
- Hierarchical Org → Project → Deliverable model
- Stellar multi-signature escrow system
- Payment request, waiver, and disbursement logic
- Browser-native AES-encrypted Stellar keypair vaulting
- ASP.NET Core Razor Pages interface
- lockb0x protocol for IPFS metadata anchoring
- Integration with Stellar Horizon SDK
- Support for Plaid-linked on-chain ledger support.

The Stellar blockchain is implemented in the these ways:
- Uses Stellar for multi-signature accounts and lbx token-based disbursement flows
- Escrow logic governed by transaction hash and waiver signatures
- lockb0x links ownership records to Stellar transactions via memo hash
  
Soroban smart contracts will be introduced to:
- Manage deliverable ownership assertions
- Verify contract milestones and fulfillment
- Automate self-custody mechanisms and disbursements
- Support asset tokenization and programmable payouts
- Implement a "keeper" function — a customizable failsafe mechanism that can move or reassign funds in multi-signature accounts under specific legal or off-chain conditions (e.g., disputes, lost keys, unmet deliverables verified by failed or missing github action events)

We will use and adapt Soroban smart contract patterns from the Stellar Developer Documentation:
- Custom Account — to manage multi-party authorization for Deliverables
- Timelock — to delay disbursements pending verification periods or lien waivers
- Atomic Swap — for trustless exchange of payment for signed deliverables or assets
- Mint Lock — to mint tokens representing unique IP claims or lien rights only after verification conditions are met
- Events — to emit transparent, auditable logs of signing, delivery, and disbursement events and lbx token-based disbursement flows
- Escrow logic governed by transaction hash and waiver signatures
- lockb0x links ownership records to Stellar transactions via memo hash

Target Audience
- Legal professionals managing IP, liens, and trust account flows
- Freelance developers and creatives asserting ownership over deliverables and transfer of their customer's Intellectual Property and/or Asset Rights after delivery and payment.
- Builders of white-label SaaS and tokenized ownership workflows
- Property developers, leasing, agents, multi-tenant property managers.
- Contractors and project managers in regulated industries such as construction contractors and tradesmen, municipal public works agencies and their contract awardees, government contractors, and various finance professionals. 

Development Team
Steven Tomlinson — Founder & Architect
30+ years of software experience. Creator of Pakana and the Stellar Razor Component ecosystem.

Josh Kassabian — Co-founder & Product Lead
UX/blockchain specialist with a focus on decentralized tooling. Co-creator of lockb0x and Pakana.


Additional Links
- https://github.com/lockb0x-llc/Pakana-Stellar-Razor-Components : Stellar Razor Components
- https://github.com/lockb0x-llc/Stellar-DotNet-Identity-Framework : Stellar Identity Framework
- https://www.lockb0x.io : lockb0x 
- https://communityfund.stellar.org/dashboard/projects/recXFpPXFBqyMWeZ8 : Stellar Community Fund Project Portfolio
