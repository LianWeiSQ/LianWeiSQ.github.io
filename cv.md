# William / LianWeiSQ

Agent Harness Engineer  
GitHub: [LianWeiSQ](https://github.com/LianWeiSQ)  
Homepage: [https://lianweisq.github.io/](https://lianweisq.github.io/)

## Profile

I build agent infrastructure around the model: tool execution, context engineering,
permission boundaries, sandbox runtimes, session ledgers, trace/replay, eval gates,
and GitOps-style workflow control planes for AI-native software engineering.

我的方向是把 coding agent 从“能跑 demo”推进到“可交付、可观测、可评测、可复盘”的工程系统。

## Core Skills

- Agent runtime architecture: loop, tools, permissions, sessions, model provider boundary.
- Context engineering: instruction snapshots, file-read state, compaction, context pack traces, session parts.
- Observability and evaluation: JSONL traces, replay, runtime warnings, CI gates, Langfuse export, benchmark adapters.
- Workflow systems: branch-per-task thinking, GitOps delivery loops, CI/eval quality gates, dashboard planning.
- Infrastructure: Python, FastAPI, Go/Kubernetes, GitLab CI, GitHub Pages, TypeScript frontend.

## Selected Projects

### OpenAgent - Agent Harness Runtime

Repository: [LianWeiSQ/openagent-ai](https://github.com/LianWeiSQ/openagent-ai)

Contributions:

- Built the direction for a Python runtime focused on the harness around LLM agents.
- Implemented / documented AgentLoop, built-in tools, permission rulesets, MCP bridge, sessions, and provider boundary.
- Designed context persistence through context pack snapshots, instruction/file assets, session memory, and session parts.
- Added trace, replay, eval reports, regression comparison, runtime warning gates, and optional Langfuse export.
- Advanced a decoupled Swarm Function Kernel supporting function, OpenAgent, subprocess, HTTP, and A2A runners.

### BrainBox - Sandbox Infrastructure

Contributions:

- Studied and documented a Go/Kubernetes sandbox platform for isolated code execution.
- Covered Manager APIs, controller reconciliation, Envoy routing, ext_authz, GitLab CI, local kind / OrbStack flows, and E2E testing.
- Used the project as an execution-infrastructure reference for future OpenAgent sandbox integration.

### Fintech Agent - Domain Agent Case Study

Contributions:

- Built a finance-domain research pipeline as an OpenAgent tool case study.
- Designed authority-first source collection, event normalization, confidence scoring, SQLite audit trail, Markdown/PDF report generation, and D0 / D1 / D5 outcome evaluation hooks.
- Demonstrated why domain agents need evidence, audit, replay, and ex-post evaluation instead of polished summaries only.

### OpenAgent Workflow - GitOps Control Plane Research

Contributions:

- Compared Codex-style GitOps collaborative development with OpenAgent's runtime-first usage.
- Proposed an outer workflow control plane: task -> branch/worktree -> runner -> commit -> CI/eval -> dashboard -> merge decision.
- Positioned OpenAgent as a traceable and evaluable coding runner inside a broader software delivery loop.

## Writing

- [Codex GitOps 协作开发方式 vs OpenAgent 使用方式](notes/codex-gitops-workflow-vs-openagent.md)
- [OpenAgent README](https://github.com/LianWeiSQ/openagent-ai)
- [Context Engineering Notes](https://github.com/LianWeiSQ/openagent-ai/blob/main/doc/context.md)

## Current Focus

- Make OpenAgent easier to run, inspect, and evaluate from the command line and GitHub.
- Build `openagent-workflow` as a small prototype for branch-per-task, eval-first agent delivery.
- Keep GitHub repositories readable, evidence-backed, and continuously updated.

