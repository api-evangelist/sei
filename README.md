# Sei

Sei is a high-performance Layer 1 blockchain optimized for trading and
decentralized exchange (DEX) applications. It is the first parallelized EVM
blockchain, delivering sub-second block times (~400ms), 100 MGas/s throughput,
and full Ethereum compatibility. Sei combines Twin Turbo Consensus, a
parallelization engine, and SeiDB for unmatched scalability.

## APIs

This repository contains an APIs.json 0.19 profile for Sei covering two
primary public API surfaces:

### 1. Sei EVM JSON-RPC API

Ethereum-compatible JSON-RPC API at `https://evm-rpc.sei-apis.com` (mainnet).
Supports the full Ethereum method set: sending transactions, querying balances
and code, block and transaction lookups, log filters, gas estimation, and
transaction tracing. Also includes Sei-specific cross-VM methods.

- Docs: https://docs.sei.io/evm/reference
- Chain ID: 1329 (mainnet), 1328 (testnet)

### 2. Sei Cosmos REST API (LCD)

Cosmos SDK REST (Light Client Daemon) API at `https://rest.sei-apis.com`
(mainnet). Exposes HTTP endpoints for bank, staking, governance, distribution,
minting, IBC, and Sei-native DEX module queries.

- Docs: https://docs.sei.io/cosmos-sdk/api

## Endpoints

| Network      | EVM JSON-RPC                          | Cosmos REST                     |
|--------------|---------------------------------------|---------------------------------|
| Mainnet      | https://evm-rpc.sei-apis.com          | https://rest.sei-apis.com       |
| Testnet      | https://evm-rpc-testnet.sei-apis.com  | https://rest-testnet.sei-apis.com|
| Devnet       | https://evm-rpc-arctic-1.sei-apis.com | https://rest-arctic-1.sei-apis.com|

Public endpoints: **free**, no API key required, rate-limited to 15 req/s.

## Resources

- Website: https://sei.io
- Documentation: https://docs.sei.io
- GitHub: https://github.com/sei-protocol
- Block Explorer: https://www.seiscan.app
- Discord: https://discord.gg/sei

## Repository Contents

```
apis.yml                                    # APIs.json 0.19 provider profile
plans/sei-plans.md                          # API access tiers and endpoint list
rate-limits/sei-evm-json-rpc-api-rate-limits.yml
rate-limits/sei-cosmos-rest-api-rate-limits.yml
finops/sei-finops.md                        # Gas costs and cost optimization
```
