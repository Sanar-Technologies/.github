# Sanar Technologies

Building developer tools that make complex workflows simple.

## What We Build

**Sanar** is an internal developer platform and automation suite that connects AI agents to internal systems. The ecosystem includes:

- **TypeScript Core** — Primary runtime and CLI for orchestration
- **Python Sidecar** — Automation bridge exposing orchestrator primitives
- **Rust Native Core** — High-performance runtime with prompt caching, workflow execution, and security primitives
- **Forge** — FFI binding generator and parser for cross-language interoperability
- **Axon** — High-performance messaging bus for service communication

## Repositories

| Repository | Description | Status |
|------------|-------------|--------|
| [sanar](https://github.com/sanar-technologies/sanar) | Developer platform & automation suite | Active |
| [forge](https://github.com/sanar-technologies/forge) | FFI binding generator and parser | Active |
| [axon](https://github.com/sanar-technologies/axon) | High-performance messaging bus | Active |

## Quick Start

```powershell
# Clone and bootstrap (Windows)
git clone https://github.com/sanar-technologies/sanar.git
cd sanar
.\scripts\dev\bootstrap.ps1
```

The bootstrap automatically installs all dependencies via [mise](https://mise.jdx.dev) — Node, Python, pnpm, Rust, and more.

## Daily Commands

```bash
mise run dev      # Start development
mise run build    # Build everything
mise run test     # Run all tests
mise run lint     # Lint everything
```

## Links

- [Contributing](./.github/CONTRIBUTING.md)
- [Security Policy](./.github/SECURITY.md)
- [Code of Conduct](./.github/CODE_OF_CONDUCT.md)
