# 📊 Spreadsheet Importer

Lambda para importar **XLSX/CSV**, transformar linhas em registros e enviar para:
- **Integração (Lambda)** via `INTEGRATION_URL`
- **Direto ao Flowch** via `x-endpoint-url`

!!! tip "Por que usar?"
    `x-limit`, `x-dry-run`, `x-preview`, logs de performance e parsing robusto para CSV/XLSX.

## Recursos
- `.xlsx` (ExcelJS) e `.csv` (delimitador auto: `;`, `,`, `\t`, `|`)
- 1ª linha = **cabeçalho obrigatório** (sem duplicatas/sem nomes vazios)
- Limites: **10.000** linhas, **200** colunas, **5MB**
- Tipos:
  - `true/false` → **boolean**
  - `Date` → **ISO** (`2025-01-31T00:00:00.000Z`)
  - Números/texto → **string** (ex.: `"10,2"`)

## Fluxo
1. Recebe arquivo (multipart) ou base64 (JSON).
2. Converte para `Array<Object>`.
3. Envia para Integração **ou** Flowch em **lotes**.
4. Retorna resumo + métricas.
