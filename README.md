<div align="center">

# 📄 DocFormatter

**Formatter for Word documents (.docx) and Google Docs -**
**like Prettier, but for documents.**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Status: Concept](https://img.shields.io/badge/status-concept-blue.svg)]()
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)]()
[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-blue.svg)]()

</div>

---

## The Problem

Every team has that one document. The one where half the text is in Arial, the
other half in Times New Roman, headings are inconsistent, line spacing changes
mid-page, and margins are different on every section.

Manual formatting is tedious, error-prone, and never consistent across a team.
Code has Prettier. Documents deserve the same.

---

## What is DocFormatter? (under review)

DocFormatter is a CLI tool and library for **automatic, deterministic formatting**
of Word documents (`.docx`) and Google Docs. You define a style config once -
DocFormatter enforces it everywhere.

> Just like Prettier stops arguments about code style -
> DocFormatter stops arguments about fonts, spacing, and heading styles in documents.

---

## Goals (under review)

- 🎯 Automatically apply a defined style to any `.docx` document
- 🎯 Support for Google Docs via the official REST API
- 🎯 Configurable via `.docformatterrc` or `docformatter.config.js`
- 🎯 Pluggable rule system - write and share your own formatting rules
- 🎯 CLI with `format` and `check` commands
- 🎯 CI/CD friendly - exit with non-zero code if document is not formatted
- 🎯 Never touch content - only formatting, never text

---

## Non-Goals

- ❌ Not a text or content editor
- ❌ Not a file format converter (docx → pdf, etc.)
- ❌ Not a grammar or spell checker
- ❌ Not a replacement for Word or Google Docs

---

## Who Is It For?

| Audience | Use Case |
|---|---|
| Technical writers | Standardize documentation style across teams |
| Legal teams | Enforce consistent formatting in contracts and reports |
| Developers | Auto-format docs in CI/CD pipelines |
| Students & educators | Apply university/company templates instantly |
| Open source projects | Keep contribution docs visually consistent |

---

## Planned Tech Stack (under review)

### Core
- **Runtime**: Node.js + TypeScript
- **`.docx` parsing**: [`docxtemplater`](https://github.com/open-xml-templating/docxtemplater) + [`pizzip`](https://github.com/open-xml-templating/pizzip)
- **XML processing**: [`fast-xml-parser`](https://github.com/NaturalIntelligence/fast-xml-parser) for OOXML manipulation
- **Google Docs**: [Google Docs REST API v1](https://developers.google.com/docs/api)
- **CLI**: [`commander.js`](https://github.com/tj/commander.js)
- **Config resolution**: [`cosmiconfig`](https://github.com/cosmiconfig/cosmiconfig) (same as Prettier)

### Testing
- `vitest` for unit and integration tests
- Fixture `.docx` files for formatting snapshot tests

---

## Roadmap (under review)

- [ ] MVP: .docx formatting (font family, size, paragraph spacing)
- [ ] Heading styles (H1–H6), page margins, page size
- [ ] CLI with format and check commands
- [ ] Config file support via cosmiconfig
- [ ] Pluggable rules API with custom rule support
- [ ] Google Docs API integration
- [ ] VSCode extension
- [ ] Stable release, full documentation, real-world examples

---

## Prior Art & Inspiration

- Prettier - the gold standard for opinionated code formatting
- Biome - fast formatter and linter for JavaScript/TypeScript
- textlint - pluggable linter for natural language text
- markdown-styler-for-word - applies styles to markdown docs in Word
- python-docx - Python library for reading/writing .docx files
- docxtemplater - generate .docx from templates

---

## Contributing

The project is in the concept stage. All feedback, ideas, and suggestions are
very welcome - open an Issue to start a discussion.

Once the initial architecture is defined, a `CONTRIBUTING.md` will be published
with setup instructions, code style guidelines, and a guide for writing custom rules.

---

## License

MIT © 2026 - see [LICENSE](LICENSE) for details.
