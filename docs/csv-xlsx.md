
### `docs/csv-xlsx.md`
```markdown
# 📄 CSV & XLSX

## CSV
- Delimitador auto (`;`, `,`, `\t`, `|`) com *fallback* pelo cabeçalho.
- Encoding: `UTF-8` → fallback `latin1` se houver “�”.
- Aspas RFC4180 (`"valor, com vírgula"`, escape `""`).
- Conversão:
  - `true/false` → **boolean**
  - Datas no CSV permanecem **string**
  - `10,2` → **"10,2"** (string; não arredonda)

## XLSX
- ExcelJS lendo a primeira planilha.
- Linha 1 = **cabeçalho** (sem duplicatas).
- `Date` → **ISO** (`toISOString()`).
- `true/false` → **boolean**.
- Números/texto → **string** (mantém `"10,2"`).
