# Histórico de Testes — Template de Registro

## Como usar este arquivo

Registrar cada ciclo de teste aqui, em ordem cronológica. Um registro por criativo ou por decisão relevante. Este arquivo é a memória do projeto — sem ele, os mesmos erros se repetem e os mesmos aprendizados se perdem.

**Regra:** ao final de cada semana de campanha, preencher ao menos um registro. Ao tomar qualquer decisão de pausar, escalar ou mudar, registrar antes de executar.

---

## Template de Registro

```
---

## Registro #[N] — [Data]

### Identificação
- **Produto:** [nome do produto]
- **Oferta:** [descrição da oferta testada — preço, bônus, upsells]
- **Preço:** R$ [valor do produto principal]
- **Canal:** Meta Ads / Google Ads / Ambos
- **Fase:** Validação / Teste / Escala

### Campanha
- **Nome da campanha:** [identificador]
- **Estrutura:** ABO / CBO
- **Público:** [descrição: broad / interesse / lookalike]
- **Orçamento diário:** R$ [valor]
- **Período:** [data início] → [data fim]

### Criativo
- **Código do criativo:** [ex: UGC-DOR-001]
- **Formato:** VSL / Estático / Carrossel / UGC / Talking Head
- **Ângulo:** [dor / transformação / mecanismo / prova social / curiosidade / contra-narrativa]
- **Avatar alvo:** [primário / secundário / nome]
- **Nível de consciência:** [inconsciente / consciente do problema / consciente da solução / consciente do produto]

### Hipótese testada
[Frase completa: "Se [avatar] sente/pensa [situação], então [ângulo] deve gerar [métrica] acima de [benchmark]"]

### Métricas de Performance
| Métrica | Resultado | Benchmark | Status |
|---|---|---|---|
| Impressões | | | |
| CPM | R$ | R$ 15–30 | ✅/⚠️/❌ |
| CTR | % | 1–3% | |
| CPC | R$ | R$ 1,50–3 | |
| Cliques | | | |
| Visitas LP | | | |
| CVR LP | % | 5–15% | |
| Checkouts iniciados | | | |
| Taxa checkout | % | >60% | |
| Compras | | | |
| CPA | R$ | R$ [meta] | |
| ROAS | x | >[meta]x | |
| Order Bumps aceitos | | | |
| Taxa OB | % | 20–40% | |
| Upsells aceitos | | | |
| Taxa Upsell 1 | % | 10–25% | |

### Financeiro
- **Budget gasto:** R$ [valor]
- **Receita gerada:** R$ [valor]
- **Ticket médio real:** R$ [valor] (inclui OB e upsell)
- **Lucro estimado:** R$ [receita − budget − custos de plataforma]

### Resultado
- [ ] Sucesso — hipótese confirmada
- [ ] Parcial — hipótese parcialmente confirmada
- [ ] Falhou — hipótese refutada
- [ ] Inconclusivo — dados insuficientes

**Decisão tomada:** [PAUSAR / MANTER / ITERAR / TROCAR ÂNGULO / TROCAR PÁGINA / TROCAR OFERTA / DUPLICAR / ESCALAR]

**Justificativa:** [1–2 frases com o número que sustenta a decisão]

### Aprendizado principal
[O que este teste revelou sobre o avatar, o mercado, o criativo ou o funil — em 2–4 frases]

### Próximo teste
**Hipótese:** [o que testar na próxima rodada com base neste aprendizado]
**Variável a testar:** [o que muda]
**Métrica de sucesso:** [o número que confirma]
**Critério de corte:** [o número que dispara pausa]

---
```

---

## Exemplo de Registro Preenchido

```
---

## Registro #1 — 12/06/2026

### Identificação
- **Produto:** eBook Como Desenhar Dragon Ball
- **Oferta:** eBook R$19,90 + OB Pack Referências R$9,90 + Upsell Masterclass R$37
- **Preço:** R$ 19,90
- **Canal:** Meta Ads
- **Fase:** Validação

### Campanha
- **Nome da campanha:** DB_VALIDACAO_JUN26
- **Estrutura:** ABO
- **Público:** Conjunto 1: Broad 16–30 anos | Conjunto 2: Interesse Anime+Desenho
- **Orçamento diário:** R$ 50 (R$25 por conjunto)
- **Período:** 09/06/2026 → 15/06/2026

### Criativo
- **Código:** UGC-DOR-001
- **Formato:** UGC Talking Head
- **Ângulo:** Dor
- **Avatar alvo:** Lucas — primário (16–28 anos, fã de DB)
- **Nível de consciência:** Consciente do problema

### Hipótese testada
"Se o avatar fã de Dragon Ball já tentou tutoriais gratuitos e se frustrou, então um criativo focado na dor de 'não conseguir desenhar direito' deve gerar CTR > 2% e Hook Rate > 30% em público frio."

### Métricas de Performance
| Métrica | Resultado | Benchmark | Status |
|---|---|---|---|
| Impressões | 8.400 | | |
| CPM | R$ 17,80 | R$ 15–30 | ✅ |
| CTR | 2,3% | 1–3% | ✅ |
| CPC | R$ 0,77 | R$ 1,50–3 | ✅ |
| Cliques | 193 | | |
| Visitas LP | 178 | | |
| CVR LP | 3,9% | 5–15% | ⚠️ |
| Checkouts iniciados | 14 | | |
| Taxa checkout | 50% | >60% | ⚠️ |
| Compras | 7 | | |
| CPA | R$ 50 | R$ 20 | ❌ |
| ROAS | 0,28x | >1,5x | ❌ |

### Financeiro
- **Budget gasto:** R$ 350
- **Receita gerada:** R$ 139,30 (7 × R$19,90)
- **Ticket médio real:** R$ 19,90 (sem OB/upsell rastreado)
- **Lucro estimado:** R$ -210,70

### Resultado
- [ ] Sucesso
- [x] Parcial — CTR confirmou hipótese, mas CPA muito acima da meta
- [ ] Falhou
- [ ] Inconclusivo

**Decisão tomada:** ITERAR — criativo validado (CTR ok), problema está na página (CVR 3,9%) e no funil (sem OB rastreado)

**Justificativa:** CTR 2,3% confirma que o ângulo de dor conecta com o avatar. O problema não é o criativo — é a LP convertendo abaixo do benchmark e o order bump provavelmente não aparecendo.

### Aprendizado principal
O ângulo de dor funciona — CTR e Hook Rate acima do benchmark. O gargalo real está na LP (CVR 3,9% vs. benchmark de 5–15%) e possivelmente no rastreamento do OB. Próxima ação é corrigir a LP antes de mudar o criativo.

### Próximo teste
**Hipótese:** Trocar headline da LP de descrição do produto para promessa de resultado específico deve aumentar CVR LP de 3,9% para 6%+
**Variável a testar:** Headline da landing page
**Métrica de sucesso:** CVR LP > 5,5% mantendo o mesmo tráfego
**Critério de corte:** CVR LP < 3% após 150 visitas com nova headline

---
```

---

## Log de Decisões

Registrar decisões relevantes que não são testes de criativo — mudanças de oferta, estrutura, budget, funil.

```
| Data | Decisão | Justificativa | Resultado esperado |
|---|---|---|---|
| DD/MM | ... | ... | ... |
```
