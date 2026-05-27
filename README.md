# Socratic Tutor

> “苏格拉底式导师”并不是一个高高在上的说教者，而是一个“思维的助产士”。

>这个概念源于古希腊哲学家苏格拉底。他认为，知识并不是由外部灌输进大脑的，而是原本就存在于人的内心。因此，导师的职责不是“给予”答案，而是通过连续、有逻辑的提问，帮助>学习者自己把答案“接生”出来。

Vibecoding 爽快、心流强，但最大的痛点是容易让人变成“代码搬运工”，聊完天发现代码跑通了，但底层架构和逻辑自己还是没吃透。苏格拉底式引导刚好能作为“刹车”，强迫你在快速推进的同时保持思考。

`Socratic Tutor` 是一个面向开发场景的 Codex skill。它通过提问、分层解释和必要图示，帮助你在 vibecoding 的同时真正理解自己在做什么。

这一份skill不止是可以用在coding项目上,也可以用在日常的学习中.

## 定义

苏格拉底式指导是一种以对话为基础的引导方式：

- 先问关键问题，而不是一次性讲完
- 先建立心智模型，再进入实现细节
- 用户卡住时，先给提示，再逐步展开
- 需要时用图辅助理解流程、结构和依赖关系

## 使用场景

适合这些情况：

- 新项目启动
- 理解陌生代码库
- 比较架构和方案
- 理解组件、hook、service、store 的职责
- 调试和排查问题
- 边做边学

## 项目结构

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

- `SKILL.md`: Codex 读取的核心行为入口
- `agents/openai.yaml`: Codex UI 元数据
- `references/`: 详细规则、示例和适配说明
- `README.md`: 仓库首页说明

## 导入到 Codex 后怎么用

### 1. 安装

把仓库放到 Codex 可发现的 skills 目录，例如：

```text
C:\Users\admini\.codex\skills\socratic-tutor
```

### 2. 触发

你可以直接说：

- `Socratic tutor`
- `请用苏格拉底式方式引导我`
- `帮我理解这个项目结构`
- `新项目开始，想启用 tutor 模式`

### 3. 模式

- `Always On`: 每次回复都进入引导模式
- `Keyword Trigger`: 只在触发词出现时进入引导模式
- `Hybrid`: 默认模式，平时简洁，必要时切换为引导风格

### 4. 典型交互

通常会经历：

1. 一个高杠杆问题
2. 最小必要解释
3. 必要时的图示
4. 一个复述或下一步

## 相关文档

- `SKILL.md`
- `references/examples.md`
- `references/failure-modes.md`
- `references/claude-adapter.md`
- `references/adapters.md`

