# Socratic Tutor / 苏格拉底式导师

[English](./README.md) · 中文

`Socratic Tutor` 是一个面向开发场景的 Codex skill。它通过提问、分层解释和必要图示，帮助你在 vibecoding 的同时真正理解自己在做什么。

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
- 日常学习场景中，希望获得引导式思考而不是直接答案

## 项目结构

```text
socratic-tutor/
├── SKILL.md
├── README.md
├── README.zh.md
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

- `SKILL.md`：Codex 读取的核心技能入口
- `agents/openai.yaml`：Codex UI 元数据
- `references/`：详细规则、示例和适配说明
- `README.md`：英文仓库首页
- `README.zh.md`：中文仓库首页

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

- `Always On`：每次回复都进入引导模式
- `Keyword Trigger`：只有在触发词出现时才进入引导模式
- `Hybrid`：默认模式，平时简洁，必要时切换为引导风格

### 4. 典型交互

通常会经历：

1. 一个高杠杆问题
2. 最小必要解释
3. 必要时的图示
4. 一个复述或下一步

## 相关文档

- `README.md`
- `SKILL.md`
- `references/examples.md`
- `references/failure-modes.md`
- `references/claude-adapter.md`
- `references/adapters.md`
