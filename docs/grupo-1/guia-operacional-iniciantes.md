# Guia Operacional para Iniciantes — GitHub + GitHub Projects

## Se você está começando agora

Este guia é o ponto de partida para qualquer pessoa do Grupo 1 que ainda não sabe como começar uma tarefa no GitHub.

Ele não cria um padrão novo. Ele apenas transforma os padrões já definidos em um passo a passo prático.

Use este guia quando você precisar:

- encontrar sua task;
- entender o que deve entregar;
- criar branch;
- editar pelo navegador do GitHub;
- editar pelo Git local ou VS Code;
- registrar fonte;
- coletar, tratar ou validar dados;
- abrir Pull Request;
- responder revisão;
- saber quando a task pode ir para `Done`.

Antes de começar, abra estes documentos:

| Documento | Para que serve |
| --- | --- |
| [processo-interno.md](processo-interno.md) | Regras oficiais do fluxo do Grupo 1. |
| [github-projects.md](github-projects.md) | Como o Project deve estar organizado. |
| [DICIONARIO_DE_DADOS.md](../../DICIONARIO_DE_DADOS.md) | Padrão oficial dos CSVs. |
| [log-fontes.md](log-fontes.md) | Onde registrar fontes entregues por PR. |
| [checklist-validacao.md](checklist-validacao.md) | Como validar uma entrega antes de concluir. |

Se você estiver perdido, siga esta ordem:

1. Abra o GitHub Projects.
2. Encontre sua task.
3. Leia a issue inteira.
4. Copie o checklist de `templates/checklist-execucao-task.template.md`.
5. Crie uma branch com o ID da task.
6. Faça a entrega.
7. Abra Pull Request.
8. Aguarde revisão.
9. Corrija se pedirem ajustes.
10. Só considere concluído depois do merge na `main`.

## Mapa rápido do projeto

O repositório é a fonte oficial da execução técnica do Grupo 1.

```txt
fonte pública
   ↓
data/raw/
   ↓
data/processed/
   ↓
data/validated/
   ↓
reports/entregas/
   ↓
Grupo 2 / Grupo 3
```

Use cada pasta assim:

| Local | Use para |
| --- | --- |
| `data/raw/` | Arquivo original baixado da fonte, sem tratamento pesado. |
| `data/processed/` | CSV tratado, limpo e padronizado. |
| `data/validated/` | CSV revisado e pronto para Grupo 2 ou Grupo 3. |
| `docs/grupo-1/` | Documentação operacional do Grupo 1. |
| `docs/grupo-1/log-fontes.md` | Registro humano das fontes entregues por PR. |
| `metadata/catalogo_fontes.csv` | Catálogo técnico oficial das fontes aceitas. |
| `metadata/dicionario_dados.csv` | Registro técnico das colunas dos CSVs validados. |
| `templates/` | Modelos para copiar e colar. |
| `.github/ISSUE_TEMPLATE/` | Modelos usados ao criar issues. |
| `.github/PULL_REQUEST_TEMPLATE.md` | Modelo usado ao abrir PR. |
| `reports/entregas/` | Registro final de entregas concluídas. |

## Regra de ouro: toda entrega tem o mesmo ID

Toda tarefa precisa manter o mesmo ID em todos os lugares.

Exemplo:

```txt
Issue:
[G1-007] Coletar dataset bruto Eurostat immigration flow

Branch:
g1-007/coletar-eurostat-immigration-flow

Commit:
data(eurostat): adiciona bruto immigration flow [G1-007]

Pull Request:
[G1-007] data(eurostat): adiciona bruto immigration flow
```

Se o ID for uma subtask com ponto, troque o ponto por hífen na branch:

```txt
Issue:
[G1-006.2] Criar guia operacional para iniciantes

Branch:
g1-006-2/guia-operacional-iniciantes
```

Nunca entregue uma task sem ID. O ID é o que permite rastrear Project, issue, branch, commit, PR e entrega final.

## Como usar o GitHub Projects

O GitHub Projects é o quadro operacional. Ele mostra o que existe, o que está em andamento e o que já foi concluído.

### Passo a passo para encontrar sua task

1. Abra o repositório no GitHub.
2. Entre na aba `Projects` ou no link do Project usado pelo grupo.
3. Abra a view `Quadro Operacional` ou `Tabela Operacional`.
4. Procure pelo seu nome em `Assignees` ou `Responsável`.
5. Abra a task pelo título.
6. Confirme o ID da task, por exemplo `G1-007`.
7. Leia o campo `Entrega esperada`.
8. Leia o `Critério de aceite`.
9. Veja a `Prioridade`.
10. Veja o `Status`.

