# Checklist de Validação — Grupo 1

## 1. Objetivo

Este checklist define os critérios mínimos para validar fontes e CSVs antes de repassar uma entrega aos Grupos 2 e 3 ou ao grupo de líderes.

## 2. Validação da Fonte

| Item | Critério | Status |
|---|---|---|
| Entidade responsável identificada | A fonte informa quem produziu ou mantém os dados | [ ] |
| URL acessível | O link abre corretamente | [ ] |
| Data de acesso registrada | A consulta foi datada | [ ] |
| Período coberto identificado | O dataset informa o intervalo temporal | [ ] |
| Cobertura geográfica identificada | País, região, município ou equivalente | [ ] |
| Licença ou condição de uso verificada | Uso público, licença aberta ou condição identificada | [ ] |
| Limitações registradas | Problemas ou restrições foram documentados | [ ] |
| Fonte registrada no catálogo | Existe `fonte_id` correspondente | [ ] |

## 3. Validação do CSV

| Item | Critério | Status |
|---|---|---|
| Nome do arquivo segue padrão | `tema_fonte_periodo_status.csv` | [ ] |
| Arquivo está na pasta correta | `raw`, `processed` ou `validated` | [ ] |
| Encoding correto | UTF-8 | [ ] |
| Separador correto | Ponto e vírgula (`;`) | [ ] |
| Cabeçalho presente | Primeira linha contém nomes de colunas | [ ] |
| Campos em `snake_case` | Nomes padronizados | [ ] |
| `fonte_id` presente | CSV rastreável ao catálogo | [ ] |
| Campos mínimos presentes | Quando aplicável | [ ] |
| Valores principais preenchidos | Sem vazios críticos | [ ] |
| Dicionário de dados atualizado | Para arquivos `processed` ou `validated` | [ ] |

## 4. Validação para Dashboard

| Item | Critério | Status |
|---|---|---|
| Indicadores claros | Campos analíticos compreensíveis | [ ] |
| Unidade de medida definida | Ex.: EUR, %, habitantes | [ ] |
| Período consistente | Datas/anos compatíveis | [ ] |
| Granularidade clara | Nacional, regional, municipal etc. | [ ] |
| Dados prontos para agregação | Possível somar, contar, comparar ou filtrar | [ ] |

## 5. Validação para Conteúdo

| Item | Critério | Status |
|---|---|---|
| Fonte confiável | Entidade reconhecida ou verificável | [ ] |
| Contexto suficiente | Fonte permite explicar o dado em texto | [ ] |
| Limitações conhecidas | Restrições foram registradas | [ ] |
| Período claro | Evita afirmações sem janela temporal | [ ] |

## 6. Resultado da Validação

```txt
Dataset: [nome do arquivo]
Fonte ID: [fonte_id]
Responsável: [nome]
Status: [aprovado / aprovado com ressalvas / rejeitado]
Motivo: [resumo]
Próximo passo: [ação necessária]
```

## 7. Critério Final

A entrega só deve ser reportada como concluída quando os itens críticos estiverem marcados e qualquer ressalva estiver registrada.
