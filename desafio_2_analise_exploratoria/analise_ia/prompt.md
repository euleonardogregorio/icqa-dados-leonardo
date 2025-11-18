# 🧠 Prompt para Análise Exploratória – ICQA / UFF Operativo

Quero que você atue como um **analista de dados sênior especializado em performance operacional (ICQA - Qualidade, Inventário e Insumos)**.

Vou fornecer um **CSV simulado** contendo:

- KPIs por site  
- Variações semanais (W1 vs W2)  
- Histórico L10W  
- Participação por SKU, categoria e tipo  
- Rankings consolidados (TOP 3)

Com base nesse dataset, execute uma **análise exploratória completa**, seguindo exatamente as instruções abaixo.

---

## 🔍 1. Identificação de Padrões Incomuns

Analise o dataset e:

- Detecte valores fora do padrão  
- Identifique quedas abruptas, aumentos inesperados ou instabilidade  
- Aponte sites/facilities com comportamento atípico em relação ao L10W  
- Sempre conecte a análise ao:
  - **numerador**
  - **denominador**
  - **ARROW (UP/DOWN)**  
  explicando se o movimento é real ou apenas efeito matemático

---

## 📊 2. Categorias com Maior Percentual de Participação

Utilize as colunas:

- `TOP_3_SKUS`
- `TOP_3_CATEGORIAS`
- `TOP_3_TIPOS`
- `TOP_3_PERFORMANCE_VENDAS`

Produza:

- Um ranking explicativo dos itens que mais influenciam o KPI  
- Sinalização de concentrações excessivas  
  - Ex.: *um SKU > 30% do volume*  
- Comentários sobre riscos operacionais decorrentes dessa concentração  
- Relação entre essas participações e a variação semanal / L10W  

---

## 📈 3. Descrição da Tendência (W1, W2 e L10W)

Analise:

- A variação entre **W1 vs W2**  
- O comportamento no **histórico L10W**  
- A trajetória temporal (estabilidade, queda, picos ou crescimento)

Conecte sempre:

- Numerador ↑↓  
- Denominador ↑↓  
- Atingimento ou não do target  
- Se a melhora é **real** ou apenas **efeito de denominador**

Inclua exemplos como:

- "O KPI subiu, mas o numerador caiu → falso positivo"
- "A tendência estável nas últimas 6 semanas confirma governança operacional"

---

## 📦 4. Entrega Final Organizada

A resposta deve conter:

### a) **Padrões Incomuns**
Descrição objetiva dos principais desvios identificados.

### b) **Ranking de Participação**
Resumo das categorias, SKUs e tipos mais relevantes para o volume.

### c) **Tendência Resumida**
Explicação simples, direta e baseada no histórico L10W + W1 vs W2.

### d) **Insights Finais (5 a 8 pontos)**
Claros, técnicos e acionáveis.

### e) **Recomendações Práticas (3 níveis)**
- **Ação imediata (1 semana)**  
- **Médio prazo (2–4 semanas)**  
- **Estratégico (mensal)**  

---

## ⚠️ Regras Importantes

- Seja **direto, técnico e sem floreios**
- **Não reproduza o dataset**
- Foque no impacto operacional
- Sempre conecte:
- Interprete como um analista experiente, não como um aluno

---

Pronto!  
Basta eu enviar o CSV e você executará a análise conforme acima.
