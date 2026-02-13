# Security Audit Report — AgentAudit

**Package:** @microsoft/workiq (microsoft/work-iq-mcp)  
**Version:** 0.2.8  
**Date:** 2026-02-13  
**Result:** ✅ Safe (risk score: 0)  
**Report ID:** [#445](https://www.agentaudit.dev)

## Summary

This repository contains only documentation, configuration (`server.json`), and EULA files for the proprietary `@microsoft/workiq` MCP server. No source code is present — the implementation is closed-source and distributed via npm.

**No security findings were identified** in the auditable materials (documentation, configuration, metadata).

## Scope

- All non-EULA files in the repository were reviewed
- Package type: `mcp-server` (MCP Server wrapping Microsoft 365 Copilot API)
- No executable code, scripts, or build hooks found in this repository

## Notes

- Source code audit of the npm binary was not possible (proprietary/closed-source)
- The `server.json` MCP manifest and documentation are consistent and well-structured
- OAuth2 permissions are clearly documented in `ADMIN-INSTRUCTIONS.md`

---
*Automated audit by [AgentAudit](https://www.agentaudit.dev)*
