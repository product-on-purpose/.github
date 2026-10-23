<a id="readme-top"></a>

<div align="center">

# Product on Purpose

**Open-source tools for product managers and the AI agents working alongside them.**

<p>
  <img src="https://img.shields.io/badge/maintainer-%40jprisant-orange?style=flat-square" alt="Maintainer: @jprisant">
</p>

</div>

A general-purpose AI agent is a blank slate. Product on Purpose fills it in: open-source skills, tools, and libraries that turn an everyday agent into a capable partner for product work, one composable piece at a time. Tools for people who tinker or live in their editors, agents, and file systems live in the sibling org, [Prisant Labs](https://github.com/prisant-labs).

Version badges on this page update themselves. Everything else is written by hand, including a plain status line for each project.

**Status**

- 🟢 **Stable:** 1.0 or later, or a live service
- 🟡 **Beta:** released, but not yet 1.0
- 🟠 **Pre-release:** no release yet, so you build from source
- 🟤 **Maintenance:** works, but no longer developed

**Tags**

- 🚀 **Start here:** the best first project in its category
- 🆕 **New:** public for under 30 days
- 🧪 **Experimental:** likely to change, and its status line says how

## Get started

Most of these install as Claude Code plugins. Add the marketplace once, then install any plugin below:

```
/plugin marketplace add product-on-purpose/agent-plugins
```

## At a glance

### Product work

- 🧭 **[pm-skills](#-pm-skills)** · 🟢 Stable · 🚀 Start here<br>68 plug-and-play product management skills covering the full product lifecycle

- 📐 **[product-lifecycle-templates](#-product-lifecycle-templates)** · 🟡 Beta · 🧪 Experimental<br>Governed document templates that ship with the research, the guide, and a worked example


### Thinking, writing, and critique

- 🤔 **[thinking-framework-skills](#-thinking-framework-skills)** · 🟡 Beta · 🚀 Start here<br>Evidence-graded thinking methods an agent can run to reason, not just chat

- 🔍 **[critique-skills](#-critique-skills)** · 🟡 Beta<br>Critique that cites a published rubric on every finding, and publishes how often it is right

- 🎨 **[writing-style-catalog](#-writing-style-catalog)** · 🟡 Beta · 🧪 Experimental<br>Composable writing instructions so AI prose lands in the voice you actually want


### Building and distributing skills

- 🤖 **[agent-skills-toolkit](#-agent-skills-toolkit)** · 🟢 Stable · 🚀 Start here<br>A standard and toolkit for grading skill libraries to a Bronze/Silver/Gold bar

- 🧩 **[agent-plugins](#-agent-plugins)** · 🟢 Stable<br>The plugin marketplace to install from


### In maintenance

- 🧰 **[pm-skills-mcp](#-pm-skills-mcp)** · 🟤 Maintenance<br>The PM catalog as an MCP server


---

## 💼 Product work

For product managers, and for the agents doing product work alongside them. New here? Start with [pm-skills](#-pm-skills).

### 🧭 [pm-skills](https://github.com/product-on-purpose/pm-skills)

*🟢 Stable · 🚀 Start here · Claude Code, Codex, Cursor, and more*

![release](https://img.shields.io/github/v/release/product-on-purpose/pm-skills?display_name=tag&style=flat-square) ![marketplace pin](https://img.shields.io/badge/dynamic/json?url=https://raw.githubusercontent.com/product-on-purpose/agent-plugins/main/.claude-plugin/marketplace.json&query=%24.plugins%5B0%5D.version&label=marketplace&prefix=v&color=blue&style=flat-square) ![license](https://img.shields.io/github/license/product-on-purpose/pm-skills?style=flat-square)

```
/plugin install pm-skills@product-on-purpose
```

Get professional-grade product management work from your agent without teaching it the method first. It hands your agent a curated set of best-practice product workflows to run on demand, end to end.

**What's inside:** 68 skills, 6 sub-agents, 12 workflows, and 202 sample outputs.

- **Stop prompting PM work from scratch.** Each skill is a best-practice workflow (PRDs, hypotheses, user stories, sprint facilitation) that you invoke by name instead of re-explaining the method every time.
- **Covers the whole lifecycle.** From Foundation Sprint and Design Sprint at the fuzzy front end through discovery, delivery, and iteration, with sub-agents and workflow orchestrators that chain skills into full routines.
- **Remembers your project, if you let it.** Opt-in project memory lets later skills reuse what earlier ones produced, so you stop pasting the same personas and context into every run.
- **Quality you can see.** 200+ real-world sample outputs set the bar, and CI-enforced contracts keep every skill conformant as the catalog grows.

**Recent releases:**

- [v2.34.0](https://github.com/product-on-purpose/pm-skills/releases/tag/v2.34.0) (Oct 2026): Two planned AI skills lost a test against an analyst with no skill, so neither shipped. What survived went into `deliver-prd`, and samples now mark invented figures as fictional.
- [v2.33.0](https://github.com/product-on-purpose/pm-skills/releases/tag/v2.33.0) (Aug 2026): PRDs, ADRs, and instrumentation specs gain sections for AI features, covering model behavior, evaluation, trace privacy, and model choice. Three user-reported fixes also landed, including prioritization that fits small teams.
- [v2.32.0](https://github.com/product-on-purpose/pm-skills/releases/tag/v2.32.0) (Aug 2026): Opt-in project memory lets eight skills reuse what earlier skills produced. For example, `deliver-prd` picks up the personas from `discover-interview-synthesis` instead of asking you to paste them again.

**Status:** actively released, with a minor release every two to four weeks. Beyond Claude Code, it installs into Cursor, Copilot, Cline, and other agents with `npx skills add product-on-purpose/pm-skills`.

---

### 📐 [product-lifecycle-templates](https://github.com/product-on-purpose/product-lifecycle-templates)

*🟡 Beta · 🧪 Experimental · Claude Code, MCP clients, and more*

![release](https://img.shields.io/github/v/release/product-on-purpose/product-lifecycle-templates?display_name=tag&style=flat-square) ![marketplace pin](https://img.shields.io/badge/dynamic/json?url=https://raw.githubusercontent.com/product-on-purpose/agent-plugins/main/.claude-plugin/marketplace.json&query=%24.plugins%5B5%5D.version&label=marketplace&prefix=v&color=blue&style=flat-square) ![license](https://img.shields.io/github/license/product-on-purpose/product-lifecycle-templates?style=flat-square)

```
/plugin install product-lifecycle-templates@product-on-purpose
```

Stop inventing the structure of every PRD, roadmap, and postmortem from scratch. Where `pm-skills` runs the method, this decides what the resulting artifact should actually look like, and defends that shape with research rather than taste.

**What's inside:** 50 template bundles in ten families, two skills, and an MCP server.

- **A bundle, not a blank file.** Every document type ships five pieces together: the blank shape you fill in, a companion explaining why it is shaped that way, a fast operator card, a fully worked example, and machine-readable metadata an agent can route on.
- **Sized to your context window.** Every type offers a `lean` variant and most also offer `full`, each with an approximate token count, so an agent pulls the version that fits the job instead of blowing context on a template built for a different scale.
- **Reachable from any agent.** Two skills fill a template and grade a finished document, and an MCP server lets any MCP-aware agent search the catalog and fetch any of 99 template variants.
- **Cited, and gated on staying that way.** Shapes are argued from primary sources, and CI enforces the claims: bundle completeness, link health, research logs, manifest freshness, and even the repo's own self-reported counts.

**Recent releases:**

- [v0.21.0](https://github.com/product-on-purpose/product-lifecycle-templates/releases/tag/v0.21.0) (Oct 2026): A design brief joins the library as its 50th bundle, in lean and full sizes. The guide says when to write a creative brief, a specification, or a Shape Up pitch instead.
- [v0.20.1](https://github.com/product-on-purpose/product-lifecycle-templates/releases/tag/v0.20.1) (Oct 2026): Searching for "point of view statement" now finds the problem statement bundle, and "opportunity statement" no longer does. New document types must show a software product team writing or using them.
- [v0.20.0](https://github.com/product-on-purpose/product-lifecycle-templates/releases/tag/v0.20.0) (Oct 2026): Two bundles arrived. A test strategy sets the default testing approach for a program, and a positioning statement records how a product stands against a named alternative.

**Status:** the repository calls itself experimental. All 50 bundles are marked beta, and the project claims none of them is proven. You can also clone the repository, add it with `npx skills add product-on-purpose/product-lifecycle-templates`, or [read every bundle online](https://product-on-purpose.github.io/product-lifecycle-templates/).

<div align="right"><a href="#readme-top">Back to top ↑</a></div>

---

## 🧠 Thinking, writing, and critique

For anyone who wants an agent to reason, review, or write with a method rather than by feel. New here? Start with [thinking-framework-skills](#-thinking-framework-skills).

### 🤔 [thinking-framework-skills](https://github.com/product-on-purpose/thinking-framework-skills)

*🟡 Beta · 🚀 Start here · Claude Code, Codex, and more*

![release](https://img.shields.io/github/v/release/product-on-purpose/thinking-framework-skills?display_name=tag&style=flat-square) ![marketplace pin](https://img.shields.io/badge/dynamic/json?url=https://raw.githubusercontent.com/product-on-purpose/agent-plugins/main/.claude-plugin/marketplace.json&query=%24.plugins%5B1%5D.version&label=marketplace&prefix=v&color=blue&style=flat-square) ![license](https://img.shields.io/github/license/product-on-purpose/thinking-framework-skills?style=flat-square)

```
/plugin install thinking-framework-skills@product-on-purpose
```

Stop letting your agent improvise its reasoning on hard problems. This library is a toolbox of decision-making moves that your agent actually executes, each one graded so you know how far to trust it.

**What's inside:** 63 frameworks, 4 meta-tools, 9 recipes, and 3 subagents.

- **Agents reason better with a method.** Canonical thinking tools (premortems, first principles, parallel-perspective review) packaged so an agent runs the actual move, not a vague impression of it.
- **Honest about the evidence.** Every skill carries a transparent grade, from replicated research down to practitioner heuristic, so you know how far to trust it. No laundered statistics.
- **Always ends in an artifact.** Each run hands back something usable, a risk register, an option matrix, an argument map, rather than more prose.
- **Hand off a whole routine.** In Claude Code, a decision stress test or a reasoning audit can run as a subagent and return only the finished brief, so the intermediate work stays out of your conversation.

**Recent releases:**

- [v0.18.6](https://github.com/product-on-purpose/thinking-framework-skills/releases/tag/v0.18.6) (Oct 2026): The premortem skill now says that, in one study, it lowered confidence in a flawed plan, instead of claiming it reduces overconfidence. The issue tree and pyramid principle evidence pages also report weaker findings.
- [v0.18.5](https://github.com/product-on-purpose/thinking-framework-skills/releases/tag/v0.18.5) (Oct 2026): The premortem evidence pages no longer claim better calibration, because the study measured confidence. Several citations were corrected, including a shareholder-letter year, three titles, and a co-author's name.
- [v0.18.4](https://github.com/product-on-purpose/thinking-framework-skills/releases/tag/v0.18.4) (Oct 2026): A retracted 2002 study is flagged and no longer counts as evidence. The premortem's "30%" figure is gone, because nobody has found it in the study it is credited to.

**Status:** actively released, with four minor releases in September. Other agents can use `npx skills add product-on-purpose/thinking-framework-skills`, and the subagents run in Claude Code only. It grades Advanced (Gold) under the agent-skills-toolkit Standard.

---

### 🔍 [critique-skills](https://github.com/product-on-purpose/critique-skills)

*🟡 Beta · Claude Code*

![release](https://img.shields.io/github/v/release/product-on-purpose/critique-skills?display_name=tag&style=flat-square) ![marketplace pin](https://img.shields.io/badge/dynamic/json?url=https://raw.githubusercontent.com/product-on-purpose/agent-plugins/main/.claude-plugin/marketplace.json&query=%24.plugins%5B4%5D.version&label=marketplace&prefix=v&color=blue&style=flat-square) ![license](https://img.shields.io/github/license/product-on-purpose/critique-skills?style=flat-square)

```
/plugin install critique-skills@product-on-purpose
```

Ask a general-purpose model to critique your work, and you get fluent, confident, forgettable commentary. These skills answer to a published rubric instead, and report how often they actually catch what is there.

**What's inside:** 7 skills, 1 reviewer subagent, 120 criteria, and a scorecard from 851 recorded runs.

- **Every finding cites a source.** Each skill operationalizes a published external standard (WCAG 2.2, Nielsen's heuristics, Diataxis, the Toulmin model, the Federal Plain Language Guidelines), so every defect it raises carries a permanent criterion ID you can look up and argue with.
- **Findings are records, not prose.** Output conforms to a frozen JSON Schema, so a critique can be diffed, filtered, tracked across revisions, or handed to another tool rather than read once and lost.
- **It publishes its own scorecard.** Measured against a corpus with deliberately planted defects, unflattering numbers first: recall, precision, and run-to-run consistency, with the weak axes named rather than buried.

**Recent releases:**

- [v0.2.0](https://github.com/product-on-purpose/critique-skills/releases/tag/v0.2.0) (Oct 2026): A seventh skill, `critique-forms`, reviews HTML forms for how easy they are to fill in, especially on a phone. A documentation site now shows every skill, criterion, and measured result.
- [v0.1.6](https://github.com/product-on-purpose/critique-skills/releases/tag/v0.1.6) (Aug 2026): A critique that could hang while searching your drives for its own scripts now finishes. Every published score also shows its run-to-run spread.
- [v0.1.5](https://github.com/product-on-purpose/critique-skills/releases/tag/v0.1.5) (Aug 2026): A script that ships with each skill now does the final tally and refuses to return an invalid report. On a small model, usable reports rose from 2 in 7 runs to 3 in 4.

**Status:** the repository calls itself pre-release, and its latest release shipped in October. For now, the benchmark can reproduce only the cheaper model tier's published figures, and the project says so. It grades Convergent (Silver) under the agent-skills-toolkit Standard.

---

### 🎨 [writing-style-catalog](https://github.com/product-on-purpose/writing-style-catalog)

*🟡 Beta · 🧪 Experimental · Claude Code, Claude.ai, and Claude Desktop*

![release](https://img.shields.io/github/v/release/product-on-purpose/writing-style-catalog?display_name=tag&style=flat-square) ![marketplace pin](https://img.shields.io/badge/dynamic/json?url=https://raw.githubusercontent.com/product-on-purpose/agent-plugins/main/.claude-plugin/marketplace.json&query=%24.plugins%5B2%5D.version&label=marketplace&prefix=v&color=blue&style=flat-square) ![license](https://img.shields.io/badge/license-Apache--2.0%20%2B%20CC%20BY%204.0-blue?style=flat-square)

```
/plugin install writing-style-catalog@product-on-purpose
```

Get an agent to write in the voice you want, not the one it defaults to. The catalog turns "make it sound professional" into a precise, reusable instruction you can drop onto any writing task.

**What's inside:** 97 entries on four axes (Voice, Tone, Style, and Format), 1,164 worked examples, 158 diff-pairs, and 14 recipes.

- **Make AI writing stop sounding like AI.** Compose precise, reusable instructions from named building blocks instead of retyping "make it sound professional" and hoping.
- **Four orthogonal axes.** Mix Voice, Tone, Style, and Format independently to dial in exactly the register and shape a piece needs.
- **Worked examples, not vibes.** Every entry ships with samples that show what it actually produces, so you can see a style before you commit to it.
- **Learns your default, then suggests the rest.** One skill captures your personal default style, and another recommends a combination for a situation you describe.

**Recent releases:**

- [v0.14.0](https://github.com/product-on-purpose/writing-style-catalog/releases/tag/v0.14.0) (Sep 2026): Every entry now carries an honest review status. All 97 are `machine-verified`, which means they pass every automated check but the maintainer has not yet read each one.
- [v0.13.0](https://github.com/product-on-purpose/writing-style-catalog/releases/tag/v0.13.0) (Aug 2026): Diff-pairs now cover all twelve anchor topics instead of five, and each of the 158 pairs carries written commentary.
- [v0.12.0](https://github.com/product-on-purpose/writing-style-catalog/releases/tag/v0.12.0) (Jul 2026): A draft `marketer` voice arrived for landing pages and launch copy. It stays hidden from the recommender until it is reviewed.

**Status:** the repository calls itself experimental. The entry schema is frozen, but the catalog, skills, and docs may still change without notice. For Claude.ai or Claude Desktop, download the ZIP from the latest release.

<div align="right"><a href="#readme-top">Back to top ↑</a></div>

---

## 🚢 Building and distributing skills

For people who author skill libraries, and for anyone installing from this one. New here? Start with [agent-skills-toolkit](#-agent-skills-toolkit).

### 🤖 [agent-skills-toolkit](https://github.com/product-on-purpose/agent-skills-toolkit)

*🟢 Stable · 🚀 Start here · Claude Code, Codex, npm, and GitHub Actions*

![release](https://img.shields.io/github/v/release/product-on-purpose/agent-skills-toolkit?display_name=tag&style=flat-square) ![marketplace pin](https://img.shields.io/badge/dynamic/json?url=https://raw.githubusercontent.com/product-on-purpose/agent-plugins/main/.claude-plugin/marketplace.json&query=%24.plugins%5B3%5D.version&label=marketplace&prefix=v&color=blue&style=flat-square) ![npm](https://img.shields.io/npm/v/agent-skills-toolkit?style=flat-square) ![license](https://img.shields.io/github/license/product-on-purpose/agent-skills-toolkit?style=flat-square)

```
/plugin install agent-skills-toolkit@product-on-purpose
```

Find out whether your skill library is actually good, and exactly what to fix next. It defines what a great, multi-agent skill library looks like, then gives you the tooling to prove yours measures up.

**What's inside:** 26 skills, 7 subagents, and a grader with 35 checks.

- **For people building skills, not just using them.** A toolkit and a normative Standard for authoring skill libraries that work across Claude Code and Codex from a single source.
- **A quality bar you can climb.** Grades a whole library against a tiered Bronze/Silver/Gold rubric and returns a burndown of exactly what blocks the next tier.
- **Deterministic, not vibes.** The grader gives the same answer on your laptop and in CI, because no model is involved, and it returns real exit codes. The repo self-validates at Gold in its own CI as the proof.
- **Runs wherever you check.** Use it as a plugin, run it once with `npx agent-skills-toolkit`, or add the GitHub Action so every push gets graded.

**Recent releases:**

- [v1.20.0](https://github.com/product-on-purpose/agent-skills-toolkit/releases/tag/v1.20.0) (Oct 2026): A new Standard revision turns three warnings into errors, but only for plugins that pin it. A broken `askit.config.json` now exits with code 2, and findings above your declared tier show as notices.
- [v1.19.0](https://github.com/product-on-purpose/agent-skills-toolkit/releases/tag/v1.19.0) (Sep 2026): A new check warns when Codex would silently drop a command because its converted skill is too large. Eight bugs from an external audit are fixed, including two patterns that could hang the grader.
- [v1.18.0](https://github.com/product-on-purpose/agent-skills-toolkit/releases/tag/v1.18.0) (Sep 2026): The GitHub Action is now documented and renamed Agent Skills Toolkit Grader. Its full report is published online, not just a badge.

**Status:** actively released. The npm package and the GitHub Action follow each release directly, and the marketplace pin can trail behind, so compare the badges above.

---

### 🧩 [agent-plugins](https://github.com/product-on-purpose/agent-plugins)

*🟢 Stable · Marketplace · Claude Code*

![plugins listed](https://img.shields.io/badge/dynamic/json?url=https://raw.githubusercontent.com/product-on-purpose/agent-plugins/main/.claude-plugin/marketplace.json&query=%24.plugins.length&label=plugins%20listed&color=blue&style=flat-square) ![registry](https://img.shields.io/badge/dynamic/json?url=https://raw.githubusercontent.com/product-on-purpose/agent-plugins/main/.claude-plugin/marketplace.json&query=%24.metadata.version&label=registry&prefix=v&color=blue&style=flat-square) ![last commit](https://img.shields.io/github/last-commit/product-on-purpose/agent-plugins?style=flat-square)

```
/plugin marketplace add product-on-purpose/agent-plugins
```

Add one marketplace, and every Product on Purpose plugin becomes a one-line install, including future ones.

**What's inside:** only the catalog. There's a single `marketplace.json`, and each plugin keeps its own repository, versions, and issues.

- **One front door to everything.** The Claude Code marketplace registry for the whole portfolio: add it once and every Product on Purpose plugin is a single command away.
- **Pinned, and watched.** Each entry pins a release commit, so nothing reaches you until it is re-pinned here, and a daily check flags any pin that falls behind its plugin's latest release.

**Recent catalog changes:**

- [Oct 22, 2026](https://github.com/product-on-purpose/agent-plugins/blob/main/CHANGELOG.md#11100---2026-10-22): [product-lifecycle-templates](https://github.com/product-on-purpose/product-lifecycle-templates) moved to a release that adds a design brief, its 50th template bundle. Run `/plugin update product-lifecycle-templates` to get it.
- [Oct 22, 2026](https://github.com/product-on-purpose/agent-plugins/blob/main/CHANGELOG.md#11090---2026-10-22): [product-lifecycle-templates](https://github.com/product-on-purpose/product-lifecycle-templates) moved to a patch release with no new bundle. The problem statement bundle now answers to "point of view statement" instead of "opportunity statement".
- [Oct 21, 2026](https://github.com/product-on-purpose/agent-plugins/blob/main/CHANGELOG.md#11080---2026-10-21): [product-lifecycle-templates](https://github.com/product-on-purpose/product-lifecycle-templates) moved to a release with two new bundles, a test strategy and a positioning statement.

**Status:** live, and all six listed plugins install now. You add the marketplace by its repository path, and you install each plugin by the marketplace name, `@product-on-purpose`.

<div align="right"><a href="#readme-top">Back to top ↑</a></div>

---

## 💤 In maintenance

These projects still work, but they are no longer developed and get security fixes only.

### 🧰 [pm-skills-mcp](https://github.com/product-on-purpose/pm-skills-mcp)

*🟤 Maintenance · Any MCP client*

![npm](https://img.shields.io/npm/v/pm-skills-mcp?style=flat-square) ![license](https://img.shields.io/github/license/product-on-purpose/pm-skills-mcp?style=flat-square)

```bash
npm install -g pm-skills-mcp
```

Give an agent that speaks the Model Context Protocol the product management catalog as native tools, with no file setup.

**What's inside:** an MCP server with 59 tools: 40 skills, 11 workflows, and 8 utilities.

**Recent releases:**

- [v2.9.3](https://github.com/product-on-purpose/pm-skills-mcp/releases/tag/v2.9.3) (May 2026): A security patch cleared every open dependency advisory, so `npm audit` now reports zero vulnerabilities. The tools themselves did not change.
- [v2.9.2](https://github.com/product-on-purpose/pm-skills-mcp/releases/tag/v2.9.2) (May 2026): The server entered maintenance mode with the 40-skill catalog embedded. Feature development is paused until there is demand for it.

**Status:** in maintenance mode since May 2026, with security patches and critical fixes only. It carries 40 skills while pm-skills now has 68, so new users should install [pm-skills](#-pm-skills) instead. Needs Node 18 or later. To ask for development to resume, [open a discussion](https://github.com/product-on-purpose/pm-skills-mcp/discussions).

---

Each project carries its own license: Apache-2.0 for most, while writing-style-catalog licenses its code under Apache-2.0 and its content under CC BY 4.0. Issues and pull requests are welcome in each project's own repository.

<div align="center">

Built and maintained by **Jonathan Prisant**, a product leader in church technology who gets unreasonably excited about solving problems, serving people, and designing elegant systems.

[@jprisant](https://github.com/jprisant) · Sibling org: [Prisant Labs](https://github.com/prisant-labs), tailored tools for people who tinker or live in their editors, agents, and file systems

</div>

<div align="right"><a href="#readme-top">Back to top ↑</a></div>
