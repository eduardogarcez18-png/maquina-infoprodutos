---
name: montar-campanha-meta
description: Gera a estrutura completa de campanha no Meta Ads com configurações por fase (validação/teste/escala), públicos recomendados, budget, regras de corte e cronograma de análise.
---

## Quando usar esta skill

Ao iniciar testes com criativos novos ou ao escalar campanhas existentes.

## Input necessário

- Produto e oferta
- Criativos disponíveis (quantos e quais ângulos)
- Budget diário disponível
- Objetivo (CPL, CPA ou ROAS meta)
- Fase atual (validação / teste / escala)
- Histórico de públicos que já foram testados (se houver)

## Processo passo a passo

1. Definir objetivo de campanha (Vendas ou Leads)
2. Definir estrutura (ABO para validação, CBO para escala)
3. Definir públicos por fase
4. Alocar budget por conjunto
5. Definir regras de corte automáticas
6. Criar cronograma de análise (quando olhar e o que decidir)

## Estruturas por fase

**Fase 1 — Validação (budget R$50–150/dia):**
- Estrutura: ABO (budget por conjunto)
- Budget por conjunto: R$20–30/dia
- Públicos: 1 broad (sem interesse), 1 interesse amplo do nicho
- Criativos: 1 por conjunto (testar ângulos separados)
- Regra de corte: sem resultado com 3x CPA alvo gasto → pausar

**Fase 2 — Teste (budget R$150–500/dia):**
- Estrutura: CBO (budget na campanha)
- Públicos: broad + 2 interesses + 1 lookalike 1%
- Criativos: vencedores da fase 1, máximo 5 por campanha
- Regra de corte: CPA > 1,5x meta após 50% do budget diário → pausar conjunto

**Fase 3 — Escala (budget R$500+/dia):**
- Escala horizontal: duplicar conjuntos vencedores antes de aumentar budget
- Escala vertical: aumentar budget máximo 20% por vez, aguardar 48h
- Monitorar: frequência (>3 = criativo cansado), CPM (aumento > 30% = saturação)

## Output obrigatório

```
## Estrutura de Campanha: [Nome do Produto]

### Fase: [Validação / Teste / Escala]

**Campanha**
- Nome: ...
- Objetivo: ...
- Tipo: ABO / CBO
- Budget total: R$ X/dia

**Conjuntos de Anúncios**
| Conjunto | Público | Budget | Criativos |
|---|---|---|---|
| ... | ... | R$ X | ... |

**Regras de Corte**
- Criativo: ...
- Conjunto: ...
- Campanha: ...

**Cronograma de Análise**
- Dia 1–2: não mexer (fase de aprendizado)
- Dia 3: primeira análise — cortar o que ultrapassou regra de corte
- Dia 5: segunda análise — decisão de escala ou novo teste
- Dia 7: relatório completo
```