### Como ler os campos da task

| Campo | Como interpretar |
| --- | --- |
| `Title` | Nome da issue. Deve começar com `[G1-000]`. |
| `Status` | Etapa atual no fluxo. |
| `Tipo` | Coleta, Tratamento, Validação, Documentação, Script ou Entrega. |
| `Prioridade` | P0 a P4. P0 é bloqueante. |
| `Fonte` | Fonte de dados relacionada. |
| `Prazo` | Data limite combinada. |
| `Entrega esperada` | Resultado que deve existir ao final. |
| `Grupo destino` | Quem usará a entrega: Grupo 2, Grupo 3, Ambos ou Interno G1. |
| `Linked pull requests` | PR relacionado à task. |

### Quando mover o card de status

| Status | Quando usar |
| --- | --- |
| `Backlog` | A demanda existe, mas ainda não está pronta para execução. |
| `Ready` | A task está clara e pode ser assumida. |
| `In Progress` | Você começou a trabalhar. |
| `Review` | O PR está aberto ou a entrega aguarda revisão. |
| `Changes Requested` | Alguém revisou e pediu correções. |
| `Done` | O PR foi revisado e mergeado na `main`. |

Regra prática:

1. Antes de começar, mova para `In Progress`.
2. Quando abrir o PR, mova para `Review`.
3. Se pedirem correção, mova para `Changes Requested`.
4. Depois de corrigir, volte para `Review`.
5. Só mova para `Done` depois do merge na `main`.

## Fluxo 1 — Fazer uma entrega pelo navegador do GitHub

Use este fluxo se você não quer usar terminal ou VS Code.

### Antes de editar

1. Abra a issue da sua task.
2. Leia o objetivo.
3. Leia os critérios de aceite.
4. Abra `templates/checklist-execucao-task.template.md`.
5. Copie o checklist para um comentário privado seu, bloco de notas ou comentário na issue.
6. Confirme quais arquivos precisam ser alterados.
7. Confirme se precisa registrar fonte, CSV, dicionário ou entrega final.

### Criar branch pelo navegador

1. Abra o repositório no GitHub.
2. Clique no seletor de branch, normalmente onde aparece `main`.
3. Digite o nome da nova branch.
4. Use o padrão `g1-000/descricao-curta-da-tarefa`.
5. Exemplo: `g1-007/coletar-eurostat-immigration-flow`.
6. Clique em `Create branch`.
7. Confirme que você está na branch nova antes de editar.

### Editar arquivo pelo navegador

1. Navegue até o arquivo que precisa alterar.
2. Clique no ícone de lápis (`Edit this file`).
3. Faça a alteração.
4. Role até `Commit changes`.
5. Escreva a mensagem no padrão correto.
6. Exemplo: `docs(fontes): registra fonte eurostat [G1-007]`.
7. Confirme que o commit será feito na sua branch, não na `main`.
8. Clique em `Commit changes`.

### Criar arquivo novo pelo navegador

1. Entre na pasta correta.
2. Clique em `Add file`.
3. Clique em `Create new file`.
4. Digite o caminho e o nome do arquivo.
5. Exemplo: `data/raw/eurostat_immigration_flow_raw.csv`.
6. Cole ou escreva o conteúdo.
7. Faça commit na sua branch.

### Abrir Pull Request pelo navegador

1. Depois do commit, clique em `Compare & pull request`.
2. Confira se a comparação está assim:
   - base: `main`;
   - compare: sua branch.
3. Use o título no padrão:

```txt
[G1-000] tipo(escopo): descrição curta
```

4. Preencha o template do PR.
5. Marque os checklists aplicáveis.
6. Informe a fonte usada, se houver.
7. Informe limitações conhecidas.
8. Coloque `Closes #NUMERO_DA_ISSUE` se o PR deve fechar a issue quando for mergeado.
9. Clique em `Create pull request`.
10. Volte ao Project e mova a task para `Review`.

## Fluxo 2 — Fazer uma entrega com Git local / VS Code

Use este fluxo se você vai trabalhar no computador, com terminal e editor.

### Preparar o repositório

1. Abra o terminal na pasta do projeto.
2. Confira em qual branch você está:

```powershell
git status -sb
```

3. Vá para a `main`:

```powershell
git switch main
```

