# Repolex Knowledge Graph of nickoneill/PermissionScope

RDF knowledge graph data for [nickoneill/PermissionScope](https://github.com/nickoneill/PermissionScope), parsed by [repolex](https://repolex.ai).

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
rlex download nickoneill/PermissionScope
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 156eb08d1123b68a9f129e9780dcb73b20b894a5
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 156eb08d1123b68a9f129e9780dcb73b20b894a5
│           └── chunk-001.nq.gz
├── blob
│   ├── 004cd5b2cbc64eb36b5c83b73c55dbb9559223c8.nq.gz
│   ├── 06c40e3923c1ca6c820288269769308dd9b43961.nq.gz
│   ├── 093730e11ae36b40a21ead5a973941df7b406e9d.nq.gz
│   ├── 09667e10a838ed24cb7af20d9a69fe9803d9e8e2.nq.gz
│   ├── 097171a1da86cfe6a334fd9d2ae73d76002c39f6.nq.gz
│   ├── 0bd072754ad97258b81966f66c185cfbaa98a72e.nq.gz
│   ├── 1532d9956bbd3bd976441a126752c30b3aa049b7.nq.gz
│   ├── 153392509b7ff9d31e22f162acf1a6e505b54703.nq.gz
│   ├── 1b2cb5d6d09fe5019d2f930632eaa15b4e51aedc.nq.gz
│   ├── 31209bf2f7643e30fd264d1056395bcd7d2e80ca.nq.gz
│   ├── 3f8f33a8beadbf82d022cb75a8c7cb05e5056515.nq.gz
│   ├── 47e507c9c4ce875d456f6b98d90a3f5bbd022525.nq.gz
│   ├── 58029043b92858758ee09f4d1ca7aa2d5638f64b.nq.gz
│   ├── 580401ad5d603747265d73a9e1bc51104d865d16.nq.gz
│   ├── 587ce7c0ade767a83a54fb03b2f46e8c217ab5a6.nq.gz
│   ├── 5a0639c01ae7fa9f95c8b25f06492d7bf23bce4a.nq.gz
│   ├── 64b984a35fefba8b0b98a4f6f5f461f8f9ccf946.nq.gz
│   ├── 69429e1ab92161e97f9245b3bb95f02ea9e878e1.nq.gz
│   ├── 6a713638f3032b6668b41d7f38e4b87378788655.nq.gz
│   ├── 6adb5c82f4800218aaba9ee2f5b700f84174adfe.nq.gz
│   ├── 6b63e3f942a075e8802d81f393e33dcf854102d2.nq.gz
│   ├── 7b4adc203c470133ef6d4f5dbe65e32fff7d844b.nq.gz
│   ├── 8bebad0d2dea405959b3cd8d6384fb89c661c765.nq.gz
│   ├── 9af6da5059524086252d1ac23d3466cf6b19e43b.nq.gz
│   ├── a5cf0e7448f6db6fa7de0ff9560cabb0a70f1137.nq.gz
│   ├── abbe1e15bdedd1b7e45a383106e9c135077cfbb3.nq.gz
│   ├── bda5037e9d255e5dd7cb30786cc2d5debe79bb1a.nq.gz
│   ├── c3e2df5aa57db71447652e22c52b0312e94fdda2.nq.gz
│   ├── d03bf096ee6025a0f9097342c716d580f6be55a2.nq.gz
│   ├── d1313d2cce747d6f3b165aa4388501f09e40c3eb.nq.gz
│   ├── de945a0b15fff0e0ce073f982c64b5c0ab36ef9a.nq.gz
│   ├── df46f35c5a7eb2202270458581e9905028cb7435.nq.gz
│   ├── ef50d52acd8cb2d03451ec82f4e23f904f1bc1ef.nq.gz
│   ├── f06fa047e6d0f7589c8fce9b1546125cdd9b2a10.nq.gz
│   ├── f398a20612afa114338cf6fec4d5378e51473059.nq.gz
│   ├── f578aab93ebba910c74c5a5dc3f93ec732c4870d.nq.gz
│   ├── f6f6bae915dda44e0775a216fa4db5916d59ec6f.nq.gz
│   └── fb2eab9d36774f397c7545aa1774a2d1427b9ea8.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 156eb08d1123b68a9f129e9780dcb73b20b894a5.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 46 files
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

[nickoneill/PermissionScope](https://github.com/nickoneill/PermissionScope)

---
*Parsed on 2026-11-09 by [repolex](https://repolex.ai)*
