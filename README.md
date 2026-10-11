# Repolex Knowledge Graph of pytest-dev/pytest-inline

RDF knowledge graph data for [pytest-dev/pytest-inline](https://github.com/pytest-dev/pytest-inline), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/pytest-inline
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── dbc8cb0bb4b005311cc408ba12abd8104b05c313
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── dbc8cb0bb4b005311cc408ba12abd8104b05c313
│           └── chunk-001.nq.gz
├── blob
│   ├── 1dd14b84aa91366a2acaea4ea986ce74032b27fc.nq.gz
│   ├── 42159384329ca4f6c9cf4395283c27da9710a972.nq.gz
│   ├── 4a0f4d727fd3526fe98cc548192deddcf0a08612.nq.gz
│   ├── 4c0f465edc75931c27e8160309bd2157751070ab.nq.gz
│   ├── 528d81d6b7a8c457e67fcd58dc1dca4768b450aa.nq.gz
│   ├── 5766542f56fc3266646047d98c3fe754123e0606.nq.gz
│   ├── 5b0b832f54b2de4551d41b48f4dc28c90862aba0.nq.gz
│   ├── 5c4cd320e9dd9f73aef0e50cb3ac4ae2dd013dcc.nq.gz
│   ├── 612bd9a85cb388520b07be8c3e2614f6fbd558a5.nq.gz
│   ├── 63f1894aad803755c5fbab7116747f7c9f643c0e.nq.gz
│   ├── 706e13b01b95378cab7e8c905fc411926b6d410c.nq.gz
│   ├── 70d1abe2e37de1946ad395e63c58fd264021c650.nq.gz
│   ├── 7bfed404f013c37d3be118400f60b8c153a96654.nq.gz
│   ├── 8143964124f2c6e550889c5afbba0a00f1a341b4.nq.gz
│   ├── 85ac2bbe97b38b110ca01130f639e257d2b60f07.nq.gz
│   ├── 89dff561afd81bbe482e9408f627d5e72e87d6b6.nq.gz
│   ├── 8e67c5d5a7202272d5eff179dab83385a7a773e5.nq.gz
│   ├── 90ac7311ce2db3e072afd207f370934a7582ba05.nq.gz
│   ├── 92757390122c4cffc29bba1aa19e21133188d098.nq.gz
│   ├── 953b61fe112397a643adbac2213bd229bd8a60a4.nq.gz
│   ├── 95f8b651ebdddffeb8ab2f1ef1392ff2e823a826.nq.gz
│   ├── a9bb10c088e7f97134f7ce9fb27958c4bcfa7125.nq.gz
│   ├── ae08656944983e1836a722a68ed5b516ba22e1c2.nq.gz
│   ├── b88fe36ce8739616f2cdef645e8c6143bf81092f.nq.gz
│   ├── bf450e7fe25a380da6f34fc903f025112aca764d.nq.gz
│   ├── c7a6c0292945a10198ae61c7d00311719a4689a2.nq.gz
│   ├── d5a01c9b4b5aa3c33fb4fd24404ef00369817365.nq.gz
│   ├── db7b3ee74bbcba1d62ee7cc61ffe3546c2661cb2.nq.gz
│   ├── de88e1b5f3822bc65ea7f613ca0397b75e5640d8.nq.gz
│   ├── e2d6112d291fe3ebc94ecfc34df899a9fcf12314.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── eae9b9367950be42099ae1d3066519d1c6a8716a.nq.gz
│   └── f55528c5a5afaa9388dfed017712b6109cbe4f9b.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── dbc8cb0bb4b005311cc408ba12abd8104b05c313.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 41 files
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

[pytest-dev/pytest-inline](https://github.com/pytest-dev/pytest-inline)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
