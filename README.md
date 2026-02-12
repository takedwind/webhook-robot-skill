---
name: webhook-robot
description: A universal skill to send messages to webhook-based chat bots (WeCom, DingTalk, Feishu).
metadata: { "openclaw": { "emoji": "🤖", "requires": { "bins": ["python3"] } } }
---

# Webhook Robot Skill (Webhook 机器人技能)

[English](#english) | [中文](#chinese)

<a name="english"></a>
## English

A universal skill for OpenClaw to send messages to various webhook-based chat bots.
Supports **WeCom (企业微信)**, **DingTalk (钉钉)**, and **Feishu (飞书)**.

### Features
- **WeCom (企业微信)**: Send Text and Markdown messages.
- **DingTalk (钉钉)**: Send Text and Markdown messages with optional Secret signing.
- **Feishu (飞书)**: Send Text messages with optional Secret signing.

### Installation
This skill is usually installed via ClawHub or manually placed in the `skills/` directory.

### Usage

#### 1. WeCom (企业微信)
Script: `scripts/send_wecom.py`
```bash
python3 scripts/send_wecom.py --key "KEY" --markdown --content "Hello"
```

#### 2. DingTalk (钉钉)
Script: `scripts/send_dingtalk.py`
```bash
# Basic
python3 scripts/send_dingtalk.py --token "TOKEN" --content "Hello"

# With Secret (Sign)
python3 scripts/send_dingtalk.py --token "TOKEN" --secret "SECRET" --content "Hello"
```

#### 3. Feishu (飞书)
Script: `scripts/send_feishu.py`
```bash
# Basic
python3 scripts/send_feishu.py --token "TOKEN" --content "Hello"

# With Secret (Sign)
python3 scripts/send_feishu.py --token "TOKEN" --secret "SECRET" --content "Hello"
```

---

<a name="chinese"></a>
## 中文 (Chinese)

一个用于 OpenClaw 的通用技能，用于向各种基于 Webhook 的聊天机器人发送消息。
支持 **企业微信**、**钉钉** 和 **飞书**。

### 功能特性
- **企业微信**: 支持文本和 Markdown。
- **钉钉**: 支持文本和 Markdown，支持加签 (Secret)。
- **飞书**: 支持文本消息，支持加签 (Secret)。

### 使用方法

#### 1. 企业微信 (WeCom)
```bash
python3 scripts/send_wecom.py --key "你的key" --markdown --content "你好"
```

#### 2. 钉钉 (DingTalk)
```bash
# 基础用法
python3 scripts/send_dingtalk.py --token "你的access_token" --content "你好"

# 加签模式
python3 scripts/send_dingtalk.py --token "你的access_token" --secret "你的secret" --content "你好"
```

#### 3. 飞书 (Feishu)
```bash
# 基础用法
python3 scripts/send_feishu.py --token "你的token" --content "你好"

# 加签模式
python3 scripts/send_feishu.py --token "你的token" --secret "你的secret" --content "你好"
```
