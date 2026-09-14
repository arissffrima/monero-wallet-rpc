# monero-wallet-rpc

> daemon · subaddress · restore-height

[![Python 3.11+](https://img.shields.io/badge/python-3.11+-3776AB)](https://python.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Build](https://img.shields.io/badge/build-passing-brightgreen)]()

Monero wallet-rpc shell — stub daemon ping, labeled subaddresses.

## Features

- HD derivation along m/44'/128'/0' for XMR
- Passphrase-wrapped vault stored as local JSON
- Deterministic address codec (SHA-256 simulation, no live keys)
- Fee estimator with low / medium / high presets
- Balance sync against a stub RPC client
- Click CLI with vault, account and portfolio commands

## Prerequisites

- Python 3.11+
- Git

## Getting Started

```bash
git clone <repo-url>
cd monero-wallet-rpc
python -m pip install -e .
python -m xmrpc --help
```

## CLI Usage

```bash
xmrpc create-vault --name "Main"
# Create an encrypted local vault

xmrpc list-vaults
# List vault files in the storage directory

xmrpc add-account --label Savings
# Derive the next HD account

xmrpc sync
# Refresh stub balances

xmrpc balance
# Print account table

xmrpc portfolio
# Show coin + stub USD total
```

## Project Structure

```
xmrpc/
  crypto/          seed, derive, address
  chain/           stub RPC and fee table
  storage/         vault JSON
  services/        wallet + sync
  cli.py           click entry
tests/             pytest
```

## Configuration

Defaults live in `xmrpc/config.py` (`WalletConfig`).

| Setting | Default | Description |
|---------|---------|-------------|
| `network` | `mainnet` | mainnet / testnet |
| `rpc_endpoint` | `http://127.0.0.1:18082` | XMR node URL (unused in stub mode) |
| `storage_dir` | `.wallets` | Local vault directory |
| `derivation_path` | `m/44'/128'/0'` | BIP path |

## Tests

```bash
python -m pytest -q
```

## Background

XMR Python ops search wallet-rpc, not monero-wallet again.

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.


---

## Topics

![monero](https://img.shields.io/badge/monero-111827?style=flat-square) ![wallet](https://img.shields.io/badge/wallet-111827?style=flat-square) ![rpc](https://img.shields.io/badge/rpc-111827?style=flat-square) ![monero-wallet-rpc](https://img.shields.io/badge/monero%20wallet%20rpc-111827?style=flat-square) ![cryptocurrency](https://img.shields.io/badge/cryptocurrency-111827?style=flat-square) ![blockchain](https://img.shields.io/badge/blockchain-111827?style=flat-square) ![web3](https://img.shields.io/badge/web3-111827?style=flat-square) ![bitcoin](https://img.shields.io/badge/bitcoin-111827?style=flat-square)

`monero` `wallet` `rpc` `monero-wallet-rpc` `cryptocurrency` `blockchain` `web3` `bitcoin` `ethereum` `hd-wallet` `open-source` `python`

Search: monero-wallet-rpc · daemon · subaddress · restore-height · Monero wallet-rpc shell — stub daemon ping, labeled subaddresses.

---

<sub>Monero wallet-rpc shell — stub daemon ping, labeled subaddresses.</sub>
