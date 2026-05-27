# Dicionário de Dados

## Objetivo

O dicionário de dados documenta as colunas dos datasets usados e produzidos pelo Grupo 1.

Ele permite que os Grupos 2 e 3 entendam o significado, tipo, unidade e limitações de cada campo sem depender de explicações informais.

## Documento normativo

O padrão completo de entrega dos CSVs está publicado na raiz do repositório:

```txt
DICIONARIO_DE_DADOS.md
```

Esse documento define encoding, separador, decimal, datas, nulos, cabeçalhos, campos mínimos e template de log de coleta.

## Arquivo operacional

O dicionário em CSV fica em:

```txt
metadata/dicionario_dados.csv
```

## Campos obrigatórios

| Campo | Descrição |
| --- | --- |
| `dataset_id` | ID do dataset. Exemplo: `DATASET-001`. |
| `arquivo` | Nome do arquivo CSV relacionado. |
| `coluna` | Nome da coluna. |
| `tipo_dado` | Tipo do dado: texto, inteiro, decimal, data, booleano etc. |
| `descricao` | Descrição objetiva da coluna. |
| `unidade` | Unidade de medida, quando aplicável. |
| `obrigatorio` | Sim ou Não. |
| `exemplo` | Exemplo de valor. |
| `observacoes` | Notas, limitações ou regras específicas. |

## Como documentar colunas

Para cada CSV validado:

1. criar ou identificar o `dataset_id`;
2. registrar o nome do arquivo;
3. listar cada coluna do CSV;
4. definir o tipo do dado;
5. escrever uma descrição curta;
6. informar unidade, quando aplicável;
7. marcar se a coluna é obrigatória;
8. adicionar exemplo de valor;
9. registrar observações relevantes.

## Exemplo de preenchimento

```csv
dataset_id;arquivo;coluna;tipo_dado;descricao;unidade;obrigatorio;exemplo;observacoes
DATASET-001;residents_by_nationality_validated.csv;year;inteiro;Ano de referência do indicador;ano;Sim;2024;Exemplo documental
```

O exemplo acima não deve permanecer em `metadata/dicionario_dados.csv`. Enquanto não houver datasets reais validados, o arquivo operacional deve manter apenas o cabeçalho.

## Campos mínimos recomendados para datasets

| Campo | Descrição |
| --- | --- |
| `record_id` | Identificador único da linha. |
| `source_id` | ID da fonte no catálogo. |
| `year` | Ano de referência. |
| `period` | Período de referência. |
| `date` | Data em `YYYY-MM-DD`, quando aplicável. |
| `country` | País. |
| `region` | Região. |
| `municipality` | Município. |
| `indicator` | Indicador analisado. |
| `value` | Valor observado. |
| `unit` | Unidade de medida. |
| `category` | Categoria principal. |
| `subcategory` | Subcategoria. |
| `updated_at` | Data de acesso ou atualização. |

## Regra de validação

Um CSV em `data/validated/` só deve ser considerado pronto se as colunas principais estiverem documentadas no dicionário de dados.