4. Baixe a versão mais recente:

```powershell
git pull --ff-only origin main
```

5. Crie sua branch:

```powershell
git switch -c g1-000/descricao-curta-da-tarefa
```

Exemplo:

```powershell
git switch -c g1-007/coletar-eurostat-immigration-flow
```

### Editar no VS Code

1. Abra o projeto no VS Code.
2. Abra a issue no navegador para consultar o objetivo.
3. Edite somente os arquivos necessários.
4. Não altere arquivos fora da sua task.
5. Salve os arquivos.
6. Volte ao terminal.

### Conferir alterações antes do commit

1. Veja os arquivos alterados:

```powershell
git status -sb
```

2. Veja o conteúdo alterado:

```powershell
git diff
```

3. Se aparecer arquivo que não faz parte da task, não coloque no commit.

### Adicionar arquivos ao commit

Adicione arquivos pelo caminho exato:

```powershell
git add docs/grupo-1/log-fontes.md
```

Se houver mais arquivos:

```powershell
git add metadata/catalogo_fontes.csv
git add data/raw/nome_do_arquivo.csv
```

Evite usar `git add .` quando existirem arquivos de outras tarefas no seu computador.

### Criar commit

Use o padrão:

```txt
tipo(escopo): descrição curta [G1-000]
```

Exemplo:

```powershell
git commit -m "data(eurostat): adiciona bruto immigration flow [G1-007]"
```

### Enviar branch para o GitHub

```powershell
git push -u origin g1-000/descricao-curta-da-tarefa
```

Exemplo:

```powershell
git push -u origin g1-007/coletar-eurostat-immigration-flow
```

### Abrir PR

1. Abra o link que o GitHub mostra no terminal.
2. Confira `base: main` e `compare: sua branch`.
3. Preencha o template do PR.
4. Inclua `Closes #NUMERO_DA_ISSUE` se o PR fecha a task.
5. Crie o PR.
6. Mova o card para `Review`.

## Como registrar uma fonte

Toda fonte candidata deve entrar em `docs/grupo-1/log-fontes.md`.

Se a fonte for aceita como oficial ou candidata forte, ela também deve entrar em `metadata/catalogo_fontes.csv`.

### Passo a passo

1. Abra sua issue.
2. Confirme qual fonte você pesquisou.
3. Abra `templates/registro-fonte.template.md`.
4. Copie o bloco do template.
5. Abra `docs/grupo-1/log-fontes.md`.
6. Cole a nova entrada no fim do arquivo.
7. Preencha todos os campos:
   - task;
   - responsável;
   - subtema;
   - pergunta relacionada;
   - `fonte_id`;
   - nome da fonte;
   - instituição;
   - URL;
   - período disponível;
   - granularidade;
   - formato;
   - viabilidade;
   - limitação principal;
   - próximo passo;
   - status de revisão.
8. Deixe `Status de revisão` como `Pendente`.
9. Se a fonte for oficial, adicione uma linha em `metadata/catalogo_fontes.csv`.
10. Abra PR.

### Como escolher `fonte_id`

1. Abra `metadata/catalogo_fontes.csv`.
2. Veja o último ID usado.
3. Use o próximo número disponível.
4. Exemplo: se o último é `FONTE-011`, a próxima fonte nova será `FONTE-012`.
5. Não reutilize `fonte_id`.
6. Não invente `fonte_id` sem registrar a fonte.

## Como fazer uma coleta

Coleta é baixar ou registrar dados brutos da fonte pública.

### Antes da coleta

1. Confirme que existe issue de coleta.
2. Confirme o `fonte_id`.
3. Confirme se a fonte está no catálogo ou no log de fontes.
4. Confirme o período esperado.
5. Confirme o formato esperado: CSV, Excel, API, PDF ou página web.
6. Confirme onde o arquivo bruto deve ficar: `data/raw/`.

### Durante a coleta

1. Baixe o arquivo original.
2. Não limpe, reordene ou altere os dados brutos sem registrar.
3. Nomeie o arquivo sem espaços, acentos ou caracteres especiais.
4. Use nomes em `snake_case`.
5. Salve em `data/raw/`.
6. Registre a URL exata.
7. Registre a data de acesso.
8. Registre limitações encontradas.

### Depois da coleta

1. Confira se o arquivo abre.
2. Atualize o log de fontes se necessário.
3. Atualize o catálogo se a fonte for oficial.
4. Abra PR.
5. Explique no PR:
   - fonte;
   - período;
   - formato;
   - limitações;
   - uso esperado por G2/G3.

