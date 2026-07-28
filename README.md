## Jim Counter

Engineer and engineering leader, twenty five years in. Currently Head of Ecosystem at
[Autonomys](https://github.com/autonomys), which in practice means splitting my week
between architecture, code review, and explaining systems to the people who have to use
them.

### Building

- [`autonomys/auto-sdk`](https://github.com/autonomys/auto-sdk) - the TypeScript SDK for
  the Autonomys Network, used by every external developer building on it. Fourth-ranked
  contributor, 197 commits.
- [`autonomys/auto-drive`](https://github.com/autonomys/auto-drive) - decentralised
  content-addressed storage. Primary reviewer on the storage and publishing services.
- [`subspace/autonomys-beneficiary-verification`](https://github.com/subspace/autonomys-beneficiary-verification) - React 19 and polkadot.js app that writes a versioned, replay-protected account
  association on chain. Live at
  [beneficiary.subspace.foundation](https://beneficiary.subspace.foundation).
- [`autonomys-unlock-tracker`](https://github.com/jim-counter/autonomys-unlock-tracker) -
  a dependency-free static dashboard that resolves staking positions at build time via
  polkadot.js and refreshes on a daily Action.

### Infrastructure

Devops is a part of the job I find engaging and satisfying.
[`autonomys/infra`](https://github.com/autonomys/infra) is Terraform IaC for the whole
network across AWS and Cloudflare: mainnet, Chronos testnet and devnet, reusable modules
for consensus, domain and farmer nodes, chain indexers and alerting, Infisical-backed
secrets, Packer AMIs, and a VictoriaMetrics, Loki and Traefik observability stack.
Everything goes through PR review before it goes near production.

Day to day that also means RabbitMQ, PostgreSQL, Docker Compose deployment profiles and
Ansible on the Auto Drive services.

### Reviewing

A fair chunk of my week goes on review now, and I think that's where the interesting problem is
moving as more code gets generated than gets read. I tend to review against a local checkout with
the suite running rather than just reading the diff. Some examples of what that turns up:

- [auto-drive #794](https://github.com/autonomys/auto-drive/pull/794) - blocked a queue
  isolation change because the new publish worker ignored the feature flag gating its
  predecessor, so hosts that publish nothing today would have quietly started signing.
- [auto-drive #797](https://github.com/autonomys/auto-drive/pull/797) - traced a
  non-idempotent insert against a primary key through to the conclusion that a slow
  upload becomes a permanently unrecoverable one.
- [auto-portal #125](https://github.com/autonomys/auto-portal/pull/125) - four rounds with
  a first-time contributor, including withdrawing one of my own earlier requests once the
  blast radius was clearer.

### Before this

Telecoms provisioning and billing for most of fifteen years at Tempest, Daisy and Alpha 9,
including work with Openreach on the WLR3 transition. Before that, share dealing platforms
and real-time market data integration at Thomson Financial. Mostly C# and SQL Server then,
mostly TypeScript now.

### Stack

TypeScript, React, Node, PostgreSQL, RabbitMQ, Terraform, AWS, Docker, Ansible,
polkadot.js, SubQuery. Twenty years of C#/.NET before that. Claude and Codex daily.
