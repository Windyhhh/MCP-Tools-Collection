# 🔧 MCP 工具集 | MCP Tools Collection

> **多种 Model Context Protocol (MCP) 服务器实现合集——文件、数据库、HTTP、系统工具等，接入 AI 智能体的标准化工具生态。**
>
> *A collection of Model Context Protocol (MCP) server implementations — file, database, HTTP, system tools, connecting standardized tool ecosystem to AI agents.*

---

## ⭐ 核心卖点 | Why Star This

| 卖点 | Feature | 一句话 |
|------|---------|--------|
| 🔌 **MCP 协议** | MCP Protocol | 基于 Model Context Protocol 标准 |
| 🧰 **多种服务器** | Multiple Servers | 文件、数据库、HTTP、系统多类型 |
| 🤖 **AI 集成** | AI Integration | 无缝接入 AI 智能体/助手 |
| 🛠️ **工具丰富** | Rich Tools | 丰富可用的工具函数集 |
| 📦 **即插即用** | Plug & Play | 标准化配置，快速接入 |

---

## 🏆 技术栈 | Tech Stack

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python)
![MCP SDK](https://img.shields.io/badge/MCP-SDK-blue?logo=modelcontextprotocol)
![FastAPI](https://img.shields.io/badge/FastAPI-0.100+-teal?logo=fastapi)
![Docker](https://img.shields.io/badge/Docker-24.0+-blue?logo=docker)

---

## 📂 服务器列表 | Server List

| 服务器 | 功能 | 工具 |
|--------|------|------|
| file-server | 文件操作 | read/write/list/search |
| db-server | 数据库访问 | query/execute/schema |
| http-server | HTTP 请求 | get/post/request |
| system-server | 系统操作 | exec/time/info |
| search-server | 搜索 | web_search/file_search |
| util-server | 工具集 | parse/convert/hash |

---

## 🚀 快速开始 | Quick Start

```bash
git clone https://github.com/Windyhhh/MCP-Tools-Collection.git
cd MCP-Tools-Collection

# 1. 安装依赖
pip install -r requirements.txt

# 2. 启动文件 MCP 服务器
python servers/file_server.py --port 9000

# 3. 启动数据库 MCP 服务器
python servers/db_server.py --config configs/db.yaml

# 4. 配置 AI 助手接入
# 将 MCP 服务器端点配置到 AI 智能体

# 5. Docker 一键启动
docker-compose up -d
```

---

## 🔬 核心实现 | Core Implementation

### MCP 服务器示例 | MCP Server Example

```python
# 基于 MCP SDK 的文件服务器
from mcp.server.fastmcp import FastMCP

mcp = FastMCP("FileServer")

@mcp.tool()
def read_file(path: str) -> str:
    """读取文件内容"""
    with open(path, 'r', encoding='utf-8') as f:
        return f.read()

@mcp.tool()
def write_file(path: str, content: str) -> str:
    """写入文件内容"""
    with open(path, 'w', encoding='utf-8') as f:
        f.write(content)
    return f"Written to {path}"

@mcp.tool()
def list_dir(path: str = ".") -> list:
    """列出目录内容"""
    import os
    return os.listdir(path)

if __name__ == "__main__":
    mcp.run()
```

---

## 🎯 应用场景 | Use Cases

- 🤖 **AI 智能体**：扩展 AI 工具能力
- 🔌 **工具标准化**：MCP 协议接入
- 🧰 **开发效率**：AI 辅助开发工具
- 🎓 **AI 工程**：MCP 生态开发实践

---

## 📄 License

MIT License — 自由使用、修改和分发。

---

> 💡 **多种 MCP 服务器实现，Star ⭐ 构建 AI 工具生态！**
