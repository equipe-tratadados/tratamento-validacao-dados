# Dicionário de Dados

## Objetivo

O dicionário de dados documenta as colunas dos datasets usados e produzidos pelo Grupo 1.

Ele permite que os Grupos 2 e 3 entendam o significado, tipo, unidade e limitações de cada campo sem depender de explicações informais.

## Arquivo principal

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
DATASET-001;inflacao_ine_2020_2024_validated.csv;ano;inteiro;Ano de referência do indicador;ano;Sim;2024;Exemplo de preenchimento
```

## Campos mínimos recomendados para datasets

| Campo | Descrição |
| --- | --- |
| `id_registro` | Identificador único da linha. |
| `fonte_id` | ID da fonte no catálogo. |
| `ano` | Ano de referência. |
| `periodo` | Período de referência. |
| `pais` | País. |
| `regiao` | Região. |
| `municipio` | Município. |
| `indicador` | Indicador analisado. |
| `valor` | Valor observado. |
| `unidade` | Unidade de medida. |
| `categoria` | Categoria principal. |
| `subcategoria` | Subcategoria. |
| `data_atualizacao` | Data de acesso ou atualização. |

## Regra de validação

Um CSV em `data/validated/` só deve ser considerado pronto se as colunas principais estiverem documentadas no dicionário de dados.
