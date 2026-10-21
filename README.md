# Repolex Knowledge Graph of scikit-image/skimage-media

RDF knowledge graph data for [scikit-image/skimage-media](https://github.com/scikit-image/skimage-media), parsed by [repolex](https://repolex.ai).

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
rlex download scikit-image/skimage-media
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 4a9f764e4ed36902b5bd4668113ecef989c3772e
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 4a9f764e4ed36902b5bd4668113ecef989c3772e
│           └── chunk-001.nq.gz
├── blob
│   ├── 02603c1e1195f40af25c9f2bac0136012df86757.nq.gz
│   ├── 0320f5128b837a7a5130149329e1d75272393fb6.nq.gz
│   ├── 110d4e2b8304fa0e9c466a44690a9d25231178b8.nq.gz
│   ├── 1443ef46f9c65154d45e4307a7d2907af3ad1f22.nq.gz
│   ├── 1b12b4be3df44d6c6319140308ff5fccddbd0eac.nq.gz
│   ├── 1bd9e86f43254c96a3c9581ff9ee9e1629dcaab6.nq.gz
│   ├── 3ae5d0c1ba6afdacd3d7991fdfcc52d2aa9bb65b.nq.gz
│   ├── 45b1bd3d950c6b7e5494237e41ef1e6a46680b3c.nq.gz
│   ├── 502c2be25aedb84e78ed57e3ad3e8c35d02d462f.nq.gz
│   ├── 572c8960e4a9c54f7f4b8b8bee51eb52f8a15162.nq.gz
│   ├── 5ad5d195f6e3a52db51d5ab65094eb491b454c02.nq.gz
│   ├── 5fadd489b0a16732c811fa5b9e1c22a75a21f10c.nq.gz
│   ├── 66112a916d2050a42b77c719aab69a09574d2e28.nq.gz
│   ├── 9591fb1b4c050b89bf6a57f915fffbc8b713b4c0.nq.gz
│   ├── 965c4aadeb615591738e3a4d47d1f374319d4d33.nq.gz
│   ├── 9f622e54ef785eb22a7daa69a90043617bc8eeef.nq.gz
│   ├── a6e04319ce0f2954166d92558fe0c4b5c589df03.nq.gz
│   ├── a81ac20c3e9823943e3d02c86f493611fdc943a5.nq.gz
│   ├── d63a98c2af32025f1916a5705e27c54afd57a6ca.nq.gz
│   ├── dc2ec0241f0083231facf72d23684fb713f77d1d.nq.gz
│   ├── dccc8c2005be683d7f96277633cbd7a47f7c9409.nq.gz
│   ├── e03d8dd8bcf0d851fe1eb89f93a39de843e5c69c.nq.gz
│   ├── e06fb99f5b301e0f316d97ca77cd846736e07883.nq.gz
│   ├── e14b26761b03b5aaddc181d1afef880fe7f7a496.nq.gz
│   ├── ea6ff545a246caa64074ba809bbc86fcb8589071.nq.gz
│   └── efedb63f9786d777b29838c7e9aa85215ec3e5bc.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 4a9f764e4ed36902b5bd4668113ecef989c3772e.nq.gz
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

[scikit-image/skimage-media](https://github.com/scikit-image/skimage-media)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
