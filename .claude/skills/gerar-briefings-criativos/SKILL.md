---
name: gerar-briefings-criativos
description: Gera briefings completos de criativos no formato Meta Andromeda. Cada briefing cobre um ângulo específico com hook, roteiro estruturado, orientações de produção e hipótese a testar.
---

## Quando usar esta skill

Após ter oferta e avatar definidos. Ao iniciar testes de criativos ou quando os criativos atuais saturaram (queda de CTR ou Hook Rate).

## Input necessário

- Oferta (output de criar-oferta)
- Mapa de avatar (output de criar-mapa-avatar)
- Ângulos a testar (ou pedir para a skill sugerir)
- Formatos desejados (VSL, estático, carrossel, UGC, talking head)
- Quantidade de briefings

## Ângulos padrão para teste (usar ao menos 3)

1. **Dor principal:** começa no problema máximo do avatar
2. **Transformação desejada:** começa no resultado que o avatar quer
3. **Mecanismo único:** começa explicando por que outros métodos falham
4. **Prova social:** começa com resultado de um cliente real
5. **Curiosidade/segredo:** começa com uma informação contra-intuitiva
6. **Contra-narrativa:** ataca a crença limitante que impede a compra

## Processo passo a passo

1. Para cada ângulo + formato, gerar um briefing completo
2. Garantir que o hook seja específico (não genérico) e testável em 1,5s
3. Documentar a hipótese: "Se este ângulo funcionar, significa que o avatar está no nível de consciência X"
4. Gerar 3 variações de hook para o mesmo corpo (mesma estrutura, hooks diferentes)

## Output obrigatório (por briefing)

```
## Briefing de Criativo #[N]

**Nome:** [identificador único]
**Formato:** [VSL / estático / carrossel / UGC / talking head]
**Ângulo:** [nome do ângulo]
**Hipótese:** Se converter, confirma que [insight sobre o avatar]

### HOOK (primeiros 3 segundos)
Variação A: [texto exato + orientação visual]
Variação B: [texto exato + orientação visual]
Variação C: [texto exato + orientação visual]

### PROBLEMA (5–15s)
[roteiro de texto + orientações visuais]

### AGITAÇÃO (15–30s)
[roteiro de texto + orientações visuais]

### SOLUÇÃO / MECANISMO (30–60s)
[apresentação do mecanismo único]

### PROVA (60–90s)
[depoimento / dado / resultado]

### OFERTA + CTA (últimos 15–30s)
[o que é + quanto custa + chamada para ação]

### ORIENTAÇÕES DE PRODUÇÃO
- Duração total: X segundos
- Formato: 9:16 / 1:1 / 16:9
- Tom de voz: ...
- Ritmo de edição: ...
- Texto sobreposto: sim/não — onde e o quê
- Referência visual: ...
```
