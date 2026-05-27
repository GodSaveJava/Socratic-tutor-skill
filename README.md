# Socratic Tutor

>苏格拉底式指导（或苏格拉底提问法）是一种以对话为基础的教学与引导方法。指导者不直接给出答案，而是通过层层递进的提问，引导对方运用自身经验和逻辑思考，自主发现问题的本质并得出结论。

Vibecoding 爽快、心流强，但最大的痛点是容易让人变成“代码搬运工”，聊完天发现代码跑通了，但底层架构和逻辑自己还是没吃透。苏格拉底式引导刚好能作为“刹车”，强迫你在快速推进的同时保持思考。
`Socratic Tutor` 是一个面向开发场景的 Codex skill，用来帮助用户在 vibecoding 的同时理解自己正在做什么。

它不是“直接给答案”的助手，而是一个会通过提问、分层解释和必要图示来引导理解的导师。

## 什么是 Socratic Tutor

Socratic Tutor 指的是一种苏格拉底式的引导方式：

- 先问关键问题，而不是一次性讲完
- 先帮助用户建立心智模型，再进入实现细节
- 当用户卡住时，先给提示，再逐步展开
- 在适合的时候，用图帮助理解流程、结构和依赖关系

它特别适合这些场景：

- 新项目启动
- 理解项目结构
- 比较架构和方案
- 理解组件、hook、service、store 的职责
- 调试和排查问题
- 需要边做边学的时候

## 使用场景

下面这些情况尤其适合启用这个 skill：

- 你刚开始一个新项目，想先搞清楚目录、入口文件和核心边界
- 你面对一个陌生代码库，希望有人帮你先建立整体地图
- 你在比较两种架构、两个实现方案，想先看 tradeoff 再决定
- 你不确定某个组件、hook、service、store 应该放在哪里、怎么使用
- 你在修 bug，希望先定位问题，再理解原因，而不是直接改代码
- 你想边写边学，希望每一步都有一点引导，而不是一次性被讲满
- 你已经会做，但想把“为什么这样做”也真正弄懂

## 项目结构

这个仓库采用“核心行为 + 参考文档”的设计，便于在 Codex 和其他 agent 之间迁移。

```text
socratic-tutor/
├── SKILL.md
├── README.md
├── LICENSE
├── agents/
│   └── openai.yaml
└── references/
    ├── adapters.md
    ├── boundaries.md
    ├── diagram-patterns.md
    ├── modes.md
    ├── project-onboarding.md
    └── question-patterns.md
```

### 目录说明

- `SKILL.md`
  - 这是 Codex 读取的核心技能入口
  - 定义触发条件、工作流、图示策略和边界

- `agents/openai.yaml`
  - Codex UI 侧元数据
  - 包括展示名、简短描述和默认提示语

- `references/`
  - 存放可展开的详细规则
  - 例如模式定义、提问模板、图示模板、新项目引导和边界规则

- `README.md`
  - 仓库说明页
  - 帮助别人快速理解这个 skill 的用途和使用方式

## 导入到 Codex 后怎么用

### 1. 安装到 Codex skills 目录

把这个仓库放到 Codex 可发现的 skills 目录中，例如：

```text
C:\Users\admini\.codex\skills\socratic-tutor
```

### 2. 在 Codex 中触发

你可以这样使用它：

- 直接说 `Socratic tutor`
- 说 `请用苏格拉底式方式引导我`
- 说 `帮我理解这个项目结构`
- 说 `新项目开始，想启用 tutor 模式`

### 3. 选择模式

这个 skill 支持三种模式：

- `Always On`
  - 每次回复都进入引导模式

- `Keyword Trigger`
  - 只有在用户说出触发词时才进入引导模式

- `Hybrid`
  - 默认模式
  - 平时保持简洁
  - 当学习价值更高时自动切换为引导风格

### 4. 期望的交互方式

Codex 使用这个 skill 时，通常会：

1. 先问一个高杠杆问题
2. 再给最小必要解释
3. 必要时补图
4. 最后要求你复述或继续下一步

## 图示能力

这个 skill 可以在合适的时候生成简单图示，用来辅助理解：

- 流程图
- 时序图
- 树状结构图
- 状态图
- 依赖图

原则是：

- 一张图只回答一个问题
- 图越简单越好
- 图必须对应真实的项目结构或真实流程
- 简单问题不要强行配图

## 跨 Agent 设计

这个 skill 的核心行为尽量保持 agent-neutral，方便迁移到 Claude 等其他 agent。

相关说明见：

- `references/adapters.md`
- `references/modes.md`
- `references/question-patterns.md`

## 目标

这个 skill 的目标不是“替你完成学习”，而是：

- 让你在做项目时理解项目
- 让你在改代码时理解架构
- 让你在解决问题时建立可迁移的知识
- 让学习和执行同时发生
