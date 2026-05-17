# Dicionário de Dados — Grupo 1

## 1. Objetivo

O dicionário de dados documenta os campos presentes nos CSVs produzidos pelo Grupo 1.

Ele permite que os Grupos 2 e 3 entendam o significado, tipo e limitações de cada coluna antes de usar os dados em dashboards, textos ou análises.

## 2. Arquivo Principal

O dicionário deve ser mantido no arquivo:

```txt
/metadata/dicionario_dados.csv
```

## 3. Campos Mínimos

```csv
dataset,campo,tipo_dado,descricao,obrigatorio,exemplo,observacoes
```

## 4. Dicionário dos Campos

| Campo | Obrigatório | Descrição | Exemplo |
|---|---:|---|---|
| `dataset` | Sim | Nome do CSV ao qual o campo pertence | `habitacao_ine_2020_2024_processed.csv` |
| `campo` | Sim | Nome da coluna documentada | `valor` |
| `tipo_dado` | Sim | Tipo esperado do dado | `integer`, `decimal`, `string`, `date` |
| `descricao` | Sim | Explicação objetiva do campo | `Valor observado do indicador` |
| `obrigatorio` | Sim | Indica se o campo deve existir no dataset | `sim` / `nao` |
| `exemplo` | Sim | Exemplo de valor válido | `235000` |
| `observacoes` | Não | Regras, limitações ou notas | `Valor em euros` |

## 5. Tipos de Dados Permitidos

| Tipo | Uso |
|---|---|
| `string` | Texto livre ou categoria |
| `integer` | Número inteiro |
| `decimal` | Número decimal |
| `date` | Data no formato `YYYY-MM-DD` |
| `boolean` | Verdadeiro/falso |
| `category` | Valor pertencente a lista fechada |

## 6. Exemplo

```csv
habitacao_ine_2020_2024_processed.csv;valor;decimal;Valor observado do indicador;sim;235000;Valor monetário em EUR
```

## 7. Regras

- Todo CSV `processed` ou `validated` deve ter seus campos documentados.
- Nomes de campos devem estar em `snake_case`.
- Campos com abreviações devem ser explicados.
- Campos calculados devem indicar a lógica de cálculo em `observacoes`.
- Campos herdados da fonte original podem ser mantidos, mas precisam de descrição.

## 8. Critério de Aceite

Um dicionário de dados é considerado suficiente quando:

- todos os campos do CSV estão listados;
- cada campo possui tipo definido;
- cada campo possui descrição compreensível;
- exemplos são compatíveis com os dados reais;
- campos obrigatórios estão identificados.
