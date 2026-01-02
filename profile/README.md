# Sanar Technologies

Building developer tools that make complex workflows simple.

## What We Build

**Sanar** is an internal developer platform and automation suite that connects AI agents to internal systems. The ecosystem includes:

| Component | Description | Tech Stack |
|-----------|-------------|------------|
| **Lattice** | Code intelligence engine with semantic search, AST parsing, and code navigation | Rust, tree-sitter |
| **Forge** | FFI binding generator for cross-language interoperability | Rust |
| **Axon** | Neural-speed messaging bus with sub-50μs latency | Rust, io_uring |
| **Sanar Desktop** | Local-first AI workspace application | Flutter, Rust |

## Repositories

| Repository | Description | Version |
|------------|-------------|---------|
| [lattice](https://github.com/Sanar-Technologies/lattice) | Code intelligence & semantic search engine | 0.5.0-alpha |
| [forge](https://github.com/Sanar-Technologies/forge) | FFI binding generator (Rust, TypeScript, Python, Go, Cap'n Proto) | 0.1.0 |
| [axon](https://github.com/Sanar-Technologies/axon) | High-performance messaging infrastructure with LLM Gateway | 0.1.0 |
| [desktop](https://github.com/Sanar-Technologies/desktop) | Cross-platform desktop workspace app | 0.1.0 |

## Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                     Sanar Desktop                           │
│                  (Flutter + Rust FFI)                       │
└─────────────────────┬───────────────────────────────────────┘
                      │
          ┌───────────┴───────────┐
          ▼                       ▼
┌─────────────────┐     ┌─────────────────┐
│     Lattice     │     │      Axon       │
│  Code Intel     │     │   Messaging     │
│  AST · Search   │     │  LLM Gateway    │
└────────┬────────┘     └────────┬────────┘
         │                       │
         └───────────┬───────────┘
                     ▼
          ┌─────────────────┐
          │      Forge      │
          │  FFI Bindings   │
          │ TS·Py·Go·Cap'n  │
          └─────────────────┘
```

## Tech Highlights

- **Lattice**: Tree-sitter parsing, RocksDB storage, SIMD-accelerated similarity search
- **Forge**: Custom IDL with code generation for 5 target languages, incremental compilation
- **Axon**: io_uring + eBPF networking, Cap'n Proto serialization, built-in chaos testing
- **Desktop**: Flutter + Rust bridge, local SQLite, cross-platform (Windows, macOS, Linux)

## Quick Start

```powershell
# Clone and bootstrap (Windows)
git clone https://github.com/Sanar-Technologies/desktop.git
cd desktop
flutter pub get
cargo build --release
```

## Links

- [Contributing](./.github/CONTRIBUTING.md)
- [Security Policy](./.github/SECURITY.md)
- [Code of Conduct](./.github/CODE_OF_CONDUCT.md)
