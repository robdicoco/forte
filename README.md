# Forte Wallet

<!-- <img src="./docs/image/forte_base.png" alt="Forte Wallet Banner" width="240" height="240" /> -->



A secure, non-custodial cryptocurrency wallet. Forte is built on a foundation of robust cryptography and mathematical principles to create a fortified vault for your digital assets, without compromising on usability.


## Forte in Motion
Experience the secure, rhythmic core of Forte.


<!-- [![Forte Wallet Animation](https://img.youtube.com/vi/t2t-exXxvBA>/hqdefault.jpg)](https://www.youtube.com/embed/t2t-exXxvBA) -->

<!-- [<img src="https://img.youtube.com/vi/t2t-exXxvBA/hqdefault.jpg" width="600" height="300"
/>](https://www.youtube.com/embed/t2t-exXxvBA) -->

[<img src="./docs/image/forte_play.png" width="400" height="400"
/>](https://www.youtube.com/embed/t2t-exXxvBA)



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

### Phase 0: Requirements Definition & Scoping 📝

- [x] **October 2025 - February 2026**: Requirements Gathering & Planning
  - [x] Define target users & threat model
  - [x] Identify primary use cases (key management, wallet functionality, secure signing)
  - [x] Audit competitor landscape (security model, usability, features)
  - [x] List minimum viable product (MVP) features

#### **MVP Feature Set**
- [x] In-memory, non-custodial key management
- [x] BIP39 seed/phrase generation
- [x] Secure transaction signing (Ethereum base support)
- [x] WASM-powered Rust core
- [x] Chrome/Edge browser extension support
- [x] Minimal React-based wallet UI

#### **Future/Optional Features**
- [ ] Multi-chain support (Solana, Cosmos, etc.)
- [ ] Hardware wallet integration
- [ ] Multi-sig and co-signing workflows
- [ ] Transaction simulation and risk diagnostics
- [ ] Browser push notifications and dApp connectivity
- [ ] Plugin architecture for extensibility
- [ ] Zero-knowledge proofs & post-quantum crypto options


### Phase 1: Foundation & Security Core ✅
- [x] **October 2025**: Rust cryptographic core development
  - [x] Secure key generation & management
  - [x] BIP39 seed phrase implementation
  - [x] Transaction signing engine
- [x] **November 2025**: WebAssembly compilation pipeline
  - [x] WASM bindings for JavaScript
  - [x] Memory-safe cryptographic operations
  - [x] Core security audit

### Phase 2: Browser Extension & UI 🚧 (Current)
- [ ] **December 2025**: TypeScript extension framework
  - [ ] Chrome extension manifest v3
  - [ ] Edge compatibility layer
  - [ ] React component library
- [ ] **January 2026**: Wallet functionality
  - [ ] Account management interface
  - [ ] Transaction signing UI
  - [ ] Network connectivity (Ethereum JSON-RPC)

### Phase 3: Enhanced Security & Features 🔄
- [ ] **February 2026**: Advanced security features
  - [ ] Hardware wallet integration (Ledger, Trezor)
  - [ ] Multi-signature support
  - [ ] Transaction simulation & risk analysis
- [ ] **Post-February 2026**: User experience
  - [ ] Portfolio tracking & analytics
  - [ ] Cross-chain compatibility (EVM, Solana, Cosmos)
  - [ ] Browser notification system

### Phase 4: Ecosystem & Scale 🌟
- [ ] **Post-February 2026**: Platform expansion
  - [ ] Mobile companion app (React Native + Rust core)
  - [ ] Developer API for dApp integration
  - [ ] Plugin system for custom functionality
  - [ ] Formal verification of critical components

### Phase 5: Future Research 🔬
- [ ] **Later 2026+**: Next-generation security
  - [ ] Zero-knowledge proof integration
  - [ ] MPC (Multi-Party Computation) protocols
  - [ ] Post-quantum cryptography readiness
  - [ ] Decentralized identity standards

## 🔒 Security Audits

| Date | Scope | Auditor | Status |
|------|-------|---------|--------|
| Q4 2025 | Rust Cryptographic Core | TBD | Scheduled |
| Q2 2026 | Full Extension Suite | TBD | Planned |
| Q4 2026 | Smart Contract Integration | TBD | Planned |

## 🏗️ Architecture Overview

```
┌───────────────────────────────────────────────┐
│           Browser Extension                   │
│ ┌─────────────────────┐   ┌────────────────┐ │
│ │  React UI           │   │ Background     │ │
│ │  Components         │   │ Script (Tx     │ │
│ │                     │   │ Routing,       │ │
│ │                     │   │ Messaging)     │ │
│ └─────────▲───────────┘   └────────┬───────┘ │
│           │   ▲                     │         │
│           │   │     ┌───────────────▼──────┐  │
│           └───┼────►│     WASM Bridge     │  │
│               │      └───────────────▲────┘  │
│               │                      │        │
└───────────────┼──────────────────────┼────────┘
                │                      │
                ▼                      ▼
      ┌─────────────────────────────────────────────┐
      │              Rust Security Core             │
      │ ┌──────────────┬─────────────┬───────────┐  │
      │ │ Key Mgmt     │ Transaction │ Crypto    │  │
      │ │ & Vault      │ Signing     │ Primitives│  │
      │ └──────────────┴─────────────┴───────────┘  │
      └─────────────────────────────────────────────┘
```

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