## Como fazer tratamento

Tratamento é transformar um arquivo bruto em CSV padronizado para uso posterior.

### Antes do tratamento

1. Confirme que o arquivo bruto está em `data/raw/`.
2. Confirme que existe `fonte_id`.
3. Abra `DICIONARIO_DE_DADOS.md`.
4. Confirme o padrão:
   - UTF-8 sem BOM;
   - separador `;`;
   - decimal `.`;
   - data `YYYY-MM-DD`;
   - nulos como célula vazia;
   - colunas em `snake_case`, em inglês, sem acentos.

### Durante o tratamento

1. Remova linhas vazias ou inválidas.
2. Remova totais e subtotais se eles atrapalharem a análise.
3. Padronize nomes de colunas.
4. Padronize datas.
5. Padronize números.
6. Inclua `source_id` quando aplicável.
7. Salve o resultado em `data/processed/`.
8. Crie log de coleta/tratamento quando aplicável.
9. Se usar script, salve em `scripts/`.

### Depois do tratamento

1. Abra o CSV e confira se as colunas separaram corretamente.
2. Confirme que o separador é `;`.
3. Confirme que números usam decimal com ponto.
4. Confirme que datas estão em `YYYY-MM-DD`.
5. Atualize `metadata/dicionario_dados.csv` quando houver dataset real validado ou quando a issue pedir.
6. Abra PR.

## Como fazer validação

Validação é revisar se a entrega está pronta para outro grupo usar.

### Passo a passo

1. Abra a issue de validação.
2. Abra o arquivo em `data/processed/`.
3. Confira se a fonte é confiável.
4. Confira se o link da fonte existe.
5. Confira se a data de acesso existe.
6. Confira se o período dos dados está claro.
7. Confira se o CSV abre corretamente.
8. Confira UTF-8.
9. Confira separador `;`.
10. Confira nomes de colunas.
11. Confira se `metadata/catalogo_fontes.csv` está atualizado.
12. Confira se `metadata/dicionario_dados.csv` está atualizado quando aplicável.
13. Copie o checklist de `docs/grupo-1/checklist-validacao.md`.
14. Registre problemas encontrados.
15. Marque o resultado:
   - `Aprovado`;
   - `Aprovado com ressalvas`;
   - `Reprovado`.
16. Se aprovado, o arquivo pode ir para `data/validated/`.
17. Abra PR ou revise o PR existente.

Pergunta final obrigatória:

```txt
Esta entrega está pronta para outro grupo trabalhar ou está apenas transferindo problema para frente?
```

## Como abrir Pull Request

O PR é o pedido oficial de revisão.

### Antes de abrir

1. Confirme que sua branch não é `main`.
2. Confirme que os arquivos alterados pertencem à task.
3. Confirme que o commit tem o ID da task.
4. Confirme que a issue existe.
5. Confirme que o Project está atualizado.

### Título do PR

Use:

```txt
[G1-000] tipo(escopo): descrição curta
```

Exemplos:

```txt
[G1-007] data(eurostat): adiciona bruto immigration flow
[G1-008] data(aima): trata residentes estrangeiros
[G1-009] test(validacao): valida csv immigration flow
[G1-010] docs(entrega): registra pacote tecnico sprint 1
```

### Corpo do PR

Preencha:

- ID da task;
- objetivo;
- arquivos criados ou alterados;
- fonte usada;
- validação realizada;
- limitações conhecidas;
- impacto para Grupo 2 ou Grupo 3;
- checklist final.

Se o PR fecha a issue, inclua:

```txt
Closes #NUMERO_DA_ISSUE
```

Exemplo:

```txt
Closes #23
```

Depois de abrir o PR, mova a task para `Review`.

## Como corrigir Changes Requested

`Changes Requested` significa que a entrega precisa de ajuste antes de concluir.

### Passo a passo

1. Leia todos os comentários do PR.
2. Não abra uma nova issue para a mesma correção, salvo se o líder pedir.
3. Volte para a mesma branch.
4. Faça os ajustes pedidos.
5. Faça novo commit com o mesmo ID da task.
6. Envie para a mesma branch.
7. O PR será atualizado automaticamente.
8. Responda no comentário explicando o que foi corrigido.
9. Mova o card de `Changes Requested` para `Review`.

Exemplo de commit de ajuste:

