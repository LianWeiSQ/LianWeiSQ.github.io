# 廉威 / William / LianWeiSQ

Personal GitHub Pages site for 廉威 / William, positioned around Agent Harness Engineering, AaaS Runtime, OpenAgent, coding-agent infrastructure, evaluation systems, sandbox execution, and AI Infra delivery.

Live site: <https://lianweisq.github.io/>

## Positioning

This repository is a public technical CV website rather than a generic portfolio. The narrative is aligned with the updated Agent Harness / AaaS Runtime resume:

- 4.5 years of backend and AI Agent engineering experience.
- Huawei 5GC Committer background with distributed microservice, Kubernetes delivery, performance, reliability, and version delivery experience.
- Focus on the model-external harness layer: AgentLoop, tool governance, context/memory, permissions, sandbox runtime, trace/replay/eval, HTTP/SSE runtime, and model gateway boundaries.
- GitHub as durable evidence: engineering works, docs, research notes, CV, and operating rhythm.

## Highlights

- **OpenAgent**: Python Agent Harness Runtime covering AgentLoop, Provider Boundary, Tool Registry, Permission Ruleset, Workspace Runtime, Session Ledger, Trace, Eval, MCP, Skill, context pack snapshots, replay, and CI gates.
- **OpenAgent Runtime HTTP / MCPHub / SkillHub**: FastAPI HTTP/SSE service boundary for session lifecycle, events, permission/question replies, quota, provider registry, structured logs, and deployable runtime shape.
- **BrainBox**: Go/Kubernetes sandbox infrastructure reference for agent execution, including Sandbox Manager API, Platform Controller, Envoy routing, ext_authz, PostgreSQL, Vue console, CRD reconciliation, audit, metrics, and tracing.
- **Fintech Agent**: vertical-domain agent evaluation case study with source collection, event normalization, evidence scoring, Chinese report generation, SQLite audit trail, publishability gate, trace/replay, and D0/D1/D5 ex-post evaluation.

## Resume

- Homepage CV section: <https://lianweisq.github.io/#cv>
- Markdown CV: <https://lianweisq.github.io/cv.md>

## Local Preview

```bash
python3 -m http.server 4173
```

Open:

```text
http://127.0.0.1:4173
```

## Repository Structure

```text
.
├── index.html
├── styles.css
├── script.js
├── cv.md
├── GITHUB_OPERATING_PLAN.md
├── notes/
└── assets/
```

## Operating Rhythm

- Keep homepage, `cv.md`, GitHub profile, and project READMEs aligned on the same keywords.
- Update proof metrics only when there is real project/resume evidence.
- Add research notes under `notes/` when workflow, architecture, or evaluation decisions become reusable.
- Refresh preview screenshots after major visual changes.

## Design Direction

The visual language is an executive technical CV website: formal navy resume bars, paper-like background, dense but readable evidence cards, restrained cyan/green highlights, and a real portrait to make the site feel credible and personal.
