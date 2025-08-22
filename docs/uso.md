# 🚀 Uso

## Upload via JSON (base64)
```bash
curl -X POST "$API_URL" \
  -H "Content-Type: application/json" \
  -H "Authorization: $FLOWCH_TOKEN" \
  -H "endpoint: recibo" \
  -H "x-limit: 5" \
  -d '{"filename":"dados.csv","contentType":"text/csv","base64":"<BASE64>"}'
