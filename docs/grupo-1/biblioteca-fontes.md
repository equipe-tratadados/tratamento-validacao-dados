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

### 12. DRE - Diario da Republica Eletronico

| Campo | Valor |
| --- | --- |
| Link direto | <https://diariodarepublica.pt/dr/pesquisa-avancada> |
| Dados disponibilizados | Legislacao, atos normativos, politicas publicas e alteracoes legais relacionadas com imigracao, residencia, asilo, nacionalidade e trabalho. |
| Periodo coberto | Serie historica do Diario da Republica ate atualidade. |
| Granularidade | Por diploma, data, serie, entidade emitente e tema pesquisado. |
| Frequencia | Diaria em dias uteis conforme publicacao oficial. |
| Formato de export | Portal de pesquisa, paginas HTML e PDF dos diplomas. |
| Como importar | Pesquisa por termos e download ou consulta de diplomas em PDF/HTML. |
| Limitacoes | Fonte juridica, nao estatistica. Requer classificacao manual dos diplomas relevantes. |
| Relevancia | Media |
| Tem API/CSV | Nao |

### 13. Dados.gov.pt

| Campo | Valor |
| --- | --- |
| Link direto | <https://dados.gov.pt/pt/datasets/> |
| Dados disponibilizados | Catalogo nacional de dados abertos com datasets publicos de entidades portuguesas, incluindo administracao publica, territorio, saude, economia e outros temas. |
| Periodo coberto | Varia por dataset e por entidade publicadora. |
| Granularidade | Varia por publicador, dataset, municipio, tema e periodo. |
| Frequencia | Varia por dataset e publicador. |
| Formato de export | CSV, XLSX, JSON, API, RDF e outros formatos conforme dataset. |
| Como importar | Pesquisa no portal, download direto do recurso ou API quando disponivel. |
| Limitacoes | Cobertura e qualidade variam por publicador. Metadados devem ser verificados caso a caso antes de usar. |
| Relevancia | Alta/Media |
| Tem API/CSV | Sim |

### 14. IEFP Estatisticas

| Campo | Valor |
| --- | --- |
| Link direto | <https://www.iefp.pt/estatisticas> |
| Dados disponibilizados | Estatisticas de emprego, desemprego, ofertas, medidas ativas e formacao profissional. |
| Periodo coberto | Series mensais e relatorios conforme indicador, com publicacoes historicas desde pelo menos 2003 em algumas series. |
| Granularidade | Mensal, nacional, regional, concelho, centro de emprego ou medida conforme publicacao. |
| Frequencia | Mensal ou periodica conforme estatistica. |
| Formato de export | PDF, Excel, tabelas e relatorios. |
| Como importar | Download de publicacoes/tabelas e extracao manual quando necessario. |
| Limitacoes | Recorte por nacionalidade pode nao estar disponivel em todos os indicadores. Validar antes de cruzar com migracao. |
| Relevancia | Media/Alta |
| Tem API/CSV | Parcial |

### 15. Autoridade Tributaria - Estatisticas

| Campo | Valor |
| --- | --- |
| Link direto | <https://info.portaldasfinancas.gov.pt/pt/dgci/divulgacao/estatisticas/Pages/default.aspx> |
| Dados disponibilizados | Estatisticas fiscais de IRS, IRC, IVA, impostos sobre patrimonio, declaracoes submetidas e outras informacoes tributarias agregadas. |
| Periodo coberto | Anual, mensal ou por publicacao conforme indicador fiscal. |
| Granularidade | Agregada por imposto, periodo e categoria fiscal conforme publicacao. |
| Frequencia | Periodica conforme divulgacao da Autoridade Tributaria. |
| Formato de export | HTML, PDF, Excel e ficheiros publicados. |
| Como importar | Consulta ou download no Portal das Financas quando publico. |
| Limitacoes | Dados por nacionalidade ou estatuto migratorio geralmente nao estao abertos. Algumas informacoes podem ter acesso condicionado. |
| Relevancia | Media |
| Tem API/CSV | Parcial |

