# Checklist de Execução de Task

Copie este checklist para sua issue, bloco de notas ou descrição do Pull Request antes de começar uma task.

## 1. Dados da task

| Campo | Valor |
| --- | --- |
| ID da task | `[G1-000]` |
| Título da task |  |
| Responsável | `@usuario` |
| Tipo | Coleta / Tratamento / Validação / Documentação / Script / Entrega |
| Prioridade | P0 / P1 / P2 / P3 / P4 |
| Status inicial | Backlog / Ready / In Progress |
| Prazo | AAAA-MM-DD |
| Grupo destino | Grupo 2 / Grupo 3 / Ambos / Interno G1 |

## 2. Antes de começar

- [ ] Li a issue inteira.
- [ ] Entendi a entrega esperada.
- [ ] Entendi os critérios de aceite.
- [ ] Confirmei se existe dependência de outra task.
- [ ] Confirmei quais arquivos devo alterar.
- [ ] Confirmei que a task está em `Ready` ou pode ir para `In Progress`.
- [ ] Movi o card para `In Progress`.

## 3. Branch

Nome da branch:

```txt
g1-000/descricao-curta-da-tarefa
```

- [ ] Criei branch a partir da `main` atualizada.
- [ ] A branch contém o ID da task.
- [ ] Não estou trabalhando direto na `main`.

## 4. Arquivos alterados

Liste os arquivos criados ou alterados:

```txt
- docs/...
- data/raw/...
- data/processed/...
- data/validated/...
- metadata/catalogo_fontes.csv
- metadata/dicionario_dados.csv
- reports/entregas/...
```

- [ ] Os arquivos estão nas pastas corretas.
- [ ] Não incluí arquivos de outra task.
- [ ] Os nomes dos arquivos estão em `snake_case`, sem espaços e sem acentos.

## 5. Fonte ou dataset

| Campo | Valor |
| --- | --- |
| `fonte_id` | `FONTE-000` |
| Nome da fonte |  |
| Instituição |  |
| URL |  |
| Data de acesso | AAAA-MM-DD |
| Período dos dados |  |
| Formato | CSV / Excel / API / PDF / página web / outro |
| Limitação principal |  |

- [ ] A fonte foi registrada em `docs/grupo-1/log-fontes.md`, quando aplicável.
- [ ] A fonte foi registrada em `metadata/catalogo_fontes.csv`, quando oficial.
- [ ] O CSV segue `DICIONARIO_DE_DADOS.md`, quando aplicável.
- [ ] O dicionário foi atualizado em `metadata/dicionario_dados.csv`, quando aplicável.

## 6. Comandos Git usados

```powershell
git switch main
git pull --ff-only origin main
git switch -c g1-000/descricao-curta-da-tarefa
git status -sb
git add caminho/do/arquivo
git commit -m "tipo(escopo): descrição curta [G1-000]"
git push -u origin g1-000/descricao-curta-da-tarefa
```

- [ ] Rodei `git status -sb`.
- [ ] Revisei `git diff` antes do commit.
- [ ] Fiz `git add` apenas dos arquivos da task.
- [ ] O commit segue o padrão.
- [ ] A branch foi enviada para o GitHub.

## 7. Pull Request

Título do PR:

```txt
[G1-000] tipo(escopo): descrição curta
```

- [ ] O PR aponta para `main`.
- [ ] O PR usa a branch correta.
- [ ] O PR contém o ID da task.
- [ ] O PR explica o objetivo.
- [ ] O PR lista arquivos alterados.
- [ ] O PR informa fonte usada, quando aplicável.
- [ ] O PR informa validação realizada.
- [ ] O PR informa limitações conhecidas.
- [ ] O PR informa impacto para Grupo 2 ou Grupo 3.
- [ ] O PR usa `Closes #NUMERO` quando deve fechar a issue.
- [ ] Movi o card para `Review`.

## 8. Revisão

- [ ] Respondi comentários do revisor.
- [ ] Corrigi ajustes solicitados, se houver.
- [ ] Fiz novo commit na mesma branch, se houver ajuste.
- [ ] Voltei o card de `Changes Requested` para `Review`, se aplicável.

## 9. Pós-merge

- [ ] O PR foi mergeado na `main`.
- [ ] A issue foi fechada como `completed`.
- [ ] O card foi movido para `Done`.
- [ ] A entrega final foi registrada em `reports/entregas/`, quando aplicável.
- [ ] O link do PR/entrega foi comunicado no canal adequado.

## 10. Conferência final

Responda antes de considerar a task finalizada:

```txt
Esta entrega está pronta para outro grupo trabalhar ou está apenas transferindo problema para frente?
```
