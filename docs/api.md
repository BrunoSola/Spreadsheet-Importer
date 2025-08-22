# 🔌 API / Headers

## Comuns
- `Authorization`: token do Flowch (**obrigatório**)
- `x-limit`: processar só N linhas
- `x-dry-run`: `true|false`
- `x-preview`: `true|false`
- `x-log-progress`: `true|false`

## Modo Integração
- `endpoint`: nome lógico (**obrigatório**)
- Env: `INTEGRATION_URL`

## Modo Direto (Flowch)
- `x-endpoint-url`: URL completa (**obrigatório**)
- `x-batch-size`: inteiro > 0 (default 20)
