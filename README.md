## Jim Counter

Engineer and engineering leader, twenty five years in. Currently Head of Ecosystem at
[Autonomys](https://github.com/autonomys), which in practice means splitting my week
between architecture, code review, and explaining systems to the people who have to use
them.

Fourth-ranked contributor to
[`auto-sdk`](https://github.com/autonomys/auto-sdk) with 197 commits. Primary reviewer on
the [`auto-drive`](https://github.com/autonomys/auto-drive) storage and publishing
services. Terraform IaC for the whole network across AWS and Cloudflare in
[`infra`](https://github.com/autonomys/infra), which is a part of the job I find very
satisfying.

### Reviewing

A fair chunk of my week goes on review now, and I think that's where the interesting problem is
moving as more code gets generated than gets read. I tend to review against a local checkout with
the suite running rather than just reading the diff. Some examples of what that turns up:

- [auto-files-gateway #170](https://github.com/autonomys/auto-files-gateway/pull/170) -
  approved a fix that repaired already-corrupted file metadata, then asked whether we
  should be validating on upload instead, since a workaround that leaves us unable to
  trust our own stored metadata causes problems elsewhere later. The upload-side
  validation shipped as a follow-up in the SDK.
- [auto-drive #788](https://github.com/autonomys/auto-drive/pull/788) - flagged that
  stored object metadata had no meaningful size bound, where real S3 rejects anything over
  2 KB, and that everything inside Node's header budget was being persisted to jsonb and
  replayed on every GET. The author pointed out my proposed guard covered only one of the
  three write paths and generalised it into a single shared validator, which was a better
  fix than the one I asked for.
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
