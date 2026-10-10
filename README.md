# Repolex Knowledge Graph of honojs/create-hono

RDF knowledge graph data for [honojs/create-hono](https://github.com/honojs/create-hono), parsed by [repolex](https://repolex.ai).

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
rlex download honojs/create-hono
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── ebc2b41876302b9a03e6a69383ceff1844824090
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── ebc2b41876302b9a03e6a69383ceff1844824090
│           └── chunk-001.nq.gz
├── blob
│   ├── 0670e88bbac02e37a9f1372222fe7e3e4c11a4a7.nq.gz
│   ├── 166878b5efbe040aac7ef6d8ced0fe043a867e44.nq.gz
│   ├── 272b655f0f7ef414c03cee9ae41eb6bb83750917.nq.gz
│   ├── 3fd3f778e4d50ef87cb419b006c775c6d7159503.nq.gz
│   ├── 493b2702ee700be0161cfb4593d52e2ca5607b0d.nq.gz
│   ├── 647e8daa1832693c0893ddeabc8008e8595db25b.nq.gz
│   ├── 6904cfb4c03df9e335e89e68dbacbb2e3b47b6f6.nq.gz
│   ├── 6c458abaecb8f28aebb2830188d48d0c3939ace1.nq.gz
│   ├── 83cc223097c4455f77df96f5892c8725e299c3bb.nq.gz
│   ├── 882f4528b33512d3a525309a718d0cf5ff9bdf03.nq.gz
│   ├── 96c650b46246c823b75ffe7fe4ec33b99136d6eb.nq.gz
│   ├── 972d966a9a423d3edb4bc9cca92f9fdcc0410f43.nq.gz
│   ├── bf47309418a46ec66cfe7c453aedf16964f8d688.nq.gz
│   ├── c0524dadaa091f6fc9fa41d2aac44dfc21e72d62.nq.gz
│   ├── c3481a758517a7af9a3bb47336bb3c2258f01594.nq.gz
│   ├── c3bc6affc3ddb55161aed51f19902fb1b610ecc2.nq.gz
│   ├── cf63c6ab73f896645376f935d2e507c078ea7b59.nq.gz
│   ├── cffe8cdef132f31903a4971117f33f60cd9a56e6.nq.gz
│   ├── d8ef911f3b624a18cbae1faa5c054f9988e63f43.nq.gz
│   ├── ef5fe870097e67ac00b8b49334b3c1269592cce7.nq.gz
│   └── f0e4d72f4325af227a5652379f4d18a407a9d533.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── ebc2b41876302b9a03e6a69383ceff1844824090.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 29 files
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

[honojs/create-hono](https://github.com/honojs/create-hono)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*
