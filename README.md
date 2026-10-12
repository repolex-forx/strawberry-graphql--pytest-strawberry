# Repolex Knowledge Graph of strawberry-graphql/pytest-strawberry

RDF knowledge graph data for [strawberry-graphql/pytest-strawberry](https://github.com/strawberry-graphql/pytest-strawberry), parsed by [repolex](https://repolex.ai).

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
rlex download strawberry-graphql/pytest-strawberry
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 27ad06477d283255d7b7c40e2f2de12f1c01dafc
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 27ad06477d283255d7b7c40e2f2de12f1c01dafc
│           └── chunk-001.nq.gz
├── blob
│   ├── 02fea44117a3495666663795b315e67ec4a58b90.nq.gz
│   ├── 1756aba62ed44c2b69f46b600d3e03846f5b9f6e.nq.gz
│   ├── 1bcd5ed7238d1739fa6b2ed4203c1a7f2a177681.nq.gz
│   ├── 35e22413175b69872b7461d016f561056cc63a12.nq.gz
│   ├── 36f833a5ee32b094a2e3f2a9019f3aa239eacb1b.nq.gz
│   ├── 3705e74af4080276e68be0232993da255c749ba9.nq.gz
│   ├── 489f58c599a77e8b29e33b2f87ff12efde7124f6.nq.gz
│   ├── 559fcf1fdee415281c44185d6e08bc6c47ea7cc8.nq.gz
│   ├── 5e648c1d2924104f99457d2ca5a04ac78688a6e2.nq.gz
│   ├── 5f633eca088d69ef514c7826fb3bd6f52e375f14.nq.gz
│   ├── 7773c237f68627fb4ec4688968045d15c8cbd2e8.nq.gz
│   ├── 7bac97dba7ab20a7de49355ce198856f833fec5f.nq.gz
│   ├── 96253315bbbb8ac1e612879055cfc4ff0291c13c.nq.gz
│   ├── 992be2876e4b99a2e5871a1b3fae61533422143f.nq.gz
│   ├── a0fa77480ae68f04a1c6a4728b78a2eec8c080c8.nq.gz
│   ├── a25d3751a9ffc1b599c23362cc548c9d17acd2bc.nq.gz
│   ├── b28f8a895d97ffb5a47f11c36df98d38cefce46b.nq.gz
│   ├── b9370a6c3c4875e0931293a11576fcbbc46a04d1.nq.gz
│   ├── c17149e0ced9ef4e9b6780e7847ff6f5ca5b024f.nq.gz
│   ├── c63224e5fdd8e35706598a08f8017455fa6377e3.nq.gz
│   ├── c6481d5f740462ec9fd3edcb32aa56806e316c77.nq.gz
│   ├── d2f2adb9f3a19bdbe59a7bd5bda9d157401b5879.nq.gz
│   ├── e1648ca7be94572a908773351bb578c90340db4b.nq.gz
│   ├── e702f80ffd187f6216ba82d88238c320b5303c37.nq.gz
│   ├── eff0d5d834bb20051f52ca330a44737eb818b1e8.nq.gz
│   └── febcc66067bff5582a9001fed2a45a2fa5859022.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 27ad06477d283255d7b7c40e2f2de12f1c01dafc.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 33 files
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

[strawberry-graphql/pytest-strawberry](https://github.com/strawberry-graphql/pytest-strawberry)

---
*Parsed on 2026-10-12 by [repolex](https://repolex.ai)*
