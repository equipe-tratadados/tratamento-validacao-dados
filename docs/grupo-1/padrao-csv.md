# Padrão de CSV

## Objetivo

Definir o padrão mínimo para arquivos CSV produzidos pelo Grupo 1.

O objetivo é garantir que os dados possam ser usados pelos Grupos 2 e 3 sem retrabalho básico de encoding, separador, nomeação, fonte ou dicionário de dados.

O contrato completo de entrega está publicado na raiz do repositório:

```txt
DICIONARIO_DE_DADOS.md
```

## Estrutura das pastas de dados

| Pasta | Uso |
| --- | --- |
| `data/raw/` | Dados originais ou minimamente alterados. |
| `data/processed/` | Dados tratados, limpos e padronizados. |
| `data/validated/` | Dados revisados e prontos para uso pelo Grupo 2 e Grupo 3. |

## Fluxo obrigatório

```txt
fonte pública → data/raw → data/processed → data/validated
```

## Formato oficial

Todos os CSVs devem seguir o padrão abaixo.

| Parâmetro | Valor |
| --- | --- |
| Encoding | UTF-8 sem BOM |
| Separador | Ponto e vírgula `;` |
| Decimal | Ponto `.` |
| Separador de milhar | Não usar |
| Data | `YYYY-MM-DD` |
| Nulos | Célula vazia |
| Cabeçalhos | `snake_case`, em inglês, sem acentos e sem espaços |

## Nome de arquivo

Usar `snake_case` ou `kebab-case`. Não usar espaços, acentos ou caracteres especiais.

Formato recomendado:

```txt
tema_fonte_periodo_status.csv
```

Status permitidos:

| Status | Uso |
| --- | --- |
| `raw` | Arquivo bruto ou minimamente alterado. |
| `processed` | Arquivo tratado e padronizado. |
| `validated` | Arquivo validado e pronto para uso. |

## Exemplos corretos

```txt
inflacao_ine_2020_2024_raw.csv
inflacao_ine_2020_2024_processed.csv
inflacao_ine_2020_2024_validated.csv
salarios_pordata_2015_2023_raw.csv
habitacao_ine_2011_2024_validated.csv
```

## Exemplos incorretos

```txt
Dados finais.csv
inflação INE.xlsx
base nova final 2.csv
arquivo_teste.csv
```

## Campos mínimos recomendados

Sempre que fizer sentido para o dataset, usar os seguintes campos:

| Campo | Descrição |
| --- | --- |
| `record_id` | Identificador único da linha. |
| `source_id` | ID da fonte registrada no catálogo de fontes. |
| `year` | Ano de referência. |
| `period` | Período de referência, quando aplicável. |
| `date` | Data em `YYYY-MM-DD`, quando aplicável. |
| `country` | País. |
| `region` | Região, NUTS ou outra divisão territorial. |
| `municipality` | Município, quando aplicável. |
| `indicator` | Nome do indicador. |
| `value` | Valor observado. |
| `unit` | Unidade de medida. |
| `category` | Categoria principal. |
| `subcategory` | Subcategoria, quando aplicável. |
| `updated_at` | Data de atualização ou acesso ao dado. |

## Regras para arquivos pesados

Se o arquivo for grande demais para versionamento simples no GitHub:

1. não fazer commit direto sem avisar;
2. registrar a fonte e o link de download;
3. documentar o motivo no README do dataset;
4. avaliar compressão ou recorte mínimo útil;
5. pedir validação do líder antes de subir.

## Regras para substituição de arquivos

Não substituir arquivo validado sem registrar motivo.

Se for necessário substituir:

1. abrir uma task com ID;
2. explicar o motivo;
3. manter registro no Pull Request;
4. atualizar dicionário de dados, se houver mudança de colunas;
5. atualizar checklist de validação.

## Regra de fonte

Todo CSV deve ter `source_id` associado a um `fonte_id` existente em:

```txt
metadata/catalogo_fontes.csv
```

## Regra de dicionário

Todo CSV validado deve ter colunas documentadas em:

```txt
metadata/dicionario_dados.csv
```
