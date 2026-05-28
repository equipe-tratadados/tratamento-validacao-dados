# Log de Fontes do Grupo 1

Este arquivo é o ponto de entrada para entregas diretas de fontes no GitHub.

A pessoa responsável pela pesquisa deve editar este arquivo pelo navegador ou pelo editor local, adicionar uma nova entrada no fim do documento e abrir um Pull Request. O líder revisa o PR; não deve precisar consolidar a entrega manualmente.

## Como entregar uma fonte

1. Abrir uma branch com o ID da task.
2. Copiar o bloco de `templates/registro-fonte.template.md`.
3. Colar uma nova entrada no fim deste arquivo.
4. Preencher todos os campos obrigatórios.
5. Se a fonte for candidata a oficial, adicionar ou atualizar a linha correspondente em `metadata/catalogo_fontes.csv`.
6. Abrir PR no padrão `[G1-000] docs(fontes): registra fontes ...`.

## Status de revisão

Usar apenas um dos valores abaixo:

```txt
Pendente
Aceita
Ajustes solicitados
Rejeitada
Duplicada
```

## Campos obrigatórios

Toda entrada deve preencher:

- task;
- responsável;
- subtema;
- pergunta relacionada;
- `fonte_id`;
- nome da fonte;
- instituição;
- URL;
- período disponível;
- granularidade;
- formato;
- viabilidade;
- limitação principal;
- próximo passo;
- status de revisão.

## Exemplo preenchido

> Exemplo documental. Não copiar como fonte real.

### Fonte: RMA/AIMA - Relatório de Migrações e Asilo

| Campo | Valor |
| --- | --- |
| Task | `G1-001.1` |
| Responsável | `@usuario` |
| Subtema | Fluxo Imigratório x Crescimento Económico |
| Pergunta relacionada | Evolução do número de imigrantes residentes em Portugal entre 2010 e 2024 |
| `fonte_id` | `FONTE-002` |
| Nome da fonte | RMA/AIMA |
| Instituição | Agência para a Integração, Migrações e Asilo |
| URL | https://aima.gov.pt/pt/a-aima/relatorios-de-migracoes-e-asilo |
| Período disponível | 2023-2024 |
| Granularidade | Anual; nacionalidade; tipo de autorização conforme relatório |
| Formato | PDF / relatório estatístico |
| Viabilidade | Alta |
| Limitação principal | Continuidade metodológica com SEF precisa ser documentada |
| Próximo passo | Extrair tabelas prioritárias e cruzar com fontes históricas do SEF |
| Status de revisão | Aceita |

## Bloco vazio para copiar

```md
### Fonte: [nome curto da fonte]

| Campo | Valor |
| --- | --- |
| Task | `G1-000` |
| Responsável | `@usuario` |
| Subtema |  |
| Pergunta relacionada |  |
| `fonte_id` | `FONTE-000` |
| Nome da fonte |  |
| Instituição |  |
| URL |  |
| Período disponível |  |
| Granularidade |  |
| Formato | CSV / Excel / API / PDF / página web / base estatística / outro |
| Viabilidade | Alta / Média / Baixa / Fonte não encontrada |
| Limitação principal |  |
| Próximo passo |  |
| Status de revisão | Pendente |
```

## Entradas de fontes

Adicionar novas entradas abaixo desta linha.

### Fonte: RIFA/SEF

| Campo | Valor |
| --- | --- |
| Task | `G1-003` |
| Responsável | `@lucasguldem` |
| Subtema | Fluxo Imigratório x Crescimento Económico |
| Pergunta relacionada | Evolução do número de imigrantes residentes em Portugal entre 2010 e 2024 |
| `fonte_id` | `FONTE-001` |
| Nome da fonte | RIFA/SEF |
| Instituição | Serviço de Estrangeiros e Fronteiras |
| URL | https://sefstat.sef.pt/forms/relatorios.aspx |
| Período disponível | 2000-2022 |
| Granularidade | Anual; nacional; nacionalidade e outros recortes conforme relatório/portal |
| Formato | Relatório estatístico anual e portal |
| Viabilidade | Alta |
| Limitação principal | Dados históricos em PDF/portal. Necessário documentar descontinuidade metodológica entre SEF e AIMA. |
| Próximo passo | Usar como base histórica para série de população estrangeira residente. |
| Status de revisão | Aceita |

### Fonte: RMA/AIMA

| Campo | Valor |
| --- | --- |
| Task | `G1-003` |
| Responsável | `@lucasguldem` |
| Subtema | Fluxo Imigratório x Crescimento Económico |
| Pergunta relacionada | Evolução do número de imigrantes residentes em Portugal entre 2010 e 2024 |
| `fonte_id` | `FONTE-002` |
| Nome da fonte | RMA/AIMA |
| Instituição | Agência para a Integração, Migrações e Asilo |
| URL | https://aima.gov.pt/pt/a-aima/relatorios-de-migracoes-e-asilo |
| Período disponível | 2023-2024 |
| Granularidade | Anual; nacionalidade; tipo de autorização conforme relatório |
| Formato | Relatório estatístico anual |
| Viabilidade | Alta |
| Limitação principal | Fonte recente pós-SEF. Confirmar erratas/adendas antes de extração final. |
| Próximo passo | Usar como base recente para série de população estrangeira residente. |
| Status de revisão | Aceita |

