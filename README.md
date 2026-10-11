# Repolex Knowledge Graph of litestar-org/dtos

RDF knowledge graph data for [litestar-org/dtos](https://github.com/litestar-org/dtos), parsed by [repolex](https://repolex.ai).

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
rlex download litestar-org/dtos
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 2ddd4a6cf4455421e03ec61e907891ce24048272
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 2ddd4a6cf4455421e03ec61e907891ce24048272
│           └── chunk-001.nq.gz
├── blob
│   ├── 01e3c54bab1c9f8a7b73988845cdd4ca77b404fa.nq.gz
│   ├── 15c2afa93fbc2c0942a25cae503dc24c7f93df99.nq.gz
│   ├── 2399cf917837e8811dd839874b9671d39f38cc2d.nq.gz
│   ├── 2e641f85b2091a69fd12a24d2bd1cacb8d7aad2c.nq.gz
│   ├── 307af6f033c4e7e8c6cfe80fead6b810bb8ca6ac.nq.gz
│   ├── 35628fcb3b427dd782b7a95ac258b7efce8d0473.nq.gz
│   ├── 425522f1fcc7ec2158accd9f1ff10172bb185a44.nq.gz
│   ├── 4f3b3ba35bce2754aa77efdf4d34f8aa73cb4e84.nq.gz
│   ├── 63bc24a41649e9e74c2093fd2787be0a3e2a49a3.nq.gz
│   ├── 6891e54b6bd480e31756fb3c956e136b89b02b0e.nq.gz
│   ├── 6d8f21122453435f2e8761c889b0749ec636fd3c.nq.gz
│   ├── 6de1357b09035f4a706950f46db8ac8e52c7c591.nq.gz
│   ├── 702655c5ff733c73882a3a988bc892d7711014ac.nq.gz
│   ├── 732cf5095a6e76b768c198cc4c321cc6e3623514.nq.gz
│   ├── 7544b1867d34b257147d5e41b754e24a3225c605.nq.gz
│   ├── 7f0cee9e3b1e4da9e7ebd0f54da62c22a6ae211d.nq.gz
│   ├── 8702f73aef60c13e91986f34d3b9d2af30049ff3.nq.gz
│   ├── 9092bc1199253a1f0ed954218e298c26d6ab3bf9.nq.gz
│   ├── 91b019de8862babee1691e840ff4d6f21f44350c.nq.gz
│   ├── 9505c63bd6f3a629897d428c9ab82dc9fb15946a.nq.gz
│   ├── 9690daf0cc8346f95343909ab84da66cd6ffeeb8.nq.gz
│   ├── a3c98e09941b3fc870e0c688d587ebf091e272ba.nq.gz
│   ├── a504dfbc3ba7c5297e07e84ba5c0292c2398f54e.nq.gz
│   ├── ac46473a3b576b64f71471f72fc3054127030549.nq.gz
│   ├── b289f2eb5b950a12d896c823e654755cc75387e4.nq.gz
│   ├── b4ad7b7b424205b877db1c399d6a4985a9538c13.nq.gz
│   ├── bbd440e7a11cd492aeadbc4fe999f354366866df.nq.gz
│   ├── c19f76a7cd0c8aa9ea89028226fe303643eaecd3.nq.gz
│   ├── c1a2aea7b06f0aee40bdbd2b75a8d6119814c931.nq.gz
│   ├── d0a7a44246b5cc4cf8de4f32577c5cfa91cc11e8.nq.gz
│   ├── d29dd919f47b74bee536186cdd9b9aac9fb7c048.nq.gz
│   ├── d9eccc0249883f7230f417d2584901932cd95224.nq.gz
│   ├── dbaadcac2fab47e032f4098f0f678cde0cc82486.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── edf0c2d2fd17adf6a66e19c1f493a068b9d2bbcc.nq.gz
│   ├── ef1921377e37dd8397e89bced757f91fd0a63fc7.nq.gz
│   ├── f0edee036dc7ce071d714888154487eee3f3dc2b.nq.gz
│   ├── f4f5d1c291462ec21a7cfa9f69229d575390af94.nq.gz
│   └── fc998c9e3c7761b65d3964648955ab3cd0f187cb.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 2ddd4a6cf4455421e03ec61e907891ce24048272.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 46 files
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

[litestar-org/dtos](https://github.com/litestar-org/dtos)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