### 16. SNS Transparencia

| Campo | Valor |
| --- | --- |
| Link direto | <https://transparencia.sns.gov.pt/> |
| Dados disponibilizados | Indicadores publicos do Servico Nacional de Saude sobre atividade, acesso, producao, mapas, graficos e catalogo de dados. |
| Periodo coberto | Series recentes conforme indicador no portal. |
| Granularidade | Nacional, regional, institucional e temporal conforme indicador. |
| Frequencia | Atualizacao periodica conforme indicador. |
| Formato de export | Dashboard, catalogo, API, mapas, graficos e tabelas quando disponiveis. |
| Como importar | Consulta no portal, API ou exportacao quando disponibilizada. |
| Limitacoes | Normalmente nao desagrega por nacionalidade ou condicao migratoria. Usar como contexto de pressao/uso de servicos. |
| Relevancia | Baixa/Media |
| Tem API/CSV | Parcial |

### 17. IHRU - Portal da Habitacao

| Campo | Valor |
| --- | --- |
| Link direto | <https://www.portaldahabitacao.pt/> |
| Dados disponibilizados | Informacao sobre habitacao, arrendamento, programas publicos, apoios, patrimonio publico e politicas de habitacao. |
| Periodo coberto | Varia por programa, relatorio ou indicador. |
| Granularidade | Nacional, municipal ou por programa conforme publicacao. |
| Frequencia | Irregular ou periodica conforme programa. |
| Formato de export | HTML, PDF, relatorios, simuladores e ficheiros quando disponiveis. |
| Como importar | Consulta ou download de relatorios e paginas do portal. |
| Limitacoes | Nem sempre ha dados estruturados ou recorte por imigrantes. Relevancia depende do subtema de habitacao. |
| Relevancia | Media |
| Tem API/CSV | Parcial |

### 18. BPstat

| Campo | Valor |
| --- | --- |
| Link direto | <https://bpstat.bportugal.pt/> |
| Dados disponibilizados | Series estatisticas macroeconomicas, financeiras, monetarias, balanca de pagamentos e indicadores economicos do Banco de Portugal. |
| Periodo coberto | Series historicas longas conforme indicador. |
| Granularidade | Mensal, trimestral, anual, nacional e por setor conforme serie. |
| Frequencia | Periodica conforme calendario estatistico. |
| Formato de export | Portal estatistico, API, CSV, Excel e downloads. |
| Como importar | Export pelo BPstat ou API quando disponivel. |
| Limitacoes | Nao e fonte migratoria direta. Deve ser usada para contexto economico e cruzamento com indicadores de imigracao. |
| Relevancia | Alta/Media |
| Tem API/CSV | Sim |

### 19. IOM Migration Data Portal

| Campo | Valor |
| --- | --- |
| Link direto | <https://www.migrationdataportal.org/> |
| Dados disponibilizados | Indicadores globais de migracao, stocks, fluxos, remessas, deslocamento, perfis por pais e fontes internacionais relacionadas. |
| Periodo coberto | Varia por indicador, geralmente series internacionais recentes e historicas. |
| Granularidade | Por pais, regiao, ano e indicador. |
| Frequencia | Atualizacao periodica conforme fonte original. |
| Formato de export | Portal de dados, downloads e visualizacoes. |
| Como importar | Consulta no portal e download quando disponivel. |
| Limitacoes | Indicadores sao globais e podem nao ter detalhe administrativo para Portugal. Validar definicoes contra Eurostat/AIMA. |
| Relevancia | Media |
| Tem API/CSV | Parcial |

### 20. World Bank Open Data

| Campo | Valor |
| --- | --- |
| Link direto | <https://data.worldbank.org/country/portugal> |
| Dados disponibilizados | Indicadores de Portugal sobre economia, populacao, emprego, desenvolvimento, migracao liquida e remessas. |
| Periodo coberto | Series anuais longas, geralmente desde 1960 conforme indicador. |
| Granularidade | Pais, ano e indicador. |
| Frequencia | Atualizacao periodica conforme indicador. |
| Formato de export | CSV, API, XML, Excel e DataBank. |
| Como importar | Download CSV ou API por indicador/pais. |
| Limitacoes | Indicadores de migracao sao limitados e definicoes podem diferir das fontes europeias. |
| Relevancia | Media |
| Tem API/CSV | Sim |