### Fonte: Observatório das Migrações

| Campo | Valor |
| --- | --- |
| Task | `G1-003` |
| Responsável | `@lucasguldem` |
| Subtema | Integração de imigrantes e indicadores sociais |
| Pergunta relacionada | Indicadores complementares de integração social e contexto migratório |
| `fonte_id` | `FONTE-003` |
| Nome da fonte | Observatório das Migrações |
| Instituição | Agência para a Integração, Migrações e Asilo / Observatório das Migrações |
| URL | https://om.aima.gov.pt/ |
| Período disponível | Séries e relatórios até 2024/2025 conforme publicação |
| Granularidade | Varia por estudo; nacional, temática ou populacional conforme publicação |
| Formato | Relatórios estatísticos, estudos e policy briefs |
| Viabilidade | Alta |
| Limitação principal | Fonte analítica complementar. Período e granularidade variam por estudo. |
| Próximo passo | Usar como apoio metodológico e contextual para análises de integração. |
| Status de revisão | Aceita |

### Fonte: INE Contas Nacionais

| Campo | Valor |
| --- | --- |
| Task | `G1-003` |
| Responsável | `@lucasguldem` |
| Subtema | Fluxo Imigratório x Crescimento Económico |
| Pergunta relacionada | Evolução de PIB e cruzamento com população estrangeira residente |
| `fonte_id` | `FONTE-004` |
| Nome da fonte | INE Contas Nacionais |
| Instituição | Instituto Nacional de Estatística |
| URL | https://www.ine.pt |
| Período disponível | Séries históricas anuais/trimestrais conforme indicador até 2024/2025 |
| Granularidade | Nacional; anual ou trimestral conforme indicador |
| Formato | Base estatística oficial |
| Viabilidade | Alta |
| Limitação principal | Selecionar indicador e unidade antes do cruzamento. |
| Próximo passo | Usar como fonte primária para PIB/VAB nos datasets económicos. |
| Status de revisão | Aceita |

### Fonte: PORDATA PIB/população estrangeira

| Campo | Valor |
| --- | --- |
| Task | `G1-003` |
| Responsável | `@lucasguldem` |
| Subtema | Fluxo Imigratório x Crescimento Económico |
| Pergunta relacionada | Evolução de PIB e população estrangeira em Portugal |
| `fonte_id` | `FONTE-005` |
| Nome da fonte | PORDATA PIB/população estrangeira |
| Instituição | Fundação Francisco Manuel dos Santos / PORDATA |
| URL | https://www.pordata.pt/portugal |
| Período disponível | Séries longas anuais variando por indicador, geralmente até 2024 |
| Granularidade | Anual; nacional; alguns indicadores com recortes adicionais |
| Formato | Base estatística agregada |
| Viabilidade | Alta |
| Limitação principal | Agrega fontes oficiais. Usar como apoio prático e confirmar fonte primária quando necessário. |
| Próximo passo | Usar como apoio prático para séries anuais de PIB e população estrangeira. |
| Status de revisão | Aceita |

### Fonte: GEP/MTSSS/SIESS

| Campo | Valor |
| --- | --- |
| Task | `G1-003` |
| Responsável | `@lucasguldem` |
| Subtema | Contribuição IRS x Prestações Sociais |
| Pergunta relacionada | Contribuições à Segurança Social e prestações sociais relacionadas a população estrangeira |
| `fonte_id` | `FONTE-006` |
| Nome da fonte | GEP/MTSSS/SIESS |
| Instituição | Gabinete de Estratégia e Planeamento / Ministério do Trabalho, Solidariedade e Segurança Social |
| URL | https://www.gep.mtsss.gov.pt/pt/-/siess-com-dados-sobre-pessoas-de-nacionalidade-estrangeira |
| Período disponível | Dados mensais e anuais conforme dashboard/publicação até 2026 |
| Granularidade | Mensal ou anual; nacionalidade estrangeira conforme publicação/dashboard |
| Formato | Dashboard e síntese estatística |
| Viabilidade | Alta / Média |
| Limitação principal | Não cobre necessariamente todas as receitas e despesas por nacionalidade. Validar extração e granularidade. |
| Próximo passo | Validar extração antes de abrir coleta em volume para Segurança Social. |
| Status de revisão | Aceita |

### Fonte: Banco de Portugal

