# Repolex Knowledge Graph of python-trio/triopg

RDF knowledge graph data for [python-trio/triopg](https://github.com/python-trio/triopg), parsed by [repolex](https://repolex.ai).

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
rlex download python-trio/triopg
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 6575b2212aca2e86c5c91d9f39cf912b6dc40396
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 6575b2212aca2e86c5c91d9f39cf912b6dc40396
│           └── chunk-001.nq.gz
├── blob
│   ├── 0319110bd8d611ec3671a20b0944eba0946ea293.nq.gz
│   ├── 1531c9c9c566e73ec1a27e948db613f4ebe44d86.nq.gz
│   ├── 291bfeaa3b207e4173c50080f22cfb473363ee5a.nq.gz
│   ├── 29846284d31e111e1a09329a375ccbb1b7f8ef8f.nq.gz
│   ├── 2c71c9d662a8386fb39cb4c7d1bd35c67ea1275e.nq.gz
│   ├── 2eb582110df5777eb7a0feebd3ffdf30912ef5a0.nq.gz
│   ├── 31c3c9c64f1aae3314c1d3266f259da6ec444ed7.nq.gz
│   ├── 40b6800b55943cac723f9a0915b82688cd89d57c.nq.gz
│   ├── 46863783e32c608b70a5b33476c231300f69346b.nq.gz
│   ├── 47ad4b1d6f68df976d9c63307c411ebab7daa205.nq.gz
│   ├── 487560ee0eb17bb9d54209812ca6b3d0bdc774ce.nq.gz
│   ├── 4edd4b18b3f9a2893c3d0a37e5e747a5f09cebe7.nq.gz
│   ├── 5181ec2e6b44b185ff2ae4ee87c367270386095d.nq.gz
│   ├── 51f3442917839f8e0f0cccb52b3c10968ad0779e.nq.gz
│   ├── 556c317a01af54dbe401d6fa407d467e2c6e2988.nq.gz
│   ├── 5b1032a693a023c55f077ba3befd97150c746c23.nq.gz
│   ├── 62fe152f1b00cf138c749ee9b6fc7c01b46d328f.nq.gz
│   ├── 67898ba6f5cffa770a3110d8c996c8203cbbdc26.nq.gz
│   ├── 7c5406b5dfa061a13b117e326c45d8887343bc1c.nq.gz
│   ├── 7f82d7b65fad5d39a0fbb4ffcdb8858b71be5225.nq.gz
│   ├── 875b9400fc07395740255d5f67e6b4e8e1b77b90.nq.gz
│   ├── 88bc5940b4657e3c59c64551d1a931b33b70428c.nq.gz
│   ├── 89bba483a8cdba4883a1b68bdc76f328600e3e85.nq.gz
│   ├── 8a8c70bbcd865302e44f4c4ef6c6f8d409c5b958.nq.gz
│   ├── ae10048ba947c2958a7413860317e8038bf4689b.nq.gz
│   ├── b6be967ddf0e9b3c2915c5490e1b91eb739e99ac.nq.gz
│   ├── b8bb97185926d7daed314609753173945ed4ff1a.nq.gz
│   ├── d645695673349e3947e8e5ae42332d0ac3164cd7.nq.gz
│   ├── e39a41806f114e7b760e884477e04414fdcf3722.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 6575b2212aca2e86c5c91d9f39cf912b6dc40396.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 38 files
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

[python-trio/triopg](https://github.com/python-trio/triopg)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
