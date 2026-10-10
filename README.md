# Repolex Knowledge Graph of aio-libs/async-lru

RDF knowledge graph data for [aio-libs/async-lru](https://github.com/aio-libs/async-lru), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download aio-libs/async-lru
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 639c403a266d99d223c649cb00fddaf40f371c85
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 639c403a266d99d223c649cb00fddaf40f371c85
│           └── chunk-001.nq.gz
├── blob
│   ├── 0628e146bc60cd7a20848bc1c6a1cf5fc7046f2d.nq.gz
│   ├── 0f5d8c0174adba76fdc71d773580413cae78ed52.nq.gz
│   ├── 1e7a3269f534931ba0810c5ed8acf01fc0f0c6ee.nq.gz
│   ├── 23f845d2cea8e56c5875b902f11df77a66bc7661.nq.gz
│   ├── 24acc9ca6e20bcf27e51cc9cf97fb0f4db20d51e.nq.gz
│   ├── 392af3f676ac0ec79b4ba180b73ce9260590608c.nq.gz
│   ├── 45e7ab27f9cdcce5249dc062fb66c64ecc3a3d94.nq.gz
│   ├── 469cca90b96b66dd834850184a9d24a863855824.nq.gz
│   ├── 4a08a9a1250883235f2d6b258d423245cfb05fb2.nq.gz
│   ├── 4c865a3cc0a907d37531ebd2818f3b34586fa1e6.nq.gz
│   ├── 52ed33b8d6a9f9cac5146ef7c152514dc1aad272.nq.gz
│   ├── 586c72e019ab6e16da57a736fe7a1f6521fb47aa.nq.gz
│   ├── 5d34f9a36eea7f1fb971ad6c14623d3c99cf526d.nq.gz
│   ├── 6160874f73dde490e898bfa6dc324d77cef5c798.nq.gz
│   ├── 62c8dc38d8d140daaf41db210bdb3ed1c854b766.nq.gz
│   ├── 695935cc42396a16dfacbed61544fa5df7bed997.nq.gz
│   ├── 6c65b46c625bff54955d135c658c2c171e6414e5.nq.gz
│   ├── 6da0785ea9e2e0e3a608de7c1168701d663ce014.nq.gz
│   ├── 6e03ffcd9f3ac0f531490ca683fa9573c371c012.nq.gz
│   ├── 70cd98ae79b255b10164fed53edcd5d17e935e14.nq.gz
│   ├── 8910ebbf8b2b68c02a85b9f0ebf897edf6a6ddcc.nq.gz
│   ├── 8caecc806661b30c507090045a9afa7b4a7dea0b.nq.gz
│   ├── 97b89b01f600f63d1044695765f98f0028cd1763.nq.gz
│   ├── 9d9c6a688c27d8657b29dab511666ba5a27dfc80.nq.gz
│   ├── aeee671c5234c51e26bcd7d1a5d65049bdcb0ea7.nq.gz
│   ├── b024da80e9c1c8c800cc1b46e90c1e783cb446cc.nq.gz
│   ├── b27fcd5d8bd64b63720efab81fb57e8983661c58.nq.gz
│   ├── b7c6e329ef8005c243be733d066b4d019e9510a6.nq.gz
│   ├── b909fa7b19fb29cc0bd2fbf2e86961478100c2b3.nq.gz
│   ├── b9fb8a6e0f4a5ce99899eb97d872c6b90f4bb678.nq.gz
│   ├── bb92a5f1e4c8e39668723a610ee537b604889add.nq.gz
│   ├── c85d5cb81ff105215fde07e265d2a7abac29dbc3.nq.gz
│   ├── da2d50f990916ca7d4317b20679bce6ccc8a967b.nq.gz
│   ├── de55d5c5574288c1fadad1c78a768b87ad85e2fd.nq.gz
│   ├── e5bb8dc2b27b44b7e1586bf84c080684c1e02996.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f070356c225a461331144f8cd7f654098fb9aaaf.nq.gz
│   ├── f38937fbb18841b9e6338887d2653c2f0fdbd001.nq.gz
│   └── faf758a6e5edc15435d5e116e2cd8aaac2e0c128.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 639c403a266d99d223c649cb00fddaf40f371c85.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 47 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[aio-libs/async-lru](https://github.com/aio-libs/async-lru)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*