| Campo | Valor |
| --- | --- |
| Task | `G1-003` |
| Responsável | `@lucasguldem` |
| Subtema | Fluxo Imigratório x Crescimento Económico |
| Pergunta relacionada | Indicadores macroeconómicos e contexto económico/setorial |
| `fonte_id` | `FONTE-007` |
| Nome da fonte | Banco de Portugal |
| Instituição | Banco de Portugal |
| URL | https://www.bportugal.pt |
| Período disponível | Séries históricas e publicações recorrentes |
| Granularidade | Nacional; mensal, trimestral ou anual conforme indicador |
| Formato | Base estatística e publicações oficiais |
| Viabilidade | Alta |
| Limitação principal | Fonte complementar para contexto macroeconómico/setorial. Cruzar com INE quando o indicador oficial for VAB/PIB. |
| Próximo passo | Usar como fonte complementar em análises económicas. |
| Status de revisão | Aceita |

### Fonte: Eurostat immigration flow

| Campo | Valor |
| --- | --- |
| Task | `G1-003` |
| Responsável | `@lucasguldem` |
| Subtema | Comparação Portugal x Europa |
| Pergunta relacionada | Ranking europeu de crescimento do fluxo imigratório entre 2012 e 2023 |
| `fonte_id` | `FONTE-008` |
| Nome da fonte | Eurostat immigration flow |
| Instituição | Eurostat |
| URL | https://ec.europa.eu/eurostat/databrowser/view/tps00176/default/table?lang=en |
| Período disponível | Aproximadamente 2013-2024 conforme país/indicador |
| Granularidade | Anual; por país |
| Formato | Base estatística internacional API/CSV |
| Viabilidade | Alta |
| Limitação principal | Ranking não vem pronto. Necessário calcular crescimento percentual ou CAGR e verificar definições por país. |
| Próximo passo | Priorizar para primeira coleta real e teste no Looker Studio. |
| Status de revisão | Aceita |

### Fonte: Eurostat foreign-born population

| Campo | Valor |
| --- | --- |
| Task | `G1-003` |
| Responsável | `@lucasguldem` |
| Subtema | Comparação Portugal x Europa |
| Pergunta relacionada | Proporção de imigrantes na população total de Portugal face aos países da UE |
| `fonte_id` | `FONTE-009` |
| Nome da fonte | Eurostat foreign-born population |
| Instituição | Eurostat |
| URL | https://ec.europa.eu/eurostat/databrowser/view/tps00178/default/table?lang=en |
| Período disponível | Aproximadamente 2009-2024 conforme país/indicador |
| Granularidade | Anual; por país |
| Formato | Base estatística internacional API/CSV |
| Viabilidade | Alta |
| Limitação principal | Definição foreign-born difere de cidadania estrangeira. Alinhar métrica oficial com Grupos 2 e 3. |
| Próximo passo | Usar depois de alinhar métrica oficial de “imigrante”. |
| Status de revisão | Aceita |

### Fonte: OECD permanent immigrant inflows

| Campo | Valor |
| --- | --- |
| Task | `G1-003` |
| Responsável | `@lucasguldem` |
| Subtema | Comparação Portugal x Europa |
| Pergunta relacionada | Entradas permanentes de imigrantes em comparação internacional |
| `fonte_id` | `FONTE-010` |
| Nome da fonte | OECD permanent immigrant inflows |
| Instituição | Organisation for Economic Co-operation and Development |
| URL | https://www.oecd.org/en/data/indicators/permanent-immigrant-inflows.html |
| Período disponível | Séries internacionais geralmente até 2023 conforme país |
| Granularidade | Anual; por país OECD |
| Formato | Indicador internacional e Data Explorer |
| Viabilidade | Alta / Média |
| Limitação principal | Comparabilidade boa para OECD, mas escopo não é exclusivamente UE27. Usar como fonte complementar. |
| Próximo passo | Usar como fonte complementar para comparação internacional. |
| Status de revisão | Aceita |

### Fonte: PORDATA taxa bruta de imigração

| Campo | Valor |
| --- | --- |
| Task | `G1-003` |
| Responsável | `@lucasguldem` |
| Subtema | Comparação Portugal x Europa |
| Pergunta relacionada | Taxa bruta de imigração em Portugal face a países europeus |
| `fonte_id` | `FONTE-011` |
| Nome da fonte | PORDATA taxa bruta de imigração |
| Instituição | Fundação Francisco Manuel dos Santos / PORDATA |
| URL | https://www.pordata.pt/europa/taxa%2Bbruta%2Bde%2Bimigracao-1934 |
| Período disponível | 1998-2024 conforme país/indicador |
| Granularidade | Anual; por país europeu |
| Formato | Base estatística agregada |
| Viabilidade | Alta |
| Limitação principal | Indicador por 1000 residentes. Alguns anos/países podem não ter valores e a fonte agrega entidades oficiais. |
| Próximo passo | Usar como apoio para comparação europeia e validação cruzada. |
| Status de revisão | Aceita |
