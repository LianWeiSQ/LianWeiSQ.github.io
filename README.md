# William / LianWeiSQ

Personal GitHub Pages site for William, focused on Agent Harness Engineering, OpenAgent, coding-agent infrastructure, evaluation systems, and AI-native software delivery.

Live site: <https://lianweisq.github.io/>

## Positioning

This site is built as a public technical profile rather than a generic portfolio. The main narrative is:

- Turning coding agents from demos into auditable, testable, repeatable engineering workflows.
- Building the model-external harness layer: tools, context, permissions, sandbox runtime, trace, replay, evaluation, and workflow orchestration.
- Operating GitHub as a durable CV: projects, notes, contribution evidence, and progress records.

## Highlights

- **OpenAgent**: agent runtime direction covering AgentLoop, tool execution, MCP bridge, permissions, context snapshots, session ledgers, trace/replay, eval CI gates, Langfuse export, benchmark adapters, and Swarm Function Kernel.
- **BrainBox**: Kubernetes sandbox infrastructure reference for agent workloads, including Manager API, controller reconciliation, Envoy routing, CI/CD, and E2E validation.
- **Fintech Agent**: auditable domain-agent case study with evidence chains, event normalization, confidence scoring, report persistence, OpenAgent tool bridge, and D0/D1/D5 evaluation hooks.
- **OpenAgent Workflow**: research direction for branch-per-task agent development, GitOps loops, eval-first merge gates, reruns, logs, and dashboard-driven review.

## CV

The site includes a dedicated CV section and a Markdown resume:

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

- Update `News & Now` when a meaningful project milestone lands.
- Keep `cv.md` aligned with the homepage CV section.
- Add research notes under `notes/` when a workflow, architecture, or evaluation decision becomes reusable.
- Refresh preview screenshots after major visual changes.

## Design Direction

The visual language is intentionally editorial and technical: calm paper-like background, crisp cards, restrained green/blue accents, and strong emphasis on readable contribution evidence.
