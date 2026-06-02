---
title: Model Registry
start_date: 2025-09-01
end_date: 2025-12-15
layout: default
summary: A full-stack ML model registry platform with AWS cloud deployment, built as part of ECE 461 (Software Engineering) — featuring model storage, discovery, system health monitoring, and user authentication.
last_updated: 2026-06-02
---

# Model Registry
{% if page.start_date %} {{ page.start_date | date: "%b %Y" }}{% endif %}
{% if page.end_date %} — {{ page.end_date | date: "%b %Y" }}
{% else %} — Present {% endif %}

<p style="text-align: right;">
  <small>Last Updated: {{ page.last_updated | date: "%b %-d, %Y" }}</small>
</p>

**ECE 461 — Software Engineering** &nbsp;·&nbsp; Purdue University

[GitHub Repository](https://github.com/ECE461ProjTeam/ModelRegistry)

As part of a full software lifecycle project in ECE 461, our team inherited and extended another team's codebase to build a **full-stack model registry platform** for managing and analysing machine learning models and their metadata. The system enables centralized model storage, discovery, and lifecycle tracking, aligning with modern MLOps practices.

## Key contributions

**Frontend development** — Built UI components for model browsing, uploads, and interaction workflows, giving researchers a clean interface to manage models without touching the backend directly.

**AWS cloud deployment architecture** — Designed and implemented the end-to-end cloud deployment:
- Backend hosted on **AWS Elastic Beanstalk**
- Database provisioned with **Amazon Aurora Serverless (RDS)**
- Frontend delivered via **AWS Amplify**
- Model artifacts stored in **AWS S3**

**System Health Dashboard** — Developed a dashboard to monitor service performance, availability, and overall system health in real time, giving operators visibility into the platform's status.

**Authentication & authorization** — Implemented secure user authentication and account management, enabling protected access to resources.

## Working in an inherited codebase

A significant challenge of this project was onboarding into a codebase we didn't write. This required careful reading of existing code, incremental refactoring to improve maintainability, and disciplined communication across the team to avoid regressions while extending functionality — all within an Agile sprint structure.

## Tech stack

AWS (Elastic Beanstalk · Aurora Serverless · Amplify · S3) · JavaScript · Full-stack development · Authentication systems · Agile development
