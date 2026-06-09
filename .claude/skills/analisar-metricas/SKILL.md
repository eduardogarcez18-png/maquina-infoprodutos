---
name: analisar-metricas
description: Interpreta dados de campanha e funil, classifica o gargalo principal por categoria, e entrega uma decisão prática com ação imediata. Requer dados de pelo menos 3 dias ou R$150 gastos.
---

## Quando usar esta skill

Após 3+ dias de campanha ativa ou R$150+ gastos. Quando uma etapa do funil está visivelmente abaixo do esperado. Antes de qualquer decisão de pausar, escalar ou mudar estrutura.

Não usar com menos de 500 impressões por criativo — dados insuficientes para qualquer conclusão.

---

## Input necessário

- Métricas de campanha: impressões, cliques, CTR, CPM, CPC, CPA, ROAS, budget gasto por criativo e conjunto
- Métricas de funil: visitas na LP, tempo na página, taxa de rejeição, inícios de checkout, compras, order bump, upsell
- Período de análise (datas)
- Meta de CPA e ROAS definida antes da campanha
- Margem do produto (necessária para calcular se o CPA cabe)

---

## Processo passo a passo

1. Montar tabela de métricas por etapa com desvio em relação ao benchmark
2. Identificar a etapa com maior desvio relativo negativo — esse é o gargalo
3. Classificar o gargalo em uma das 9 categorias (ver abaixo)
4. Para o gargalo, gerar: hipótese + evidência + teste específico + métrica de sucesso
5. Responder as 5 perguntas duras (ver abaixo)
6. Emitir decisão prática e ação imediata

---

## Classificação do Gargalo (obrigatório)

Classificar o gargalo em uma — e apenas uma — das categorias:

| Categoria | Quando usar |
|---|---|
| **Criativo** | CTR < 1%, Hook Rate < 20%, alto CPM com poucos cliques |
| **Público** | CPM > 40% acima da média, frequência > 3, saturação de audiência |
| **Página** | CVR LP < 3%, rejeição > 70%, tempo na página < 30s |
| **Oferta** | CVR LP 5%+ mas checkout abaixo do esperado, preço contestado |
| **Checkout** | Abandono > 50%, queda entre início e conclusão |
| **Campanha** | CPM instável, fase de aprendizado sem sair, budget insuficiente |
| **Ticket / Margem** | CPA real impossível de caber na margem mesmo com funil funcionando |
| **Rastreamento** | Dados inconsistentes, conversões subnotificadas, CTR sem cliques rastreados |
| **Produto** | Reembolsos > 5%, reclamações de entrega, suporte com volume alto |

---

## Benchmarks de referência

| Etapa | Métrica | Benchmark |
|---|---|---|
| Criativo | CTR (feed) | 1–3% |
| Criativo | Hook Rate (3s / impressões) | > 30% |
| Criativo | Hold Rate (50% / 3s) | > 40% |
| LP | CVR | 5–15% |
| LP | Taxa de rejeição | < 60% |
| LP | Tempo na página | > 45s |
| Checkout | Conclusão | > 60% |
| Order Bump | Aceite | 20–40% |
| Upsell 1 | Aceite | 10–25% |

---

## 5 Perguntas Duras (obrigatório responder)

Toda análise deve responder estas 5 perguntas com base nos dados disponíveis — não em suposições.

1. **Existe desejo comprador real?** O CTR e o volume de cliques indicam interesse genuíno ou apenas curiosidade?
2. **A promessa é forte ou genérica?** A LP está gerando scroll e tempo de página compatíveis com uma oferta crível?
3. **O criativo chama atenção ou só é bonito?** Hook Rate e Hold Rate confirmam que o criativo está prendendo atenção ou é apenas esteticamente agradável sem engajamento?
4. **O CPA cabe na margem?** Calcular: margem líquida do produto vs. CPA atual vs. CPA meta. Responder sim ou não com o número.
5. **Os dados são suficientes para tomar esta decisão?** Quantas impressões, cliques e conversões existem? A conclusão está sendo forçada antes do volume mínimo?

---

## Decisões possíveis (toda análise termina com uma)

| Decisão | Quando usar |
|---|---|
| **Pausar** | CPA > 2x a meta com volume suficiente, sem sinal de melhora |
| **Manter** | Dados insuficientes, tendência de melhora visível |
| **Iterar** | Gargalo identificado, hipótese clara de melhora com pequena mudança |
| **Trocar ângulo** | CTR e Hook Rate baixos — criativo não conecta com o avatar |
| **Trocar página** | CTR ok, CVR LP baixo — problema na página |
| **Trocar oferta** | LP com bom engajamento, CVR baixo — problema na proposta de valor |
| **Duplicar** | CPA dentro da meta, ROAS positivo, dados confiáveis |
| **Escalar** | ROAS consistente 5+ dias, CPA estável, funil sem gargalo crítico |

---

## Output obrigatório

```
## Análise de Métricas: [Produto] — [Período]

### Tabela de Performance
| Etapa | Métrica | Resultado | Benchmark | Desvio | Status |
|---|---|---|---|---|---|
| Criativo | CTR | X% | 1–3% | X% | ✅/⚠️/❌ |
| Criativo | Hook Rate | X% | >30% | ... | ... |
| LP | CVR | X% | 5–15% | ... | ... |
| LP | Rejeição | X% | <60% | ... | ... |
| Checkout | Conclusão | X% | >60% | ... | ... |
| Order Bump | Aceite | X% | 20–40% | ... | ... |

### Gargalo Principal
**Categoria:** [uma das 9 categorias]
**Etapa:** ...
**CVR / métrica real:** X% | **Benchmark:** X% | **Desvio:** -X%
**Hipótese:** ...
**Evidência nos dados:** ...
**Teste específico:** ...
**Métrica de sucesso:** ...
**Prazo para reavaliação:** X dias

### 5 Perguntas Duras
1. Existe desejo comprador real? → ...
2. A promessa é forte ou genérica? → ...
3. O criativo chama atenção ou só é bonito? → ...
4. O CPA cabe na margem? → CPA atual: R$X | CPA meta: R$X | Margem: R$X → [cabe / não cabe]
5. Os dados são suficientes? → [sim/não — impressões: X, cliques: X, conversões: X]

### Outros pontos de atenção
1. ...

### Decisão
**[PAUSAR / MANTER / ITERAR / TROCAR ÂNGULO / TROCAR PÁGINA / TROCAR OFERTA / DUPLICAR / ESCALAR]**

Justificativa: [1–2 frases com o número que sustenta a decisão]
Ação imediata: [o que fazer agora — específico]
Agente a acionar: [qual agente executa a próxima etapa]
Prazo para reavaliação: [data ou budget]

### Próximos 3 testes priorizados
1. Teste: ... | Hipótese: ... | Métrica de sucesso: ... | Critério de corte: ...
2. ...
3. ...
```
