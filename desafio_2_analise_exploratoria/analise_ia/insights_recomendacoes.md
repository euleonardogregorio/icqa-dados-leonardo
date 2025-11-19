# 📊 Análise Exploratória – Insights, Tendências e Recomendações

Este documento resume os principais achados identificados na análise exploratória dos dados semanais (W1 vs W2 + histórico L10W), incluindo padrões incomuns, tendências, categorias dominantes e recomendações acionáveis.

---

## 🔍 1. Padrões Incomuns Identificados

- **BRSP01** apresentou queda abrupta no KPI (**W1 −12% vs W2**), acompanhada por:
  - ↓ numerador  
  - ↑ denominador  
  ➝ Indica processo mais lento e menos eficiente.

- **MXCD02** teve variação **positiva > 20% WoW**, sugerindo recuperação de performance.  
  Porém, o numerador permanece abaixo da média histórica L10W.

- **ARBA01** mostra comportamento instável:
  - Grande amplitude no histórico L10W  
  ➝ Sugere falta de padronização operacional.

- **CLSA01** ficou acima do target, com:
  - ↑ numerador  
  - denominador estável  
  ➝ Melhoria consistente e sustentável.

---

## 📊 2. Categorias com Maior Participação

- **CAT1** e **CAT2** representam juntas **> 55%** do volume total UFF.  
  ➝ Forte concentração operacional.

- **SKU1** aparece constantemente como principal contribuinte:
  - Representa **até 30%** do volume em alguns sites.

- No recorte por tipo, **TIPO1** domina a movimentação.  
  ➝ Dependência operacional elevada deste tipo de ordem.

**⚠️ Risco:** a dependência de poucos SKUs/tipos amplifica a instabilidade quando há variação de demanda.

---

## 📈 3. Tendência Temporal (L10W + Comparação W1 vs W2)

- A maioria dos sites manteve estabilidade até **W33**, com pico/queda significativa em **W34**.
- Sites com **ARROW = UP** só apresentaram **melhora real** quando:
  - ↑ numerador  
  - ↓ denominador  
- Alguns sites tiveram valor maior, mas numerador menor:  
  ➝ **Falso positivo** provocado por redução do denominador.
  
---

## 💡 4. Principais Insights

- **Dois sites** apresentam sinais de processo crítico (queda simultânea de valor + numerador).
- Forte concentração de categorias pode gerar gargalos em semanas de alta demanda.
- Recuperações WoW não representam ganho sustentável quando o denominador segue alto.
- Sites estáveis no L10W tendem a ter **melhores índices de governança**.
- **Picos isolados** raramente sustentam tendência quando contradizem o histórico.
- **SKU1** e **CAT1** precisam de monitoramento constante por dominarem o volume.
- **ARROW DOWN + numerador crescente** indica **correção real** do processo.

---

## 🛠️ 5. Recomendações Finais

### ✔ Ação Imediata (1 semana)
- Revisar processos operacionais do **BRSP01** (picking/packing).  
  O aumento do denominador indica lentidão detectável.

### 🟧 Médio Prazo (2–4 semanas)
- Criar **alertas automáticos** de concentração de categorias/SKUs  
  ↳ Evita risco operacional em períodos de alta demanda.

### 🟦 Estratégico (mensal)
- Implementar **monitoramento automatizado baseado em L10W** para:
  - Validar tendências reais  
  - Evitar falsos ganhos semanais  
  - Auxiliar decisões de governança operacional