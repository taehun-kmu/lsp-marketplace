# lsp-marketplace

Language-server plugins for Claude Code, powered by texlab (LaTeX/BibTeX) and vscode-json-languageserver (JSON/JSONC).

[![License: Apache 2.0](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](LICENSE)
[![Claude Code Plugin](https://img.shields.io/badge/Claude_Code-Plugin-D97757?logo=claude&logoColor=white)](https://docs.claude.com/en/docs/claude-code)
[![LaTeX](https://img.shields.io/badge/LaTeX-008080?logo=latex&logoColor=white)](https://www.latex-project.org/)

## Overview

lsp-marketplace provides language-server plugins for Claude Code. It packages texlab and vscode-json-languageserver as Claude Code plugins, enabling code intelligence, diagnostics, and completion directly on LaTeX/BibTeX and JSON/JSONC files.

## Plugins

- **latex-lsp** — texlab language server for LaTeX/BibTeX: completion, navigation, diagnostics, symbols, and `latexmk`/`pdflatex` build integration
- **json-lsp** — vscode-json-languageserver for JSON/JSONC: completion, hover, diagnostics, and schema validation

### Supported Extensions

- **latex-lsp** — `.tex` `.sty` `.cls` `.clo` `.def` `.lco` `.rnw` (`latex`); `.bib` `.bibtex` (`bibtex`)
- **json-lsp** — `.json` (`json`); `.jsonc` (`jsonc`)

## Project Structure

```text
lsp-marketplace/
├── .claude-plugin/
│   └── marketplace.json     # Marketplace manifest + lspServers for both plugins
├── plugins/
│   ├── latex-lsp/           # texlab plugin (README + LICENSE)
│   └── json-lsp/            # vscode-json-languageserver plugin (README + LICENSE)
├── LICENSE
└── README.md
```

## Getting Started

### Prerequisites

- Claude Code
- texlab on your `PATH` (for latex-lsp)
- vscode-json-languageserver on your `PATH` (for json-lsp)
- latexmk or pdflatex (optional, for latex-lsp build features)

### Installation

Add the marketplace, then install the plugins you want.

```bash
claude plugin marketplace add taehun-kmu/lsp-marketplace
claude plugin install latex-lsp@lsp-marketplace
claude plugin install json-lsp@lsp-marketplace
```

### Usage

Reload plugins to load them in the current session:

```text
/reload-plugins
```

Open a supported file (`.tex`, `.bib`, `.json`, `.jsonc`) and the matching language server activates automatically.

## License

Copyright (C) 2026 Taehun Jung

Licensed under the Apache License, Version 2.0.

See [LICENSE](LICENSE) for full license text.
