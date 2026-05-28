# Biblioteca de Fontes Publicas — Grupo 1

## Objetivo

Esta biblioteca registra fontes publicas relevantes para o projeto **Imigracao e Economia**.

Ela atende a entrega solicitada para inventario de fontes em Markdown. O catalogo tecnico oficial usado pelos datasets continua sendo:

```txt
metadata/catalogo_fontes.csv
```

Use esta biblioteca para leitura humana, triagem e selecao inicial de fontes. Use o catalogo oficial para relacionar datasets a `fonte_id`.

## Relacao com o catalogo oficial

| Arquivo | Funcao |
| --- | --- |
| `docs/grupo-1/biblioteca-fontes.md` | Inventario amplo em Markdown, facil de ler e revisar. |
| `metadata/biblioteca_fontes.csv` | Versao CSV da biblioteca, conforme nomenclatura solicitada na task. |
| `docs/grupo-1/catalogo-fontes.md` | Documentacao do catalogo oficial de fontes. |
| `metadata/catalogo_fontes.csv` | Catalogo oficial usado pelos datasets e pelo campo `source_id`. |

## Fontes documentadas

### 1. RIFA/SEF

| Campo | Valor |
| --- | --- |
| Link direto | <https://sefstat.sef.pt/forms/relatorios.aspx> |
| Dados disponibilizados | Imigracao e populacao estrangeira residente em Portugal. |
| Periodo coberto | 2000-2022 |
| Granularidade | Anual; nacional; nacionalidade e outros recortes conforme relatorio/portal. |
| Frequencia | Anual, conforme publicacoes historicas do SEF. |
| Formato de export | Relatorio estatistico anual e portal. |
| Como importar | Download/consulta no portal SEFStat; extracao manual ou tecnica conforme tabela. |
| Limitacoes | Dados historicos em PDF/portal. Necessario documentar descontinuidade metodologica entre SEF e AIMA. |
| Relevancia | Alta |
| Tem API/CSV | Parcial |

### 2. RMA/AIMA

| Campo | Valor |
| --- | --- |
| Link direto | <https://aima.gov.pt/pt/a-aima/relatorios-de-migracoes-e-asilo> |
| Dados disponibilizados | Migracoes, asilo e populacao estrangeira residente. |
| Periodo coberto | 2023-2024 |
| Granularidade | Anual; nacionalidade; tipo de autorizacao conforme relatorio. |
| Frequencia | Anual, conforme publicacao da AIMA. |
| Formato de export | Relatorio estatistico anual. |
| Como importar | Download do relatorio; extracao manual ou tecnica das tabelas prioritarias. |
| Limitacoes | Fonte recente pos-SEF. Confirmar erratas/adendas antes de extracao final. |
| Relevancia | Alta |
| Tem API/CSV | Nao |

### 3. Observatorio das Migracoes

| Campo | Valor |
| --- | --- |
| Link direto | <https://om.aima.gov.pt/> |
| Dados disponibilizados | Integracao de imigrantes e indicadores sociais. |
| Periodo coberto | Series e relatorios ate 2024/2025 conforme publicacao. |
| Granularidade | Varia por estudo; nacional, tematica ou populacional conforme publicacao. |
| Frequencia | Irregular, conforme publicacoes e estudos. |
| Formato de export | Relatorios estatisticos, estudos e policy briefs. |
| Como importar | Consulta/download de relatorios; extracao manual quando houver tabelas. |
| Limitacoes | Fonte analitica complementar. Periodo e granularidade variam por estudo. |
| Relevancia | Alta |
| Tem API/CSV | Nao |

### 4. INE Contas Nacionais

| Campo | Valor |
| --- | --- |
| Link direto | <https://www.ine.pt> |
| Dados disponibilizados | PIB, contas nacionais e VAB. |
| Periodo coberto | Series historicas anuais/trimestrais conforme indicador ate 2024/2025. |
| Granularidade | Nacional; anual ou trimestral conforme indicador. |
| Frequencia | Periodica, conforme calendario estatistico do INE. |
| Formato de export | Base estatistica oficial. |
| Como importar | Consulta no portal INE e export de tabelas quando disponivel. |
| Limitacoes | Fonte primaria para PIB/VAB. Selecionar indicador e unidade antes do cruzamento. |
| Relevancia | Alta |
| Tem API/CSV | Sim |

### 5. PORDATA PIB/populacao estrangeira

| Campo | Valor |
| --- | --- |
| Link direto | <https://www.pordata.pt/portugal> |
| Dados disponibilizados | PIB, populacao residente e populacao estrangeira. |
| Periodo coberto | Series longas anuais variando por indicador, geralmente ate 2024. |
| Granularidade | Anual; nacional; alguns indicadores com recortes adicionais. |
| Frequencia | Atualizacao periodica conforme fonte estatistica original. |
| Formato de export | Base estatistica agregada. |
| Como importar | Consulta e export pela interface PORDATA quando disponivel. |
| Limitacoes | Agrega fontes oficiais. Usar como apoio pratico e confirmar fonte primaria quando necessario. |
| Relevancia | Alta |
| Tem API/CSV | Sim |

