---
name: incra_sigef_planta-mcp
description: Skill da REST API do INCRA SIGEF: Planta na MCP.AI: 1 endpoint em /api/incra_sigef_planta. INCRA SIGEF: Planta, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# INCRA SIGEF: Planta — REST API skill

Você tem acesso à **INCRA SIGEF: Planta** REST API na MCP.AI.

> INCRA SIGEF: Planta, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/incra_sigef_planta
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/incra_sigef_planta/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"codigo_parcela":"...","login_cpf":"...","login_senha":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/incra_sigef_planta/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `incra_sigef_planta_consultar`

INCRA SIGEF: Planta, consulta em fonte oficial. _(POST /api/incra_sigef_planta/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `codigo_parcela` | string | Sim | Parâmetro de consulta "codigo_parcela". |
| `escala` | string | Não | Parâmetro de consulta "escala". |
| `login_cpf` | string | Sim | Parâmetro de consulta "login_cpf". |
| `login_senha` | string | Sim | Parâmetro de consulta "login_senha". |
| `pkcs12_cert` | string | Não | Parâmetro de consulta "pkcs12_cert". |
| `pkcs12_pass` | string | Não | Parâmetro de consulta "pkcs12_pass". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_incra_sigef_planta` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
