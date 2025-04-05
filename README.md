# 🌐 Claude MCP Server Quickstart

A ready-to-use implementation of the [Model Context Protocol (MCP)](https://modelcontextprotocol.io/) server that integrates with Claude AI models.

## 🔍 Overview

This project provides a fully functional MCP server implementation that allows you to:

- Connect Claude AI models through a standardized protocol
- Process context-aware requests
- Handle model responses efficiently
- Streamline AI integrations in your applications

Built following the official [MCP Server Quickstart guide](https://modelcontextprotocol.io/quickstart/server).

## ✨ Features

- ✅ Complete MCP protocol implementation
- ✅ Claude AI model integration
- ✅ Context-aware request processing
- ✅ Streaming response support
- ✅ Easy configuration and setup
- ✅ Well-documented codebase

## 📋 Prerequisites

- Python 3.8+
- Access to Claude AI API credentials
- Basic understanding of REST APIs

## 🚀 Installation

```bash
# Clone the repository
git clone https://github.com/gabrieldsguilherme/mcp-server.git
cd mcp-server

# Create and activate virtual environment
uv venv
source .venv/bin/activate

# Install dependencies
uv add "mcp[cli]" httpx
```

## ⚙️ Configuration

### 1. Open your Claude Desktop configuration file

Open your Claude for Desktop App configuration at `~/Library/Application Support/Claude/claude_desktop_config.json` in a text editor. Make sure to create the file if it doesn’t exist.

### 2. Update your Claude Desktop configuration file

```json
{
    "mcpServers": {
        "weather": {
            "command": "/ABSOLUTE/PATH/TO/PARENT/FOLDER/uv",
            "args": [
                "--directory",
                "/ABSOLUTE/PATH/TO/PARENT/FOLDER/weather",
                "run",
                "weather.py"
            ]
        }
    }
}
```

This tells Claude for Desktop:

a. There’s an MCP server named “weather”

b. To launch it by running uv --directory /ABSOLUTE/PATH/TO/PARENT/FOLDER/weather run weather.py

### 3. Save the file and restart Claude for Desktop

## 📖 Usage

### 1. Ask Claude "What’s the weather in Sacramento?"

### 2. Ask Claude "What are the active weather alerts in Texas?"