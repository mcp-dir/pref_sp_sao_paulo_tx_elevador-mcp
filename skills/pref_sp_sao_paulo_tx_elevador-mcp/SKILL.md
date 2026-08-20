---
name: pref_sp_sao_paulo_tx_elevador-mcp
description: Skill da REST API do Prefeitura SP São Paulo: 2ª Via da Taxa de Elevadores na MCP.AI: 1 endpoint em /api/pref_sp_sao_paulo_tx_elevador. Prefeitura SP São Paulo: 2ª Via da Taxa de Elevadores, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Prefeitura SP São Paulo: 2ª Via da Taxa de Elevadores — REST API skill

Você tem acesso à **Prefeitura SP São Paulo: 2ª Via da Taxa de Elevadores** REST API na MCP.AI.

> Prefeitura SP São Paulo: 2ª Via da Taxa de Elevadores, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/pref_sp_sao_paulo_tx_elevador
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
curl -X POST https://api.mcp.ai/api/pref_sp_sao_paulo_tx_elevador/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"data_vencimento":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/pref_sp_sao_paulo_tx_elevador/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `pref_sp_sao_paulo_tx_elevador_consultar`

Prefeitura SP São Paulo: 2ª Via da Taxa de Elevadores, consulta em fonte oficial. _(POST /api/pref_sp_sao_paulo_tx_elevador/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `chapa` | string | Não | Parâmetro de consulta "chapa". |
| `guia` | string | Não | Parâmetro de consulta "guia". |
| `data_vencimento` | string | Sim | Parâmetro de consulta "data_vencimento". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_pref_sp_sao_paulo_tx_elevador` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
