# 廉威 / William / LianWeiSQ

Agent Harness / AaaS Runtime 架构师方向<br>
Location: 上海<br>
GitHub: [LianWeiSQ](https://github.com/LianWeiSQ)  
Homepage: [https://lianweisq.github.io/](https://lianweisq.github.io/)

## 求职定位

资深 Agent Runtime / AI Infra 后端工程师，目标 AaaS 平台架构师。强攻 Agent Harness、Tool Runtime、Context/Memory、Trace/Eval、Sandbox 和 Model Gateway。

## 职业摘要

- 华为 5GC Committer 与后端平台工程师，具备 5G 核心网微服务、Kubernetes 交付、性能治理和 AI Agent 工程化经验。
- 当前主线聚焦 Agent Harness / AaaS Runtime：Run/Step/ToolCall/Artifact/Checkpoint/Event 建模、上下文与记忆、Tool/MCP/Skill 治理、权限与沙箱、Trace/Replay/Eval、HTTP/SSE Runtime 与 Model Gateway。
- 优势不是单点 Prompt/RAG Demo，而是能把不确定的模型行为约束进可恢复、可观测、可审计、可评测的后端执行系统，并用 5GC 分布式系统经验补齐可靠性、性能和交付闭环。

## 核心能力

- Agent Runtime: AgentLoop、Run/Step 状态机、ToolCall、Artifact、Checkpoint、Event、Session Ledger。
- Tool/MCP/Skill: Tool Registry、Schema、权限、风险等级、版本、审计、MCP Bridge、Skill 生命周期。
- Context/Memory: Context Budget、结构化 Compaction、File Context、短期/长期/领域记忆、RAG 混合检索。
- Observability/Eval: JSONL Trace、Replay、Runtime Warning、Langfuse Export、Eval CI Gate、Regression。
- Sandbox: Docker/K8s、Workspace Isolation、Envoy/ext_authz、资源/网络/Secret 边界、审计。
- AI Platform: OpenAI-compatible API、Provider Registry、Model Routing、Token/Quota/Rate Limit、Fallback。

## 技术栈

- 后端: Go/Gin、Python/FastAPI、Redis、PostgreSQL/MySQL、Kafka、REST/SSE、异步任务。
- 云原生: Docker、Kubernetes、HPA、金丝雀发布、Prometheus、GitLab CI、灰度与回滚。
- AI 平台: OpenAI-compatible API、Provider Registry、Model Routing、Token/Quota/Rate Limit、Fallback。
- 工程方法: 架构设计、性能优化、可观测、故障定位、跨团队版本交付、技术文档与面试表达。

## 工作经历

### 华为技术有限公司 - 云计算 BU - 高级工程师 B / Committer

2024.12 - 2025.09 | 上海 | AI4S / Multi-Agent 研发平台与记忆检索链路

- 参与企业级 Multi-Agent 研发平台建设，围绕需求拆解、意图规划、知识检索、工具调用、代码合规入库形成端到端闭环。
- 设计长/短期记忆 + 领域知识三层记忆模型，结合滑动窗口、语义分段、向量 + BM25 混合检索，解决长设计文档 Context Window 溢出问题，关键信息检索精度提升约 70%。
- 研发基于长文本哈希编码的工具调用加速机制，减少复杂任务中的重复工具调用与冗余生成，Token 消耗降低约 40%，响应延迟同步下降。
- 建立跨 Agent 上下文蒸馏与标签化映射方案，支撑复杂研发任务自动分解、状态同步和多 Agent 协作；通过语义关联链优化私有领域知识召回，召回率提升约 25%。

### 华为技术有限公司 - 分组控制开发部 - 高级工程师 B / 5GC Committer

2021.01 - 2024.12 | 上海 | 5G 核心网微服务架构设计、性能优化与云原生交付

- 参与 5GC 控制面从 0 到 1 的微服务架构设计与代码开发，作为项目组 PL 推进重点功能、微服务部署、性能优化和版本交付。
- 采用 DCI 架构进行复杂业务建模与服务解耦，沉淀 Role 接口组合、配置中心、预加载本地缓存等方案，数据库查询开销降低约 30%。
- 构建心跳检测、熔断降级、自适应流控、有界队列、多优先级队列和去重 DB 写等稳定性治理机制；专项优化后性能提升约 20%，吞吐上限提升约 10 倍，定位效率提升约 80%。
- 集成 HPA 与金丝雀发布，Pod 副本从 3 扩展到 15 以应对峰值流量 3 倍增长，资源成本降低约 40%，迭代周期从 2 周缩短到 3 天。

## Agent Harness 工程作品

### OpenAgent - Agent Harness Runtime

Repository: [LianWeiSQ/openagent-ai](https://github.com/LianWeiSQ/openagent-ai)

- 构建 Python Agent Harness Runtime，核心包括 AgentLoop、Provider Boundary、Tool Registry、Permission Ruleset、Workspace Runtime、Session Ledger、Trace 与 Eval。
- 实现/文档化上下文工程：context budget、结构化 compaction、instruction/file assets、context pack snapshot、session parts，避免把所有状态粗暴塞进 Prompt。
- 建设 Tool/MCP/Skill 能力：内置 bash/read/write/edit/grep/web/memory/todo/question/skill 工具，MCP config/discovery/runtime/bridge，Skill loader/registry。
- 建设可观测与评测链路：JSONL trace、run summary、runtime warning、eval runner、ci_gate、replay、Terminal-Bench/Harbor adapter、Langfuse metadata export。

### OpenAgent Runtime HTTP / MCPHub / SkillHub

- 用 FastAPI 将 OpenAgent core 封装为 HTTP/SSE Runtime，P0 接口覆盖 session create、message、events、abort、permission reply、question reply、config、health。
- 设计 RuntimeService 分层，管理 session 生命周期、turn 启动/取消、quota、provider registry、MCP bootstrap、permission/question pending request 与事件转发。
- 通过 Bearer API Key、request_id、structured logs、并发 quota、provider registry 和安全字段裁剪，使 Agent Runtime 具备可部署、可排障的服务形态。

### BrainBox - Go/Kubernetes Sandbox Infrastructure

- 研究并建设 Go/Kubernetes 沙箱平台，核心组件包括 Sandbox Manager HTTP API、Platform Controller、Envoy routing、ext_authz、PostgreSQL 持久层和 Vue 控制台。
- 覆盖 environment/sandbox/pool/batch/exec/proxy/lifecycle 等 API，具备 auth/authz/quota/audit/metrics/tracing middleware 与 K8s CRD 对账、GC、配额释放。
- 作为 OpenAgent 未来代码执行、Shell、文件工具和高风险外部调用的 sandbox backend 参考，明确文件、网络、进程、资源、Secret 和 artifact 回收边界。

### Fintech Agent - 垂类 Agent 评测样例

- 构建金融研究 Agent 流水线，覆盖权威源采集、事件归一、去重、证据质量评分、宏观资产映射、中文研究简报生成、SQLite 审计和 D0/D1/D5 事后评估。
- 证明垂类 Agent 不能只产出漂亮摘要，必须保留 evidence、audit trail、degraded reason、publishability gate、trace/replay 与 ex-post evaluation。

## 100w 岗位叙事关键词

- Agent Runtime: 不是 ReAct 节点串联，而是状态化、不确定、可恢复的后端任务系统。
- Tool Runtime: 工具 schema、权限、风险等级、幂等、副作用、审计、评测和生命周期治理。
- Context/Memory: Context 是当前运行态，Memory 是跨任务经验，Knowledge 是稳定领域事实，RAG 是检索机制，Trace 是执行证据。
- Sandbox: 按工具风险选择受控执行环境，核心是文件、网络、进程、资源、Secret、artifact 和租户隔离。
- MaaS 边界: 当前强在 Model Gateway、模型路由、Token/Quota/Cost 和服务观测；GPU/vLLM/TGI/KV Cache 是正在补齐的方向。

## 可深挖模块与证据链

- OpenAgent: `core/loop`, `core/tool`, `core/mcp`, `core/skill`, `core/context_pack`, `core/session`, `core/trace`, `core/eval`.
- Runtime HTTP: `app.py`, `service.py`, `provider_registry.py`, `quota.py`, `sse.py`, `observability.py`, `tests/test_app.py`.
- BrainBox: `pkg/sandbox/manager/api`, `middleware`, `store`, `controller`, `k8s`, `observability`, `deploy/k8s`.
- 文档证据: `harness/README.md`, `openagent/README.md`, `openagent/doc/context.md`, `openagent/doc/operations.md`, `brainbox/README.md`.

## 教育与语言

- 法国特鲁瓦技术大学 - 工程信息自动化（计算机视觉）硕士 | 2017.08 - 2020.11。
- 上海大学 - 信息工程 - 中欧学院 211 双一流 | 2014.08 - 2020.08。
- 英语 CET-6 | 法语 TEF B2。

## 下一阶段补齐

- MaaS 执行面：vLLM/TGI/TensorRT-LLM、prefill/decode、KV Cache、continuous batching、显存与副本调度。
- 平台负责人表达：三年 Roadmap、业务指标、开放生态、模型准入/灰度/回滚、FinOps 与成本分摊。
- 生产级 Runtime 细节：多实例 lease、dead-letter、reconciliation、SSE 断线补发、ToolCall 副作用补偿。
