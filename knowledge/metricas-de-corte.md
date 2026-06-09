# Métricas de Corte — Critérios para Campanhas de Infoprodutos

## Lógica de Diagnóstico por Etapa

Antes de ver os números, identificar onde o funil quebra seguindo esta lógica:

```
Impressão sem clique      → problema: CRIATIVO (hook, ângulo, formato)
Clique sem checkout       → problema: PÁGINA ou OFERTA (headline, copy, prova, clareza)
Checkout sem compra       → problema: PREÇO, CONFIANÇA ou CHECKOUT TÉCNICO
Venda sem escala          → problema: CONSISTÊNCIA, MARGEM, PÚBLICO ou CRIATIVO CANSADO
```

Nunca mudar duas variáveis ao mesmo tempo. Identificar a etapa com problema, testar uma mudança, medir.

---

## Métricas e Critérios

### CPM — Custo por Mil Impressões

| Faixa | Status | Interpretação |
|---|---|---|
| < R$ 15 | Excelente | Público pouco disputado ou criativo com alto score de relevância |
| R$ 15–30 | Bom | Normal para a maioria dos nichos de infoproduto |
| R$ 30–50 | Atenção | Custo elevado — pode indicar público saturado ou baixa relevância |
| > R$ 50 | Crítico | Investigar: público muito pequeno, saturação, problema de qualidade do anúncio |

**Quando agir:** CPM subindo mais de 40% em 3 dias sem mudança de público = sinal de saturação. Testar novo público ou novo ângulo de criativo.

---

### CTR — Taxa de Cliques

| Faixa | Status | Interpretação |
|---|---|---|
| > 3% | Excelente | Criativo altamente relevante |
| 1,5–3% | Bom | Saudável para a maioria dos produtos |
| 1–1,5% | Atenção | Monitorar junto com CPA — pode ser ok se CPA está na meta |
| < 1% | Crítico | Cortar criativo após 1.000 impressões e R$ 30+ gastos |

**Armadilha:** CTR alto sem conversão = criativo que atrai curiosidade mas não comprador. Verificar CVR da página.

---

### CPC — Custo por Clique

| Faixa | Status | Interpretação |
|---|---|---|
| < R$ 1,50 | Excelente | Eficiência alta |
| R$ 1,50–3,00 | Bom | Normal para infoprodutos |
| R$ 3–5 | Atenção | Verificar CTR e CPM — custo alto pode vir de público ruim |
| > R$ 5 | Crítico | Pausar e investigar — difícil chegar em CPA viável |

**Relação:** CPC = CPM ÷ CTR × 10. CPM alto + CTR baixo = CPC muito alto.

---

### CPA — Custo por Aquisição (por compra)

O CPA máximo viável depende da margem do produto. Calcular antes de rodar qualquer campanha.

**Fórmula:**
```
Ticket médio com upsells (LTV estimado)
× Margem líquida (após plataforma, impostos, suporte)
= CPA máximo viável (margem 0%)

CPA meta = CPA máximo × 70% (reserva 30% de margem)
CPA de corte = CPA máximo × 120% (tolerância de 20% acima do limite)
```

**Exemplo com produto de R$ 19,90:**
```
LTV estimado (com order bump e upsell): R$ 28
Margem líquida (~90%): R$ 25
CPA máximo: R$ 25
CPA meta: R$ 17,50
CPA de corte: R$ 30
```

**Quando pausar:** CPA acima do corte com budget ≥ 2× o CPA de corte gasto sem melhora.

---

### ROAS — Retorno sobre Investimento em Mídia

```
ROAS = Receita gerada ÷ Investimento em mídia
```

| ROAS | Status |
|---|---|
| < 1x | Prejuízo — pausar e diagnosticar |
| 1–1,5x | Empate ou prejuízo leve — não escalar |
| 1,5–2x | Viável para produto com LTV alto — manter e otimizar |
| 2–3x | Bom — candidato a escala com validação |
| > 3x | Excelente — escalar com cautela |

