<a id="readme-top"></a>

<div align="center">


# Product on Purpose

**An open-source portfolio for building products with intent, augmented by AI agents.**

A collection of composable skills, MCP servers, desktop tools, and reference libraries for product managers, builders, and the agents that work alongside them.

<p>
  <a href="#-portfolio-at-a-glance"><strong>Explore the portfolio</strong></a>
  &nbsp;·&nbsp;
  <a href="#-find-your-way-in"><strong>Find your way in</strong></a>
  &nbsp;·&nbsp;
  <a href="#-philosophy"><strong>Philosophy</strong></a>
  &nbsp;·&nbsp;
  <a href="#-contributing"><strong>Contributing</strong></a>
</p>


<p>
  <img src="https://img.shields.io/badge/projects-9-brightgreen?style=flat-square" alt="Projects: 9">
  <img src="https://img.shields.io/badge/license-Apache--2.0-blue?style=flat-square" alt="License: Apache-2.0 (per project)">
  <img src="https://img.shields.io/badge/status-active-success?style=flat-square" alt="Status: Active">
  <img src="https://img.shields.io/badge/AI--native-yes-purple?style=flat-square" alt="AI-native">
  <img src="https://img.shields.io/badge/maintainer-@jprisant-orange?style=flat-square" alt="Maintainer: @jprisant">
</p>


</div>

---

## Table of Contents

