# 🧰 Troubleshooting

## Cabeçalho virou uma chave só
Delimitador detectado errado. O parser usa fallback pelo header; confirme que a linha 1 é o cabeçalho com `;` ou `,`.

## "Não" saiu "N�o"
Encoding do CSV. Parser tenta `UTF-8` e cai para `latin1` automaticamente.

## "10,2" virou 10.0
Alguma etapa converteu para número. O importador entrega `"10,2"` como **string** — evite `parseFloat` sem normalizar vírgula.

## Booleans viraram string
Cheque se etapas posteriores não fazem coerção. O importador preserva `true/false`.
