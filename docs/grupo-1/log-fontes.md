# Log de Fontes do Grupo 1

Este arquivo é o ponto de entrada para entregas diretas de fontes no GitHub.

A pessoa responsável pela pesquisa deve editar este arquivo pelo navegador ou pelo editor local, adicionar uma nova entrada no fim do documento e abrir um Pull Request. O líder revisa o PR; não deve precisar consolidar a entrega manualmente.

## Como entregar uma fonte

1. Abrir uma branch com o ID da task.
2. Copiar o bloco de `templates/registro-fonte.template.md`.
3. Colar uma nova entrada no fim deste arquivo.
4. Preencher todos os campos obrigatórios.
5. Se a fonte for candidata a oficial, adicionar ou atualizar a linha correspondente em `metadata/catalogo_fontes.csv`.
6. Abrir PR no padrão `[G1-000] docs(fontes): registra fontes ...`.

## Status de revisão

Usar apenas um dos valores abaixo:

```txt
Pendente
Aceita
Ajustes solicitados
Rejeitada
Duplicada
```

## Campos obrigatórios

Toda entrada deve preencher:

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

## Exemplo preenchido

> Exemplo documental. Não copiar como fonte real.

### Fonte: RMA/AIMA - Relatório de Migrações e Asilo

| Campo | Valor |
| --- | --- |
| Task | `G1-001.1` |
| Responsável | `@usuario` |
| Subtema | Fluxo Imigratório x Crescimento Económico |
| Pergunta relacionada | Evolução do número de imigrantes residentes em Portugal entre 2010 e 2024 |
| `fonte_id` | `FONTE-002` |
| Nome da fonte | RMA/AIMA |
| Instituição | Agência para a Integração, Migrações e Asilo |
| URL | https://aima.gov.pt/pt/a-aima/relatorios-de-migracoes-e-asilo |
| Período disponível | 2023-2024 |
| Granularidade | Anual; nacionalidade; tipo de autorização conforme relatório |
| Formato | PDF / relatório estatístico |
| Viabilidade | Alta |
| Limitação principal | Continuidade metodológica com SEF precisa ser documentada |
| Próximo passo | Extrair tabelas prioritárias e cruzar com fontes históricas do SEF |
| Status de revisão | Aceita |

## Bloco vazio para copiar

```md
### Fonte: [nome curto da fonte]

| Campo | Valor |
| --- | --- |
| Task | `G1-000` |
| Responsável | `@usuario` |
| Subtema |  |
| Pergunta relacionada |  |
| `fonte_id` | `FONTE-000` |
| Nome da fonte |  |
| Instituição |  |
| URL |  |
| Período disponível |  |
| Granularidade |  |
| Formato | CSV / Excel / API / PDF / página web / base estatística / outro |
| Viabilidade | Alta / Média / Baixa / Fonte não encontrada |
| Limitação principal |  |
| Próximo passo |  |
| Status de revisão | Pendente |
```

## Entradas de fontes

Adicionar novas entradas abaixo desta linha.
