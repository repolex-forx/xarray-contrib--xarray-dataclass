# Repolex Knowledge Graph of xarray-contrib/xarray-dataclass

RDF knowledge graph data for [xarray-contrib/xarray-dataclass](https://github.com/xarray-contrib/xarray-dataclass), parsed by [repolex](https://repolex.ai).

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
rlex download xarray-contrib/xarray-dataclass
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── a4890916239acce02e41985750960d7285ac745c
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── a4890916239acce02e41985750960d7285ac745c
│           └── chunk-001.nq.gz
├── blob
│   ├── 1176164d0e2270d711ae42d983bee1e957005c12.nq.gz
│   ├── 1363477304366609abff2476a9f8556a3fde9169.nq.gz
│   ├── 22a2d64c1a8b6fb3813e910bfa4b225e9aff1a12.nq.gz
│   ├── 2894adc3fe509a0b834d06cd2a006a879a742c69.nq.gz
│   ├── 2f53db087418d85df137e55e114df186fd57b27e.nq.gz
│   ├── 2fa9e6b641a80efe6033ec4b0e8da1198d6ba799.nq.gz
│   ├── 41b25644ae090e72fdf97073054664e1a8d39074.nq.gz
│   ├── 445f99dab878558f17a8c540c5e0a851bd181294.nq.gz
│   ├── 450b9d804e45645e99b6d7bbb7fa7d0bf7186c04.nq.gz
│   ├── 4924f9fdfe730de86c60f539d7aeb6e529a072fd.nq.gz
│   ├── 587eb1407e6d27a108033454bd5dacc5f77af750.nq.gz
│   ├── 590d9dea736b33f5c428876e0c340154fdeb5374.nq.gz
│   ├── 5b75ddd78ea31fb72e2b5af28a6b7554e2053128.nq.gz
│   ├── 8730848dc3eb431ec07b54cb213b81c94286187c.nq.gz
│   ├── 8a9741cc32b949ed2cd7a60029d74902b797355b.nq.gz
│   ├── 8f109fc291333a95f30bf5d876b24bef68db9064.nq.gz
│   ├── 91d4c1364b0b0439d32b3816dd4e8bc4302eecc4.nq.gz
│   ├── 978f239fdde1315c34451bdb52f7b4889cf56255.nq.gz
│   ├── 9f4bd2ff5cae7e53d4380062fc1e21f9b72b1ff1.nq.gz
│   ├── a820ecddfa84d48808229bab89c2a3272903d4c1.nq.gz
│   ├── aaed3918d35107acea9377dc21cd4b9c3841b6ef.nq.gz
│   ├── abc824216ee919359b37165b8f38a94aa926c0a5.nq.gz
│   ├── bf6146cdee6fd45d838e006cffa5c36395e3dd74.nq.gz
│   ├── bf89cc51d788263b066a30b5d6719867bc55b003.nq.gz
│   ├── ce782c12d32c97de2555cd14f818639269d3b6ed.nq.gz
│   ├── e10c2ed0b72479ceba087eba549984510506ca1e.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── ff4c347cafb1f1534a36083fc2a38bc8802213f7.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── a4890916239acce02e41985750960d7285ac745c.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 36 files
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

[xarray-contrib/xarray-dataclass](https://github.com/xarray-contrib/xarray-dataclass)

---
*Parsed on 2026-10-28 by [repolex](https://repolex.ai)*
