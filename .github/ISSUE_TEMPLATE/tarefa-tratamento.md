---
name: Tarefa de tratamento
about: Modelo para limpeza, transformação e padronização de dados
labels: tratamento, dados
---

# [G1-000] Título da tarefa

## Tipo

Tratamento de dados.

Se estiver perdido sobre como executar esta tarefa, siga:

```txt
docs/grupo-1/guia-operacional-iniciantes.md
templates/checklist-execucao-task.template.md
```

## Dataset de entrada

| Campo | Valor |
| --- | --- |
| Arquivo de entrada | `data/raw/` |
| Fonte associada |  |
| Task de coleta relacionada | `[G1-000]` |

## Objetivo do tratamento

Descrever o resultado esperado após limpeza e padronização.

```txt
Exemplo: Padronizar nomes de colunas, remover linhas vazias, normalizar separador decimal e salvar versão tratada.
```

## Transformações esperadas

- [ ] Renomear colunas.
- [ ] Remover linhas vazias ou inválidas.
- [ ] Padronizar tipos de dados.
- [ ] Padronizar datas.
- [ ] Padronizar separador decimal, quando aplicável.
- [ ] Criar `id_registro`, quando aplicável.
- [ ] Incluir `fonte_id`, quando aplicável.
- [ ] Outras transformações: `descrever`.

## Arquivo de saída

```txt
data/processed/nome_do_dataset_processed.csv
```

## Prioridade

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
g1-002/tratar-dados-salarios-pordata
```

## Padrão de commit

```txt
data(escopo): descrição curta [G1-000]
```

Exemplo:

```txt
data(pordata): trata base de salarios [G1-002]
```

## Critérios de aceite

- [ ] Dataset de entrada identificado.
- [ ] Transformações descritas.
- [ ] Arquivo tratado salvo em `data/processed/`.
- [ ] CSV em UTF-8.
- [ ] Separador `;`.
- [ ] Nome do arquivo segue o padrão definido.
- [ ] Dicionário de dados atualizado, quando aplicável.
- [ ] Commit segue o padrão definido.
- [ ] Pull Request aberto com ID da task.

## Observações

```txt
Adicionar limitações, dúvidas ou instruções adicionais.
```
