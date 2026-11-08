# Repolex Knowledge Graph of cohere-ai/htn-2025-techtalk

RDF knowledge graph data for [cohere-ai/htn-2025-techtalk](https://github.com/cohere-ai/htn-2025-techtalk), parsed by [repolex](https://repolex.ai).

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
rlex download cohere-ai/htn-2025-techtalk
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9cbf9068d942de171ac25a9dd77b3d46d54614f0
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 9cbf9068d942de171ac25a9dd77b3d46d54614f0
│           └── chunk-001.nq.gz
├── blob
│   ├── 1d9290cbfeed4dd6972c126eb1aef6a402e5ae26.nq.gz
│   ├── 39d3a5b897405ef67be3175b246ecce1d1d007e7.nq.gz
│   ├── 3b751565c0626f08612adad6ba8dcee2bfe9ecd6.nq.gz
│   ├── 56a2b1bda57abb4899d68562c136604b7d96c6b1.nq.gz
│   ├── 8f3505cfb738e68fef1fd82db810fd73046ce764.nq.gz
│   ├── 9a866ccb274e15f4a371ca31313941d7229bb581.nq.gz
│   ├── abadb5ede122573a8b5de23166976ad7ca621d1f.nq.gz
│   ├── c8cfe3959183f8e9a50f83f54cd723f2dc9c252d.nq.gz
│   ├── cdff847dbabea531c8c6c04792f7f7885872b80a.nq.gz
│   ├── d331c3089c8658208dceee43b3396c80bc789cb8.nq.gz
│   └── f529008c3c87556ee683e869e1efde746de1b209.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 9cbf9068d942de171ac25a9dd77b3d46d54614f0.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 18 files
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

[cohere-ai/htn-2025-techtalk](https://github.com/cohere-ai/htn-2025-techtalk)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
