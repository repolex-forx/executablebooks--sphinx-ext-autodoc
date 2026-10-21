# Repolex Knowledge Graph of executablebooks/sphinx-ext-autodoc

RDF knowledge graph data for [executablebooks/sphinx-ext-autodoc](https://github.com/executablebooks/sphinx-ext-autodoc), parsed by [repolex](https://repolex.ai).

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
rlex download executablebooks/sphinx-ext-autodoc
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 5f04a3b36aa8279932b1c4733b9f9f9f27f942df
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 5f04a3b36aa8279932b1c4733b9f9f9f27f942df
│           └── chunk-001.nq.gz
├── blob
│   ├── 02eda4a8ff229e099cea33c68b98d58292ef7370.nq.gz
│   ├── 0cfa1a324bb721ace27b51efa6ccb170e051fb8b.nq.gz
│   ├── 112ab8e29c5b57f4051c9e17917d651431a4b285.nq.gz
│   ├── 1274f9132a13a59f2026374bcf9daa4fe4ab09d5.nq.gz
│   ├── 256ae2d7e524286d1af6fdd49176e6f924662e2f.nq.gz
│   ├── 282e17cb86138bd8eda8303670d0d7a4fcc032cc.nq.gz
│   ├── 29ffc88ece2c322d3b882d52eb2372bcb9fcee0a.nq.gz
│   ├── 3ca185ac0c637c2dc2c8b95e184cbd4b5b13d4b1.nq.gz
│   ├── 414302f675b8bbcd585c3ea2a63f7b752e3d8f87.nq.gz
│   ├── 527d9e2a04e092546fe33dd1ee657b4f507b0e01.nq.gz
│   ├── 5f485e522fa78676f9777d570856901a56a81773.nq.gz
│   ├── 61959eb6991ee93da2b468b1c752f63c6256d406.nq.gz
│   ├── 691945b406dba9e92b2acf134723a86c73a5d032.nq.gz
│   ├── 81a191e7afec69f5af4c39e8646deadf41481706.nq.gz
│   ├── 81fcf6ad0eb1762d571cbad3cd4a33896490c004.nq.gz
│   ├── 851867571ce601ed1749b600f71d9ee2d29de452.nq.gz
│   ├── 914a4f5a233dede578264860912339428c96a3e1.nq.gz
│   ├── 96a6fa5a1b9916332984076b3934577a411efbea.nq.gz
│   ├── a03068c22e8f6ae9743858271974159d216b3097.nq.gz
│   ├── a993d75ca3fb0c98bd161c68496ce18685efa91c.nq.gz
│   ├── acb867017e11bfa7c3bd4cb86fc82cc40733e97f.nq.gz
│   ├── b471e41a7ffa4df4f9cec25513e1dd12b2071cf1.nq.gz
│   ├── c30476658811637b4cdd2b170a9c078fa4127ace.nq.gz
│   ├── ce66abb1dae7d9a172aab80d085b4a5375f911da.nq.gz
│   ├── d05be2579c38c84b59c477335f733c3eea71c07a.nq.gz
│   ├── d073c86a9822fcce704c6c320b4d5420f5dda845.nq.gz
│   ├── d0fa394c87a34920cad3eac4c63fd0c3a4bb1886.nq.gz
│   ├── db3e396a37896c3256e10def7103532e38586709.nq.gz
│   ├── dff10096d6f079607be60a8b48e83627ca7b4e90.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e9b626cd9b918f72cc1f7f68ca54d04bf1558d96.nq.gz
│   ├── f098ac4c9669704ca715cc9c246e9ca4e9afcf58.nq.gz
│   └── f39568ed68df5e0c303c1cdffa3f9708d632057f.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 5f04a3b36aa8279932b1c4733b9f9f9f27f942df.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 40 files
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

[executablebooks/sphinx-ext-autodoc](https://github.com/executablebooks/sphinx-ext-autodoc)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
