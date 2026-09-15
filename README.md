# Repolex Knowledge Graph of jshttp/http-errors

RDF knowledge graph data for [jshttp/http-errors](https://github.com/jshttp/http-errors), parsed by [repolex](https://repolex.ai).

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
lexq download jshttp/http-errors
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 61aee5769e92678ff25a2da8e3a2dd1504762432
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 61aee5769e92678ff25a2da8e3a2dd1504762432.nq.gz
│   └── repolex
│       └── 61aee5769e92678ff25a2da8e3a2dd1504762432
│           └── chunk-001.nq.gz
├── blob
│   ├── 17c705f6c72b975a5fdcc3ac26dc357479cefe1b.nq.gz
│   ├── 27aa832d7666c16b213c9288a4961a836d5dcc39.nq.gz
│   ├── 2d0891e930f67a78896fec42dc1930b1376ca9ac.nq.gz
│   ├── 3d81d265fce0e22b50480e292188d9d5b733fd7f.nq.gz
│   ├── 4b46d62ada7a01dc123d18a30dbcf1071b70ab0a.nq.gz
│   ├── 62562b74a3b5a79e82ca417b02e0f597d85f5e2f.nq.gz
│   ├── 7db9f16af3d24d6f85fc6bfcabdd5880c3832d1b.nq.gz
│   ├── 82271f6f5a843dcc944ee26ecd790e77152de1f6.nq.gz
│   ├── 82af4df54b4ce9aad915485c4660a0abab727a07.nq.gz
│   ├── 9808c3b2b6602da61eb4afcb4caf33368e3e2bd4.nq.gz
│   ├── 99485bbdc04d4b2eb1127e66c28ef5d8a9f759c3.nq.gz
│   ├── a8b7330b09582701c7f06f4b4e5a332b3481c55c.nq.gz
│   ├── ac783602e596b0b2f78336972eb466b98f07ac12.nq.gz
│   ├── c58268ad26e98c128bf936c8fd32c63453d23f82.nq.gz
│   ├── cf3015fb3b6ee818a7e76aff5854cde130fc5fe0.nq.gz
│   └── e73838f32a7fd15997fd05cad47a819b5c24ba9a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 61aee5769e92678ff25a2da8e3a2dd1504762432.nq.gz
├── filetree
│   └── 61aee5769e92678ff25a2da8e3a2dd1504762432.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 26 files
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

[jshttp/http-errors](https://github.com/jshttp/http-errors)

---
*Parsed on 2026-09-15 by [repolex](https://repolex.ai)*