1. [About](#-about)
2. [Portfolio at a Glance](#-portfolio-at-a-glance)
3. [Find Your Way In](#-find-your-way-in)
4. [Project Families](#-project-families)
5. [Workspace Layout](#-workspace-layout)
6. [Philosophy](#-philosophy)
7. [Status Legend](#-status-legend)
8. [Contributing](#-contributing)
9. [License](#-license)
10. [Maintainer](#-maintainer)

---

## About

> *"Build products on purpose, not by accident."*

**Product on Purpose** is the home for a set of open-source projects that share a single thesis: the work of product management - thinking, framing, deciding, writing, shipping - is on the cusp of a step-change as agentic AI matures. The projects in this org explore three questions in parallel:

1. **What does excellent PM practice look like when an agent can do the rote work?** (see `pm-skills`, `pm-skills-mcp`, `thinking-framework-skills`)
2. **How should we configure, orchestrate, and trust the agents we work with?** (see `agent-config-toolkit`, `agent-skill-toolkit`)
3. **What infrastructure do we need around AI artifacts and outputs so they don't rot?** (see `writing-style-library`)

Each project is independent, open-source (Apache-2.0 unless noted), and usable on its own. Together they form a working portfolio for the AI-native product practitioner.

---

## Portfolio at a Glance

| Project                                                      | What it does                                                 | Status                  | Stack                        |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ----------------------- | ---------------------------- |
| [**pm-skills**](./pm-skills)                                 | 59 plug-and-play PM agent skills (Foundation Sprint, Design Sprint, lifecycle phases, utilities, tools). | `Active · v2.16.0`      | Markdown skills, Astro docs  |
| [**pm-skills-mcp**](./pm-skills-mcp)                         | MCP server exposing the PM skill catalog to any agent that speaks Model Context Protocol. | `Maintenance`           | TypeScript, MCP SDK          |
| [**writing-style-library**](./writing-style-library)         | Composable catalog of writing instructions across three orthogonal axes (Voice/Tone, Style, Format). | `Active · v0.1.0`       | Plugin + Py/TS SDKs          |
| [**thinking-framework-skills**](./thinking-framework-skills) | Skills wrapping canonical thinking tools (Six Hats, First Principles, etc.) for agent-driven reasoning. | `Discovery`             | 
| [**agent-skill-toolkit**](./agent-skill-toolkit)             | Tooling for authoring, validating, and packaging agent skills. | `Discovery`             | Prototype                    |
| [**project-knowledge-os**](./project-knowledge-os)           | Local-first system for managing AI-generated artifacts (PRDs, research, decisions) across projects. | `Planning`              | TBD (Tauri likely)           |

> See the [Status Legend](#-status-legend) for what each label means.

---

## Find Your Way In

A quick router. Pick the row that matches your situation.

| If you want to...                                           | Start here                                                   |
| ----------------------------------------------------------- | ------------------------------------------------------------ |
| Use AI to do better PM work                                 | [`pm-skills`](./pm-skills) (or [`pm-skills-mcp`](./pm-skills-mcp) if you prefer an MCP server) |
| Apply a structured thinking framework to a problem          | [`thinking-framework-skills`](./thinking-framework-skills)   |
| Make AI-generated writing sound less like AI                | [`writing-style-library`](./writing-style-library)           |
| Audit your `CLAUDE.md` / `AGENTS.md` for quality and safety | [`agent-config-toolkit`](./agent-config-toolkit)             |

---

## Project Families

The portfolio clusters into four working families. The line between families is intentionally fuzzy, since the projects share ideas.

### 1. PM Practice

Skills, frameworks, and reference material for doing the actual work of product management.

- **[pm-skills](./pm-skills)** - the flagship catalog of 59 skills covering Foundation Sprint, Design Sprint, lifecycle phases, foundation primitives, utilities, and external tool integrations.
- **[pm-skills-mcp](./pm-skills-mcp)** - the same skill catalog served over MCP, so any agent (Claude, Codex, Cursor, etc.) can call them as tools.
- **[thinking-framework-skills](./thinking-framework-skills)** - canonical thinking frameworks (Six Thinking Hats, First Principles, Pre-Mortem, etc.) packaged as agent skills.

### 2. Agent Infrastructure

Tools for building, configuring, and trusting the agents themselves.

- **[agent-config-toolkit](./agent-config-toolkit)** - reads `CLAUDE.md`, `AGENTS.md`, `.claude/settings.json`, `.mcp.json` and grades them on quality, security, and cross-platform consistency.
- **[agent-skill-toolkit](./agent-skill-toolkit)** - tooling for authoring, validating, and shipping agent skills.

### 3. Writing & Thinking

Composable instructions for how an agent should sound and reason.

- **[writing-style-library](./writing-style-library)** - three-axis model (Voice & Tone, Style/Mode/Genre, Format/Output) plus a composer that mixes them into a ready-to-prepend prompt prefix.

---

## Workspace Layout

```text
product-on-purpose/
├── pm-skills/                  # PM agent skill catalog (flagship)
├── pm-skills-mcp/              # MCP server wrapping the catalog
├── thinking-framework-skills/  # Thinking frameworks as skills
├── writing-style-library/      # Composable writing instructions
├── agent-config-toolkit/       # Config quality / security auditor
├── agent-skill-toolkit/        # Skill authoring tools
└── README.md                   # You are here
```

Every sub-project is self-contained: it has its own `README.md`, `LICENSE`, `CHANGELOG.md`, and (where applicable) `AGENTS.md` / `CLAUDE.md`. The umbrella directory exists to make the family relationships legible.

---

## Philosophy

A few opinions that shape the work across the portfolio.

| Principle                                 | What it means in practice                                    |
| ----------------------------------------- | ------------------------------------------------------------ |
| **Composable over monolithic**            | Small skills, small libraries, clean boundaries. A user should be able to pull one piece without inheriting the rest. |
| **Open-source by default**                | Apache-2.0 unless there's a deliberate reason to choose otherwise. The work is more valuable as a public artifact than as a private one. |
| **Agent-native, not agent-translated**    | The skills and tools are designed for an agent reader from the start. They are not human docs that an agent happens to consume. |
| **Local-first where it matters**          | Knowledge and configuration live on disk, owned by the user, not in someone else's cloud database. |
| **Every line of context earns its place** | Frontier models reliably follow roughly 150 to 200 instructions. Bloat is the enemy of quality. (See `agent-config-toolkit` for receipts.) |
| **Ship the smallest useful thing**        | Each project starts with a real version, however small. Internal drafts are clearly marked. |

---

## Status Legend

| Label         | Meaning                                                      |
| ------------- | ------------------------------------------------------------ |
| `Active`      | Shipping releases, accepting issues, has at least one tagged version. |
| `Maintenance` | Stable but not under active feature work. Security and breakage fixes only. |
| `Planning`    | Architecture, design, and scoping work in progress. Not yet implemented. |
| `Discovery`   | Early exploration. Expect rapid change or scope shifts.      |
| `Draft v0.x`  | Versioned but pre-1.0. Public API may break.                 |

---

## Contributing

Each sub-project has its own `CONTRIBUTING.md` (where applicable). General notes:

- **Issues, ideas, questions**: file them in the relevant sub-project's GitHub repo, not at the umbrella level.
- **Cross-cutting proposals** (e.g., a convention change that affects multiple projects): open a discussion in the most-affected project and tag this README in the description.
- **Security disclosures**: see `SECURITY.md` in the affected project. Do not file public issues for vulnerabilities.

If you're not sure where something belongs, default to the project whose name is closest to your concern.

---

## License

Each sub-project ships its own license file. The default is **Apache-2.0**; the few exceptions are marked in the relevant project's `LICENSE` and `README.md`. There is no umbrella license at the portfolio level; treat each project as independently licensed.

---

## Maintainer

**Jeremy Prisant** ([@jprisant](https://github.com/jprisant))
Building product, on purpose.

<div align="right"><a href="#readme-top">Back to top ↑</a></div>
