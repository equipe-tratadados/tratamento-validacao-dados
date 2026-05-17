# Catálogo de Fontes

## Objetivo

O catálogo de fontes registra todas as fontes públicas usadas pelo Grupo 1.

Ele serve para garantir rastreabilidade, confiabilidade e reutilização das fontes pelos outros grupos.

## Arquivo principal

O catálogo em CSV fica em:

```txt
metadata/catalogo_fontes.csv
```

## Campos obrigatórios

| Campo | Descrição |
| --- | --- |
| `fonte_id` | ID único da fonte. Exemplo: `FONTE-001`. |
| `nome_fonte` | Nome claro da fonte. |
| `instituicao` | Instituição responsável pelo dado. |
| `url` | Link direto ou página oficial da fonte. |
| `tema` | Tema relacionado ao dado. |
| `pais` | País de referência. |
| `periodo_disponivel` | Período disponível na fonte. |
| `data_acesso` | Data em que a fonte foi consultada. |
| `tipo_fonte` | API, CSV, Excel, PDF, página web, base estatística etc. |
| `confiabilidade` | Alta, média ou baixa. |
| `observacoes` | Limitações, notas ou cuidados. |

## Como registrar uma nova fonte

1. Verificar se a fonte já existe em `metadata/catalogo_fontes.csv`.
2. Criar novo `fonte_id`, seguindo a sequência existente.
3. Registrar nome, instituição, URL, tema e período disponível.
4. Informar data de acesso.
5. Classificar confiabilidade.
6. Indicar limitações ou observações.
7. Usar o `fonte_id` nos datasets relacionados.

## Critérios de confiabilidade

| Classificação | Critério |
| --- | --- |
| Alta | Fonte oficial, institucional, pública e com metodologia clara. |
| Média | Fonte secundária confiável, mas dependente de interpretação ou agregação. |
| Baixa | Fonte não oficial, incompleta, sem metodologia clara ou difícil de verificar. |

## Fontes preferenciais

Priorizar fontes oficiais e públicas, como:

- INE;
- PORDATA;
- Eurostat;
- Banco de Portugal;
- Direção-Geral competente pelo tema;
- portais públicos de dados abertos.

## Exemplo de registo

```csv
fonte_id;nome_fonte;instituicao;url;tema;pais;periodo_disponivel;data_acesso;tipo_fonte;confiabilidade;observacoes
FONTE-001;Índice de Preços no Consumidor;INE;https://www.ine.pt;Inflação;Portugal;2020-2024;2026-05-17;Base estatística;Alta;Exemplo de preenchimento
```

## Relação com os datasets

Todo arquivo em `data/raw/`, `data/processed/` ou `data/validated/` deve poder ser ligado a uma linha do catálogo de fontes.
