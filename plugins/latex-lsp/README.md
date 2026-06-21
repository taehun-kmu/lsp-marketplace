# latex-lsp

LaTeX/BibTeX language server (texlab) for Claude Code, providing code intelligence, diagnostics, and completion.

## Supported Extensions

`.tex`, `.sty`, `.cls`, `.clo`, `.def`, `.lco`, `.rnw`, `.bib`, `.bibtex`

## Installation

### Via mise (recommended)

```bash
mise use -g github:latex-lsp/texlab
```

### Via cargo

```bash
cargo install --git https://github.com/latex-lsp/texlab --locked --tag v5.25.1
```

texlab no longer publishes to crates.io, so install from Git. Requires a recent stable Rust toolchain.

### Via Homebrew (macOS)

```bash
brew install texlab
```

### Via package manager (Linux)

```bash
# Debian/Ubuntu
sudo apt install texlab
```

Ensure `texlab` is on your `PATH` (verify with `texlab --version`) so Claude Code can launch it.

## More Information

- [texlab on GitHub](https://github.com/latex-lsp/texlab)
- [Installation & Configuration](https://github.com/latex-lsp/texlab/blob/master/README.md)
