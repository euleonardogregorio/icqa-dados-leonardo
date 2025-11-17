------ Correção 1 - Sintaxe CTE ------

Código Original:
DADOS_L10W AS (
   WITH DADOS_HISTORICOS AS (
     SELECT...

SELECT
     SITE_ID...


Código Corrigido:
 DADOS_HISTORICOS AS (...),
 DADOS_L10W AS (...),


obs: A estrutura do CTE estava incorreta, desta forma podemos seguir com o CTE Historico e consumir sem erro.

------ Correção 2 - Sintaxe CTE ------
Código Original:
ANALISE_UFF AS (
    WITH
 DADOS_BASE_CUSTO AS (
SELECT (...),

SELECT
   WAREHOUSE_IDS.WAREHOUSE_ID...

Código Corrigido:
DADOS_BASE_CUSTO AS (...),
ANALISE_UFF AS (...),

obs: A estrutura do CTE estava incorreta, desta forma podemos seguir com o DADOS_BASE_CUSTO e consumir sem erro no CTE ANALISE_UFF.


------ Correção 3 - Sintaxe CTE ------
Código Original:
 ANALISE_PERFORMANCE_VENDAS AS (
   WITH
   DADOS_VENDAS_WOW AS (...),
   CALCULO_FINAL_VENDAS AS (...),

   SELECT
     WAREHOUSE_ID...

Código Corrigido:
  DADOS_VENDAS_WOW AS (...),
  CALCULO_FINAL_VENDAS AS (...),
  ANALISE_PERFORMANCE_VENDAS AS (...)
obs: 

------ Correção 4 - Limpeza da query ------
Código Original:
AND DATE_VALUE BETWEEN DATE_SUB(DATE_TRUNC(CURRENT_DATE(), WEEK(SUNDAY)), INTERVAL 2 WEEK) AND DATE_SUB(DATE_TRUNC(CURRENT_DATE(), WEEK(SUNDAY)), INTERVAL 1 DAY)

FECHA BETWEEN DATE_SUB(DATE_TRUNC(CURRENT_DATE(), WEEK(SUNDAY)), INTERVAL 1 WEEK) AND DATE_SUB(DATE_TRUNC(CURRENT_DATE(), WEEK(SUNDAY)), INTERVAL 1 DAY)


Código Corrigido:
AND DATE_VALUE BETWEEN DATE_SUB(DATE_TRUNC(CURRENT_DATE(), WEEK(MONDAY)), INTERVAL 2 WEEK) AND DATE_SUB(DATE_TRUNC(CURRENT_DATE(), WEEK(MONDAY)), INTERVAL 1 DAY)

FECHA BETWEEN DATE_SUB(DATE_TRUNC(CURRENT_DATE(), WEEK(MONDAY)), INTERVAL 1 WEEK) AND DATE_SUB(DATE_TRUNC(CURRENT_DATE(), WEEK(MONDAY)), INTERVAL 1 DAY)

obs: Alterar a logica para filtrar a semana de Segunda a Domingo e não de Domingo a Sábado.

------ Correção 5 - Limpeza da query ------
Código Original:

WHERE
1=1
AND FECHA BETWEEN DATE_SUB(DATE_TRUNC(CURRENT_DATE(), WEEK(SUNDAY)), INTERVAL 1 WEEK) 

Código Corrigido:

WHERE
AND FECHA BETWEEN DATE_SUB(DATE_TRUNC(CURRENT_DATE(), WEEK(SUNDAY)), INTERVAL 1 WEEK) 

obs: o 1=1 não estava sendo utilizado.


------ Correção 6 - Erro de Sintaxe ------

Código Original:
GROUP BY ALL

Código Corrigido:
GROUP BY SITE, FECHA, SKU, CATEGORIA, TIPO_ORDEN

obs: GROUP BY ALL não é permitido, é preciso listar explicitamente todas as colunas a serem agrupadas.

------ Correção 7 - Erro Lógico ------

Código Original:
WHERE week_rank_vendas = 2

Código Corrigido:
WHERE week_rank_vendas = 1

obs: Bloco 1 do CALCULO_FINAL_VENDAS está com ORDER BY SEMANA DESC, logo week_rank_vendas = 1 é a mais recente. Se eu seguir o CTE e e deixar week_rank_vendas = 2 vai desalinhar a analise.


------ Correção 8 - Erro de Sintaxe ------

Código Original:
VENDAS.TOP_3_PERFORMANCE_VENDAS,
"" AS INSIGHT

Código Corrigido:
VENDAS.TOP_3_PERFORMANCE_VENDAS,

 '' AS INSIGHT

 obs: Aspas simples é utilziado para definir valores de string, já aspas duplas para identificar colunas com caracteres especiais, nomes de projetos...


------ Correção 9 - Padronizar Sitaxe ------

Código Original:
FROM meli-sbox.ICQACENTRAL.UFFDET as A

Código Corrigido:
FROM meli-sbox.ICQACENTRAL.UFFDET AS A

obs: Modificando AS para maiusculo,seguindo o padrão das tabelas.

------ Correção 10 - Padronizar Sitaxe ------

Código Original:
SITE AS WAREHOUSE_ID,FECHA,SKU,CATEGORIA, TIPO_ORDEN, SUM(PIEZAS) PIEZAS

Código Corrigido:
SITE AS WAREHOUSE_ID,FECHA,SKU,CATEGORIA, TIPO_ORDEN, SUM(PIEZAS) AS PIEZAS

obs: Adicionando AS, para ficar no padrão de todo código.