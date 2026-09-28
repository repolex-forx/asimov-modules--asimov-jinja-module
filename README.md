# Repolex Knowledge Graph of asimov-modules/asimov-jinja-module

RDF knowledge graph data for [asimov-modules/asimov-jinja-module](https://github.com/asimov-modules/asimov-jinja-module), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-modules/asimov-jinja-module
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── fc80359120b3a3fe4ab3d65dfd97430e026f7c13
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── fc80359120b3a3fe4ab3d65dfd97430e026f7c13.nq.gz
│   └── repolex
│       └── fc80359120b3a3fe4ab3d65dfd97430e026f7c13
│           └── chunk-001.nq.gz
├── blob
│   ├── 08c455665fcf832986b4357d0a73200c262b8578.nq.gz
│   ├── 105693260c084e6992596ad8661d7a6a29e19fb3.nq.gz
│   ├── 10b359dd05935c73efb064470f9ecda90f6d28aa.nq.gz
│   ├── 12a4ffd88d6d476472bd15476f371b671e454cc1.nq.gz
│   ├── 165231faabc5ee83295789304e389fe312647c3c.nq.gz
│   ├── 3c17d8c20cff2871eb4ff941cd94512c387561da.nq.gz
│   ├── 46d1c6c58f600b96dbc4cecab7a06eaafce34194.nq.gz
│   ├── 60a467ff52e5f17dfd46e7d683e9fbc51691cf66.nq.gz
│   ├── 655fe848a9c90af3d8b9551a384e1cda12f94efa.nq.gz
│   ├── 6b23d61018f43b840f8d2ff3b45a1c02d76df38d.nq.gz
│   ├── 75e3b65f99b29f48ab230e3eab3de8d0b7a9229f.nq.gz
│   ├── 9faa1b7a7339db85692f91ad4b922554624a3ef7.nq.gz
│   ├── 9fe50de16e59d550235aa6d7d15ee12ddf054414.nq.gz
│   ├── a36fedab8db68b26a76fbbf1de1f549e4a12261b.nq.gz
│   ├── af9908b08f4b33c32a0080af73f53bc0fa0cdce4.nq.gz
│   ├── cf42f6893594e2f8be2b722de51123d65e4d61c4.nq.gz
│   ├── e385bb64478a00b594d3629f9a57aab24ed68d90.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── e5d42da6ac3e38561e242165a103e3e415cdaec5.nq.gz
│   ├── ee4d9362508d63f9e156fe9ee1b11ebc1a3e86d6.nq.gz
│   ├── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
│   └── f9d321c6518bf0141a09104ba2d57d3989b88327.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── fc80359120b3a3fe4ab3d65dfd97430e026f7c13.nq.gz
├── filetree
│   └── fc80359120b3a3fe4ab3d65dfd97430e026f7c13.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 30 files
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

[asimov-modules/asimov-jinja-module](https://github.com/asimov-modules/asimov-jinja-module)

---
*Parsed on 2026-09-28 by [repolex](https://repolex.ai)*