### 6. GEP/MTSSS/SIESS

| Campo | Valor |
| --- | --- |
| Link direto | <https://www.gep.mtsss.gov.pt/pt/-/siess-com-dados-sobre-pessoas-de-nacionalidade-estrangeira> |
| Dados disponibilizados | Seguranca Social, trabalho e nacionalidade estrangeira. |
| Periodo coberto | Dados mensais e anuais conforme dashboard/publicacao ate 2026. |
| Granularidade | Mensal ou anual; nacionalidade estrangeira conforme publicacao/dashboard. |
| Frequencia | Mensal/anual conforme indicador. |
| Formato de export | Dashboard e sintese estatistica. |
| Como importar | Consulta no dashboard/publicacao; validar possibilidade de export antes da coleta. |
| Limitacoes | Nao cobre necessariamente todas as receitas e despesas por nacionalidade. Validar extracao e granularidade. |
| Relevancia | Alta/Media |
| Tem API/CSV | Parcial |

### 7. Banco de Portugal

| Campo | Valor |
| --- | --- |
| Link direto | <https://www.bportugal.pt> |
| Dados disponibilizados | Economia, setores de atividade economica e indicadores macroeconomicos. |
| Periodo coberto | Series historicas e publicacoes recorrentes. |
| Granularidade | Nacional; mensal, trimestral ou anual conforme indicador. |
| Frequencia | Periodica, conforme indicador. |
| Formato de export | Base estatistica e publicacoes oficiais. |
| Como importar | Consulta no portal/BPstat e export quando disponivel. |
| Limitacoes | Fonte complementar para contexto macroeconomico/setorial. Cruzar com INE quando o indicador oficial for VAB/PIB. |
| Relevancia | Alta |
| Tem API/CSV | Sim |

### 8. Eurostat immigration flow

| Campo | Valor |
| --- | --- |
| Link direto | <https://ec.europa.eu/eurostat/databrowser/view/tps00176/default/table?lang=en> |
| Dados disponibilizados | Fluxos de imigracao comparaveis. |
| Periodo coberto | Aproximadamente 2013-2024 conforme pais/indicador. |
| Granularidade | Anual; por pais. |
| Frequencia | Anual. |
| Formato de export | Base estatistica internacional API/CSV. |
| Como importar | Export pelo Eurostat Data Browser ou API Eurostat. |
| Limitacoes | Ranking nao vem pronto. Necessario calcular crescimento percentual ou CAGR e verificar definicoes por pais. |
| Relevancia | Alta |
| Tem API/CSV | Sim |

### 9. Eurostat foreign-born population

| Campo | Valor |
| --- | --- |
| Link direto | <https://ec.europa.eu/eurostat/databrowser/view/tps00178/default/table?lang=en> |
| Dados disponibilizados | Populacao nascida no estrangeiro e comparacao europeia. |
| Periodo coberto | Aproximadamente 2009-2024 conforme pais/indicador. |
| Granularidade | Anual; por pais. |
| Frequencia | Anual. |
| Formato de export | Base estatistica internacional API/CSV. |
| Como importar | Export pelo Eurostat Data Browser ou API Eurostat. |
| Limitacoes | Definicao foreign-born difere de cidadania estrangeira. Alinhar metrica oficial com Grupos 2 e 3. |
| Relevancia | Alta |
| Tem API/CSV | Sim |

### 10. OECD permanent immigrant inflows

| Campo | Valor |
| --- | --- |
| Link direto | <https://www.oecd.org/en/data/indicators/permanent-immigrant-inflows.html> |
| Dados disponibilizados | Entradas permanentes de imigrantes. |
| Periodo coberto | Series internacionais geralmente ate 2023 conforme pais. |
| Granularidade | Anual; por pais OECD. |
| Frequencia | Anual. |
| Formato de export | Indicador internacional e Data Explorer. |
| Como importar | Consulta/export no Data Explorer da OECD. |
| Limitacoes | Comparabilidade boa para OECD, mas escopo nao e exclusivamente UE27. Usar como fonte complementar. |
| Relevancia | Alta/Media |
| Tem API/CSV | Sim |

### 11. PORDATA taxa bruta de imigracao

| Campo | Valor |
| --- | --- |
| Link direto | <https://www.pordata.pt/europa/taxa%2Bbruta%2Bde%2Bimigracao-1934> |
| Dados disponibilizados | Taxa bruta de imigracao. |
| Periodo coberto | 1998-2024 conforme pais/indicador. |
| Granularidade | Anual; por pais europeu. |
| Frequencia | Anual. |
| Formato de export | Base estatistica agregada. |
| Como importar | Consulta e export pela interface PORDATA quando disponivel. |
| Limitacoes | Indicador por 1000 residentes. Alguns anos/paises podem nao ter valores e a fonte agrega entidades oficiais. |
| Relevancia | Alta |
| Tem API/CSV | Sim |
