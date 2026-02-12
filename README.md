---
name: webhook-robot
description: A universal skill to send messages to webhook-based chat bots (WeCom, etc.).
metadata: { "openclaw": { "emoji": "🤖", "requires": { "bins": ["python3"] } } }
---

# Webhook Robot Skill (Webhook 机器人技能)

[English](#english) | [中文](#chinese)

<a name="english"></a>
## English

A universal skill for OpenClaw to send messages to various webhook-based chat bots.
Currently supports **WeCom (企业微信)**, with planned support for DingTalk (钉钉) and Feishu (飞书).

### Features
- **WeCom (企业微信)**: Send Text and Markdown messages.
- **Easy Integration**: Simple CLI scripts ready for OpenClaw agents.

### Installation
This skill is usually installed via ClawHub or manually placed in the `skills/` directory.

### Usage

#### 1. WeCom (企业微信)

**Script:** `scripts/send_wecom.py`

**Arguments:**
- `--key <KEY>`: The key part of your webhook URL.
- `--url <URL>`: The full webhook URL (alternative to --key).
- `--content <TEXT>`: The message content.
- `--markdown`: (Optional) Send as Markdown instead of plain text.

**Examples:**

```bash
# Send plain text
python3 scripts/send_wecom.py --key "your-key-here" --content "Hello World"

# Send Markdown
python3 scripts/send_wecom.py --key "your-key-here" --markdown --content "### Title\n> Hello **World**"
```

---

<a name="chinese"></a>
## 中文 (Chinese)

一个用于 OpenClaw 的通用技能，用于向各种基于 Webhook 的聊天机器人发送消息。
目前支持 **企业微信 (WeCom)**，计划支持钉钉和飞书。

### 功能特性
- **企业微信 (WeCom)**: 支持发送文本 (Text) 和 Markdown 消息。
- **易于集成**: 提供简单的 CLI 脚本，方便 OpenClaw Agent 调用。

### 安装
本技能通常通过 ClawHub 安装，或手动放置在 `skills/` 目录下。

### 使用方法

#### 1. 企业微信 (WeCom)

**脚本路径:** `scripts/send_wecom.py`

**参数说明:**
- `--key <KEY>`: Webhook URL 中的 key 参数部分。
- `--url <URL>`: 完整的 Webhook URL (与 --key 二选一)。
- `--content <TEXT>`: 消息内容。
- `--markdown`: (可选) 使用 Markdown 格式发送 (默认是纯文本)。

**示例:**

```bash
# 发送纯文本
python3 scripts/send_wecom.py --key "你的key" --content "你好，世界"

# 发送 Markdown
python3 scripts/send_wecom.py --key "你的key" --markdown --content "### 标题\n> 你好 **OpenClaw**"
```

## Contributing / 贡献
Feel free to add support for DingTalk, Feishu, or Slack!
欢迎提交 PR 增加对钉钉、飞书或 Slack 的支持！
