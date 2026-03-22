# OpenClaw Skill 系统研究

> Issue: [#4](https://github.com/lotosbin/openclaw-research/issues/4)

## 概述

OpenClaw 的 Skill 系统允许扩展 AI 智能体的能力，通过预定义的技能文件提供特定领域的指导。

## Skill 结构

```
~/.openclaw/skills/<skill-name>/
├── SKILL.md          # 核心定义文件
├── references/       # 参考文档
├── scripts/         # 辅助脚本
└── assets/          # 静态资源
```

## SKILL.md 格式

```yaml
---
name: <skill-name>
description: <触发场景描述>
---

# Skill 名称

## 指令内容...
```

## 内置 Skills

- `github` - GitHub 操作 (gh CLI)
- `weather` - 天气查询
- `summarize` - URL/文件摘要
- `coding-agent` - 编码任务委托
- `feishu-*` - 飞书相关操作
- `wecom-*` - 企业微信操作

## ClawHub

官方 Skill 市场: https://clawhub.com

## 状态

🟢 进行中 - 2026-03-22
