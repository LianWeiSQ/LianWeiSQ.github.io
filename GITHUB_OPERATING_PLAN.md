# GitHub 经营计划

目标：把 GitHub 从“代码仓库”经营成“可信个人品牌入口”，围绕 Agent Harness Engineering 建立持续输出。

## 1. 仓库矩阵

| 仓库 | 角色 | 每周动作 |
| --- | --- | --- |
| `LianWeiSQ.github.io` | 个人主页和导航入口 | 更新 News、Writing、Selected Projects |
| `openagent-ai` | 主项目，展示 runtime 能力 | README、demo、eval report、release notes |
| `brainbox` | 沙箱基础设施能力证明 | 架构图、E2E 结果、部署说明 |
| `fintech-agent` | 垂直 agent case study | 样例报告、审计链路、domain eval |
| `agent-course` | 课程和研究材料 | 章节目录、讲稿、PPT 预览 |

## 2. 每周节奏

- 周一：选一个主题，写 5-8 行 GitHub issue / roadmap。
- 周三：合并一个小 PR，附测试或截图。
- 周五：更新个人主页 News 和项目 README。
- 周末：写一篇短 note：工具、上下文、评测、沙箱、GitOps 或 Claude Code / OpenCode 研究。

## 3. README 标准

每个重点仓库至少包含：

- 一句话定位。
- 架构图。
- Quickstart。
- Feature matrix。
- 测试命令和最近一次结果。
- 当前限制。
- Roadmap。
- 安全边界。

## 4. Pinned Repositories 建议

1. `openagent-ai`
2. `LianWeiSQ.github.io`
3. `brainbox`
4. `fintech-agent`
5. `agent-course`
6. `openagent-workflow`（后续创建）

## 5. 内容主线

- Agent Harness 不是 prompt engineering，而是模型外的工程系统。
- 好的 coding agent 需要 context、tools、permissions、sandbox、trace、eval 一起设计。
- GitOps + CI + eval 是 agent 进入团队交付流的关键。
- Domain agents 必须有 evidence、audit、replay 和 outcome evaluation。

