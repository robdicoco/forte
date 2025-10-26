# Forte Wallet

<img src="./docs/image/forte_base.png" alt="Forte Wallet Banner" width="240" height="240" />



A secure, non-custodial cryptocurrency wallet. Forte is built on a foundation of robust cryptography and mathematical principles to create a fortified vault for your digital assets, without compromising on usability.


## Forte in Motion
Experience the secure, rhythmic core of Forte.

<iframe width="360" height="640" src="https://www.youtube.com/embed/t2t-exXxvBA" title="Forte Wallet Animation" frameborder="0" allowfullscreen></iframe>


> **Where Security is Our Strength**

## Features
- **Non-Custodial:** You own your keys.
- **Cryptographically Secure:** Leveraging industry-proven algorithms.
- **Intuitive Design:** Complex security, made simple.


## 🛡️ Technology Stack

Forte employs a hybrid architecture that isolates security-critical operations from the presentation layer, ensuring maximum protection without compromising usability.

### Core Architecture: Rust + TypeScript Hybrid

#### **Secure Core** (Rust 🦀)
- **Cryptographic Operations**: All private key management, signing, and encryption handled in memory-safe Rust
- **WebAssembly Compilation**: Core logic compiled to WASM for browser execution
- **Zero Runtime Exceptions**: Rust's ownership model prevents memory safety vulnerabilities
- **Key Libraries**:
  - `ring` - Cryptographically secure primitives
  - `serde` - Safe serialization/deserialization
  - `wasm-bindgen` - Seamless JavaScript interoperability
  - `bip39` - BIP39 seed phrase generation
  - `secp256k1` - Elliptic curve cryptography

#### **Presentation Layer** (TypeScript 🌐)
- **Browser Extension API**: Native Chrome & Edge extension support
- **React UI Framework**: Modern, component-based user interface
- **State Management**: Zustand for predictable state container
- **Build Tooling**: Webpack with Rust WASM compilation pipeline
- **Testing**: Jest + Playwright for comprehensive testin

### Security Foundation

| Layer | Technology | Security Benefit |
|-------|------------|------------------|
| **Memory Safety** | Rust Compiler | Eliminates buffer overflows, use-after-free, data races |
| **Cryptography** | ring/WebCrypto | Audited implementations, constant-time operations |
| **Isolation** | WebAssembly | Sandboxed execution environment |
| **Type Safety** | TypeScript | Catch errors at compile time |
| **Key Storage** | Encrypted in-memory only | Never persisted to disk |

## 🗺️ Development Roadmap

### Phase 1: Foundation & Security Core ✅
- [x] **Q1 2024**: Rust cryptographic core development
  - [x] Secure key generation & management
  - [x] BIP39 seed phrase implementation
  - [x] Transaction signing engine
- [x] **Q2 2024**: WebAssembly compilation pipeline
  - [x] WASM bindings for JavaScript
  - [x] Memory-safe cryptographic operations
  - [x] Core security audit

### Phase 2: Browser Extension & UI 🚧 (Current)
- [ ] **Q3 2024**: TypeScript extension framework
  - [ ] Chrome extension manifest v3
  - [ ] Edge compatibility layer
  - [ ] React component library
- [ ] **Q4 2024**: Wallet functionality
  - [ ] Account management interface
  - [ ] Transaction signing UI
  - [ ] Network connectivity (Ethereum JSON-RPC)

### Phase 3: Enhanced Security & Features 🔄
- [ ] **Q1 2025**: Advanced security features
  - [ ] Hardware wallet integration (Ledger, Trezor)
  - [ ] Multi-signature support
  - [ ] Transaction simulation & risk analysis
- [ ] **Q2 2025**: User experience
  - [ ] Portfolio tracking & analytics
  - [ ] Cross-chain compatibility (EVM, Solana, Cosmos)
  - [ ] Browser notification system

### Phase 4: Ecosystem & Scale 🌟
- [ ] **H2 2025**: Platform expansion
  - [ ] Mobile companion app (React Native + Rust core)
  - [ ] Developer API for dApp integration
  - [ ] Plugin system for custom functionality
  - [ ] Formal verification of critical components

### Phase 5: Future Research 🔬
- [ ] **2026+**: Next-generation security
  - [ ] Zero-knowledge proof integration
  - [ ] MPC (Multi-Party Computation) protocols
  - [ ] Post-quantum cryptography readiness
  - [ ] Decentralized identity standards

## 🔒 Security Audits

| Date | Scope | Auditor | Status |
|------|-------|---------|--------|
| Q3 2024 | Rust Cryptographic Core | TBD | Scheduled |
| Q1 2025 | Full Extension Suite | TBD | Planned |
| Q4 2025 | Smart Contract Integration | TBD | Planned |

## 🏗️ Architecture Overview

┌─────────────────────────────────────────────────┐
│ Browser Extension │
│ ┌─────────────┐ ┌──────────────────────────┐ │
│ │ React UI │ │ Background Script │ │
│ │ Components │ │ (Transaction Routing) │ │
│ └─────────────┘ └──────────────────────────┘ │
│ │ │ │
│ └────────────────────┘ │
│ WASM Bridge │
└─────────────────────────┬───────────────────────┘
│
┌─────────────────────────▼───────────────────────┐
│ Rust Security Core │
│ ┌─────────────┐ ┌─────────────┐ ┌─────────┐ │
│ │ Key Management │ Transaction │ │Crypto │ │
│ │ │ Signing │ │Primitives│ │
│ └─────────────┘ └─────────────┘ └─────────┘ │
└─────────────────────────────────────────────────┘

---

**Forte Wallet** - *Building trust through mathematical certainty.*

## Post-Graduation Project - NearX

This project is part of the [NearX](https://nearx.com.br/) Post-Graduation Program in Blockchain Technology, Tokenization, and Smart Contract Security.

### Participants

- Lucas Campos
- Thiago Pereira Dos Santos
- [Roberto Pavusa Junior](https://github.com/robdicoco)
- Vinicius Viana

---


## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guidelines](CONTRIBUTING.md) for details on:
- Security vulnerability reporting
- Code style and standards
- Testing requirements
- Pull request process


### See it on github pages

> https://robdicoco.github.io/forte/