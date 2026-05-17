# Padrão de CSV

## Objetivo

Definir o padrão mínimo para arquivos CSV produzidos pelo Grupo 1.

O objetivo é garantir que os dados possam ser usados pelos Grupos 2 e 3 sem retrabalho básico de encoding, separador, nomeação, fonte ou dicionário de dados.

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

## Encoding

Todos os CSVs devem usar:

```txt
UTF-8
```

## Separador

Todos os CSVs devem usar ponto e vírgula:

```txt
;
```

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
| `id_registro` | Identificador único da linha. |
| `fonte_id` | ID da fonte registrada no catálogo de fontes. |
| `ano` | Ano de referência. |
| `periodo` | Período de referência, quando aplicável. |
| `pais` | País. |
| `regiao` | Região, NUTS ou outra divisão territorial. |
| `municipio` | Município, quando aplicável. |
| `indicador` | Nome do indicador. |
| `valor` | Valor observado. |
| `unidade` | Unidade de medida. |
| `categoria` | Categoria principal. |
| `subcategoria` | Subcategoria, quando aplicável. |
| `data_atualizacao` | Data de atualização ou acesso ao dado. |

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

Todo CSV deve ter `fonte_id` associado em:

```txt
metadata/catalogo_fontes.csv
```

## Regra de dicionário

Todo CSV validado deve ter colunas documentadas em:

```txt
metadata/dicionario_dados.csv
```
