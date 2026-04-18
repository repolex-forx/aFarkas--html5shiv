# Repolex Knowledge Graph of aFarkas/html5shiv

RDF knowledge graph data for [aFarkas/html5shiv](https://github.com/aFarkas/html5shiv), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download aFarkas/html5shiv
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── ed28c56c071bddfe7d635ad88995674957a016be
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── ed28c56c071bddfe7d635ad88995674957a016be.nq.gz
│   └── repolex
│       └── ed28c56c071bddfe7d635ad88995674957a016be
│           └── chunk-001.nq.gz
├── blob
│   ├── 0806680af3600857fbd27eb4ad62fa1eec620bb8.nq.gz
│   ├── 085708e7d69a7f61969b4623c3b8a94e3af7db51.nq.gz
│   ├── 0900cd921e0b8b0c75b81a521c788c75fff3606e.nq.gz
│   ├── 0a4de90a2587709b93a9e7c0b13fd82c6988cfe8.nq.gz
│   ├── 1218a46cb7cd2b2d5c080a91a39f7062abeeb937.nq.gz
│   ├── 156cd5eccba6bbdeec99446b1aa49371d9f84aa8.nq.gz
│   ├── 208c6ee6f321ea6de4d8e3ff8bd16702585e6372.nq.gz
│   ├── 2125666142eb661091cc5f32af2ed2f3fc65571d.nq.gz
│   ├── 28c988a7b57ceb71481a1e6f6d0b580277aec63c.nq.gz
│   ├── 2e3dc9ea3aadb13fa94f50104a5f2c8e2ec4a0e3.nq.gz
│   ├── 45ea723dd58206fe80a847b259b035927dcd7623.nq.gz
│   ├── 4ae846563ed49d32fe30aa66c683ec062e38705c.nq.gz
│   ├── 52e8c9c11dac759853e1a7b00bfd78f24b4fe448.nq.gz
│   ├── 5814f00bfe61eb9898c0f9a37669bb3412bc6230.nq.gz
│   ├── 5a6f56142be9957cf19929ecb38e7a2c850e1668.nq.gz
│   ├── 5d55d4729fb62b9e7564fe7b93b2cc56a2bf146e.nq.gz
│   ├── 69f492dcc8cbdbd04a0d0f55dd882631d272d18a.nq.gz
│   ├── 6b4a9e0e3cdf3c2c58af6148a018168da5018d0b.nq.gz
│   ├── 6d2a8a7b8abccaaac6e29a723fec2b3238182d63.nq.gz
│   ├── 6d8dfaa25e8581c92c5582a7e53cee4b167978c9.nq.gz
│   ├── 8727016b0866b98214db9ed233e1f9ea550c45aa.nq.gz
│   ├── 87b10f163a8f441ff0012d670de013520b1254a7.nq.gz
│   ├── 91dfed8d4a8b9288b24b1b683fca652c4ff266fa.nq.gz
│   ├── a9538ee4ee865ce48a5707cd5b3d906b1819b274.nq.gz
│   ├── aeda2433bf941108e04c88bd0109d88195479cee.nq.gz
│   ├── afd77b1150ac162ba68402663f7299e0ae53ad3a.nq.gz
│   ├── b8f225140246c182fc414ac6936f0f86754a7c3b.nq.gz
│   ├── bcd3a974e7633c21ed47d5f16f33b5abc41a5b51.nq.gz
│   ├── bcecc4c0daf92a00f11e24d922c23e36d9ecca3f.nq.gz
│   ├── bdfbcac9a62e782a8791fc8e37c36ca516408770.nq.gz
│   ├── d3e4b4e40a949620186c59fdf199779dd8bced52.nq.gz
│   ├── e4f5049f5600de188f37ef3a1b3aa87417d05d16.nq.gz
│   ├── f4b7790da07bce5364f95a74157a69dbf1024ce8.nq.gz
│   └── f69e58bdcac7343fd222b2642933a8f764b99904.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── ed28c56c071bddfe7d635ad88995674957a016be.nq.gz
├── filetree
│   └── ed28c56c071bddfe7d635ad88995674957a016be.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 44 files
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

## Source repository

[aFarkas/html5shiv](https://github.com/aFarkas/html5shiv)

---
*Parsed on 2026-04-18 by [repolex](https://repolex.ai)*
