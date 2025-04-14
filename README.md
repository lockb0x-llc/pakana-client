# Pakana Client

The **Pakana Client** is the front-end user interface for interacting with the Pakana platform — a decentralized system for managing asset ownership, escrow-based contracts, lien waivers, and IP verification. Built with ASP.NET Razor and Blazor, it is modular, extensible, and built to interface with the Pakana API and lockb0x.io for encrypted metadata management.

---

## 🌐 Features

- Role-based identity and authentication using the Stellar Identity Framework
- Stellar multi-signature wallet integration (via Stellar Razor Components)
- Modular Razor/Blazor UI for managing:
  - Organizations
  - Projects
  - Deliverables
  - Payment Requests and Waivers
- Integration with lockb0x for secure ZK-encrypted IPFS metadata storage
- Ready for Soroban smart contract integration
- OAuth-based scoped API access
- Support for encrypted Stellar keypair vaulting

---

## 🚀 Getting Started

### Prerequisites

- [.NET 8 SDK](https://dotnet.microsoft.com/download)
- Node.js (for optional asset bundling)
- PostgreSQL database
- Pakana API + lockb0x.io instance or endpoint
- Stellar Horizon access (public or private)

### Running the Client Locally

```bash
git clone https://github.com/lockb0x-llc/pakana-client.git
cd pakana-client
dotnet run
```

---

## 🔐 Security

All secret keys are managed client-side using browser-native AES-GCM encryption. No unencrypted keys are stored or transmitted.

---

## 📦 Project Structure

```
/Pages         → Razor Pages and UI logic
/Components    → Reusable UI components (Razor)
/Services      → API, KeyVault, and Stellar integrations
/wwwroot       → Static assets
/_Imports.razor → Global namespaces
Program.cs     → App configuration
```

---

## 🔧 Environment Variables

Create a `.env` file or configure your launch profile for:

```
PAKANA_API_URL=https://api.pakana.net
LOCKB0X_API_URL=https://api.lockb0x.io
STELLAR_NETWORK=TestNet
```

---

## 🧩 Related Repositories

- [Stellar Razor Components](https://github.com/lockb0x-llc/Pakana-Stellar-Razor-Components)
- [Stellar Identity Framework](https://github.com/lockb0x-llc/Stellar-DotNet-Identity-Framework)
- [lockb0x.io](https://github.com/lockb0x-llc/lockb0x)

---

## 📄 License

This project is licensed under the MIT License. Custom APIs and lockb0x components may be proprietary.

---

## 🤝 Contributing

PRs welcome. Please fork the repo and open a pull request against `dev`.

---

## 🧠 About Pakana

Pakana enables decentralized, legally-aware contract automation for real-world assets, IP, and escrow-based collaboration. From legal firms and developers to fiduciaries and builders, Pakana provides programmable trust for the 21st century.
