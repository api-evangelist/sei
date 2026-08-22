# Sei

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
