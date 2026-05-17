# Catálogo de Fontes — Grupo 1

## 1. Objetivo

O catálogo de fontes registra a origem, a confiabilidade, a cobertura e o estado de validação das fontes usadas pelo Grupo 1.

Nenhum CSV deve ser considerado validado sem uma fonte registrada neste catálogo.

## 2. Arquivo Principal

O catálogo deve ser mantido no arquivo:

```txt
/metadata/catalogo_fontes.csv
```

## 3. Campos Mínimos

```csv
fonte_id,tema,nome_dataset,origem,entidade_responsavel,url_fonte,data_acesso,periodo_coberto,cobertura_geografica,formato_original,licenca_uso,status_validacao,responsavel_coleta,observacoes
```

## 4. Dicionário dos Campos

| Campo | Obrigatório | Descrição | Exemplo |
|---|---:|---|---|
| `fonte_id` | Sim | Identificador único da fonte | `FONTE_001` |
| `tema` | Sim | Tema ao qual a fonte está associada | `habitacao` |
| `nome_dataset` | Sim | Nome do dataset ou tabela | `Índice de preços da habitação` |
| `origem` | Sim | Plataforma, portal ou base consultada | `INE` |
| `entidade_responsavel` | Sim | Instituição responsável pelo dado | `Instituto Nacional de Estatística` |
| `url_fonte` | Sim | Link direto ou página de acesso | `https://...` |
| `data_acesso` | Sim | Data em que a fonte foi consultada | `2026-05-17` |
| `periodo_coberto` | Sim | Intervalo temporal dos dados | `2015-2024` |
| `cobertura_geografica` | Sim | País, região, distrito ou município | `Portugal` |
| `formato_original` | Sim | Formato em que o dado foi encontrado | `CSV`, `XLSX`, `API`, `HTML` |
| `licenca_uso` | Sim | Condição de uso ou licença declarada | `Dados públicos` |
| `status_validacao` | Sim | Estado atual da fonte | `encontrada`, `em_validacao`, `validada`, `rejeitada` |
| `responsavel_coleta` | Sim | Pessoa que encontrou ou coletou a fonte | `Nome` |
| `observacoes` | Não | Limitações, notas ou decisões | `Sem granularidade municipal` |

## 5. Status de Validação da Fonte

| Status | Significado |
|---|---|
| `encontrada` | Fonte identificada, mas ainda não analisada |
| `em_validacao` | Fonte em análise técnica |
| `validada` | Fonte aprovada para uso no projeto |
| `rejeitada` | Fonte descartada com justificativa |

## 6. Critérios de Validação

Uma fonte pode ser validada quando:

- possui entidade responsável identificável;
- possui URL acessível;
- tem período coberto claro;
- tem cobertura geográfica compatível com o projeto;
- permite extração ou consulta dos dados;
- tem licença ou condição de uso minimamente verificável;
- não apresenta limitações críticas para a análise proposta.

## 7. Exemplo de Registro

```csv
FONTE_001;habitacao;Índice de preços da habitação;INE;Instituto Nacional de Estatística;https://www.ine.pt;2026-05-17;2015-2024;Portugal;CSV;Dados públicos;em_validacao;Lucas;Fonte útil para análise nacional
```

## 8. Regras

- Cada fonte deve possuir um `fonte_id` único.
- Uma fonte rejeitada não deve ser apagada; deve permanecer registrada com justificativa.
- O `fonte_id` deve aparecer nos CSVs derivados da fonte.
- Sempre que uma fonte for atualizada, registrar a nova data de acesso.
