# Polkadot Parachain Development Setup

[![Setup Test Status](https://github.com/brunopgalvao/set-up-a-template/actions/workflows/test-polkadot-setup-simple.yml/badge.svg)](https://github.com/brunopgalvao/set-up-a-template/actions/workflows/test-polkadot-setup-simple.yml)
![Rust ](https://img.shields.io/badge/Rust--orange.svg)
![Auto-Generated](https://img.shields.io/badge/README-Auto%20Generated-brightgreen.svg)

> **🤖 Fully Automated Setup**: This README and all instructions are automatically generated and tested by CI. Every command is guaranteed to work.

## Overview

This repository provides a complete, tested setup for Polkadot parachain development using:

- **Rust**:  (with WASM target)
- **Chain Spec Builder**: v  
- **Polkadot Omni Node**: v
- **Template**:  branch

All components are automatically tested together in CI on every change.

## Quick Start

Copy and paste these commands to get started immediately:

```bash
# 1. Install system dependencies (Ubuntu/Debian)


# 2. Install Rust and configure toolchain
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y
source ~/.cargo/env


# 3. Install Polkadot tools



# 4. Clone and build parachain template  

cd parachain-template


# 5. Generate chain specification


# 6. Start development node
polkadot-omni-node --chain ./chain_spec.json --dev
```

## Detailed Setup Instructions

### Prerequisites

**Ubuntu/Debian:**
```bash

```

**macOS:**
```bash
# Install Xcode command line tools
xcode-select --install

# Install Homebrew if not already installed
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Install dependencies
brew install cmake protobuf
```

**Windows:**


### Step 1: Rust Installation and Configuration

Install Rust and set up the toolchain exactly as tested in CI:

```bash
# Install Rust
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y
source ~/.cargo/env

# Configure toolchain (from CI)

```

**Platform-specific WASM target installation:**
```bash
# Apple Silicon Macs
rustup target add wasm32-unknown-unknown --toolchain -aarch64-apple-darwin
rustup component add rust-src --toolchain -aarch64-apple-darwin

# Intel Macs
rustup target add wasm32-unknown-unknown --toolchain -x86_64-apple-darwin
rustup component add rust-src --toolchain -x86_64-apple-darwin

# Linux (as used in CI)
rustup target add wasm32-unknown-unknown --toolchain -x86_64-unknown-linux-gnu
rustup component add rust-src --toolchain -x86_64-unknown-linux-gnu
```

### Step 2: Install Polkadot Development Tools

Install the exact versions tested in CI:

```bash


```

### Step 3: Clone and Build Parachain Template

```bash

cd parachain-template

```

### Step 4: Generate Development Chain Specification

```bash
# From parachain-template directory

```

This creates a `chain_spec.json` file configured for development with:
- Development relay chain: Paseo
- Parachain ID: 1000
- Runtime: Built from the parachain template

### Step 5: Start the Development Node

```bash
# From parachain-template directory
polkadot-omni-node --chain ./chain_spec.json --dev
```

## Verification

When everything is set up correctly, you should see output similar to:

```
🎉 All setup instructions completed successfully!
✅ Rust  installed and configured
✅ WASM target and rust-src added
✅ staging-chain-spec-builder@ installed
✅ polkadot-omni-node@ installed
✅ Parachain template cloned and built
✅ Chain spec generated
✅ Node can start with generated chain spec
```

The node will start producing blocks and you'll see log output indicating successful operation.

## Troubleshooting

### Common Issues

**Build Failures:**
- Ensure all system dependencies are installed
- Check that you have at least 8GB of RAM and 10GB free disk space
- Try `cargo clean` and rebuild if you encounter caching issues

**Toolchain Issues:**
- Verify Rust version: `rustup show`
- Ensure WASM target is installed: `rustup target list --installed`
- Check component installation: `rustup component list --installed`

**Network Issues:**
- Some downloads are large; ensure stable internet connection
- Corporate firewalls may block certain domains
- Try using a VPN if experiencing geographic restrictions

### Platform-Specific Notes

**macOS:**
- Requires Xcode command line tools
- May need to install additional dependencies via Homebrew
- Apple Silicon Macs use different toolchain targets

**Linux:**
- Ubuntu 20.04+ or equivalent is recommended
- Ensure `build-essential` package is installed
- Some distributions may require additional `*-dev` packages

**Windows:**
- WSL2 is strongly recommended over native Windows
- Native Windows support exists but is less tested
- Visual Studio Build Tools may be required for native builds

## Development Workflow

Once set up, your typical development workflow will be:

1. **Modify Runtime Code**: Edit files in `parachain-template/runtime/`
2. **Rebuild**: `cargo build --release`
3. **Update Chain Spec**: Regenerate if runtime changes affect genesis
4. **Restart Node**: Stop and restart with updated runtime
5. **Test**: Use Polkadot.js Apps or other tools to interact

## Resources

- **[Polkadot SDK Documentation](https://docs.substrate.io/)**: Official developer documentation
- **[Substrate Stack Exchange](https://substrate.stackexchange.com/)**: Community Q&A
- **[Polkadot Technical Chat](https://matrix.to/#/#polkadot-technical:matrix.org)**: Real-time developer support
- **[Parachain Template Docs](https://github.com/paritytech/polkadot-sdk-parachain-template)**: Template-specific documentation

## CI Status and Information

- **Latest Test Results**: [View CI Runs](https://github.com/brunopgalvao/set-up-a-template/actions/workflows/test-polkadot-setup-simple.yml)
- **Test Frequency**: Runs on every documentation change
- **Test Environment**: Ubuntu Latest with clean environment
- **Test Duration**: Typically 30-60 minutes

---

<details>
<summary>📋 CI Metadata</summary>

- **Generated**: 2025-08-12 20:58:18 UTC
- **From Commit**: db6818f
- **Workflow**: `Polkadot Setup Test`
- **Repository**: `brunopgalvao/set-up-a-template`
- **Auto-Generated**: This entire README is generated from CI workflow

</details>
