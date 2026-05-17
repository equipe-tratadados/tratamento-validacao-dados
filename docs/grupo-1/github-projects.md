# Configuração do GitHub Projects — Grupo 1

Este documento registra a configuração final do GitHub Projects usada pelo Grupo 1 — Tratamento e Validação de Dados.

O objetivo é deixar o ambiente pronto para iniciar a execução quando o tema base do projeto for definido, evitando que os membros do grupo precisem descobrir o fluxo do GitHub e do GitHub Projects durante a sprint.

## Estado atual

O GitHub Projects foi configurado como quadro operacional do Grupo 1.

No momento, ainda não devem ser criadas as tasks de execução `G1-001` até `G1-007`, porque o tema base do projeto ainda não foi formalmente definido.

A configuração atual serve como preparação estrutural.

## Quando criar novas tasks

Novas tasks devem ser criadas quando pelo menos uma das condições abaixo estiver cumprida:

- o tema base do projeto estiver definido;
- houver demanda oficial do Grupo 2;
- houver demanda oficial do Grupo 3;
- houver decisão da liderança geral;
- houver necessidade interna de documentação, organização ou correção do repositório.

Enquanto o tema não estiver definido, o Project deve permanecer preparado, mas sem backlog artificial de coleta, tratamento ou validação.

## Views configuradas

O Project deve conter as seguintes views.

| View | Layout | Finalidade |
| --- | --- | --- |
| Tabela Operacional | Table | Visão completa das tasks e campos operacionais. |
| Quadro Operacional | Board | Fluxo Kanban principal do Grupo 1. |
| Backlog Priorizado | Table | Priorização por prioridade e prazo. |
| Por Responsável | Table ou Board | Acompanhamento de carga por membro do grupo. |
| Validação e Entregas | Table | Controle de datasets validados e entregas para outros grupos. |

## Status do fluxo

O campo `Status` deve conter as seguintes opções:

| Status | Uso |
| --- | --- |
| Backlog | Demanda ainda não refinada. |
| Ready | Tarefa pronta para ser assumida. |
| In Progress | Tarefa em execução. |
| Review | Entrega ou Pull Request aguardando revisão. |
| Changes Requested | Revisão solicitou correções. |
| Done | Tarefa concluída, revisada e mergeada na `main`. |

Fluxo padrão:

```txt
Backlog → Ready → In Progress → Review → Changes Requested → Done
```

## Campos customizados

O Project deve conter os seguintes campos.

| Campo | Tipo | Uso |
| --- | --- | --- |
| ID da task | Text | ID único da tarefa, exemplo `G1-001`. |
| Tipo | Single select | Classificação da tarefa. |
| Prioridade | Single select | Prioridade operacional P0 a P4. |
| Fonte | Text | Fonte de dados associada, exemplo INE, PORDATA ou Eurostat. |
| Sprint | Text | Sprint associada, exemplo `Sprint 01`. |
| Prazo | Date | Data limite acordada. |
| Entrega esperada | Text | Resultado esperado da tarefa. |
| Dataset | Text | Nome do dataset ou arquivo relacionado. |
| Status da validação | Single select | Situação da validação dos dados. |
| Grupo destino | Single select | Grupo que receberá a entrega. |

## Opções do campo Tipo

```txt
Coleta
Tratamento
Validação
Documentação
Script
Entrega
```

## Opções do campo Prioridade

```txt
P0
P1
P2
P3
P4
```

Critérios:

| Prioridade | Significado |
| --- | --- |
| P0 | Bloqueante. Sem isso, outros grupos ou etapas não avançam. |
| P1 | Alto valor e pouca incerteza. |
| P2 | Dependência externa. |
| P3 | Documentação ou validação. |
| P4 | Melhoria ou baixo impacto. |

Não utilizar Matriz de Eisenhower.

## Opções do campo Status da validação

```txt
Não iniciado
Em validação
Aprovado
Aprovado com ressalvas
Reprovado
```

## Opções do campo Grupo destino

```txt
Grupo 2
Grupo 3
Ambos
Interno G1
```

## Ordem recomendada dos campos na Tabela Operacional

```txt
Title
Assignees
Status
ID da task
Tipo
Prioridade
Fonte
Sprint
Prazo
Entrega esperada
Dataset
Status da validação
Grupo destino
Linked pull requests
```

## Labels do repositório

As labels abaixo devem existir no repositório para apoiar filtros, automações e leitura rápida das Issues e Pull Requests.

```txt
grupo-1
tipo:coleta
tipo:tratamento
tipo:validacao
tipo:documentacao
tipo:script
tipo:entrega
prioridade:p0
prioridade:p1
prioridade:p2
prioridade:p3
prioridade:p4
status:bloqueado
```

As labels não substituem os campos do Project. Elas apenas complementam a gestão das Issues e Pull Requests.

## Relação obrigatória entre Issue, Project, branch, commit e Pull Request

Toda tarefa executável deve seguir o mesmo ID de rastreabilidade.

Exemplo:

```txt
Issue:
[G1-001] Coletar dados de inflação no INE

Branch:
g1-001/coletar-dados-inflacao-ine

Commit:
data(ine): adiciona base bruta de inflacao [G1-001]

Pull Request:
[G1-001] data(ine): adiciona base bruta de inflacao
```

## Quando uma task pode ir para Done

Uma task só pode ir para `Done` quando cumprir os pontos aplicáveis:

- Issue ou card atualizado;
- branch criada com ID da task;
- commits no padrão definido;
- Pull Request aberto com ID da task;
- arquivos colocados nas pastas corretas;
- documentação atualizada, quando aplicável;
- fonte documentada, quando aplicável;
- dicionário de dados atualizado, quando aplicável;
- checklist de validação preenchido, quando aplicável;
- revisão concluída;
- merge feito na `main`.

## Uso esperado quando o tema for definido

Após a definição do tema base, o PO deve criar as primeiras tasks reais no Project seguindo esta ordem:

1. mapear fontes oficiais do tema;
2. criar ou atualizar catálogo de fontes;
3. definir datasets prioritários;
4. criar tasks de coleta;
5. criar tasks de tratamento;
6. criar tasks de validação;
7. registrar entrega para Grupo 2 e Grupo 3.

## Modelo inicial de task após definição do tema

```txt
[G1-001] Mapear fontes oficiais para [tema definido]
```

Campos recomendados:

| Campo | Valor |
| --- | --- |
| Status | Ready |
| Tipo | Coleta |
| Prioridade | P0 |
| Fonte | A definir |
| Sprint | Sprint 01 |
| Entrega esperada | Lista de fontes oficiais com links, período disponível e limitações |
| Grupo destino | Interno G1 |

## Regra final

Enquanto o tema base não estiver definido, o GitHub Projects deve ficar configurado e pronto, mas sem criação de tarefas fictícias de coleta, tratamento ou validação.

Quando o tema for definido, toda execução deve começar pelo Project, passar por Issue, branch, commit, Pull Request, revisão e merge.
