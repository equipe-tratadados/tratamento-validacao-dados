# Processo Interno do Grupo 1

## Objetivo

Definir o fluxo operacional do Grupo 1 para coleta, tratamento, validação e documentação de dados públicos.

Este processo deve ser seguido por todos os membros do grupo para manter rastreabilidade, reduzir retrabalho e permitir que os Grupos 2 e 3 utilizem os dados sem depender de explicações informais.

Para o passo a passo detalhado de execução, use o guia:

```txt
docs/grupo-1/guia-operacional-iniciantes.md
```

Checklist copiável para qualquer task:

```txt
templates/checklist-execucao-task.template.md
```

## Papéis do Grupo 1

| Papel | Responsabilidade |
| --- | --- |
| PO / Líder do Grupo 1 | Organizar backlog, prioridades, critérios de aceite e alinhamento com outros grupos. |
| Scrum Master | Acompanhar prazos, bloqueios, fluxo das tasks e atualização do GitHub Projects. |
| Responsável pela coleta | Identificar fonte pública, baixar dados e registrar fonte. |
| Responsável pelo tratamento | Limpar, padronizar e preparar dados para validação. |
| Responsável pela validação | Revisar estrutura, consistência, encoding, separador, dicionário e utilidade da entrega. |

## Fluxo semanal

1. Verificar demandas do Grupo 2, Grupo 3 ou liderança geral.
2. Criar ou atualizar cards no GitHub Projects.
3. Definir prioridade P0 a P4.
4. Atribuir responsável e prazo.
5. Executar coleta, tratamento ou validação.
6. Abrir Pull Request.
7. Revisar entrega.
8. Fazer merge na `main`.
9. Registrar entrega em `reports/entregas/`.

## Entrega direta de fontes

Para reduzir retrabalho de consolidação, a entrega de fontes deve ser feita diretamente no GitHub:

1. o responsável abre uma branch com o ID da task;
2. copia o modelo de `templates/registro-fonte.template.md`;
3. cola uma nova entrada no fim de `docs/grupo-1/log-fontes.md`;
4. preenche todos os campos obrigatórios da fonte;
5. se a fonte for candidata a oficial, atualiza também `metadata/catalogo_fontes.csv`;
6. abre Pull Request para revisão.

O líder deve revisar o PR e solicitar ajustes no próprio PR, em vez de copiar a entrega manualmente para outro documento.

## GitHub Projects

### Colunas obrigatórias

| Coluna | Uso |
| --- | --- |
| Backlog | Ideias, demandas e tarefas ainda não prontas para execução. |
| Ready | Tarefas claras, com responsável possível e critério de aceite definido. |
| In Progress | Tarefas em execução. |
| Review | Tarefas com Pull Request aberto ou aguardando validação. |
| Changes Requested | Tarefas que precisam de ajuste antes de concluir. |
| Done | Tarefas concluídas, revisadas e com merge feito na `main`. |

### Campos recomendados

- ID da task;
- responsável;
- tipo;
- prioridade;
- sprint;
- fonte;
- entrega esperada;
- prazo;
- status;
- link do PR.

## Padrão de task

Toda task deve ter ID único no formato:

```txt
[G1-001] Título objetivo da tarefa
```

Exemplos:

```txt
[G1-001] Coletar dados de inflação no INE
[G1-002] Tratar dados de salários da PORDATA
[G1-003] Validar CSV de habitação
```

## Padrão único de branch

Formato obrigatório:

```txt
g1-000/descricao-curta-da-tarefa
```

Exemplos válidos:

```txt
g1-001/coletar-dados-inflacao-ine
g1-002/tratar-dados-salarios-pordata
g1-003/validar-csv-habitacao
```

Exemplos inválidos:

```txt
task/g1-coleta-ine-ipc
data/g1-habitacao-raw
docs/g1-dicionario
```

## Padrão de commit

Os commits devem seguir Conventional Commits adaptado para dados.

Formato:

```txt
tipo(escopo): descrição curta [ID-DA-TASK]
```

Tipos permitidos:

| Tipo | Uso |
| --- | --- |
| `data` | Inclusão ou alteração de dados. |
| `docs` | Documentação. |
| `fix` | Correção. |
| `refactor` | Reorganização sem alterar resultado. |
| `test` | Validação ou checks. |
| `chore` | Organização interna. |
| `feat` | Novo script, automação ou funcionalidade. |

Exemplos válidos:

```txt
data(ine): adiciona base bruta de inflacao [G1-001]
docs(fontes): documenta fonte de salarios da pordata [G1-002]
fix(csv): corrige separador do arquivo de habitacao [G1-003]
test(validacao): registra checklist da base de inflacao [G1-004]
```

Exemplos inválidos:

```txt
update
dados
final
arrumei coisas
teste
```

## Padrão de Pull Request

Título obrigatório:

```txt
[G1-000] tipo(escopo): descrição curta
```

Exemplo:

```txt
[G1-001] data(ine): adiciona base bruta de inflacao
```

O PR deve explicar:

- ID da task;
- objetivo;
- arquivos criados ou alterados;
- fonte usada;
- validação realizada;
- limitações conhecidas;
- impacto para Grupo 2 ou Grupo 3.

## Prioridades

Não utilizar Matriz de Eisenhower. A priorização deve seguir o fluxo real dos dados e as dependências entre grupos.

| Prioridade | Critério | Exemplo |
| --- | --- | --- |
| P0 — Bloqueante | Sem isso, outros grupos ou etapas não avançam. | Definir fonte oficial de inflação, salários ou habitação. |
| P1 — Alto valor / pouca incerteza | Fonte confiável, dados acessíveis e entrega rápida. | Coletar dados do INE já mapeados. |
| P2 — Dependência externa | Depende de outra pessoa, grupo ou decisão. | Tratar dados apenas depois da coleta estar concluída. |
| P3 — Documentação / validação | Não bloqueia de imediato, mas garante qualidade e rastreabilidade. | Atualizar dicionário de dados ou checklist. |
| P4 — Melhoria / baixo impacto | Ajuste secundário. | Melhorar README, nomes ou formatação. |

## Fluxo dos dados

```txt
fonte pública → data/raw → data/processed → data/validated → entrega para Grupo 2/Grupo 3
```

## Definition of Done

Uma task só pode ir para `Done` quando cumprir todos os pontos aplicáveis:

- fonte documentada;
- fonte registrada em `docs/grupo-1/log-fontes.md`, quando aplicável;
- link da fonte informado;
- data de acesso registrada;
- período dos dados identificado;
- CSV salvo na pasta correta;
- encoding UTF-8;
- separador ponto e vírgula;
- dicionário de dados atualizado, quando aplicável;
- catálogo de fontes atualizado, quando a fonte for aceita como oficial;
- checklist de validação preenchido;
- commit no padrão definido;
- Pull Request aberto;
- Pull Request revisado;
- correções aplicadas, se houver;
- merge feito na `main`.

## Regra de comunicação técnica

Decisões operacionais devem ser registradas no GitHub, em Markdown ou no card da task. O WhatsApp deve ser usado apenas para comunicação breve, alinhamento e aviso de bloqueios.
