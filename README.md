# Microsoft WorkIQ (Public Preview)

> Query your Microsoft 365 data with natural language — emails, meetings, documents, Teams messages, and more.

[![npm version](https://img.shields.io/npm/v/@microsoft/workiq)](https://www.npmjs.com/package/@microsoft/workiq)

WorkIQ is a CLI and an MCP (Model Context Protocol) server that connects AI assistants to your Microsoft 365 Copilot data. Ask questions like *"What did my manager say about the project deadline?"* or *"Find my recent documents about Q4 planning."*

> ⚠️ **Public Preview:** Features and APIs may change.

---

## 🚀 Quick Start with GitHub Copilot CLI

The fastest way to get started is with GitHub Copilot CLI:

```bash
# 1. Open GitHub Copilot CLI
copilot

# 2. Add the plugins marketplace (one-time setup)
/plugins marketplace add github/copilot-plugins

# 3. Install WorkIQ
/plugin install workiq@copilot-plugins
```

**That's it!** Restart Copilot CLI and start querying your M365 data:

```
You: What are my upcoming meetings this week?
You: Summarize emails from Sarah about the budget
You: Find documents I worked on yesterday
```

---

## 📦 Alternative: Standalone Installation

[![Install in VS Code](https://img.shields.io/badge/VS_Code-Install_Server-0098FF?style=flat-square&logo=visualstudiocode&logoColor=white)](https://vscode.dev/redirect/mcp/install?name=workiq&config=%7B%22command%22%3A%22npx%22%2C%22args%22%3A%5B%22-y%22%2C%22%40microsoft%2Fworkiq%22%2C%22mcp%22%5D%7D)
[![Install in VS Code Insiders](https://img.shields.io/badge/VS_Code_Insiders-Install_Server-24bfa5?style=flat-square&logo=visualstudiocode&logoColor=white)](https://insiders.vscode.dev/redirect/mcp/install?name=workiq&config=%7B%22command%22%3A%22npx%22%2C%22args%22%3A%5B%22-y%22%2C%22%40microsoft%2Fworkiq%22%2C%22mcp%22%5D%7D&quality=insiders)

If you prefer to run WorkIQ as a standalone MCP server:

```bash
# Install globally
npm install -g @microsoft/workiq

# Run the MCP server
workiq mcp
```

Or use npx without installing:

```bash
npx -y @microsoft/workiq mcp
```

Or add it as a MCP server in your coding agent or IDE:

```json
{
  "workiq": {
    "command": "npx",
    "args": [
      "-y",
      "@microsoft/workiq",
      "mcp"
    ],
    "tools": [
      "*"
    ]
  }
}
```

---

## 🎯 What You Can Query

| Data Type | Example Questions |
|-----------|-------------------|
| **Emails** | "What did John say about the proposal?" |
| **Meetings** | "What's on my calendar tomorrow?" |
| **Documents** | "Find my recent PowerPoint presentations" |
| **Teams** | "Summarize today's messages in the Engineering channel" |
| **People** | "Who is working on Project Alpha?" |

---

## 📖 CLI Reference

### Commands

| Command | Description |
|---------|-------------|
| `workiq accept-eula` | Accept the End User License Agreement (EULA) |
| `workiq ask` | Ask a question to a specific agent or run in interactive mode |
| `workiq mcp` | Start MCP stdio server for agent communication |
| `workiq version` | Show version information |

### Global Options

| Option | Description | Default |
|--------|-------------|---------|
| `-p, --protocol <protocol>` | Protocol to use | `rest` |
| `-t, --tenant-id <tenant-id>` | The Entra tenant ID to use for authentication | `common` |
| `--version` | Show version information | |
| `-?, -h, --help` | Show help and usage information | |

### `workiq ask` Options

| Option | Description |
|--------|-------------|
| `-q, --question <question>` | The question to ask the agent |

### Examples

```bash
# Accept the EULA (required on first use)
workiq accept-eula

# Interactive mode
workiq ask

# Ask a specific question
workiq ask -q "What meetings do I have tomorrow?"

# Use a specific tenant
workiq ask -t "your-tenant-id" -q "Show my emails"

# Start MCP server
workiq mcp
```

---

## 📄 License

By using this package, you accept the license agreement. See [NOTICES.TXT](https://github.com/microsoft/work-iq-mcp) and EULA within the package for legal terms.
