<a id="readme-top"></a>

<div align="center">

# Product on Purpose

**An open-source portfolio for building products with intent, augmented by AI agents.**

Composable skills, MCP servers, and reference libraries for product managers, builders, and the agents that work alongside them.

<p>
  <img src="https://img.shields.io/badge/AI--native-yes-purple?style=flat-square" alt="AI-native">
  <img src="https://img.shields.io/badge/license-Apache--2.0-blue?style=flat-square" alt="License: Apache-2.0 (per project)">
  <img src="https://img.shields.io/badge/maintainer-%40jprisant-orange?style=flat-square" alt="Maintainer: @jprisant">
</p>

</div>

---

## About

> *"Build products on purpose, not by accident."*

**Product on Purpose** builds open-source tools around a single bet: as agentic AI matures, product management itself is about to change shape, from how we think and frame to how we decide, write, and ship. Rather than wait to find out, these projects put that bet to work.

Each one chases a different question:

1. **What does great PM practice look like once an agent handles the rote work?**
2. **How do we configure, orchestrate, and genuinely trust the agents we work with?**
3. **What infrastructure keeps the artifacts agents produce from rotting?**

Every project stands on its own: independent, usually Apache-2.0, and useful in isolation. Together they form a working toolkit for the AI-native product practitioner.

---

## Featured Projects

### PM Practice

Skills and frameworks for doing the actual work of product management.

- **[pm-skills](https://github.com/product-on-purpose/pm-skills)** `Active`
  63 plug-and-play PM skills for AI agents spanning Foundation Sprint, Design Sprint, lifecycle phases, utilities, and tools, with sub-agents, templates, and CI-enforced contracts.
- **[pm-skills-mcp](https://github.com/product-on-purpose/pm-skills-mcp)** `Maintenance`
  The same catalog served over Model Context Protocol (59 tools), callable by any MCP-speaking agent. New users should prefer the file-based install from `pm-skills`.
- **[thinking-framework-skills](https://github.com/product-on-purpose/thinking-framework-skills)** `Active`
  34 agent-executable thinking methods plus 5 recipes, each stripped to its working mechanism, evidence-graded, and built to produce a concrete artifact.

### Agent Infrastructure

Tools for building, configuring, and trusting the agents themselves.

- **[agent-skills-toolkit](https://github.com/product-on-purpose/agent-skills-toolkit)** `Active`
  A toolkit and standard for building, grading, and scaling cross-agent skill libraries (Claude Code and Codex) against a Bronze/Silver/Gold quality bar.
- **[agent-plugins](https://github.com/product-on-purpose/agent-plugins)** `Active`
  The Product on Purpose plugin marketplace for Claude Code. Add it once, then install anything in the ecosystem.

### Writing

Composable instructions for how an agent should sound on the page.

- **[writing-style-catalog](https://github.com/product-on-purpose/writing-style-catalog)** `Experimental`
  Composable writing instructions for AI agents across four orthogonal axes: Voice, Tone, Style, and Format.

---

## Find Your Way In

A quick router. Pick the row that matches your situation.

| If you want to... | Start here |
|---|---|
| Use AI to do better PM work | [`pm-skills`](https://github.com/product-on-purpose/pm-skills) (or [`pm-skills-mcp`](https://github.com/product-on-purpose/pm-skills-mcp) for an MCP server) |
| Apply a structured thinking framework to a problem | [`thinking-framework-skills`](https://github.com/product-on-purpose/thinking-framework-skills) |
| Make AI-generated writing sound less like AI | [`writing-style-catalog`](https://github.com/product-on-purpose/writing-style-catalog) |
| Build and grade your own cross-agent skill library | [`agent-skills-toolkit`](https://github.com/product-on-purpose/agent-skills-toolkit) |
| Install our plugins in Claude Code | [`agent-plugins`](https://github.com/product-on-purpose/agent-plugins) |

---

## Install via the Marketplace

Most of the skill libraries above ship as Claude Code plugins. Add the marketplace once:

```text
/plugin marketplace add product-on-purpose/agent-plugins
```

Then browse and install any plugin in the ecosystem with `/plugin`.

---

## Philosophy

A few opinions that shape the work across the portfolio.

- **Composable over monolithic.** Small skills, clean boundaries. Pull one piece without inheriting the rest.
- **Open-source by default.** Apache-2.0 unless there is a deliberate reason to choose otherwise.
- **Agent-native, not agent-translated.** Designed for an agent reader from the start, not human docs an agent happens to consume.
- **Local-first where it matters.** Knowledge and configuration live on disk, owned by the user.
- **Every line of context earns its place.** Frontier models reliably follow roughly 150 to 200 instructions. Bloat is the enemy of quality.

---

## Maintainer

**Jeremy Prisant** ([@jprisant](https://github.com/jprisant))
Building product, on purpose.

<div align="right"><a href="#readme-top">Back to top ↑</a></div>
