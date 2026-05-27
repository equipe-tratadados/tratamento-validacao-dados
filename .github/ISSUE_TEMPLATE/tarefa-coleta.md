---
name: Tarefa de coleta
about: Modelo para solicitar coleta de dados públicos
labels: coleta, dados
---

# [G1-000] Título da tarefa

## Tipo

Coleta de dados.

Se estiver perdido sobre como executar esta tarefa, siga:

```txt
docs/grupo-1/guia-operacional-iniciantes.md
templates/checklist-execucao-task.template.md
```

## Objetivo

Descrever de forma objetiva o que deve ser coletado.

```txt
Exemplo: Coletar dados de inflação em Portugal no período 2020-2024.
```

## Fonte esperada

| Campo | Valor |
| --- | --- |
| Nome da fonte |  |
| Instituição |  |
| Link |  |
| Período esperado |  |
| Tipo de arquivo esperado |  |

## Entrega esperada

```txt
Exemplo: CSV bruto salvo em data/raw/ e fonte registrada em metadata/catalogo_fontes.csv.
```

## Registro obrigatório da fonte

Antes de concluir a coleta, registrar a fonte em:

```txt
docs/grupo-1/log-fontes.md
```

Use o modelo:

```txt
templates/registro-fonte.template.md
```

Se a fonte for candidata a oficial, atualizar também:

```txt
metadata/catalogo_fontes.csv
```

## Prioridade

Marcar uma opção:

```txt
[ ] P0 — Bloqueante
[ ] P1 — Alto valor / pouca incerteza
[ ] P2 — Dependência externa
[ ] P3 — Documentação / validação
[ ] P4 — Melhoria / baixo impacto
```

## Responsável

```txt
@usuario
```

## Prazo

```txt
AAAA-MM-DD HH:MM
```

## Branch esperada

```txt
g1-000/descricao-curta-da-tarefa
```

Exemplo:

```txt
g1-001/coletar-dados-inflacao-ine
```

## Padrão de commit

```txt
data(escopo): descrição curta [G1-000]
```

Exemplo:

```txt
data(ine): adiciona base bruta de inflacao [G1-001]
```

## Critérios de aceite

- [ ] Fonte pública identificada.
- [ ] Link da fonte informado.
- [ ] Data de acesso registrada.
- [ ] Período dos dados identificado.
- [ ] Arquivo salvo em `data/raw/`.
- [ ] Nome do arquivo segue o padrão definido.
- [ ] Entrada registrada em `docs/grupo-1/log-fontes.md`.
- [ ] Fonte registrada em `metadata/catalogo_fontes.csv`.
- [ ] Commit segue o padrão definido.
- [ ] Pull Request aberto com ID da task.

## Observações

```txt
Adicionar limitações, dúvidas ou instruções adicionais.
```
