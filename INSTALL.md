# Instalação rápida

JUCESP: REDESIM, Acompanhamento de Protocolo é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_jucesp_redesim_protocolo`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `JUCESP: REDESIM, Acompanhamento de Protocolo` / `https://api.mcp.ai/p_jucesp_redesim_protocolo`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "jucesp_redesim_protocolo": { "type": "http", "url": "https://api.mcp.ai/p_jucesp_redesim_protocolo" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=jucesp_redesim_protocolo&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9qdWNlc3BfcmVkZXNpbV9wcm90b2NvbG8ifQ==)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "jucesp_redesim_protocolo": { "url": "https://api.mcp.ai/p_jucesp_redesim_protocolo" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=jucesp_redesim_protocolo&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_jucesp_redesim_protocolo%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "jucesp_redesim_protocolo": { "type": "http", "url": "https://api.mcp.ai/p_jucesp_redesim_protocolo" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_jucesp_redesim_protocolo
```

Dúvidas? [jucesp_redesim_protocolo@mcp.ai](mailto:jucesp_redesim_protocolo@mcp.ai)
