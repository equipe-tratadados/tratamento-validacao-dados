# Padrão Inicial de CSVs Versionados

## 1. Objetivo

Garantir que todos os arquivos CSV do Grupo 1 tenham estrutura previsível, rastreável e reutilizável pelos Grupos 2 e 3.

Este padrão permite:

- rastrear a origem dos dados;
- diferenciar dados brutos, tratados e validados;
- reduzir retrabalho entre grupos;
- facilitar o uso dos arquivos em dashboards, análises e textos;
- manter histórico de alterações no GitHub.

## 2. Estrutura Recomendada de Pastas

```txt
/data
  /raw
    .gitkeep
  /processed
    .gitkeep
  /validated
    .gitkeep

/metadata
  catalogo_fontes.csv
  dicionario_dados.csv

/docs
  /grupo-1
    padrao-csv.md
    catalogo-fontes.md
    dicionario-dados.md
    checklist-validacao.md
```

## 3. Camadas dos Dados

| Camada | Pasta | Descrição |
|---|---|---|
| Raw | `/data/raw` | Arquivo original ou minimamente alterado |
| Processed | `/data/processed` | Arquivo tratado, limpo ou padronizado |
| Validated | `/data/validated` | Arquivo validado para uso pelo dashboard/texto |

## 4. Padrão de Nome dos Arquivos

```txt
tema_fonte_periodo_status.csv
```

### 4.1 Componentes do Nome

| Campo | Descrição | Exemplo |
|---|---|---|
| `tema` | Tema principal do dataset | `habitacao` |
| `fonte` | Entidade ou base de origem | `ine`, `pordata`, `eurostat` |
| `periodo` | Ano ou intervalo coberto | `2020_2024` |
| `status` | Estado do arquivo | `raw`, `processed`, `validated` |

### 4.2 Exemplos

```txt
habitacao_ine_2020_2024_raw.csv
habitacao_ine_2020_2024_processed.csv
habitacao_pordata_2015_2023_validated.csv
```

## 5. Status Permitidos

| Status | Uso |
|---|---|
| `raw` | Arquivo original ou minimamente alterado |
| `processed` | Arquivo tratado, limpo, renomeado ou normalizado |
| `validated` | Arquivo validado para uso por dashboard ou texto |

## 6. Campos Mínimos Recomendados nos CSVs de Dados

```csv
id_registro,fonte_id,ano,periodo,pais,regiao,municipio,indicador,valor,unidade,categoria,subcategoria,data_atualizacao
```

## 7. Descrição dos Campos Mínimos

| Campo | Obrigatório | Descrição | Exemplo |
|---|---:|---|---|
| `id_registro` | Sim | Identificador único da linha | `hab_ine_000001` |
| `fonte_id` | Sim | Chave da fonte registrada no catálogo | `FONTE_001` |
| `ano` | Sim, se aplicável | Ano de referência do dado | `2024` |
| `periodo` | Sim | Período coberto pelo registro | `2020-2024`, `T1-2024` |
| `pais` | Sim | País do dado | `Portugal` |
| `regiao` | Não | Região, distrito, NUTS ou equivalente | `Norte` |
| `municipio` | Não | Município, se existir granularidade local | `Porto` |
| `indicador` | Sim | Nome do indicador medido | `preco_medio_habitacao` |
| `valor` | Sim | Valor observado | `235000` |
| `unidade` | Sim | Unidade de medida | `EUR`, `%`, `habitantes` |
| `categoria` | Não | Categoria analítica principal | `mercado_imobiliario` |
| `subcategoria` | Não | Recorte secundário | `compra` |
| `data_atualizacao` | Não | Data em que o registro foi atualizado | `2026-05-17` |

## 8. Regras de Versionamento

- Não substituir arquivos sem histórico.
- Não alterar CSV validado sem registrar o motivo.
- Toda fonte deve estar documentada no catálogo de fontes.
- Todo CSV deve possuir um `fonte_id` correspondente.
- Arquivos `raw` devem preservar ao máximo a estrutura original.
- Arquivos `processed` devem registrar alterações relevantes.
- Arquivos `validated` devem estar prontos para uso pelos Grupos 2 e 3.

## 9. Regras de Formatação

| Item | Padrão |
|---|---|
| Encoding | UTF-8 |
| Separador | Ponto e vírgula (`;`) |
| Cabeçalho | Obrigatório |
| Nome de campos | `snake_case` |
| Datas | `YYYY-MM-DD` |
| Decimal | Ponto (`.`), salvo exigência contrária da fonte |
| Valores ausentes | Campo vazio ou `null`, conforme decisão do dataset |

## 10. Critério de Aceite

Um CSV só será aceito quando:

- estiver na pasta correta;
- seguir o padrão de nome definido;
- possuir cabeçalho;
- possuir `fonte_id` documentado;
- tiver origem registrada no catálogo de fontes;
- indicar período e cobertura geográfica;
- estiver legível em UTF-8;
- tiver separador padronizado;
- não apresentar colunas sem explicação no dicionário de dados, quando for arquivo `processed` ou `validated`.
