# Microsoft WorkIQ (Public Preview)

MCP (Model Context Protocol) server for interacting with Microsoft 365 Copilot.

By using this package you are accepting license agreement linked below.

## Installation

```bash
npm install -g @microsoft/workiq
```

## Usage

To run MCP server, use `workiq mcp` command. You will be prompted to provide your M365 Copilot credentials when you run it for the first time.

Alternatively you can run with npx command

```bash
npx @microsoft/workiq mcp
```

## GitHub Copilot CLI Integration

To use this MCP server with GitHub Copilot CLI, add it to your configuration:

### Using `gh copilot config` (Recommended)

```bash
gh copilot config mcp add @microsoft/workiq
```

### Manual Configuration

Alternatively, edit your Copilot CLI configuration file:

**Windows**: `%APPDATA%\GitHub Copilot\config.json`  
**macOS/Linux**: `~/.config/github-copilot/config.json`

Add the following to the `mcpServers` section:

```json
{
  "mcpServers": {
    "@microsoft/workiq": {
      "command": "npx",
      "args": ["@microsoft/workiq", "mcp"]
    }
  }
}
```

After configuration, restart GitHub Copilot CLI to load the MCP server.

## License

See NOTICES.TXT and EULA for the information about licensing.