# Documentação do Grupo 1

Este diretório reúne a documentação operacional do Grupo 1 — Tratamento e Validação de Dados.

## Índice

| Documento | Finalidade |
| --- | --- |
| [guia-operacional-iniciantes.md](guia-operacional-iniciantes.md) | Passo a passo para iniciantes usarem GitHub, GitHub Projects, issues, branches, commits e Pull Requests no projeto. |
| [processo-interno.md](processo-interno.md) | Fluxo de trabalho, papéis, GitHub Projects, branches, commits, PRs, prioridades e Definition of Done. |
| [padrao-csv.md](padrao-csv.md) | Regras para organização, nomeação, encoding e validação de arquivos CSV. |
| [catalogo-fontes.md](catalogo-fontes.md) | Como registrar fontes públicas e avaliar confiabilidade. |
| [log-fontes.md](log-fontes.md) | Log central para entregas diretas de fontes via Pull Request. |
| [dicionario-dados.md](dicionario-dados.md) | Como documentar colunas, tipos, unidades e observações dos datasets. |
| [checklist-validacao.md](checklist-validacao.md) | Checklist mínimo antes de concluir uma entrega. |
| [extrato-conversas-whatsapp.md](extrato-conversas-whatsapp.md) | Decisões, ações, riscos e prazos extraídos das conversas do estágio. |
| [matriz-viabilidade-g1-001.md](matriz-viabilidade-g1-001.md) | Matriz preliminar para validar fontes por pergunta do Grupo 3. |
| [datasets-prioritarios-g1-006.md](datasets-prioritarios-g1-006.md) | Seleção oficial dos datasets prioritários para a primeira coleta real da Sprint 1. |

## Status atual

O grupo concluiu a validação preliminar da **G1-001 — Validar viabilidade preliminar de dados das perguntas do Grupo 3**, atualizou a matriz oficial, publicou o catálogo de fontes reais e definiu o padrão CSV/Dicionário de Dados.

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
| G1-004 | Concluída | Status operacional da documentação do Grupo 1 atualizado. |
| G1-005 | Concluída | Compatibilidade CSV e Dicionário de Dados publicados. |
| G1-006 | Review | Datasets prioritários selecionados para a primeira coleta real. |
| G1-007 | Próxima | Coletar o primeiro dataset bruto aprovado. |

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
| Entregas de fontes candidatas | `docs/grupo-1/log-fontes.md` |
| Fontes aceitas no catálogo oficial | `metadata/catalogo_fontes.csv` |
| Dicionário de dados | `metadata/dicionario_dados.csv` |
| Entrega final | `reports/entregas/` |
| Regras do processo | `docs/grupo-1/` |

## Para quem está começando

Antes de assumir uma task, leia o [guia operacional para iniciantes](guia-operacional-iniciantes.md) e copie o checklist de execução em `templates/checklist-execucao-task.template.md`.
