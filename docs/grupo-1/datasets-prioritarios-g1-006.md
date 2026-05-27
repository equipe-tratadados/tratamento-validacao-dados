# Datasets Prioritários — G1-006

## Objetivo

Selecionar os 2 ou 3 datasets prioritários para a primeira coleta real da Sprint 1, após a conclusão do padrão CSV com o Grupo 2.

Esta entrega fecha a etapa de seleção. Ela não inicia coleta em volume, tratamento, validação final ou entrega de CSV para dashboard. A coleta real deve ser aberta em task própria, a partir da `G1-007`.

## Dependências Operacionais

| Dependência | Status | Evidência |
|---|---|---|
| `G1-005` — padrão CSV e Dicionário de Dados | Concluída | Issue [#17](https://github.com/equipe-tratadados/tratamento-validacao-dados/issues/17) e PR [#19](https://github.com/equipe-tratadados/tratamento-validacao-dados/pull/19). |
| `G1-006.1` — log padrão de entrega direta de fontes | Concluída | Issue [#20](https://github.com/equipe-tratadados/tratamento-validacao-dados/issues/20) e PR [#21](https://github.com/equipe-tratadados/tratamento-validacao-dados/pull/21). |
| Catálogo oficial de fontes | Concluído para esta etapa | `metadata/catalogo_fontes.csv` contém os `fonte_id` usados abaixo. |

## Critérios de Priorização

Os datasets abaixo foram escolhidos com base em:

- fonte pública disponível e confiável;
- possibilidade de export em CSV, Excel, API ou extração simples;
- período mínimo de 5 anos sempre que possível;
- aderência aos subtemas aprovados pelo Grupo 3;
- utilidade direta para teste inicial no Looker Studio pelo Grupo 2;
- existência de `fonte_id` no catálogo oficial.

## Seleção Oficial

### 1. `eu_immigration_flow_growth_2013_2023`

| Campo | Valor |
|---|---|
| Prioridade de coleta | 1 |
| Subtema | Comparação Portugal × Europa |
| Pergunta relacionada | Posição de Portugal no ranking europeu de crescimento do fluxo imigratório entre 2012 e 2023. |
| `fonte_id` | `FONTE-008` |
| Fonte | Eurostat immigration flow |
| Instituição | Eurostat |
| Link direto | <https://ec.europa.eu/eurostat/databrowser/view/tps00176/default/table?lang=en> |
| Período previsto | 2013–2023 para a primeira análise comparável, ajustável conforme disponibilidade por país. |
| Granularidade | Anual, por país. |
| Formato | Tabela Eurostat, export CSV/API. |
| Viabilidade | Alta |
| Limitação principal | O ranking não vem pronto. Será necessário calcular crescimento percentual ou CAGR. O período pode começar em 2013, não 2012, dependendo da disponibilidade final. |
| Próximo passo | Abrir `G1-007` para coletar o bruto via export/API Eurostat, calcular crescimento por país e salvar o arquivo original em `data/raw/`. |
| Uso pelo Grupo 2 | Ranking europeu e gráfico comparativo no Looker Studio. |
| Uso pelo Grupo 3 | Narrativa comparativa Portugal × Europa. |

**Motivo da escolha:** é o dataset mais limpo para iniciar a Sprint 1 porque tem fonte internacional confiável, estrutura tabular, export/API e uso direto em dashboard.

### 2. `portugal_resident_foreign_population_2000_2024`

| Campo | Valor |
|---|---|
| Prioridade de coleta | 2 |
| Subtema | Fluxo Imigratório × Crescimento Económico |
| Pergunta relacionada | Evolução do número de imigrantes residentes em Portugal entre 2010 e 2024. |
| `fonte_id` | `FONTE-001`; `FONTE-002` |
| Fonte | RIFA/SEF; RMA/AIMA |
| Instituição | Serviço de Estrangeiros e Fronteiras; Agência para a Integração, Migrações e Asilo |
| Links diretos | <https://sefstat.sef.pt/forms/relatorios.aspx>; <https://aima.gov.pt/pt/a-aima/relatorios-de-migracoes-e-asilo> |
| Período previsto | 2000–2022 via SEF/RIFA; 2023–2024 via AIMA/RMA. |
| Granularidade | Anual; nacional; por nacionalidade, género ou idade conforme relatório disponível. |
| Formato | Relatórios estatísticos, portal e PDF; possível extração manual/técnica. |
| Viabilidade | Alta |
| Limitação principal | Há quebra institucional e possível quebra metodológica entre SEF e AIMA. Parte relevante dos dados está em PDF/relatório, exigindo log de extração e revisão manual. |
| Próximo passo | Coletar relatórios/exports brutos, documentar a transição SEF/AIMA e montar uma série anual normalizada de residentes estrangeiros. |
| Uso pelo Grupo 2 | Série temporal principal de população estrangeira residente. |
| Uso pelo Grupo 3 | Base factual da narrativa central sobre evolução da imigração em Portugal. |

**Motivo da escolha:** responde diretamente ao eixo central do projeto e oferece uma série histórica longa, ainda que com maior custo de extração do que o Eurostat.

### 3. `portugal_gdp_vs_foreign_population_2010_2024`

| Campo | Valor |
|---|---|
| Prioridade de coleta | 3 |
| Subtema | Fluxo Imigratório × Crescimento Económico |
| Pergunta relacionada | Relação visual entre evolução da população estrangeira residente e PIB no mesmo período. |
| `fonte_id` | `FONTE-004`; `FONTE-005`; `FONTE-001`; `FONTE-002` |
| Fonte | INE Contas Nacionais; PORDATA PIB/população estrangeira; RIFA/SEF; RMA/AIMA |
| Instituições | INE; Fundação Francisco Manuel dos Santos/PORDATA; SEF; AIMA |
| Links diretos | <https://www.ine.pt>; <https://www.pordata.pt/portugal>; <https://sefstat.sef.pt/forms/relatorios.aspx>; <https://aima.gov.pt/pt/a-aima/relatorios-de-migracoes-e-asilo> |
| Período previsto | 2010–2024, conforme disponibilidade e revisão final das séries. |
| Granularidade | Anual, nacional. |
| Formato | Tabelas estatísticas INE/PORDATA e série migratória derivada das fontes SEF/AIMA. |
| Viabilidade | Alta |
| Limitação principal | O dataset cruza séries independentes. Deve ser tratado como comparação temporal/correlação visual, sem inferir causalidade entre imigração e PIB. |
| Próximo passo | Definir colunas mínimas (`year`, `foreign_resident_count`, `gdp_eur`, `gdp_growth_rate`, `source_id`, `notes`) e coletar as séries brutas antes do tratamento. |
| Uso pelo Grupo 2 | Linha temporal, gráfico indexado ou painel PIB × população estrangeira. |
| Uso pelo Grupo 3 | Apoio à narrativa económica com cautela metodológica explícita. |

**Motivo da escolha:** entrega a base mínima do Subtema 1 e permite um primeiro gráfico simples, compreensível e útil para o dashboard.

## Ordem de Coleta Recomendada

1. `eu_immigration_flow_growth_2013_2023` — começar pelo Eurostat porque é mais limpo, exportável e adequado ao teste inicial no Looker Studio.
2. `portugal_resident_foreign_population_2000_2024` — coletar em seguida porque sustenta a narrativa principal do projeto.
3. `portugal_gdp_vs_foreign_population_2010_2024` — montar depois que a série de população estrangeira estiver definida, evitando retrabalho no cruzamento com PIB.

## Datasets Não Priorizados Agora

| Candidato | Motivo para adiar |
|---|---|
| Contribuições à Segurança Social × prestações sociais | Apesar de relevante, ainda exige validação de granularidade e forma de extração no SIESS/GEP/MTSSS. |
| IRS/contribuição fiscal por nacionalidade | Fonte pública direta ainda não confirmada. Risco metodológico alto para Sprint 1. |
| Proporção de imigrantes na população total UE27 | Viável, mas depende de alinhar a métrica oficial de “imigrante” (`foreign-born`, cidadania estrangeira ou outra definição). |
| Trabalhadores imigrantes por setor × peso setorial no PIB | Relevante, mas exige cruzamento CAE/NACE e validação adicional de compatibilidade setorial. |

## Próxima Task Recomendada

Abrir `G1-007` para coletar o primeiro dataset bruto aprovado:

```txt
[G1-007] Coletar dataset bruto Eurostat immigration flow
```

Entrega esperada da `G1-007`:

- arquivo bruto salvo em `data/raw/`;
- URL e data de coleta registradas;
- entrada correspondente no `docs/grupo-1/log-fontes.md`, se houver fonte nova ou ajuste relevante;
- log de coleta criado;
- preparação para tratamento posterior em `data/processed/`.

## Status Final da G1-006

Status recomendado no GitHub Projects:

```txt
Review
```

A coleta em volume ainda não começou. Esta etapa apenas seleciona os datasets prioritários e documenta a ordem técnica de execução.
