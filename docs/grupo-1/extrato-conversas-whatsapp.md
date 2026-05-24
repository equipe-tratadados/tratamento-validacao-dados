# Extrato das Conversas do WhatsApp — Grupo 1

## 1. Objetivo

Este documento resume apenas decisões, ações abertas, responsáveis, prazos e riscos extraídos das conversas do WhatsApp relacionadas ao projeto do estágio.

O conteúdo bruto das conversas não deve ser versionado no repositório. Telefones, links de convite, mensagens pessoais, brincadeiras e discussões informais foram descartados.

## 2. Decisões Confirmadas

| Data | Decisão | Registro operacional |
|---|---|---|
| 11/05/2026 | O fluxo geral do projeto foi dividido por grupos. | Grupo 3 define problemática/perguntas, Grupo 1 busca, organiza e valida dados, Grupo 2 constrói dashboard. |
| 12/05/2026 | Lucas ficou como líder do Grupo 1. | Responsável por traduzir demandas em tarefas, organizar prioridades e consolidar entregas do Grupo 1. |
| 12/05/2026 a 15/05/2026 | Stack do Grupo 1 foi confirmada. | GitHub para repositório e documentação técnica, GitHub Projects para tarefas, Notion como apoio executivo, CSV UTF-8 como formato inicial de dados. |
| 15/05/2026 | Metodologia de trabalho do Grupo 1 foi alinhada. | CRISP-DM como base para projeto de dados, com Kanban/GitHub Projects para acompanhamento operacional. |
| 23/05/2026 | O Grupo 1 foi reorientado a não redefinir perguntas de negócio. | Business Understanding fica com o Grupo 3; Grupo 1 valida viabilidade técnica das fontes públicas. |
| 23/05/2026 a 24/05/2026 | A task G1-001 passou a focar na validação preliminar de fontes por pergunta do Grupo 3. | As entregas devem ser registradas nas issues do GitHub, não perdidas no WhatsApp. |

## 3. Estado Atual do Projeto

Tema atual: **Imigração e Economia**.

Subtemas recebidos do Grupo 3:

1. **Fluxo Imigratório x Crescimento Económico**
   - Pergunta A: Qual foi a evolução do número de imigrantes residentes em Portugal entre 2010 e 2024, e como se relaciona com a evolução do PIB no mesmo período?
   - Pergunta B: Em que setores de atividade económica se concentram os trabalhadores imigrantes, e qual o peso desses setores no PIB nacional?
2. **Contribuição IRS x Prestações Sociais**
   - Pergunta A: Quanto pagaram os imigrantes à Segurança Social entre 2015 e 2025, e quanto receberam em prestações sociais no mesmo período?
   - Pergunta B: Como se distribui a contribuição fiscal dos imigrantes por nacionalidade de origem?
3. **Comparação Portugal x Europa**
   - Pergunta A: Qual a posição de Portugal no ranking europeu de crescimento do fluxo imigratório entre 2012 e 2023?
   - Pergunta B: Em termos de proporção de imigrantes na população total, onde se situa Portugal face aos 27 países da UE?

## 4. Issues Oficiais da G1-001

| Issue | Responsável | Frente | Entrega esperada |
|---|---|---|---|
| [#5](https://github.com/equipe-tratadados/tratamento-validacao-dados/issues/5) | Lucas | Task principal G1-001 | Acompanhar a validação preliminar por pergunta. |
| [#6](https://github.com/equipe-tratadados/tratamento-validacao-dados/issues/6) | Tabata | Imigração, integração e população estrangeira | Comentar pelo menos 2 fontes ou registrar limitação/fonte não encontrada. |
| [#7](https://github.com/equipe-tratadados/tratamento-validacao-dados/issues/7) | Antony | Economia, fiscalidade, Segurança Social, IRS e setores | Comentar pelo menos 2 fontes ou registrar limitação/fonte não encontrada. |
| [#8](https://github.com/equipe-tratadados/tratamento-validacao-dados/issues/8) | Nubia | Comparação Portugal x Europa e fontes acessíveis para dashboard | Comentar pelo menos 2 fontes ou registrar limitação/fonte não encontrada. |
| [#9](https://github.com/equipe-tratadados/tratamento-validacao-dados/issues/9) | Ana Cláudia | Fluxo, prazos, bloqueios e padrão das respostas | Comentar resumo de acompanhamento. |
| [#10](https://github.com/equipe-tratadados/tratamento-validacao-dados/issues/10) | Lucas | Consolidação da matriz de viabilidade | Consolidar entregas e preparar resposta preliminar aos líderes. |

Prazo operacional:

- Entregas individuais: **26/05/2026 18:00 Europe/Lisbon**.
- Consolidação da matriz: **26/05/2026 23:59 Europe/Lisbon**.

## 5. Ações Abertas

1. Cada responsável deve comentar a sua issue com fontes encontradas, limitações ou fonte não encontrada.
2. Ana Cláudia deve registrar status, bloqueios, pendências e cards em andamento.
3. Lucas deve consolidar a matriz preliminar de viabilidade após as entregas individuais.
4. Perguntas com baixa viabilidade devem ser sinalizadas ao Grupo 3 sem alterar o escopo por conta própria.
5. O WhatsApp deve ser usado apenas para avisos rápidos, dúvidas e bloqueios; a execução oficial fica no GitHub Projects/Issues.

## 6. Riscos e Pontos de Atenção

| Risco | Impacto | Mitigação |
|---|---|---|
| Ruído no WhatsApp | Membros perdem prazos, tarefas e contexto. | Centralizar descrição e entrega nas issues. |
| Permissões do GitHub Projects | Responsáveis podem não conseguir visualizar ou mover cards. | Reportar bloqueio no WhatsApp e registrar na issue de acompanhamento. |
| Nenhum comentário de entrega nas issues | Não há evidência verificável de avanço. | Cada responsável deve comentar diretamente na sua issue. |
| Confusão entre IRS e Segurança Social | Pode gerar análise incorreta. | Separar imposto fiscal, contribuição social e prestação social em todas as validações. |
| Fontes candidatas tratadas como validadas | Risco de usar dado inadequado no dashboard. | Classificar viabilidade e registrar limitações antes de marcar qualquer fonte como validada. |

## 7. Regra de Registro

Uma fonte citada em conversa só entra como fonte validada quando houver evidência mínima na issue correspondente:

```txt
Subtema:
Pergunta relacionada:
Fonte encontrada:
Instituição responsável:
Link:
Período disponível:
Granularidade:
Formato de acesso:
Viabilidade: Alta / Média / Baixa / Fonte não encontrada
Limitação principal:
Próximo passo:
```
