# Dicionário de Dados

Este documento define o padrão oficial de entrega dos CSVs produzidos pelo Grupo 1 para uso pelo Grupo 2 no dashboard e pelo Grupo 3 na validação de conteúdo.

O padrão deve ser aplicado antes de qualquer coleta em volume. Mudanças futuras precisam ser registradas em issue, Pull Request e no histórico de decisões.

## Padrão de arquivo

| Parâmetro | Valor oficial |
| --- | --- |
| Encoding | UTF-8 sem BOM |
| Separador | Ponto e vírgula `;` |
| Decimal | Ponto `.` |
| Separador de milhar | Não usar |
| Data | ISO 8601 `YYYY-MM-DD` |
| Nulos | Célula vazia |
| Cabeçalhos | `snake_case`, em inglês, sem acentos e sem espaços |
| Extensão | `.csv` |

Exemplo correto:

```csv
year;country;region;indicator;value;unit;source_id;updated_at
2024;Portugal;Lisboa;resident_foreign_population;1234567;people;FONTE-002;2026-05-27
2024;Portugal;Lisboa;unemployment_rate;6.8;percent;FONTE-008;2026-05-27
```

Exemplo incorreto:

```csv
Ano,País,Região,Nº Residentes,Taxa de Desemprego (%)
2024,Portugal,Lisboa,1.234.567,6,8
```

## Campos mínimos recomendados

Os datasets podem ter colunas específicas, mas devem incluir os campos abaixo sempre que forem aplicáveis ao indicador.

| Campo | Obrigatório quando aplicável | Descrição |
| --- | --- | --- |
| `record_id` | Sim | Identificador único da linha. |
| `source_id` | Sim | ID da fonte no catálogo oficial `metadata/catalogo_fontes.csv`. |
| `year` | Sim | Ano de referência. |
| `period` | Quando houver recorte não anual | Período de referência, como mês, trimestre ou intervalo. |
| `date` | Quando o dado for diário ou mensal | Data em `YYYY-MM-DD`. |
| `country` | Sim | País de referência. |
| `region` | Quando houver recorte territorial | Região, NUTS, distrito ou outra divisão territorial. |
| `municipality` | Quando houver recorte municipal | Município. |
| `indicator` | Sim | Nome normalizado do indicador. |
| `value` | Sim | Valor observado. |
| `unit` | Sim | Unidade de medida. |
| `category` | Quando houver segmentação | Categoria principal. |
| `subcategory` | Quando houver segmentação adicional | Subcategoria. |
| `updated_at` | Sim | Data de coleta, atualização ou acesso ao dado. |

## Template de log de coleta

Cada CSV entregue em `data/processed/` ou `data/validated/` deve ter um log correspondente em `data/processed/logs/` ou `data/validated/logs/`.

```txt
FICHEIRO: residents_by_nationality_2024.csv
FONTE: AIMA - Relatório de Imigração e Asilo 2024
URL: https://www.aima.gov.pt/...
DATA DE COLETA: 2026-05-27
PERÍODO DOS DADOS: 2015-2024
TRANSFORMAÇÕES APLICADAS:
  - Removidas linhas de totais e subtotais
  - Coluna "País de origem" renomeada para "nationality"
  - Valores monetários convertidos de milhares para euros
LIMITAÇÕES CONHECIDAS:
  - Dados de 2024 podem ser preliminares
RESPONSÁVEL: [nome do estagiário]
```

## Registro no catálogo e no dicionário

Todo CSV deve referenciar uma fonte existente em:

```txt
metadata/catalogo_fontes.csv
```

Todo CSV validado deve ter suas colunas registradas em:

```txt
metadata/dicionario_dados.csv
```

Enquanto ainda não houver datasets reais validados, `metadata/dicionario_dados.csv` deve manter apenas o cabeçalho oficial. Exemplos de preenchimento ficam na documentação, não no arquivo operacional.

## Datasets mapeados

| Ficheiro | Fonte | Período | Colunas principais | Estado |
| --- | --- | --- | --- | --- |
| A selecionar | A selecionar | A selecionar | A selecionar | A selecionar em G1-006 |

## Confirmação com Grupo 2

Decisão registrada até 27/05/2026:

| Item | Estado |
| --- | --- |
| Ferramenta de dashboard | Looker Studio |
| Fluxo esperado | CSV -> Google Sheets -> Looker Studio |
| Separador oficial atual | `;` |
| Pendência | Juliana confirmar importação via Google Sheets, separador final e campos obrigatórios do dashboard |

Se o Grupo 2 confirmar necessidade técnica de vírgula, esta página, `docs/grupo-1/padrao-csv.md` e `metadata/dicionario_dados.csv` devem ser atualizados via nova issue e Pull Request antes da coleta em volume.
