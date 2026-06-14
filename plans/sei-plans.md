# Sei API Plans

Sei is a public blockchain. Its EVM JSON-RPC and Cosmos REST (LCD) APIs are
available through community-operated public endpoints and commercial RPC
infrastructure providers. Sei itself does not sell API plans directly; access
tiers are determined by the infrastructure provider chosen.

## Public Endpoints (No API Key Required)

Sei's official public endpoints are operated by RHINO (sei-apis.com) and are
free to use with no registration or API key.

| Tier    | Cost | Rate Limit        | Notes                        |
|---------|------|-------------------|------------------------------|
| Public  | Free | 15 req/s per IP   | Mainnet and testnet available |

**Mainnet (pacific-1, Chain ID 1329)**
- EVM JSON-RPC: `https://evm-rpc.sei-apis.com`
- EVM WebSocket: `wss://evm-ws.sei-apis.com`
- Cosmos REST:   `https://rest.sei-apis.com`
- Tendermint RPC:`https://rpc.sei-apis.com`
- gRPC:          `grpcs://grpc.sei-apis.com:443`

**Testnet (atlantic-2, Chain ID 1328)**
- EVM JSON-RPC: `https://evm-rpc-testnet.sei-apis.com`
- Cosmos REST:  `https://rest-testnet.sei-apis.com`
- Tendermint RPC:`https://rpc-testnet.sei-apis.com`

**Devnet (arctic-1)**
- EVM JSON-RPC: `https://evm-rpc-arctic-1.sei-apis.com`
- Tendermint RPC:`https://rpc-arctic-1.sei-apis.com`

## Commercial / Dedicated Plans

For production workloads requiring higher throughput, teams can use commercial
RPC providers with dedicated node access.

| Provider     | Free Tier | Paid Plans Starting At | Notes                        |
|--------------|-----------|------------------------|------------------------------|
| RHINO        | Yes       | Custom / Enterprise    | Operates sei-apis.com infra  |
| Ankr         | Yes       | Pay-per-use            | https://www.ankr.com         |
| QuickNode    | Yes       | From ~$9/mo            | https://www.quicknode.com    |
| DRPC         | Yes       | Pay-per-use            | https://drpc.org             |
| Nodies       | Yes       | Custom                 | https://nodies.app           |
| Lavender.Five| Yes       | Custom                 | https://lavenderfive.com     |
| 1RPC         | Yes       | Custom                 | https://1rpc.io              |
| Pocket Network| Yes      | Custom                 | https://pokt.network         |
| Allnodes     | Yes       | Paid node hosting      | https://www.allnodes.com     |

## Running Your Own Node

Developers may also run a `seid` node for unlimited self-hosted access:
- Source: https://github.com/sei-protocol/sei-chain
- Docs:   https://docs.sei.io/node

Default listening ports:
- REST (LCD): 1317
- Tendermint RPC: 26657
- P2P: 26656
