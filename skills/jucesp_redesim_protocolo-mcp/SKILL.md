---
name: jucesp_redesim_protocolo-mcp
description: Skill da REST API do JUCESP: REDESIM, Acompanhamento de Protocolo na MCP.AI: 1 endpoint em /api/jucesp_redesim_protocolo. Acompanha o andamento de um protocolo REDESIM na JUCESP (abertura, alteração ou baixa de empresa). Hospedado pela plataforma, sem credenciais, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# JUCESP: REDESIM, Acompanhamento de Protocolo — REST API skill

Você tem acesso à **JUCESP: REDESIM, Acompanhamento de Protocolo** REST API na MCP.AI.

> Acompanha o andamento de um protocolo REDESIM na JUCESP (abertura, alteração ou baixa de empresa). Hospedado pela plataforma, sem credenciais, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/jucesp_redesim_protocolo
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
curl -X POST https://api.mcp.ai/api/jucesp_redesim_protocolo/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"protocolo":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/jucesp_redesim_protocolo/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `jucesp_redesim_protocolo_consultar`

Acompanha o andamento de um protocolo REDESIM na JUCESP (abertura, alteração ou baixa de empresa). _(POST /api/jucesp_redesim_protocolo/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `protocolo` | string | Sim | Parâmetro de consulta "protocolo". |
| `login_cpf` | string | Não | Parâmetro de consulta "login_cpf". |
| `login_senha` | string | Não | Parâmetro de consulta "login_senha". |
| `pkcs12_cert` | string | Não | Parâmetro de consulta "pkcs12_cert". |
| `pkcs12_pass` | string | Não | Parâmetro de consulta "pkcs12_pass". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_jucesp_redesim_protocolo` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
