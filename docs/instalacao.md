# Instalação detalhada

JUCESP: REDESIM, Acompanhamento de Protocolo é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_jucesp_redesim_protocolo`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_jucesp_redesim_protocolo` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_jucesp_redesim_protocolo` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_jucesp_redesim_protocolo` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.jucesp_redesim_protocolo` (ou `servers.jucesp_redesim_protocolo` no VS Code) do config do cliente e reinicie.
