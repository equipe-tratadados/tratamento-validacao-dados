# Documentação do Grupo 1

Este diretório reúne a documentação operacional do Grupo 1 — Tratamento e Validação de Dados.

## Índice

| Documento | Finalidade |
| --- | --- |
| [processo-interno.md](processo-interno.md) | Fluxo de trabalho, papéis, GitHub Projects, branches, commits, PRs, prioridades e Definition of Done. |
| [padrao-csv.md](padrao-csv.md) | Regras para organização, nomeação, encoding e validação de arquivos CSV. |
| [catalogo-fontes.md](catalogo-fontes.md) | Como registrar fontes públicas e avaliar confiabilidade. |
| [dicionario-dados.md](dicionario-dados.md) | Como documentar colunas, tipos, unidades e observações dos datasets. |
| [checklist-validacao.md](checklist-validacao.md) | Checklist mínimo antes de concluir uma entrega. |
| [extrato-conversas-whatsapp.md](extrato-conversas-whatsapp.md) | Decisões, ações, riscos e prazos extraídos das conversas do estágio. |
| [matriz-viabilidade-g1-001.md](matriz-viabilidade-g1-001.md) | Matriz preliminar para validar fontes por pergunta do Grupo 3. |

## Status atual

O grupo concluiu a validação preliminar da **G1-001 — Validar viabilidade preliminar de dados das perguntas do Grupo 3** e está na fase de transformar a validação em documentação operacional reutilizável.

Tema atual: **Imigração e Economia**.

Registro oficial de contexto:

- [Extrato das conversas do WhatsApp](extrato-conversas-whatsapp.md)
- [Matriz preliminar de viabilidade — G1-001](matriz-viabilidade-g1-001.md)
- [Issue principal G1-001](https://github.com/equipe-tratadados/tratamento-validacao-dados/issues/5)
- [Pull Request G1-002](https://github.com/equipe-tratadados/tratamento-validacao-dados/pull/13)
- [Pull Request G1-003](https://github.com/equipe-tratadados/tratamento-validacao-dados/pull/15)

Andamento operacional:

| Task | Estado | Entrega |
| --- | --- | --- |
| G1-001 | Concluída | Validação preliminar das perguntas do Grupo 3. |
| G1-002 | Concluída | Matriz oficial de viabilidade atualizada no repositório. |
| G1-003 | Concluída | Catálogo oficial de fontes atualizado com fontes reais. |
| G1-004 | Ready | Atualizar status operacional da documentação do Grupo 1. |
| G1-005 | Ready / In Progress | Confirmar compatibilidade CSV com Grupo 2 e publicar Dicionário de Dados. |
| G1-006 | Backlog | Selecionar datasets prioritários para coleta inicial. |

## Regra central

Toda atividade relevante deve ter um ID único de task.

Exemplo:

```txt
[G1-001] Coletar dados de inflação no INE
```

Esse ID deve aparecer no card do GitHub Projects, na branch, no commit, no Pull Request e na entrega documentada.

## Fluxo do Grupo 1

```txt
fonte pública → data/raw → data/processed → data/validated → entrega para Grupo 2/Grupo 3
```

## Onde registrar informação

| Informação | Local correto |
| --- | --- |
| Dados brutos | `data/raw/` |
| Dados tratados | `data/processed/` |
| Dados validados | `data/validated/` |
| Fontes | `metadata/catalogo_fontes.csv` |
| Dicionário de dados | `metadata/dicionario_dados.csv` |
| Entrega final | `reports/entregas/` |
| Regras do processo | `docs/grupo-1/` |