```txt
fix(csv): corrige separador do arquivo eurostat [G1-007]
```

## Como o líder revisa e fecha

O líder ou revisor deve revisar no PR, não consolidar manualmente fora do GitHub.

### Revisão do líder

1. Abrir o PR.
2. Conferir se o título tem o ID da task.
3. Conferir se a branch segue o padrão.
4. Conferir se os arquivos estão nas pastas corretas.
5. Conferir se a fonte foi registrada quando aplicável.
6. Conferir se o catálogo foi atualizado quando aplicável.
7. Conferir se o dicionário foi atualizado quando aplicável.
8. Conferir se o padrão CSV foi respeitado.
9. Conferir se a entrega ajuda Grupo 2 ou Grupo 3.
10. Aprovar ou pedir mudanças.

### Fechamento

1. Se houver ajustes, pedir em `Changes Requested`.
2. Se estiver correto, aprovar.
3. Fazer merge na `main`.
4. Confirmar que a issue fechou automaticamente ou fechar como `completed`.
5. Mover o card para `Done`.
6. Se for entrega final, registrar em `reports/entregas/`.
7. Comunicar no canal adequado com link do PR ou entrega.

## O que nunca fazer

- Não fazer commit direto na `main`.
- Não criar branch sem ID da task.
- Não abrir PR sem ID da task.
- Não usar nomes como `final`, `teste`, `dados`, `arrumei`.
- Não salvar CSV tratado em `data/raw/`.
- Não mover arquivo para `data/validated/` sem validação.
- Não entregar fonte só por WhatsApp.
- Não deixar fonte sem URL.
- Não criar `fonte_id` sem registrar no catálogo quando a fonte for oficial.
- Não usar vírgula como separador de CSV sem decisão formal nova.
- Não usar acentos, espaços ou símbolos em nomes de arquivo.
- Não mover task para `Done` antes do PR revisado e mergeado.
- Não misturar arquivos de várias tasks no mesmo PR sem combinar antes.
- Não alterar padrões oficiais sem issue e PR próprios.

## Modelos prontos para copiar e colar

### Nome de branch

```txt
g1-000/descricao-curta-da-tarefa
```

### Commit de documentação

```txt
docs(escopo): descrição curta [G1-000]
```

### Commit de dados

```txt
data(escopo): descrição curta [G1-000]
```

### Commit de correção

```txt
fix(escopo): descrição curta [G1-000]
```

### Commit de validação

```txt
test(validacao): descrição curta [G1-000]
```

### Título de PR

```txt
[G1-000] tipo(escopo): descrição curta
```

### Comentário curto de entrega na issue

```txt
Entrega realizada para a task `G1-000`.

PR: #000
Arquivos principais:
- caminho/do/arquivo.csv
- caminho/do/documento.md

Observações:
- [limitação ou ponto de atenção]
```

### Mensagem para o grupo de líderes

```txt
ENTREGA GRUPO 1 — [DATA]

Task: [G1-000] Nome da task
PR: [link]
Entrega: [resumo em 1 frase]
Uso para G2/G3: [como pode ser usado]
Limitações: [se houver]
Status: em revisão / mergeado / entregue
```

### Caminho rápido por tipo de tarefa

| Se sua task é... | Comece por | Entrega mínima |
| --- | --- | --- |
| Fonte | `docs/grupo-1/log-fontes.md` | Fonte registrada e PR aberto. |
| Coleta | `data/raw/` | Arquivo bruto + fonte + PR. |
| Tratamento | `data/processed/` | CSV tratado + log + PR. |
| Validação | `docs/grupo-1/checklist-validacao.md` | Checklist + decisão + PR. |
| Entrega | `reports/entregas/` | Registro final + links + PR. |

## Interface com Grupo 2 e Grupo 3

O Grupo 1 entrega dados e documentação. O Grupo 2 e o Grupo 3 não devem depender de explicações soltas no WhatsApp para entender a entrega.

Para o Grupo 2, sempre deixar claro:

- arquivo CSV final;
- separador `;`;
- colunas principais;
- período;
- limitações;
- fonte;
- se o dado está pronto para Looker Studio.

Para o Grupo 3, sempre deixar claro:

- pergunta ou subtema relacionado;
- fonte usada;
- período dos dados;
- interpretação segura;
- limitações metodológicas;
- o que não pode ser afirmado com os dados.

Se uma entrega ainda não está validada, diga explicitamente:

```txt
Esta entrega ainda não está validada para uso final.
```
