<a id="readme-top"></a>

<div align="center">

# Product on Purpose

**Open-source tools for product managers and the AI agents working alongside them.**

<p>
  <img src="https://img.shields.io/badge/AI--native-yes-purple?style=flat-square" alt="AI-native">
  <img src="https://img.shields.io/badge/license-Apache--2.0-blue?style=flat-square" alt="License: Apache-2.0 (per project)">
  <img src="https://img.shields.io/badge/maintainer-%40jprisant-orange?style=flat-square" alt="Maintainer: @jprisant">
</p>

</div>

A general-purpose AI agent is a blank slate. Product on Purpose fills it in: open-source skills, tools, and libraries that turn an everyday agent into a capable partner for product work, one composable piece at a time.

| Repo | What it is |
|---|---|
| [**pm-skills**](https://github.com/product-on-purpose/pm-skills) | 65 plug-and-play product management skills covering the full product lifecycle. |
| [**thinking-framework-skills**](https://github.com/product-on-purpose/thinking-framework-skills) | Evidence-graded thinking methods an agent can run to reason, not just chat. |
| [**agent-skills-toolkit**](https://github.com/product-on-purpose/agent-skills-toolkit) | A standard and toolkit for grading skill libraries to a Bronze/Silver/Gold bar. |
| [**writing-style-catalog**](https://github.com/product-on-purpose/writing-style-catalog) | Composable writing instructions so AI prose lands in the voice you actually want. |
| [**agent-plugins**](https://github.com/product-on-purpose/agent-plugins) | The marketplace that puts every Product on Purpose plugin one command away. |
| [**pm-skills-mcp**](https://github.com/product-on-purpose/pm-skills-mcp) | The PM catalog as an MCP server (maintenance mode). |

**Get started.** Most of these install as Claude Code plugins. Add the marketplace once, then grab any plugin below:

```bash
/plugin marketplace add product-on-purpose/agent-plugins
```

---

## [pm-skills](https://github.com/product-on-purpose/pm-skills)
*Flagship · Active · 65 skills · 4 sub-agents · 10 workflows · templates · 95+ samples*

The flagship of the portfolio and the place most people should start. It hands your agent a curated set of best-practice product workflows to run on demand, end to end.

- **Stop prompting PM work from scratch.** Each skill is a best-practice workflow (PRDs, hypotheses, user stories, sprint facilitation) that you invoke by name instead of re-explaining the method every time.
- **Covers the whole lifecycle.** From Foundation Sprint and Design Sprint at the fuzzy front end through discovery, delivery, and iteration, with sub-agents and workflow orchestrators that chain skills into full routines.
- **Quality you can see.** 95+ real-world sample outputs set the bar, and CI-enforced contracts keep every skill conformant as the catalog grows.

```bash
/plugin install pm-skills@product-on-purpose
```

## [thinking-framework-skills](https://github.com/product-on-purpose/thinking-framework-skills)
*Active · 34 skills · 5 recipes · evidence-graded*

Structured reasoning your agent can actually execute, not just name-drop. Think of it as a toolbox of decision-making moves, each one graded so you know how far to trust it.

- **Agents reason better with a method.** Canonical thinking tools (premortems, first principles, parallel-perspective review) packaged so an agent runs the actual move, not a vague impression of it.
- **Honest about the evidence.** Every skill carries a transparent grade, from replicated research down to practitioner heuristic, so you know how far to trust it. No laundered statistics.
- **Always ends in an artifact.** Each run hands back something usable, a risk register, an option matrix, an argument map, rather than more prose.

```bash
/plugin install thinking-framework-skills@product-on-purpose
```

## [agent-skills-toolkit](https://github.com/product-on-purpose/agent-skills-toolkit)
*Active · Standard + toolkit · 23 skills · 25 checks · Gold-in-CI*

The meta-layer for anyone authoring skills at scale. It defines what a great, multi-agent skill library looks like, then gives you the tooling to prove yours measures up.

- **For people building skills, not just using them.** A toolkit and a normative Standard for authoring skill libraries that work across Claude Code and Codex from a single source.
- **A quality bar you can climb.** Grades a whole library against a tiered Bronze/Silver/Gold rubric and returns a burndown of exactly what blocks the next tier.
- **Deterministic, not vibes.** Zero-dependency Node validators with real exit codes, and the repo self-validates at Gold in its own CI as the proof.

```bash
git clone https://github.com/product-on-purpose/agent-skills-toolkit.git
```

## [writing-style-catalog](https://github.com/product-on-purpose/writing-style-catalog)
*Experimental · 60 entries · 4 axes (Voice/Tone/Style/Format)*

Composable control over how an agent sounds on the page. It turns "make it sound professional" into a precise, reusable instruction you can drop onto any writing task.

- **Make AI writing stop sounding like AI.** Compose precise, reusable instructions from named building blocks instead of retyping "make it sound professional" and hoping.
- **Four orthogonal axes.** Mix Voice, Tone, Style, and Format independently to dial in exactly the register and shape a piece needs.
- **Worked examples, not vibes.** Every entry ships with samples that show what it actually produces, so you can see a style before you commit to it.

```bash
git clone https://github.com/product-on-purpose/writing-style-catalog.git
```

## [agent-plugins](https://github.com/product-on-purpose/agent-plugins)
*Marketplace · Active · Claude Code*

The registry that ties the whole ecosystem together. It is how every plugin above becomes a one-line install inside Claude Code.

- **One front door to everything.** The Claude Code marketplace registry for the whole portfolio: add it once and every Product on Purpose plugin is a single command away.
- **Deliberately thin.** No plugin code lives here, just the index, so it stays fast to load and easy to trust.

```bash
/plugin marketplace add product-on-purpose/agent-plugins
```

---

## [pm-skills-mcp](https://github.com/product-on-purpose/pm-skills-mcp)
*MCP server · Maintenance · 59 tools (40 skills, 11 workflows, 8 utilities)*

The same product management catalog, delivered over the Model Context Protocol for agents that prefer native tools to files.

- **The PM catalog over Model Context Protocol.** Exposes 59 tools to any MCP-aware agent with no file setup.
- **Stable, but paused.** Fully functional at v2.9.3; active development is on hold, so new users are better served by the file-based install from `pm-skills`.

```bash
npm install -g pm-skills-mcp
```

---

<div align="center">

Built and maintained by **Jonathan Prisant**, a product leader in church technology who gets unreasonably excited about solving problems, serving people, and designing elegant systems.

[@jprisant](https://github.com/jprisant)

</div>

<div align="right"><a href="#readme-top">Back to top ↑</a></div>