### 21. ACM - Alto Comissariado para as Migracoes

| Campo | Valor |
| --- | --- |
| Link direto | <https://www.acm.gov.pt/> |
| Dados disponibilizados | Relatorios, programas, politicas e servicos de integracao, diversidade, acolhimento e apoio a migrantes. |
| Periodo coberto | Varia conforme relatorio, programa e publicacao. |
| Granularidade | Por programa, servico, publico-alvo ou territorio conforme documento. |
| Frequencia | Irregular conforme publicacao institucional. |
| Formato de export | HTML, PDF, relatorios e documentos. |
| Como importar | Consulta ou download de paginas e relatorios. |
| Limitacoes | Instituicao sofreu alteracoes no ecossistema AIMA/ACM e os dados podem nao estar estruturados para dashboard. |
| Relevancia | Media |
| Tem API/CSV | Nao |

### 22. Censos INE

| Campo | Valor |
| --- | --- |
| Link direto | <https://censos.ine.pt/> |
| Dados disponibilizados | Dados censitarios sobre populacao, territorio, habitacao, nacionalidade, naturalidade e caracteristicas demograficas. |
| Periodo coberto | Censos 2011, Censos 2021 e series censitarias historicas conforme disponibilidade. |
| Granularidade | Nacional, regional, municipal, freguesia e unidade estatistica conforme tabela. |
| Frequencia | Decenal. |
| Formato de export | Tabelas, portal de consulta, downloads e ficheiros estatisticos. |
| Como importar | Consulta ou export no portal dos Censos/INE. |
| Limitacoes | Nao e serie anual e nao mede fluxos migratorios recentes. Util para contexto estrutural. |
| Relevancia | Alta/Media |
| Tem API/CSV | Parcial |

### 23. Portal Europeu de Dados

| Campo | Valor |
| --- | --- |
| Link direto | <https://data.europa.eu/en> |
| Dados disponibilizados | Catalogo europeu de dados abertos, incluindo datasets de instituicoes europeias, Estados membros, portais nacionais, regionais e locais. |
| Periodo coberto | Varia por dataset e publicador. |
| Granularidade | Varia por pais, instituicao, tema e periodo. |
| Frequencia | Varia por dataset. |
| Formato de export | CSV, RDF, JSON, API, ficheiros e links externos. |
| Como importar | Pesquisa no portal, download direto, bulk download, SPARQL/API ou acesso ao portal original. |
| Limitacoes | Metadados heterogeneos e possiveis duplicacoes com portais nacionais. Validar fonte original antes de usar. |
| Relevancia | Media |
| Tem API/CSV | Sim |

### 24. Comissao Europeia - Migration and Home Affairs

| Campo | Valor |
| --- | --- |
| Link direto | <https://home-affairs.ec.europa.eu/policies/migration-and-asylum_en> |
| Dados disponibilizados | Politicas, relatorios e informacao europeia sobre migracao, asilo, residencia, fronteiras, integracao e gestao migratoria. |
| Periodo coberto | Atual e historico conforme relatorios e secoes tematicas. |
| Granularidade | UE, pais, tema e documento conforme publicacao. |
| Frequencia | Atualizacao periodica conforme politica, relatorio ou programa. |
| Formato de export | HTML, PDF, links para Eurostat, EMN e bases relacionadas. |
| Como importar | Consulta ou download de relatorios e ligacoes para dados oficiais. |
| Limitacoes | Fonte muitas vezes e de policy/reporting, nao CSV pronto para dashboard. Usar para enquadramento e validacao institucional. |
| Relevancia | Media/Alta |
| Tem API/CSV | Parcial |
