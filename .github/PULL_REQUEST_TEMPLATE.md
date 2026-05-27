# Pull Request

Se estiver em dúvida sobre como preencher este PR, siga:

```txt
docs/grupo-1/guia-operacional-iniciantes.md
templates/checklist-execucao-task.template.md
```

## ID da task

```txt
[G1-000]
```

## Título esperado

```txt
[G1-000] tipo(escopo): descrição curta
```

Exemplo:

```txt
[G1-001] data(ine): adiciona base bruta de inflacao
```

## Objetivo

Descrever de forma objetiva o que este PR entrega.

```txt
Exemplo: Adiciona a base bruta de inflação do INE e registra a fonte no catálogo de fontes.
```

## Tipo de alteração

Marcar uma opção:

```txt
[ ] data — inclusão ou alteração de dados
[ ] docs — documentação
[ ] fix — correção
[ ] refactor — reorganização sem alterar resultado
[ ] test — validação/checks
[ ] chore — organização interna
[ ] feat — novo script, automação ou funcionalidade
```

## Arquivos criados ou alterados

```txt
- data/raw/...
- data/processed/...
- data/validated/...
- metadata/catalogo_fontes.csv
- metadata/dicionario_dados.csv
- docs/...
```

## Fonte usada

| Campo | Valor |
| --- | --- |
| Nome da fonte |  |
| Instituição |  |
| Link |  |
| Data de acesso |  |
| Período dos dados |  |

## Validação realizada

- [ ] CSV abre corretamente.
- [ ] Encoding UTF-8.
- [ ] Separador `;`.
- [ ] Nome do arquivo segue o padrão.
- [ ] Fonte registrada.
- [ ] Dicionário atualizado, quando aplicável.
- [ ] Checklist de validação preenchido, quando aplicável.

## Impacto para Grupo 2 / Grupo 3

Descrever como esta entrega pode ser usada pelos outros grupos.

```txt
Exemplo: O Grupo 2 pode usar o CSV validado para criar visualizações de evolução anual. O Grupo 3 pode usar a série temporal para contextualizar o texto sobre custo de vida.
```

## Limitações conhecidas

```txt
Descrever limitações, lacunas ou pontos que exigem cautela.
```

## Checklist final

- [ ] O PR contém o ID da task.
- [ ] A branch segue o padrão `g1-000/descricao-curta`.
- [ ] Os commits seguem o padrão definido.
- [ ] Os arquivos foram salvos nas pastas corretas.
- [ ] A documentação foi atualizada, quando aplicável.
- [ ] A entrega não transfere problema para o próximo grupo.
