# Repolex Knowledge Graph of prettier/html-event-attributes

RDF knowledge graph data for [prettier/html-event-attributes](https://github.com/prettier/html-event-attributes), parsed by [repolex](https://repolex.ai).

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
rlex download prettier/html-event-attributes
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── d13b4f0050fa97f7733f2884b6ce5e8a61210aea
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── d13b4f0050fa97f7733f2884b6ce5e8a61210aea
│           └── chunk-001.nq.gz
├── blob
│   ├── 026de7a1429d1f19c6cfb06c4534232846b3032e.nq.gz
│   ├── 0967ef424bce6791893e9a57bb952f80fd536e93.nq.gz
│   ├── 4a76439c74d81849fe54758fd1487be64b0227e1.nq.gz
│   ├── 502fce0c050a6c965118bd5f80888c2c09e56f79.nq.gz
│   ├── 5aff0365ddcafd2bf9dc21ad4e71233468d0a016.nq.gz
│   ├── 5e4ab772476c839b13a888ed881a9c6a79f8baa1.nq.gz
│   ├── 6313b56c57848efce05faa7aa7e901ccfc2886ea.nq.gz
│   ├── 659b1af31d3217bfbbb97f4963ae6d3809b0d109.nq.gz
│   ├── 7b9752edeb616e07be51279d9b1be0fbdb010675.nq.gz
│   ├── e751d20a772babd939c0025a64d5347cee683876.nq.gz
│   ├── f5ba945f2225384050c7461b44e2151e2a804410.nq.gz
│   ├── f9064696ace88292e2c0cb66b489d5441be8bdf1.nq.gz
│   ├── f9c9f9f83b9b2a0339fa35ad73eb267036dcb82d.nq.gz
│   ├── f9ef6c311192e604b115994e43e9889b940c5faf.nq.gz
│   └── fff7c5ffd010d8d1f4e3decfd4783cca6aa61ade.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── d13b4f0050fa97f7733f2884b6ce5e8a61210aea.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 23 files
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

[prettier/html-event-attributes](https://github.com/prettier/html-event-attributes)

---
*Parsed on 2026-11-10 by [repolex](https://repolex.ai)*
