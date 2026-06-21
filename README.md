# latex-lsp

LaTeX and BibTeX code intelligence for Claude Code, powered by the texlab language server.

[![License: Apache 2.0](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](LICENSE)
[![Claude Code Plugin](https://img.shields.io/badge/Claude_Code-Plugin-D97757?logo=claude&logoColor=white)](https://docs.claude.com/en/docs/claude-code)
[![LaTeX](https://img.shields.io/badge/LaTeX-008080?logo=latex&logoColor=white)](https://www.latex-project.org/)

## Overview

latex-lsp provides LaTeX and BibTeX language support for Claude Code. It integrates the texlab language server as a Claude Code plugin, enabling code intelligence, diagnostics, and completion directly on LaTeX and BibTeX files.

## Features

### Language Intelligence

- **Completion**: commands, citations, labels, and cross-references
- **Navigation**: go-to-definition, find references, and hover documentation
- **Symbols**: document outline and workspace-wide symbol search

### Diagnostics

- **Real-time checks**: undefined references, unused BibTeX entries, and syntax errors

### Build Integration

- **Compile support**: texlab coordinates with `latexmk` / `pdflatex` for building and error reporting

### Supported Extensions

| Group  | Extensions                                       | Language ID |
|--------|--------------------------------------------------|-------------|
| LaTeX  | `.tex` `.sty` `.cls` `.clo` `.def` `.lco` `.rnw` | `latex`     |
| BibTeX | `.bib` `.bibtex`                                 | `bibtex`    |

## Project Structure

```text
latex-lsp/
├── .claude-plugin/
│   └── marketplace.json     # Marketplace manifest + latex-lsp lspServers definition
├── plugins/
│   └── latex-lsp/
│       ├── README.md        # Plugin readme (texlab install methods)
│       └── LICENSE
├── LICENSE
└── README.md
```

## Getting Started

### Prerequisites

- Claude Code
- texlab language server (must be on your `PATH`)
- latexmk or pdflatex (optional, for build features)

### Installation

Add this marketplace, then install the plugin.

```bash
claude plugin marketplace add taehun-kmu/latex-lsp
claude plugin install latex-lsp@latex-lsp
```

### Usage

Reload plugins to load it in the current session:

```text
/reload-plugins
```

Open a `.tex` or `.bib` file and `texlab` activates automatically.

## License

Copyright (C) 2026 Taehun Jung

Licensed under the Apache License, Version 2.0.

See [LICENSE](LICENSE) for full license text.