**Atenção:** ROAS sem considerar LTV (upsells, recompra) pode parecer ruim quando o modelo é saudável. Sempre calcular ROAS sobre o ticket médio real, não apenas o produto principal.

---

### Taxa de Conversão da Página (CVR LP)

| Faixa | Status |
|---|---|
| > 10% | Excelente |
| 5–10% | Bom |
| 3–5% | Atenção — testar headline ou prova social |
| < 3% | Crítico — problema na LP |

**Variável por preço:** produtos acima de R$ 297 naturalmente têm CVR menor. Ajustar benchmark conforme o ticket.

**Diagnóstico rápido:**
- CVR baixo + tempo na página baixo = headline não conecta, avatar errado ou dissonância criativo-página
- CVR baixo + tempo na página alto = copy convence mas falta prova ou CTA fraco

---

### Checkout Iniciado vs. Compra

| Taxa de conclusão | Status |
|---|---|
| > 70% | Excelente |
| 60–70% | Bom |
| 40–60% | Atenção |
| < 40% | Crítico — abandono alto |

**Causas comuns de abandono:**
- Formulário longo ou campos desnecessários
- Falta de selos de segurança e garantia visíveis no checkout
- Preço sem ancoragem (chega no checkout sem contexto de valor)
- Problema técnico (lentidão, erro de carregamento)
- Método de pagamento não disponível

---

### Ticket Médio e Margem

```
Ticket médio real = (Receita total ÷ Número de compras)
Inclui: produto principal + order bumps + upsells aceitos

Margem líquida = Ticket médio − custos de plataforma − impostos − suporte − produção de criativos
```

**Erro comum:** calcular CPA sobre o produto principal ignorando o LTV dos upsells. Isso faz o produto parecer inviável quando o modelo é saudável.

---

### Frequência

| Faixa | Status |
|---|---|
| < 1,5 | Normal — público ainda não saturado |
| 1,5–2,5 | Atenção — monitorar CTR e CPM |
| > 3 | Sinal de saturação — introduzir novos criativos |
| > 5 | Crítico — necessário novo criativo ou novo público |

**Frequência alta + CTR caindo + CPM subindo = saturação confirmada.** Ação: pausar criativos atuais, lançar novos ângulos.

---

## Quando Pausar

Pausar imediatamente quando:
- CPA > CPA de corte com ≥ 2× o valor do corte gasto
- ROAS < 1 após 3+ dias e ≥ R$ 150 gastos
- CTR < 0,8% com ≥ 1.000 impressões (criativo específico)
- Criativo reprovado repetidamente pelo Meta sem solução

---

## Quando Manter

Manter e aguardar quando:
- Menos de 3 dias de campanha ativa
- Menos de R$ 150 gastos no conjunto
- Tendência de melhora nos últimos 24h
- Dentro do período de aprendizado do algoritmo (primeiros 50 eventos de otimização)

---

## Quando Iterar

Iterar (testar variação) quando:
- Gargalo identificado com hipótese clara
- CPA acima da meta mas dentro do corte
- CTR ok mas CVR da página baixo (problema isolado)
- Hook Rate baixo mas Hold Rate ok (trocar o hook, manter o corpo)

---

## Quando Escalar

Escalar somente quando **todos** os critérios abaixo estiverem confirmados com número:

1. CPA abaixo da meta por 5+ dias consecutivos
2. ROAS acima do mínimo viável por 5+ dias
3. Volume de dados suficiente (≥ 50 conversões no período)
4. Frequência < 2,5 (público não saturado)
5. CTR estável ou em tendência de melhora
6. Rastreamento confirmado (pixel + API disparando corretamente)
7. Validação pelo `advogado-do-diabo` concluída

**Regra de escala:** aumentar budget máximo 20% por vez. Aguardar 48h antes do próximo aumento. Nunca duplicar budget de uma vez.
