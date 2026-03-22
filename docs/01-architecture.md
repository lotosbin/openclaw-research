# OpenClaw 官方文档与架构研究

> Issue: [#3](https://github.com/lotosbin/openclaw-research/issues/3)

## 概述

OpenClaw 是一个**自托管网关**，连接聊天应用到 AI 编程智能体。

## 核心架构

```
聊天应用(WhatsApp/Telegram/Discord/iMessage) → Gateway → AI Agent(Pi)
```

**关键组件：**
- **Gateway**: 单一数据源，负责会话、路由、通道连接
- **Channel Plugins**: 接入各聊天平台
- **Agent**: AI 智能体，支持工具调用、会话、记忆
- **Web Control UI**: 浏览器仪表板

## 技术栈

- **运行时**: Node 22+ (推荐), Node 22 LTS (最低要求 22.16+)
- **许可证**: MIT
- **部署**: 自托管

## 快速开始

```bash
npm install -g openclaw@latest
openclaw onboard --install-daemon
openclaw channels login  # 连接渠道
openclaw gateway --port 18789  # 启动网关
```

## 配置

配置文件: `~/.openclaw/openclaw.json`

```json5
{
  channels: {
    whatsapp: {
      allowFrom: ["+15555550123"],
      groups: { "*": { requireMention: true } },
    },
  },
}
```

## 文档

- 官方文档: https://docs.openclaw.ai
- 源码: https://github.com/openclaw/openclaw
- 社区: https://discord.com/invite/clawd

## 状态

🟢 进行中 - 2026-03-22
