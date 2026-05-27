---
name: Tarefa de validação
about: Modelo para validar datasets antes da entrega final
labels: validacao, dados
---

# [G1-000] Título da tarefa

## Tipo

Validação de dados.

Se estiver perdido sobre como executar esta tarefa, siga:

```txt
docs/grupo-1/guia-operacional-iniciantes.md
templates/checklist-execucao-task.template.md
```

## Dataset a validar

| Campo | Valor |
| --- | --- |
| Arquivo de entrada | `data/processed/` |
| Arquivo final esperado | `data/validated/` |
| Task relacionada | `[G1-000]` |

## Checklist de validação

- [ ] Fonte confiável.
- [ ] Link da fonte informado.
- [ ] Data de acesso registrada.
- [ ] Período dos dados identificado.
- [ ] CSV abre corretamente.
- [ ] Encoding UTF-8.
- [ ] Separador ponto e vírgula `;`.
- [ ] Nome do arquivo sem espaços e sem caracteres problemáticos.
- [ ] Colunas principais documentadas.
- [ ] Arquivo na pasta correta.
- [ ] Commit com ID da task.
- [ ] PR com ID da task.
- [ ] Entrega útil para Grupo 2 ou Grupo 3.

## Problemas encontrados

```txt
Descrever inconsistências, erros, lacunas ou limitações.
```

## Resultado da validação

Marcar uma opção:

```txt
[ ] Aprovado
[ ] Aprovado com ressalvas
[ ] Reprovado
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
g1-003/validar-csv-habitacao
```

## Padrão de commit

```txt
test(validacao): registra checklist da base [G1-000]
```

Exemplo:

```txt
test(validacao): registra checklist da base de habitacao [G1-003]
```

## Decisão final

```txt
Descrever a decisão final: aprovado, aprovado com ressalvas ou reprovado.
```

## Observações

```txt
Adicionar limitações, dúvidas ou instruções adicionais.
```
