# Repolex Knowledge Graph of astral-sh/docstring-adder

RDF knowledge graph data for [astral-sh/docstring-adder](https://github.com/astral-sh/docstring-adder), parsed by [repolex](https://repolex.ai).

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
rlex download astral-sh/docstring-adder
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── e13d4bc0c83b223c329b357a84157a6deb6207a9
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── e13d4bc0c83b223c329b357a84157a6deb6207a9
│           └── chunk-001.nq.gz
├── blob
│   ├── 0158a2523d948658bd9aca55a37460b8be0bc00e.nq.gz
│   ├── 0dc8824876e22e69be9c1cc51fd35ba869b67759.nq.gz
│   ├── 0f12c6cc5e7aa27a5b30a0d98b54751ec487f8a1.nq.gz
│   ├── 18ae9a1eb6f383bae920faae616ebfda2933ba14.nq.gz
│   ├── 33a95cda389f7779956994e76602b8eda76e2d03.nq.gz
│   ├── 3e0ee0f3aa6372071a4673ac77325c226ddaf70d.nq.gz
│   ├── 5c46b768693e3afadd7f042eae816998d11c7a8f.nq.gz
│   ├── 729166b798daaf806432b6cfa8d6a6e4c5bd5237.nq.gz
│   ├── 87af87a23da24cdd9921158c559b7ce8cc5ad321.nq.gz
│   ├── 963f53ccc9188b8aac256a18a4fe55a2e4de9c4d.nq.gz
│   ├── a9a7f6080f5568ad1158516a5d4d649bd03d01ca.nq.gz
│   ├── b1fd5f0b170454b43fb521cadc6a40b85d9a055d.nq.gz
│   ├── e9ae7f9091d068f3ff6f6b759581dc1e42fd686f.nq.gz
│   ├── f0589c849763cef036079a049bf607a2b080dd28.nq.gz
│   └── f752786e56a2ffb73ab984aed1385ed68bf9e1aa.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── e13d4bc0c83b223c329b357a84157a6deb6207a9.nq.gz
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

[astral-sh/docstring-adder](https://github.com/astral-sh/docstring-adder)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*
