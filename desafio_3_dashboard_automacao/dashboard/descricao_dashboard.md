# Dashboard de Performance ICQA – Qualidade, Inventário e Insumos

Este dashboard foi desenvolvido para oferecer uma visão clara, objetiva e integrada da performance operacional semanal, com foco em vendas, eficiência e comportamento dos produtos dentro dos principais indicadores de qualidade ICQA.

Ele permite monitorar resultados, identificar produtos críticos, acompanhar evolução semanal e analisar desvios de meta — tudo em um único ambiente visual moderno, responsivo e alinhado ao padrão visual de times analíticos e operacionais.

---

## 🎯 Objetivo Geral do Dashboard

Fornecer uma visão executiva e analítica da performance semanal, permitindo:

- Analisar evolução do volume de vendas ao longo do tempo.
- Comparar desempenho versus metas.
- Identificar rapidamente produtos com pior desempenho.
- Avaliar ranking de vendas por categoria/produto.
- Filtrar métricas por qualquer semana específica.
- Sustentar tomadas de decisão tática e estratégica.

---

## 🏗 Estrutura do Dashboard

### 1. **Header ICQA – Identidade Visual**
O topo do dashboard contém o logotipo ICQA e elementos visuais que reforçam a identidade da área.  
Serve como identificação institucional e organização visual do painel.

---

## 2. 📊 Indicadores-Chave (KPIs)

### **• Vendas Totais**
Mostra o volume total acumulado de vendas no período selecionado.  
Ajuda a avaliar o tamanho da operação e seu comportamento ao longo da semana ou período filtrado.

### **• Ticket Médio**
Indica o valor médio das vendas realizadas.  
É útil para entender comportamento de compra e otimização de receita.

---

## 3. 🗂 Filtro de Semana (Interatividade Global)

Um seletor de semana permite refinar todas as visualizações do dashboard simultaneamente.  
Ao escolher uma semana específica, **todos os gráficos e tabelas são atualizados automaticamente**, garantindo análise da performance exata daquele período.

---

## 4. 📈 Evolução Semanal das Vendas

Gráfico de linha que apresenta a tendência das vendas ao longo do tempo.  
Inclui:

- Pontos semanais
- Linha de tendência
- Variação visual clara entre semanas

Permite identificar:

- Crescimento consistente
- Picos ou quedas bruscas
- Efeitos sazonais ou operacionais

---

## 5. 🔻 Produtos com Baixo Desempenho

Lista os produtos que tiveram performance inferior à meta na semana filtrada.

Campos exibidos:

- **PRODUTO**  
- **Percentual W1 vs Target**  
  (quanto abaixo da meta o produto se encontra)

Essa tabela destaca rapidamente **os produtos críticos** que exigem atenção imediata.

---

## 6. 🔼 Ranking de Vendas por Produto

Exibe os produtos com maior volume de vendas ou melhor performance na semana selecionada.

Campos exibidos:

- **Produto**
- **Numerador W1**
- **Valor W1**

É útil para análises de:

- Tendências de consumo
- Produtos-chave
- Planejamento de estoque
- Decisões de abastecimento

---

## 🧠 Metodologia dos Dados

- Os dados são processados via SQL (BigQuery) e transformados no padrão ICQA.
- Arrays de produtos são explodidos para permitir ranking individual.
- Métricas de variação e desempenho consideram:
  - W1 (semana atual)
  - Target
  - Gap para atingir meta
  - Evolução W0 → W1 (variação temporal)

---

## 🔍 Filtros e Interatividade

- Filtro único de Semana aplicado a todas as fontes compatíveis.
- Tabelas responsivas com paginação.
- Ordenação dinâmica por qualquer coluna.
- Atualização automática ao alterar filtros.

---

## 📌 Conclusão

Este dashboard fornece uma visão consolidada e ágil da performance semanal da área ICQA, permitindo análise rápida, decisões operacionais eficientes e detecção imediata de produtos de baixa performance.

Sua estrutura modular e visual moderno favorecem apresentações executivas e análise contínua por analistas, gerentes e líderes de operação.

