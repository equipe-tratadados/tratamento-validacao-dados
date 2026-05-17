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
