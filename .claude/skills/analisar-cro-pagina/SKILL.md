---
name: analisar-cro-pagina
description: Checklist para avaliar uma página de vendas existente, identificar gargalos de conversão por seção e gerar recomendações de teste com hipótese, métrica e critério de corte.
---

# Skill: Analisar CRO de Página de Vendas

## Quando usar

Acionar quando:
- A página de vendas está no ar e recebendo tráfego
- A taxa de conversão está abaixo do benchmark (< 2% para produto low ticket, < 1% para médio ticket)
- O CTR do anúncio está bom mas o CPA está alto — indicativo de problema na página
- Antes de reescrever a copy completa — diagnosticar primeiro, reescrever depois

**Não acionar** sem dados de tráfego. Análise de CRO sem dados de comportamento é chute.

---

## Input Necessário

| Campo | Obrigatório | Descrição |
|---|---|---|
| URL da página ou copy completa | Sim | Para avaliar o conteúdo |
| CVR atual da página | Sim | Visitas / compras |
| Taxa de início de checkout | Sim | Visitas / inícios de checkout |
| Taxa de abandono de checkout | Sim | Inícios / compras concluídas |
| Fonte de tráfego principal | Sim | Meta Ads / Google / orgânico |
| Copy do criativo principal | Sim | Para avaliar congruência |
| Dados de scroll/heatmap | Não | Se disponível no Hotjar, Microsoft Clarity ou similar |
| Taxa de abandono por seção | Não | Se disponível via analytics |

---

## Processo

### Passo 1 — Diagnóstico do funil por etapa

Primeiro, classificar onde está o maior vazamento:

| Etapa | Métrica | Benchmark | Status |
|---|---|---|---|
| Clique no anúncio → visita LP | Alinhamento do criativo | — | Congruência ok? |
| Visita → permanência > 30s | Taxa de permanência | > 50% | |
| Permanência → início de checkout | CVR da página | 2–8% low ticket | |
| Início de checkout → compra | Taxa de conclusão do checkout | > 70% | |

Se a taxa de permanência for baixa (< 30% ficam mais de 30s), o problema está na hero — não nas seções seguintes.

---

### Passo 2 — Checklist por seção

Avaliar cada seção com nota 0 (ausente/ruim), 0,5 (parcial) ou 1 (presente/forte).

#### Hero (Seção 1)

| Critério | Nota | Problema identificado |
|---|---|---|
| Headline espelha a promessa do criativo? | | |
| Promessa é específica com prazo e ponto de partida? | | |
| CTA está acima da dobra em mobile? | | |
| Há elemento de prova visual imediata? | | |
| Headline passa no teste de 3 segundos? | | |

**Benchmark:** se a hero pontua < 3/5, é o primeiro ponto a corrigir antes de qualquer outra otimização.

---

#### Agitação do problema (Seção 2)

| Critério | Nota | Problema identificado |
|---|---|---|
| Identifica situações específicas de dor (não genéricas)? | | |
| O avatar se reconhece nessas situações? | | |
| A seção cria urgência sem fazer claim absoluto? | | |

---

#### Mecanismo único (Seção 4)

| Critério | Nota | Problema identificado |
|---|---|---|
| O mecanismo tem nome próprio? | | |
| Explica por que métodos anteriores não funcionaram? | | |
| O diferencial é claro e simples de entender? | | |

---

#### Prova social (Seção 7)

| Critério | Nota | Problema identificado |
|---|---|---|
| Depoimentos têm foto, nome e resultado específico? | | |
| Resultados apresentados são críveis (não exagerados)? | | |
| Há depoimento que trata a objeção principal do avatar? | | |
| Número de alunos ou avaliações está visível? | | |

---

#### Oferta e preço (Seção 9)

| Critério | Nota | Problema identificado |
|---|---|---|
| O preço aparece após construção de valor (stack)? | | |
| O contraste de preço (âncora vs. preço real) está claro? | | |
| Bônus estão listados com valor individual? | | |
| Há urgência ou escassez — e é verificável? | | |

