# Tratamento e Validação de Dados

Repositório operacional do Grupo 1 do projeto Prepara Portugal Estágio.

O Grupo 1 é responsável por coletar, tratar, validar e documentar dados públicos sobre temas sociais e económicos em Portugal. A entrega final do grupo deve permitir que o Grupo 2 construa dashboards e que o Grupo 3 produza textos e análises com rastreabilidade mínima.

## Objetivo do repositório

Centralizar:

- dados brutos, tratados e validados;
- catálogo de fontes;
- dicionário de dados;
- documentação operacional;
- templates de tarefas, entregas e Pull Requests;
- histórico rastreável por task, branch, commit e PR.

## Estrutura de pastas

```txt
tratamento-validacao-dados/
├── README.md
├── DICIONARIO_DE_DADOS.md
├── .github/
│   ├── PULL_REQUEST_TEMPLATE.md
│   └── ISSUE_TEMPLATE/
│       ├── tarefa-coleta.md
│       ├── tarefa-tratamento.md
│       └── tarefa-validacao.md
├── data/
│   ├── raw/
│   ├── processed/
│   └── validated/
├── docs/
│   └── grupo-1/
├── metadata/
│   ├── catalogo_fontes.csv
│   └── dicionario_dados.csv
├── templates/
├── scripts/
└── reports/
    └── entregas/
```

## Fluxo dos dados

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

## Pastas principais

| Pasta | Uso |
| --- | --- |
| `data/raw/` | Dados originais ou minimamente alterados. |
| `data/processed/` | Dados tratados, limpos e padronizados. |
| `data/validated/` | Dados revisados e prontos para uso pelos outros grupos. |
| `docs/grupo-1/` | Documentação operacional do Grupo 1. |
| `DICIONARIO_DE_DADOS.md` | Padrão oficial de entrega dos CSVs. |
| `metadata/` | Catálogo de fontes e dicionário de dados em CSV. |
| `.github/ISSUE_TEMPLATE/` | Modelos de tarefas reconhecidos pelo GitHub. |
| `.github/PULL_REQUEST_TEMPLATE.md` | Modelo padrão para Pull Requests. |
| `templates/` | Modelos reutilizáveis para fontes, datasets e entregas. |
| `scripts/` | Scripts de coleta, tratamento ou validação. |
| `reports/entregas/` | Registos finais das entregas concluídas. |

## Rastreabilidade obrigatória

Toda entrega deve ser ligada pelo mesmo ID da task.

Exemplo:

```txt
Task no GitHub Projects:
[G1-001] Coletar dados de inflação no INE

Branch:
g1-001/coletar-dados-inflacao-ine

Commit:
data(ine): adiciona base bruta de inflacao [G1-001]

Pull Request:
[G1-001] data(ine): adiciona base bruta de inflacao
```

## Regra de branch

Usar sempre:

```txt
g1-000/descricao-curta-da-tarefa
```

Não usar:

```txt
task/...
data/...
docs/...
```

## Documentação do Grupo 1

A documentação operacional está em:

[docs/grupo-1/README.md](docs/grupo-1/README.md)

## Padrão de CSV

Os CSVs devem seguir o contrato oficial em [DICIONARIO_DE_DADOS.md](DICIONARIO_DE_DADOS.md):

- encoding UTF-8 sem BOM;
- separador ponto e vírgula `;`;
- decimal com ponto `.`;
- datas em `YYYY-MM-DD`;
- cabeçalhos em `snake_case`, em inglês, sem acentos e sem espaços;
- fonte registrada em `metadata/catalogo_fontes.csv`;
- dicionário atualizado em `metadata/dicionario_dados.csv`, quando aplicável.

## Status de entrega

Uma task só pode ir para `Done` no GitHub Projects após:

- fonte documentada;
- CSV salvo na pasta correta;
- checklist de validação preenchido;
- commit no padrão definido;
- Pull Request aberto e revisado;
- merge feito na `main`.
