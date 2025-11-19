# 🛠️ Documentação de Correções e Ajustes da Query

Este documento consolida todas as correções aplicadas à Query, incluindo ajustes de sintaxe, padronização, correções lógicas e melhorias de boas práticas.

---

## 🔧 Correção 1 — Estrutura de CTE

**Código Original**
DADOS_L10W AS (
WITH DADOS_HISTORICOS AS (
SELECT...
SELECT
SITE_ID...

**Código Corrigido**
DADOS_HISTORICOS AS (...),
DADOS_L10W AS (...),

**Motivo**  
A estrutura do `WITH` estava incorreta. Agora o CTE histórico é criado primeiro e utilizado corretamente no seguinte.

---

## 🔧 Correção 2 — Estrutura de CTE

**Código Original**
ANALISE_UFF AS (
WITH
DADOS_BASE_CUSTO AS (
SELECT (...),

SELECT
WAREHOUSE_IDS.WAREHOUSE_ID...

**Código Corrigido**
DADOS_BASE_CUSTO AS (...),
ANALISE_UFF AS (...),

**Motivo**  
O `WITH` interno estava inválido. A ordem correta dos CTEs foi restabelecida.

---

## 🔧 Correção 3 — Estrutura de CTE

**Código Original**
ANALISE_PERFORMANCE_VENDAS AS (
WITH
DADOS_VENDAS_WOW AS (...),
CALCULO_FINAL_VENDAS AS (...),

SELECT
WAREHOUSE_ID...

**Código Corrigido**
DADOS_VENDAS_WOW AS (...),
CALCULO_FINAL_VENDAS AS (...),
ANALISE_PERFORMANCE_VENDAS AS (...),

**Motivo**  
Remoção do `WITH` duplicado e alinhamento na estrutura do CTE.

---

## 🧹 Correção 4 — Intervalo Semanal

**Código Original**
AND DATE_VALUE BETWEEN DATE_SUB(DATE_TRUNC(CURRENT_DATE(), WEEK(SUNDAY)), INTERVAL 2 WEEK)
AND DATE_SUB(DATE_TRUNC(CURRENT_DATE(), WEEK(SUNDAY)), INTERVAL 1 DAY)

**Código Corrigido**
AND DATE_VALUE BETWEEN DATE_SUB(DATE_TRUNC(CURRENT_DATE(), WEEK(MONDAY)), INTERVAL 2 WEEK)
AND DATE_SUB(DATE_TRUNC(CURRENT_DATE(), WEEK(MONDAY)), INTERVAL 1 DAY)

**Motivo**  
A lógica foi corrigida para semanas de **segunda a domingo**, evitando desalinhamento de períodos.

---

## 🧹 Correção 5 — Limpeza da Query

**Código Original**
WHERE
1=1
AND FECHA BETWEEN ...

**Código Corrigido**
WHERE
FECHA BETWEEN ...

**Motivo**  
`1=1` não estava sendo utilizado para concatenar filtros dinamicamente.

---

## ❌ Correção 6 — GROUP BY inválido

**Código Original**
GROUP BY ALL

**Código Corrigido**
GROUP BY SITE, FECHA, SKU, CATEGORIA, TIPO_ORDEN

**Motivo**  
`GROUP BY ALL` não é suportado. A listagem de colunas deve ser explícita.

---

## 🧠 Correção 7 — Ajuste Ranking Semanal

**Código Original**
WHERE week_rank_vendas = 2

**Código Corrigido**
WHERE week_rank_vendas = 1

**Motivo**  
O ranking está em ordem decrescente (`ORDER BY SEMANA DESC`). Portanto, `1` representa a semana mais recente.

---

## ❌ Correção 8 — Aspas incorretas

**Código Original**
"" AS INSIGHT

**Código Corrigido**
'' AS INSIGHT

**Motivo**  
Strings devem ser definidas com aspas simples.

---

## 📐 Correção 9 — Padronização de Sintaxe

**Código Original**
FROM meli-sbox.ICQACENTRAL.UFFDET as A

**Código Corrigido**
FROM meli-sbox.ICQACENTRAL.UFFDET AS A

**Motivo**  
Padronização do uso de `AS` em maiúsculas.

---

## 📐 Correção 10 — Padronização de Sintaxe

**Código Original**
SUM(PIEZAS) PIEZAS

**Código Corrigido**
SUM(PIEZAS) AS PIEZAS

**Motivo**  
Uso consistente de `AS` em alias de colunas.

# ✅ Conclusão

As correções acima garantem:

- Estrutura de CTEs funcional e padronizada  
- Lógica temporal correta  
- Sintaxe apropriada para BigQuery  
- Padronização estética e semântica  
- Redução de erros futuros  