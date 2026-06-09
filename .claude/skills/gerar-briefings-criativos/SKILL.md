---
name: gerar-briefings-criativos
description: Gera briefings completos de criativos no formato Meta Andromeda. Cada briefing cobre um ângulo específico com hipótese clara, critério de sucesso e critério de corte definidos antes da produção.
---

## Quando usar esta skill

Após ter oferta e avatar definidos. Ao iniciar testes de criativos ou quando os criativos atuais saturaram (queda de CTR ou Hook Rate abaixo do benchmark).

Não gerar briefing sem ter: oferta definida, avatar mapeado e pelo menos um ângulo claro para testar.

---

## Input necessário

- Oferta (output de `criar-oferta`) — promessa, mecanismo único, preço
- Mapa de avatar (output de `criar-mapa-avatar`) — dores, desejos, objeções, nível de consciência
- Ângulos a testar (ou solicitar sugestão com base no avatar)
- Formatos desejados: VSL / Estático / Carrossel / UGC / Talking Head
- Quantidade de briefings
- CPA meta e CPA de corte (para definir critérios)

---

## Ângulos padrão (cobrir ao menos 3 na primeira rodada)

1. **Dor principal** — falar da frustração mais intensa. Avatar no nível: consciente do problema.
2. **Transformação desejada** — mostrar o resultado. Avatar que acredita ser possível, busca o como.
3. **Mecanismo único** — por que outros métodos falharam + o que é diferente. Avatar que já tentou antes.
4. **Prova social** — resultado de alguém igual ao avatar. Avatar cético que precisa ver para acreditar.
5. **Curiosidade / segredo** — informação que muda o quadro. Avatar em scroll passivo.
6. **Contra-narrativa** — atacar o conselho convencional. Para scroll pela dissonância cognitiva.

---

## Processo passo a passo

1. Para cada ângulo + formato, preencher todos os 12 campos do briefing
2. Garantir que o hook seja específico (nunca genérico) e testável em 1,5s
3. Escrever a hipótese completa antes de escrever o roteiro — ela define o que está sendo testado
4. Gerar 3 variações de hook para o mesmo corpo — o hook é a variável da primeira rodada de testes
5. Preencher o texto exato de legendas sobrepostas — não apenas indicar "sim, tem texto"
6. Definir critério de sucesso e critério de corte antes de entregar o briefing

---

## Output obrigatório (por briefing)

```
## Briefing de Criativo — [CÓDIGO]

### 1. METADADOS
- **Código:** [formato-ângulo-número]
- **Formato:** VSL / Estático / Carrossel / UGC / Talking Head
- **Ângulo:** [nome do ângulo]

### 2. AVATAR ALVO
- **Avatar:** [primário / secundário — nome]
- **Nível de consciência:** [inconsciente / consciente do problema / consciente da solução / consciente do produto]

### 3. CONTEXTO PSICOLÓGICO
- **Dor explorada:** [dor específica — não genérica]
- **Desejo ativado:** [desejo específico que este criativo promete]
- **Objeção antecipada:** [objeção que o avatar vai ter — e como o criativo a neutraliza]

### 4. HIPÓTESE
"Se [avatar específico] sente/pensa [situação/crença], então um criativo focado em [ângulo]
deve gerar [métrica] acima de [benchmark] em público frio."

### 5. HOOK (primeiros 3 segundos)
- **Variação A:** [texto exato da fala ou legenda] | [orientação visual]
- **Variação B:** [texto exato] | [orientação visual]
- **Variação C:** [texto exato] | [orientação visual]

### 6. TEXTO NA IMAGEM / LEGENDA SOBREPOSTA
[Texto exato que aparece em tela — escrever o texto, não apenas "sim"]

### 7. ROTEIRO / DIREÇÃO DE ARTE
**PROBLEMA (s 3–15):**
[roteiro de texto + o que acontece em tela]

**AGITAÇÃO (s 15–30):**
[roteiro + visual]

**SOLUÇÃO / MECANISMO (s 30–60):**
[roteiro + visual — apresentar o mecanismo sem revelar tudo]

**PROVA (s 60–90):**
[depoimento / dado — específico: número, prazo, ponto de partida]

**OFERTA + CTA (últimos 15–30s):**
[o que é + preço + o que leva + chamada para ação diretiva]

### 8. ORIENTAÇÕES DE PRODUÇÃO
- **Duração total:** X segundos
- **Formato de tela:** 9:16 / 1:1 / 4:5
- **Tom de voz:** urgente / empático / coloquial / autoritativo
- **Ritmo de edição:** [cortes a cada Xs / narrativa / dinâmico]
- **Música:** [mood e referência concreta]
- **Referência visual:** [referência concreta de estilo]

### 9. MÉTRICA PRINCIPAL
[A métrica que define se este criativo funciona — ex: CTR, Hook Rate, CPA]

### 10. CRITÉRIO DE SUCESSO
[O número que confirma a hipótese — ex: "CTR > 1,8% com 1.500+ impressões em 3 dias"]

### 11. CRITÉRIO DE CORTE
[O número que dispara a pausa — ex: "CTR < 0,8% com R$30+ gastos"]

### 12. O QUE ESTE CRIATIVO RESPONDE
[A pergunta estratégica que este criativo testa sobre o avatar ou o mercado]
```

---

## Regras de qualidade

- Hook genérico = briefing rejeitado. Reescrever antes de entregar.
- Hipótese sem métrica = hipótese inválida. Toda hipótese tem um número.
- Critério de corte ausente = briefing incompleto. Define antes de produzir, não depois de gastar.
- Texto sobreposto descrito como "sim" sem o texto exato = campo incompleto.
