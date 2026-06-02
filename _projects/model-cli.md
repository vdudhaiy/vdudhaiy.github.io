---
title: Model Reuse CLI
start_date: 2025-08-01
end_date: 2025-09-30
layout: default
summary: A CLI tool to evaluate open-source software modules for reuse trustworthiness, scoring them across metrics like maintainability, responsiveness, license compliance, and bus factor using the GitHub API and LLMs.
last_updated: 2026-06-02
---

# Model Reuse CLI
{% if page.start_date %} {{ page.start_date | date: "%b %Y" }}{% endif %}
{% if page.end_date %} — {{ page.end_date | date: "%b %Y" }}
{% else %} — Present {% endif %}

<p style="text-align: right;">
  <small>Last Updated: {{ page.last_updated | date: "%b %-d, %Y" }}</small>
</p>

**ECE 461 — Software Engineering** &nbsp;·&nbsp; Purdue University

[GitHub Repository](https://github.com/ECE461ProjTeam/ModelReuseCLI)

A command-line interface tool that helps developers make informed decisions when selecting third-party open-source dependencies. The tool ingests module URLs, analyses multiple quality metrics, and produces a **composite trustworthiness score** — making the reuse decision transparent and data-driven.

## Key contributions

**Core metric evaluation logic** — Developed the primary evaluation engine, which includes:
- Dataset quality scoring
- License compliance analysis
- LLM-assisted metrics using **Purdue GenAI Studio** for automated assessment and validation of harder-to-quantify signals

**GitHub API integration** — Built the foundation for GitHub-based metrics by integrating with the GitHub API to extract repository insights (contributors, activity levels, open issues, etc.).

**Bus factor analysis** — Implemented an analysis module that assesses project sustainability risk based on contributor distribution. A low bus factor (heavy dependence on one or two contributors) is flagged as a risk signal.

**isomorphic-git** — Utilized isomorphic-git to enable repository cloning and local analysis without requiring native Git installations, improving portability across environments.

**Structured logging** — Designed and integrated a logging system to support debugging, traceability, and system transparency throughout the evaluation pipeline.

**Testing** — Wrote comprehensive unit and integration tests to ensure high code coverage, reliability, and maintainability.

## Development process

The project followed Agile practices throughout: sprint planning, iterative implementation, and postmortem evaluations. Working as a team on a CLI tool with many moving parts (API calls, file I/O, scoring logic) made testing and clear interfaces between modules especially important.

## Tech stack

Python · GitHub REST API · isomorphic-git · CLI design · Software quality metrics · Automated testing · Purdue GenAI Studio
