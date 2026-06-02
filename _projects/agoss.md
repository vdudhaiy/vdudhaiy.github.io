---
title: "AgOSS: Mapping the Agricultural OSS Supply Chain"
start_date: 2026-01-01
end_date: 2026-05-01
layout: default
summary: A Mining Software Repositories study auditing 42 open-source agricultural repositories, quantifying a 42% security posture gap and identifying 1,861 vulnerabilities across the ag software supply chain.
last_updated: 2026-06-02
---

# AgOSS: A Dataset and Mapping of the OSS Agricultural Software Supply Chain
{% if page.start_date %} {{ page.start_date | date: "%b %Y" }}{% endif %}
{% if page.end_date %} — {{ page.end_date | date: "%b %Y" }}
{% else %} — Present {% endif %}

<p style="text-align: right;">
  <small>Last Updated: {{ page.last_updated | date: "%b %-d, %Y" }}</small>
</p>

AgOSS is a research project in the **Mining Software Repositories (MSR)** tradition, focused on characterizing the open-source software supply chain for the agricultural sector — a critical but understudied domain from a security perspective.

## What we built

**MSR pipeline** — Co-developed an automated pipeline to audit 42 repositories spanning the agricultural software stack, from firmware for field sensors to cloud platforms for farm data analytics. The pipeline used:

- [**OpenSSF Scorecards**](https://securityscorecards.dev/) to assess repository security posture across dimensions like branch protection, code review practices, and dependency management
- [**Augur**](https://augur.chaoss.io/) for repository health metrics and contributor activity analysis

**Finding:** Agricultural-specific repositories showed a **42% security posture gap** compared to non-agricultural software at the same stack layer.

**Vulnerability analysis tool** — Engineered a separate tool that:

- Fetched **GitHub SBOMs** (Software Bills of Materials) for each repository
- Queried the **OSV (Open Source Vulnerabilities)** database to identify known CVEs in all direct and transitive dependencies
- Identified **1,861 vulnerabilities** across the audited projects

**Finding:** Top-layer ag platforms inherit an average of **63.17 vulnerable dependencies**, most of which originate from transitive (indirect) dependencies that operators are often unaware of.

## Why it matters

The agricultural sector increasingly depends on open-source software to run irrigation systems, sensor networks, and precision farming platforms. Yet this software stack has received little security scrutiny. AgOSS provides the first systematic dataset and analysis of this supply chain, giving researchers and practitioners a baseline to improve from.

## Tech stack

Python · GitHub API · OpenSSF Scorecards · Augur · OSV API · SBOM analysis · Data analysis
