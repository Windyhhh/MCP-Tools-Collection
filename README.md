<div align="center">

# MCP 工具集 | MCP-Tools-Collection

### A collection of MCP (Model Context Protocol) servers.

Multiple Model Context Protocol server implementations and agent rules for building tool-connected AI apps.

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/JavaScript)
[![MCP](https://img.shields.io/badge/MCP-SDK-blue)](https://modelcontextprotocol.io/)

</div>

---

**MCP-Tools-Collection** is a collection of **Model Context Protocol (MCP)** server implementations, plus curated agent rules for building tool-connected AI applications.

> [!NOTE]
> 中文项目：多种 MCP（模型上下文协议）服务器实现——构建可接入 AI 智能体的工具生态。

---

## Quickstart

```bash
git clone https://github.com/Windyhhh/MCP-Tools-Collection.git
cd MCP-Tools-Collection

# Explore the bundled agent rules
ls agent-rules-main/docs/

# follow the MCP best-practices docs to build your own server
```

---

## Features

- **MCP servers** — multiple implementations.
- **Agent rules** — MCP best practices, releasing, and app-kit guidance.
- **AI tool ecosystem** — connect models to external tools.

---

## Project Structure

```
MCP-Tools-Collection/
├── agent-rules-main/          # MCP + agent best-practices docs (mcp-best-practices, mcp-releasing, ...)
└── README.md
```

---

## 技术实现细节

### 架构概览

项目采用模块化设计，核心目录包括：**agent-rules-main, mcp-feedback-enhanced-main**。

### 核心类与模块

- **WebUIManager**

### 关键函数

- `preload_i18n`, `init_encoding`, `is_wsl_environment`, `is_remote_environment`

### 技术栈与依赖

**核心框架/库**：FastAPI

**主要 import**：
```python
import asyncio
import concurrent.futures
import os
import threading
import time
import uuid
from datetime import datetime
from pathlib import Path
from typing import Any
import uvicorn
```

### 实现要点

- 以 `WebUIManager` 为核心类，封装主要业务逻辑
- 通过 `preload_i18n` 等函数实现核心流程编排
- 基于 FastAPI 构建，技术栈成熟稳定
- 代码结构清晰，模块间低耦合，便于扩展和维护

---
## License

MIT — free to use, modify and distribute.
