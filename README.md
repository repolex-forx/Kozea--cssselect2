# Repolex Knowledge Graph of Kozea/cssselect2

RDF knowledge graph data for [Kozea/cssselect2](https://github.com/Kozea/cssselect2), parsed by [repolex](https://repolex.ai).

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
rlex download Kozea/cssselect2
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── fc22accd5fdba764d95263fa8e6c97ce24f75f3e
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── fc22accd5fdba764d95263fa8e6c97ce24f75f3e
│           └── chunk-001.nq.gz
├── blob
│   ├── 03c8cf8cd9faecf2e1b0d3a009c62fd8f09050bb.nq.gz
│   ├── 1fe17d64245f478fac823e8d3edf8ea4e2b8bcce.nq.gz
│   ├── 22107ee32262c937b306d5097fd50ec62a10dfa0.nq.gz
│   ├── 284a4d2fd8b4e3859686110b54c78b34e1148c19.nq.gz
│   ├── 325f58c9467f589ce0e2bffdb01fbf1a4a8084a8.nq.gz
│   ├── 3c618f2fc41fadeeef0feb09a2081a4df46aaa24.nq.gz
│   ├── 3f5a9170a5a7cbeabc2d46c3d190582af7aea694.nq.gz
│   ├── 405f68b7885da8d48cfb7a12b8fae8f8eb9e3a27.nq.gz
│   ├── 40ac48d826b83ac20f67556c5048f96f180366c0.nq.gz
│   ├── 507bf242221d66043daa5c8eee27d3f5db7d1a11.nq.gz
│   ├── 520a431b122dba66bd2310534be4df9062fd5a11.nq.gz
│   ├── 5672211ecda5d6b1de6fb25cc765e74846e3af65.nq.gz
│   ├── 6a1505e31e677eedf9a6bdbf2735acbed8fe6249.nq.gz
│   ├── 78a92561a173921561d5cd559e7c44766ea78133.nq.gz
│   ├── a7a2ee3e6e94d924c7925a3683619b10def9054d.nq.gz
│   ├── b7a8085526853d5b1ce7ca94a6caf047a1522434.nq.gz
│   ├── bcc3106fcde1e7b3fbb4229ea816dd0b9a77a7cf.nq.gz
│   ├── c6ca1a246c1828c741338a04170b4307c1ca920a.nq.gz
│   ├── d0107d64b0852288ea8cb75289576c0d211210a9.nq.gz
│   ├── d1106d665e35b485dbb25b977e98618fa947e36d.nq.gz
│   ├── d5910edd16c6b7905181bb24f378a3a12481eaeb.nq.gz
│   ├── d8c6cd0fd8e7c5483112aa334e8db3b838c1433a.nq.gz
│   ├── deb6346e9291f40e7e7062f5703a02f5f3c6b306.nq.gz
│   ├── deb6e1c9dee6a7a3235eff1c749be8bb7f7db2ba.nq.gz
│   ├── eb070df76759db77a94a03e81849a1a28d704ab1.nq.gz
│   └── ecfce978450c5ec1b8a879da6114e8848bdc12a9.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── fc22accd5fdba764d95263fa8e6c97ce24f75f3e.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 34 files
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

[Kozea/cssselect2](https://github.com/Kozea/cssselect2)

---
*Parsed on 2026-10-28 by [repolex](https://repolex.ai)*