---

#### Garantia (Seção 10)

| Critério | Nota | Problema identificado |
|---|---|---|
| A garantia está clara e em destaque? | | |
| O prazo da garantia está especificado? | | |
| A linguagem inverte o risco para o vendedor? | | |

---

#### CTAs

| Critério | Nota | Problema identificado |
|---|---|---|
| CTA acima da dobra? | | |
| CTA após stack de valor? | | |
| CTA após garantia? | | |
| Cada CTA tem texto de ação (não "comprar")? | | |
| A cor do CTA é única na página? | | |

---

#### Checkout

| Critério | Nota | Problema identificado |
|---|---|---|
| O checkout carrega em menos de 3 segundos? | | |
| O checkout tem menos de 5 campos? | | |
| O CTA da página leva direto ao checkout (sem etapa intermediária)? | | |
| Order bump está visível e com benefício claro? | | |

---

### Passo 3 — Classificar o gargalo principal

Após o checklist, classificar o gargalo principal em uma das categorias:

| Categoria | Sintoma | Seção responsável |
|---|---|---|
| **Congruência criativo/página** | CTR alto, taxa de permanência baixa | Hero — headline não espelha o criativo |
| **Hero fraca** | > 60% saem antes de 30s | Headline ou subheadline sem promessa clara |
| **Argumento fraco** | Permanência ok, CVR baixo | Mecanismo único ou stack de valor insuficiente |
| **Prova insuficiente** | Começam checkout, não concluem | Ceticismo não resolvido — depoimentos fracos ou ausentes |
| **Preço sem âncora** | CVR da página baixo em produto com bom criativo | Stack de valor sem ancoragem clara |
| **CTA mal posicionado** | Boa taxa de permanência, baixa de checkout | CTA ausente ou invisível após seções-chave |
| **Fricção no checkout** | Alta taxa de início, baixa taxa de conclusão | Checkout com muitos campos ou lento |
| **Garantia fraca** | Taxa de início de checkout > 50% mas conclusão < 50% | Risco percebido alto, garantia não resolve |

---

### Passo 4 — Gerar hipóteses de teste

Para o gargalo principal identificado, gerar 1–3 hipóteses de teste:

**Formato:**
> "Se [avatar] está abandonando na [etapa] por causa de [problema identificado], então [mudança específica] deve aumentar [métrica] de [valor atual] para [meta]."

**Regra:** testar uma variável por vez. Não mudar headline e garantia ao mesmo tempo.

---

## Output

### Diagnóstico geral

```
## CRO Diagnóstico — [Nome da página] — [Data]

**CVR atual:** [%]
**Gargalo principal:** [categoria]
**Seção crítica:** [seção com maior problema]
**Ação imediata:** [o que fazer agora]
```

### Score por seção

| Seção | Score | Problema |
|---|---|---|
| Hero | /5 | |
| Agitação | /3 | |
| Mecanismo único | /3 | |
| Prova social | /4 | |
| Oferta e preço | /4 | |
| Garantia | /3 | |
| CTAs | /5 | |
| Checkout | /4 | |

### Hipóteses priorizadas

| # | Hipótese | Variável | Métrica | Meta | Critério de corte |
|---|---|---|---|---|---|
| 1 | ... | ... | CVR | % | % |
| 2 | ... | ... | ... | | |

### Decisão

- [ ] Ajuste pontual (< 1 hora de implementação) — não requer novo teste
- [ ] Teste A/B de elemento específico (headline, CTA, garantia)
- [ ] Reescrita de seção completa
- [ ] Reescrita completa da página — problema estrutural

---

## Regras de Qualidade

- Análise sem dados de CVR real = hipótese, não diagnóstico — sinalizar para o usuário
- Mais de 1 variável no mesmo teste = experimento inválido — corrigir antes de implementar
- Recomendação de reescrita completa sem testar ajuste pontual = desperdício — testar elemento antes de reescrever tudo
