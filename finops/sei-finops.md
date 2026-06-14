# Sei FinOps

## Overview

Sei is a public blockchain. API access costs are zero for public endpoints
(no subscription fees). The primary cost driver for developers building on
Sei is **on-chain gas fees** paid in SEI tokens for transaction execution.
Off-chain API querying (read-only calls) via public endpoints is free.

## Gas and Transaction Fees

### Fee Formula

```
Fee = Gas Price × Gas Used
```

The fee is capped at `Gas Price × Gas Limit`. Unused gas within the limit
is not fully refunded, so setting excessively high gas limits can result in
over-payment.

### Chain Parameters

- **Chain ID**: 1329 (pacific-1 mainnet), 1328 (atlantic-2 testnet)
- **Minimum gas price**: Enforced chain-wide to prevent spam
- **Block time**: ~400ms
- **Gas capacity**: 100 MGas/s
- **Consensus params endpoint**: `/consensus_params` (Tendermint RPC)

### Gas Estimation

Use `eth_estimateGas` (EVM JSON-RPC) to estimate gas before submitting
transactions. Blocknative's Gas API also provides real-time fee estimates
for Sei mainnet (chain ID 1329), available free with an API key at
https://docs.blocknative.com/gas-prediction.

## API Infrastructure Costs

### Free (Public Endpoints)

Public sei-apis.com endpoints incur no cost. Rate limit: 15 req/s per IP.

- No registration required
- No API key required
- Suitable for: development, testing, low-volume production reads

### Commercial RPC Providers

For production dApps with high query volume, teams pay infrastructure
providers rather than Sei directly.

| Provider    | Free Tier               | Paid Tier              |
|-------------|-------------------------|------------------------|
| RHINO       | 15 req/s public         | Enterprise (custom)    |
| Ankr        | Limited free credits    | Pay-per-use            |
| QuickNode   | 10M credits/mo (free)   | From ~$9/mo            |
| DRPC        | Free tier available     | Pay-per-use            |
| Nodies      | Free tier               | Custom pricing         |

### Self-Hosted Node

Running a `seid` full node eliminates per-query API costs but incurs
infrastructure expenses (server, storage, bandwidth):

- Estimated server cost: ~$50–200/mo (depending on provider and specs)
- Storage: grows with chain history; SSDs recommended
- Source: https://github.com/sei-protocol/sei-chain
- Docs: https://docs.sei.io/node

## Cost Optimization Tips

1. **Batch requests** where supported to reduce the number of round trips.
2. **Cache responses** for static data (block finality is ~400ms; immutable
   data never changes).
3. **Use `eth_estimateGas`** before transactions to set accurate gas limits
   and avoid overpayment.
4. **Minimize smart contract storage operations** — storage writes are the
   most expensive gas operations.
5. **Use fixed-size data structures** in contracts to reduce gas consumption.
6. **Avoid unnecessary computations** in contract logic.
7. **Upgrade to a dedicated endpoint** before hitting public rate limits to
   prevent failed requests and retry overhead in production.

## References

- Gas docs: https://docs.sei.io/learn/dev-gas
- Fee estimation: https://docs.blocknative.com/gas-prediction
- Node setup: https://docs.sei.io/node
- Chain registry (params): https://github.com/sei-protocol/chain-registry
