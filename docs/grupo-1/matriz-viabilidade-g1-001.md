# Matriz Preliminar de Viabilidade — G1-001

## 1. Objetivo

Registrar a viabilidade preliminar de fontes públicas para responder às perguntas de pesquisa enviadas pelo Grupo 3 no tema **Imigração e Economia**.

Esta matriz ainda não representa validação final de dados, coleta definitiva, tratamento ou entrega para dashboard/texto.

O objetivo deste documento é indicar:

- se existem fontes públicas suficientes para responder cada pergunta;
- quais fontes foram identificadas;
- quais limitações foram encontradas;
- qual é a viabilidade preliminar de cada pergunta;
- qual deve ser o próximo passo técnico do Grupo 1.

Esta consolidação não altera as perguntas de pesquisa do Grupo 3. Perguntas com baixa viabilidade ou limitação metodológica devem ser sinalizadas como risco, não alteradas diretamente pelo Grupo 1.

---

## 2. Contexto da Task

Task principal:

```txt
[G1-001] Validar viabilidade preliminar de dados das perguntas do Grupo 3
```

Issues relacionadas:

| Issue | Responsável | Frente |
|---|---|---|
| [#6](https://github.com/equipe-tratadados/tratamento-validacao-dados/issues/6) | Tabata | Imigração, integração e população estrangeira |
| [#7](https://github.com/equipe-tratadados/tratamento-validacao-dados/issues/7) | Antony | Economia, fiscalidade, Segurança Social, IRS e setores económicos |
| [#8](https://github.com/equipe-tratadados/tratamento-validacao-dados/issues/8) | Nubia | Comparação Portugal × Europa e fontes acessíveis para dashboard |
| [#9](https://github.com/equipe-tratadados/tratamento-validacao-dados/issues/9) | Ana Cláudia | Fluxo, prazos, bloqueios e padrão das respostas |
| [#10](https://github.com/equipe-tratadados/tratamento-validacao-dados/issues/10) | Lucas | Consolidação da matriz preliminar de viabilidade |

---

## 3. Prazo

- Entregas individuais: **26/05/2026 18:00 Europe/Lisbon**.
- Consolidação da matriz: **26/05/2026 23:59 Europe/Lisbon**.

---

## 4. Critérios de Viabilidade

| Status | Uso |
|---|---|
| Alta | Existe fonte pública acessível, com período e formato compatíveis ou tecnicamente tratáveis. |
| Média | Existe fonte provável, mas com limitação de período, granularidade, formato, conceito ou metodologia. |
| Baixa | Existe apenas fonte indireta, agregada, desatualizada, incompleta ou difícil de extrair. |
| Fonte não encontrada | Não foi identificada fonte pública suficiente para responder à pergunta. |

Observação: fonte parcial, limitada ou não encontrada também é considerada uma entrega válida nesta etapa, desde que a limitação esteja documentada.

---

## 5. Fontes de Entrada Utilizadas

Esta matriz foi consolidada a partir das entregas das seguintes subtasks:

- `G1-001.1` — Tabata: fontes de imigração, integração e população estrangeira.
- `G1-001.2` — Antony: fontes económicas, fiscais, Segurança Social, IRS e setores económicos.
- `G1-001.3` — Nubia: fontes comparativas Portugal × Europa e fontes acessíveis para dashboard.
- `G1-001.4` — Ana Cláudia: acompanhamento de fluxo, prazos, bloqueios e status.

---

## 6. Matriz por Pergunta

| Subtema | Pergunta | Fonte encontrada | Instituição responsável | Link | Período disponível | Granularidade | Formato de acesso | Viabilidade | Limitação principal | Próximo passo | Responsável | Issue |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| Fluxo Imigratório × Crescimento Económico | Evolução do número de imigrantes residentes em Portugal entre 2010 e 2024 e relação com PIB no mesmo período. | RIFA/SEF; RMA/AIMA; INE Contas Nacionais; PORDATA | SEF; AIMA; INE; Fundação Francisco Manuel dos Santos/PORDATA | <https://sefstat.sef.pt/forms/relatorios.aspx>; <https://aima.gov.pt/pt/a-aima/relatorios-de-migracoes-e-asilo>; <https://www.ine.pt>; <https://www.pordata.pt> | SEF/RIFA: 2000–2022; AIMA/RMA: 2023–2024; INE/PORDATA: séries longas anuais para PIB | Anual; nacional; por nacionalidade/género/idade em alguns relatórios; PIB nacional/anual | PDF; anexos estatísticos; tabelas online; CSV/Excel em algumas fontes | Alta | Os dados migratórios estão maioritariamente em PDF e há descontinuidade/revisão metodológica entre SEF e AIMA. A relação com PIB será feita por cruzamento de séries independentes, não por causalidade direta. | Extrair série anual de residentes estrangeiros e cruzar com série anual de PIB do INE/PORDATA. Documentar quebra metodológica SEF/AIMA. | Tabata / Antony | [#6](https://github.com/equipe-tratadados/tratamento-validacao-dados/issues/6), [#7](https://github.com/equipe-tratadados/tratamento-validacao-dados/issues/7) |
| Fluxo Imigratório × Crescimento Económico | Setores de atividade económica onde se concentram trabalhadores imigrantes e peso desses setores no PIB nacional. | GEP/MTSSS; Quadros de Pessoal; Banco de Portugal; INE; Eurostat LFS | GEP/MTSSS; Banco de Portugal; INE; Eurostat | <https://www.gep.mtsss.gov.pt/pt/inicio>; <https://www.bportugal.pt>; <https://www.ine.pt>; <https://ec.europa.eu/eurostat/data/database> | Aproximadamente 2014–2024, dependendo da fonte e indicador | Anual ou mensal; nacional; por setor/atividade económica; possível recorte por nacionalidade em algumas fontes | PDF; Excel; tabela online; API Eurostat | Média/Alta | Pode exigir cruzamento entre trabalhadores estrangeiros por setor e peso económico setorial. As classificações CAE/NACE e os formatos podem variar entre fontes. Dados setoriais e nacionalidade podem não aparecer juntos numa única fonte limpa. | Validar qual fonte possui melhor combinação entre nacionalidade/condição migratória e setor económico. Cruzar com VAB/PIB setorial do INE. | Tabata / Antony | [#6](https://github.com/equipe-tratadados/tratamento-validacao-dados/issues/6), [#7](https://github.com/equipe-tratadados/tratamento-validacao-dados/issues/7) |
| Contribuição IRS × Prestações Sociais | Quanto os imigrantes pagaram à Segurança Social entre 2015 e 2025 e quanto receberam em prestações sociais no mesmo período. | SIESS/GEP/MTSSS; Segurança Social; relatórios do Ministério do Trabalho | GEP/MTSSS; Segurança Social; Ministério do Trabalho, Solidariedade e Segurança Social | <https://www.gep.mtsss.gov.pt/pt/inicio>; <https://www.seg-social.pt/estatisticas> | 2015–2025/2026, dependendo da publicação | Mensal ou anual; nacional; por nacionalidade em algumas publicações recentes | PDF; dashboard; tabela online; possível extração manual/técnica | Alta/Média | A pergunta fala de Segurança Social e prestações sociais, não exatamente de IRS. Dados podem estar em PDF ou dashboard, exigindo extração manual ou técnica. | Separar claramente contribuição social de imposto fiscal. Validar extração da série 2015–2025 de contribuições e prestações. | Antony | [#7](https://github.com/equipe-tratadados/tratamento-validacao-dados/issues/7) |
| Contribuição IRS × Prestações Sociais | Distribuição da contribuição fiscal dos imigrantes por nacionalidade de origem. | Autoridade Tributária; Portal das Finanças; Segurança Social; relatórios oficiais | Autoridade Tributária e Aduaneira; Segurança Social; entidades governamentais | <https://www.portaldasfinancas.gov.pt>; <https://www.seg-social.pt/estatisticas> | Não confirmado para IRS por nacionalidade | Agregado; possível recorte social/contributivo por nacionalidade, mas não confirmado para IRS | Relatórios; páginas institucionais; possível ausência de base aberta | Média/Baixa | Não foi confirmada fonte pública direta com IRS por nacionalidade. Pode haver dados sociais/contributivos por nacionalidade, mas não necessariamente dados fiscais de IRS abertos. | Sinalizar ao Grupo 3 que a pergunta pode precisar de ajuste. Alternativa provável: contribuição à Segurança Social por nacionalidade, se houver fonte pública validada. | Antony | [#7](https://github.com/equipe-tratadados/tratamento-validacao-dados/issues/7) |
| Comparação Portugal × Europa | Posição de Portugal no ranking europeu de crescimento do fluxo imigratório entre 2012 e 2023. | Eurostat Immigration; PORDATA Taxa Bruta de Imigração; OECD Permanent Immigrant Inflows | Eurostat; PORDATA; OECD | <https://ec.europa.eu/eurostat/databrowser/view/tps00176/default/table?lang=en>; <https://www.pordata.pt/db/europa/ambiente+de+consulta/tabela>; <https://www.oecd.org/migration/mig/inflowsofpermanentimmigrants.htm> | Eurostat: aproximadamente 2013–2024; PORDATA: 1998–2024, conforme indicador; OECD: geralmente desde 2000 até 2023, conforme país | Anual; por país; agregado nacional | Tabela online; CSV; JSON/API; Excel; base interativa | Alta | As fontes não entregam necessariamente o ranking pronto. Será necessário calcular crescimento percentual ou CAGR por país. Alguns períodos começam em 2013, não 2012. Pode haver diferenças metodológicas entre países. | Extrair série por país da UE, calcular crescimento entre ano inicial e final disponíveis e posicionar Portugal no ranking. | Nubia | [#8](https://github.com/equipe-tratadados/tratamento-validacao-dados/issues/8) |
| Comparação Portugal × Europa | Proporção de imigrantes na população total de Portugal face aos 27 países da UE. | Eurostat Foreign-born Population; Eurostat população total; PORDATA | Eurostat; PORDATA | <https://ec.europa.eu/eurostat/databrowser/view/tps00178/default/table?lang=en>; <https://www.pordata.pt/europa/quadro+resumo/portugal-826973> | Eurostat: 2009–2024, varia por país; PORDATA: anos selecionados | Anual por país em Eurostat; agregada/anos selecionados na PORDATA | Tabela online; CSV; JSON/API; Excel/PDF em algumas fontes | Alta | É necessário escolher a métrica oficial: população nascida no estrangeiro, população estrangeira por cidadania ou outro critério. Cada definição altera a interpretação. | Definir a métrica com o Grupo 3/Grupo 2 e calcular proporção por país: imigrantes / população total. | Nubia | [#8](https://github.com/equipe-tratadados/tratamento-validacao-dados/issues/8) |

---

## 7. Leitura Técnica por Subtema

### 7.1 Subtema 1 — Fluxo Imigratório × Crescimento Económico

#### Pergunta A — Evolução de imigrantes residentes × PIB

**Viabilidade:** Alta.

Fontes principais:

- RIFA/SEF para série histórica até 2022.
- RMA/AIMA para 2023–2024.
- INE para PIB e Contas Nacionais.
- PORDATA como fonte prática complementar para séries anuais.

Conclusão preliminar:

A pergunta é viável. Há fontes públicas para construir a série de residentes estrangeiros e a série de PIB. A análise deve ser apresentada como comparação temporal, evolução conjunta ou correlação visual, não como relação causal direta.

Limitações:

- relatórios SEF/AIMA em PDF;
- possível quebra metodológica entre SEF e AIMA;
- revisão de valores históricos pela AIMA;
- necessidade de documentação metodológica na base final;
- PIB não é desagregado por nacionalidade de trabalhadores.

---

#### Pergunta B — Trabalhadores imigrantes por setor × peso dos setores no PIB

**Viabilidade:** Média/Alta.

Fontes principais:

- GEP/MTSSS;
- Quadros de Pessoal;
- Banco de Portugal;
- INE;
- Eurostat Labour Force Survey.

Conclusão preliminar:

A pergunta é possível, mas exige mais trabalho técnico do que a Pergunta A. A dificuldade está em cruzar trabalhadores estrangeiros por setor com o peso económico dos setores no PIB/VAB.

Limitações:

- dados setoriais podem estar em PDF ou em tabelas não imediatamente exportáveis;
- pode haver diferença entre CAE, NACE e classificações setoriais;
- a fonte pode trazer trabalhadores estrangeiros por setor, mas não necessariamente “imigrantes” no sentido migratório completo;
- a compatibilidade entre setor económico e peso no PIB precisa ser validada.

---

### 7.2 Subtema 2 — Contribuição IRS × Prestações Sociais

#### Observação conceitual obrigatória

Há uma inconsistência conceitual no título do subtema.

O título menciona **IRS**, mas a Pergunta A trata de **contribuições à Segurança Social** e **prestações sociais recebidas**.

São conceitos diferentes:

| Conceito | Instituição | O que mede |
|---|---|---|
| IRS | Autoridade Tributária | Imposto sobre rendimento. |
| Contribuições à Segurança Social | Segurança Social / MTSSS / GEP | Descontos e contribuições contributivas. |
| Prestações sociais | Segurança Social | Benefícios recebidos, como subsídios, pensões e apoios. |

Essa distinção deve ser comunicada ao Grupo 3 para evitar erro metodológico.

---

#### Pergunta A — Contribuições à Segurança Social × prestações sociais

**Viabilidade:** Alta/Média.

Fontes principais:

- SIESS/GEP/MTSSS;
- Segurança Social;
- relatórios do Ministério do Trabalho.

Conclusão preliminar:

A pergunta é tecnicamente viável se for tratada como **contribuições à Segurança Social versus prestações sociais**, não como IRS. Há indicação de fontes públicas com dados relevantes, mas o formato pode exigir extração de PDF ou validação de dashboard.

Limitações:

- formato de acesso pode não ser CSV/API;
- pode exigir extração manual ou técnica;
- necessário confirmar granularidade por ano, nacionalidade e tipo de prestação;
- deve ser evitada a mistura entre imposto fiscal e contribuição social.

---

#### Pergunta B — Contribuição fiscal por nacionalidade

**Viabilidade:** Média/Baixa.

Fontes prováveis:

- Autoridade Tributária;
- Portal das Finanças;
- Segurança Social;
- relatórios oficiais.

Conclusão preliminar:

A pergunta ainda é incerta. Não foi confirmada fonte pública direta que apresente IRS/contribuição fiscal de imigrantes por nacionalidade.

Limitações:

- dados fiscais podem estar protegidos ou agregados;
- pode não haver recorte público por nacionalidade;
- dados sociais/contributivos podem existir, mas não substituem automaticamente IRS;
- pode ser necessário reformular a pergunta para contribuição social/contributiva, caso a fonte fiscal não exista.

Recomendação ao Grupo 3:

Reformular ou manter como hipótese condicionada. Alternativa mais viável: contribuição à Segurança Social por nacionalidade, se a fonte pública for confirmada.

---

### 7.3 Subtema 3 — Comparação Portugal × Europa

#### Pergunta A — Ranking europeu de crescimento do fluxo imigratório

**Viabilidade:** Alta.

Fontes principais:

- Eurostat;
- PORDATA;
- OECD.

Conclusão preliminar:

A pergunta é viável. Existem fontes comparáveis para países europeus, mas o ranking terá de ser calculado pelo Grupo 1 ou Grupo 2.

Limitações:

- ranking não vem pronto;
- pode ser necessário calcular variação percentual ou CAGR;
- alguns datasets começam em 2013, não 2012;
- definições de fluxo migratório podem variar entre fontes;
- é necessário definir se será usado fluxo absoluto, taxa bruta de imigração ou outro indicador.

---

#### Pergunta B — Proporção de imigrantes na população total na UE27

**Viabilidade:** Alta.

Fontes principais:

- Eurostat foreign-born population;
- Eurostat população total;
- PORDATA.

Conclusão preliminar:

A pergunta é viável, desde que seja definida a métrica oficial de “imigrante”.

Limitações:

- “foreign-born” mede nascidos no estrangeiro;
- “foreign citizenship” mede cidadãos estrangeiros;
- os resultados podem variar conforme a definição escolhida;
- é necessário alinhar a definição com os Grupos 2 e 3 antes da visualização final.

---

## 8. Síntese Executiva

### 8.1 Perguntas com alta viabilidade

- Evolução de imigrantes residentes × PIB.
- Ranking europeu de crescimento do fluxo imigratório.
- Proporção de imigrantes na população total UE27.

### 8.2 Perguntas com viabilidade média/alta

- Trabalhadores imigrantes por setor × peso setorial no PIB.
- Contribuições à Segurança Social × prestações sociais.

### 8.3 Pergunta com maior risco

- Contribuição fiscal/IRS por nacionalidade de origem.

Motivo:

Não há confirmação preliminar de fonte pública direta com IRS por nacionalidade. A pergunta pode exigir reformulação ou troca para contribuição social/contributiva.

---

## 9. Recomendações para o Grupo 3

1. Manter o Subtema 1, Pergunta A.
2. Manter o Subtema 3, Perguntas A e B.
3. Ajustar conceitualmente o Subtema 2 para separar IRS, Segurança Social e prestações sociais.
4. Tratar a pergunta sobre contribuição fiscal por nacionalidade como incerta até validação adicional.
5. Evitar linguagem causal forte, principalmente em imigração × PIB.
6. Apresentar imigração × PIB como evolução conjunta, comparação temporal ou correlação visual, não como causalidade comprovada.

---

## 10. Próximos Passos Técnicos do Grupo 1

1. Validar quais fontes serão promovidas para coleta na próxima task.
2. Definir métrica oficial de “imigrante” para comparação europeia.
3. Definir se o Subtema 2 usará IRS, Segurança Social ou ambos.
4. Atualizar `metadata/catalogo_fontes.csv` com as fontes aprovadas.
5. Criar task de seleção dos datasets prioritários.
6. Criar task de coleta inicial dos dados aprovados.
7. Criar ou atualizar `metadata/dicionario_dados.csv` quando os primeiros datasets forem coletados/tratados.
8. Registrar a entrega final em `reports/entregas/` quando houver dataset validado para Grupo 2/Grupo 3.

---

## 11. Observações de Consolidação

- Separar claramente IRS, contribuições à Segurança Social e prestações sociais.
- Registrar fonte parcial ou fonte limitada como entrega válida, desde que a limitação esteja explícita.
- Não alterar perguntas do Grupo 3 nesta matriz; perguntas inviáveis devem ser sinalizadas como risco.
- A matriz consolida viabilidade preliminar, não validação final de dados.
- A próxima etapa deve transformar as fontes aprovadas em catálogo oficial de fontes.
- Após consolidação, atualizar a issue [#10](https://github.com/equipe-tratadados/tratamento-validacao-dados/issues/10) e reportar o resumo no grupo de líderes.

---

## 12. Status da G1-001.5

A matriz preliminar foi consolidada a partir das entregas disponíveis.

Status recomendado no GitHub Projects:

```txt
Review
```
