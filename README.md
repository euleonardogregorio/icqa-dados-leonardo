# Desafio Técnico: Analista de Dados (Mercado Livre)

Este repositório contém a resolução do desafio técnico para a posição de Analista de Dados, focado em performance operacional (ICQA / UFF Operativo).

O projeto está estruturado em três etapas principais, cada uma em sua respectiva pasta, facilitando a navegação e a avaliação.

## Estrutura do Repositório

* [`/1-query-sql/`](./1-query-sql/)
* [`/2-analise-exploratoria-ia/`](./2-analise-exploratoria-ia/)
* [`/3-dashboard-automacao/`](./3-dashboard-automacao/)

---

## 1. Otimização e Análise de Query (SQL)

Nesta etapa, o foco foi a análise, correção e documentação de uma query SQL para extração de dados de performance.

**Local dos Arquivos:** [`/1-query-sql/`](./1-query-sql/)

### O que você encontrará nesta pasta:

* **`README.md` (ou arquivo `.md`)**: Documento detalhado contendo:
    * A identificação de pelo menos três erros ou más práticas na query original.
    * A query SQL corrigida e otimizada, pronta para produção.
    * Uma explicação clara sobre o que os dados retornados representam (KPI, Numerador, Denominador) e por que são relevantes para a gestão operacional.
* **`automacao_ingestao.md`**: Documentação técnica do processo para:
    * Salvar os resultados da query em uma nova tabela (ex: `CREATE TABLE AS SELECT...`).
    * Configurar a atualização automática semanal dos dados (ex: *Scheduled Queries* no BigQuery).

---

## 2. Análise Exploratória com IA

Utilizando um dataset simulado (CSV) derivado da query, foi realizada uma análise exploratória para identificar padrões e gerar insights acionáveis, demonstrando a habilidade de usar IA para acelerar a análise.

**Local dos Arquivos:** [`/2-analise-exploratoria-ia/`](./2-analise-exploratoria-ia/)

### O que você encontrará nesta pasta:

* **`prompt.txt`**: O prompt exato (em português) elaborado e fornecido à ferramenta de IA para guiar a análise técnica e de negócios.
* **`analise_ia.md`**: O relatório completo gerado pela IA, contendo:
    * Identificação de padrões incomuns (picos, quedas, comportamento atípico).
    * Análise de participação de SKUs e Categorias.
    * Descrição da tendência temporal (W1 vs W2 + L10W) conectada aos drivers operacionais.
* **`insights_recomendacoes.md`**: Um resumo executivo com os principais insights e 3 recomendações práticas (curto, médio e longo prazo) derivadas da análise.

---

## 3. Dashboard e Automação (Looker Studio)

Para permitir o acompanhamento semanal das metas de forma visual e acessível, foi desenvolvido um dashboard e documentado um fluxo de automação para distribuição.

**Local dos Arquivos:** [`/3-dashboard-automacao/`](./3-dashboard-automacao/)

### O que você encontrará nesta pasta:

* **`dashboard.md`**: Documentação contendo capturas de tela (ou o link público) do dashboard construído no Looker Studio.
    * Visão de Vendas Totais e Ticket Médio.
    * Gráfico de evolução semanal de vendas.
    * Tabelas de ranking de produtos (Top e Low performance).
* **`automacao_dashboard.md`**: Descrição técnica detalhada do fluxo de automação proposto para o envio do relatório (PDF ou link) via e-mail, toda segunda-feira às 9:00.
    * **Solução Proposta:** Looker Studio (para o relatório) + Google Sheets (como fonte de dados) + Google Apps Script (para acionar e enviar o e-mail).