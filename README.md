# Socratic Tutor / 苏格拉底式导师

`Socratic Tutor` is a Codex skill for development scenarios. It helps you understand what you are building through questions, layered explanations, and diagrams when they genuinely help.

`Socratic Tutor` 是一个面向开发场景的 Codex skill。它通过提问、分层解释和必要图示，帮助你在 vibecoding 的同时真正理解自己在做什么。

> “苏格拉底式导师”并不是一个高高在上的说教者，而是一个“思维的助产士”。
>
> 这个概念源于古希腊哲学家苏格拉底。他认为，知识并不是由外部灌输进大脑的，而是原本就存在于人的内心。因此，导师的职责不是“给予”答案，而是通过连续、有逻辑的提问，帮助学习者自己把答案“接生”出来。

Vibecoding 爽快、心流强，但最大的痛点是容易让人变成“代码搬运工”，聊完天发现代码跑通了，但底层架构和逻辑自己还是没吃透。苏格拉底式引导刚好能作为“刹车”，强迫你在快速推进的同时保持思考。

## Definition / 定义

Socratic guidance is a dialog-based approach:

- Ask the key question first instead of giving the full answer immediately.
- Build the mental model before diving into implementation details.
- When the user is stuck, give a hint first and expand gradually.
- Use diagrams when they help explain flow, structure, or dependencies.

苏格拉底式指导是一种以对话为基础的引导方式：

- 先问关键问题，而不是一次性讲完
- 先建立心智模型，再进入实现细节
- 用户卡住时，先给提示，再逐步展开
- 需要时用图辅助理解流程、结构和依赖关系

## Use Cases / 使用场景

Use this skill for:

- Starting a new project
- Understanding an unfamiliar codebase
- Comparing architecture options
- Understanding the role of a component, hook, service, or store
- Debugging and root-cause analysis
- Learning while building
- Daily learning outside of coding projects, when you want guided thinking instead of a direct answer

适合这些情况：

- 新项目启动
- 理解陌生代码库
- 比较架构和方案
- 理解组件、hook、service、store 的职责
- 调试和排查问题
- 边做边学
- 日常学习场景中，希望获得引导式思考而不是直接答案

## Project Structure / 项目结构

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
    ├── claude-adapter.md
    ├── diagram-patterns.md
    ├── examples.md
    ├── failure-modes.md
    ├── modes.md
    ├── project-onboarding.md
    └── question-patterns.md
```

- `SKILL.md`: Core skill entry for Codex / Codex 读取的核心技能入口
- `agents/openai.yaml`: Codex UI metadata / Codex UI 元数据
- `references/`: Detailed rules, examples, and adapters / 详细规则、示例和适配说明
- `README.md`: Repository homepage / 仓库首页说明

## How to Use in Codex / 导入到 Codex 后怎么用

### 1. Install / 安装

Place the repository in a Codex-discoverable skills directory, for example:

```text
C:\Users\admini\.codex\skills\socratic-tutor
```

把仓库放到 Codex 可发现的 skills 目录，例如：

```text
C:\Users\admini\.codex\skills\socratic-tutor
```

### 2. Trigger / 触发

You can start it by saying:

- `Socratic tutor`
- `Please guide me in a Socratic way`
- `Help me understand this project structure`
- `I’m starting a new project and want tutor mode`

你可以直接说：

- `Socratic tutor`
- `请用苏格拉底式方式引导我`
- `帮我理解这个项目结构`
- `新项目开始，想启用 tutor 模式`

### 3. Modes / 模式

- `Always On`: Guide every reply with Socratic prompting.
- `Keyword Trigger`: Enter tutor mode only when a trigger phrase appears.
- `Hybrid`: Default mode. Stay concise, and switch into tutor mode when learning value is high.

- `Always On`: 每次回复都进入引导模式
- `Keyword Trigger`: 只有在触发词出现时才进入引导模式
- `Hybrid`: 默认模式，平时简洁，必要时切换为引导风格

### 4. Typical Flow / 典型交互

Usually it goes like this:

1. One high-leverage question
2. Minimal necessary explanation
3. A diagram if it adds real clarity
4. A teach-back or next action

通常会经历：

1. 一个高杠杆问题
2. 最小必要解释
3. 必要时的图示
4. 一个复述或下一步

## Related Docs / 相关文档

- `SKILL.md`
- `references/examples.md`
- `references/failure-modes.md`
- `references/claude-adapter.md`
- `references/adapters.md`

