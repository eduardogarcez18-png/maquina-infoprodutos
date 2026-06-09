---
name: analisar-metricas
description: Interpreta dados de campanha e funil, identifica o gargalo principal e gera lista priorizada de hipóteses para o próximo ciclo de testes. Requer dados de pelo menos 3 dias.
---

## Quando usar esta skill

Após 3+ dias de campanha ativa, ou quando uma etapa do funil está claramente abaixo do esperado.

## Input necessário

- Métricas de campanha: impressões, cliques, CTR, CPM, CPC, CPA, ROAS, budget gasto
- Métricas de funil: visitas na LP, tempo na página, taxa de rejeição, inícios de checkout, compras, taxa de order bump, taxa de upsell
- Período de análise
- Meta de CPA ou ROAS

## Processo passo a passo

1. Montar tabela de métricas por etapa do funil
2. Comparar cada métrica com o benchmark de referência
3. Identificar a etapa com maior desvio negativo (o gargalo principal)
4. Para o gargalo, gerar hipótese + evidência + teste + métrica de sucesso
5. Listar as demais etapas com problema em ordem de prioridade
6. Gerar veredicto: pausar / manter / testar variação / escalar

## Benchmarks de referência

- CTR (feed): 1–3%
- Hook Rate (views 3s / impressões): > 30%
- Hold Rate (views 50% / views 3s): > 40%
- CVR Landing Page: 5–15% (depende do preço)
- Abandono de checkout: < 40%
- Taxa de Order Bump: 20–40%
- Taxa de Upsell 1: 10–25%
- ROAS mínimo viável: depende da margem (calcular com o usuário)

## Output obrigatório

```
## Análise de Métricas: [Produto] — [Período]

### Tabela de Performance
| Etapa | Métrica | Resultado | Benchmark | Status |
|---|---|---|---|---|
| Criativo | CTR | X% | 1–3% | ✅/⚠️/❌ |
| ...

### Gargalo Principal
**Etapa:** ...
**Problema:** ...
**Hipótese:** ...
**Teste recomendado:** ...
**Métrica de sucesso:** ...

### Outros pontos de atenção
1. ...

### Veredicto
[ ] Pausar campanha
[ ] Manter e aguardar dados
[ ] Testar variação de [criativo / página / oferta]
[ ] Escalar — condições atingidas

### Próximos 3 testes priorizados
1. Teste: ... | Hipótese: ... | Impacto esperado: ...
```
