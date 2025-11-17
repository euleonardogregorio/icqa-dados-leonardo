# Desafio de Dados – ICQA (Mercado Livre)

Este repositório contém minha solução completa para o desafio de dados da área de ICQA, cobrindo:

- Diagnóstico e correção de uma query SQL
- Criação de tabela final no BigQuery com atualização semanal
- Análise exploratória com IA (prompt + insights)
- Dashboard semanal com automação de envio

---

## Estrutura do repositório

### `desafio_1_diagnostico_correcao_query/`

Entrega da primeira etapa do desafio.

Aqui você encontra:

- **Query original e query corrigida** em SQL  
- **Documento explicando**:
  - Pelo menos **3 erros ou más práticas** identificados na query original  
  - Como a query corrigida passa a retornar **apenas colunas com dados válidos**  
  - **Quais informações o resultado final apresenta** e **por que são relevantes** para o negócio
- **Passo a passo / pseudocódigo** para:
  - Salvar o resultado em **uma nova tabela** no BigQuery, no mesmo projeto/dataset  
  - Configurar uma **scheduled query semanal** (atualização automática dos dados)

---

### `desafio_2_analise_exploratoria/analise_ia/`

Entrega da etapa de **análise exploratória com IA**.

Nesta pasta estão:

- O **prompt** utilizado para a ferramenta de IA (ex.: ChatGPT / Claude), construído a partir do CSV com os resultados da query corrigida  
- O **resultado resumido da IA**, com:
  - Padrões e comportamentos incomuns  
  - Categorias com maior participação  
  - Tendências semanais (ex.: semanas estáveis vs. picos)  
  - Conexão das tendências com **numerador, processos críticos e possíveis causas operacionais**

---

### `desafio_3_dashboard_automacao/`

Entrega da etapa de **dashboard e automação**.

Aqui você encontra:

- Arquivos e/ou **capturas de tela do dashboard**, mostrando:
  - **Vendas totais**
  - **Ticket médio**
  - **Ranking de produtos**
  - **Evolução semanal das vendas**
  - Destaque para **produtos com baixo desempenho**
- Um arquivo de documentação técnica descrevendo:
  - A ferramenta utilizada (ex.: Looker Studio / Power BI)  
  - Como o dashboard consome os dados da tabela final  
  - O **fluxo de automação** proposto para envio automático toda segunda-feira às 9h, por e-mail ou chat  
    - Exemplo: *Looker Studio + Google Sheets + App Script* ou fluxo equivalente  
    - Lógica de agendamento (cron / scheduler) e envio do link e/ou snapshot do dashboard

---

### `desenho_solucao/`

Materiais visuais da solução end-to-end.

Nesta pasta estão:

- O **desenho da arquitetura** da solução (pipeline de dados)  
- Visão do fluxo desde:
  - Fonte de dados / CSV inicial  
  - Correção da query  
  - Criação da tabela no BigQuery  
  - Análise com IA  
  - Dashboard  
  - Automação semanal de atualização e envio

---

## Como a solução responde ao desafio

- **Diagnóstico e correção da query**  
  - Identifico erros/más práticas, corrijo a query e documento o raciocínio.  

- **Tabela final + agendamento semanal**  
  - Mostro como criar a tabela no BigQuery e configurar a scheduled query para atualizar semanalmente.  

- **Análise exploratória com IA**  
  - Entrego o prompt elaborado e o resumo dos insights/recomendações da IA.  

- **Dashboard + automação**  
  - Disponibilizo o dashboard com os KPIs pedidos e descrevo o fluxo técnico de automação para envio semanal.


