# Instalação detalhada

INCRA SIGEF: Planta é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_incra_sigef_planta`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_incra_sigef_planta` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_incra_sigef_planta` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_incra_sigef_planta` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.incra_sigef_planta` (ou `servers.incra_sigef_planta` no VS Code) do config do cliente e reinicie.
