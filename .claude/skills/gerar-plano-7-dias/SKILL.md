---
name: gerar-plano-7-dias
description: Gera plano de ação operacional com tarefas por dia para os próximos 7 dias. Cada dia tem foco fixo e tarefas concretas com métrica de sucesso e critério de corte.
---

## Quando usar esta skill

Ao final de cada ciclo de análise para transformar diagnóstico em ação. Sempre como última entrega de uma sessão de trabalho. Também ao iniciar uma nova semana de testes.

Não gerar plano sem ter: diagnóstico atual, fase do produto e recursos disponíveis definidos.

---

## Input necessário

- Diagnóstico atual (output de `diagnosticar-produto` ou `analisar-metricas`)
- Fase do produto: Validação / Teste / Escala
- Budget semanal disponível
- Criativos prontos vs. a produzir
- CPA meta e CPA de corte

---

## Estrutura fixa dos 7 dias

Cada dia tem um foco que não muda — independente do produto ou fase.

| Dia | Foco | O que acontece |
|---|---|---|
| Dia 1 | Preparação | Funil, pixel, criativos, campanha — tudo pronto e testado antes de ligar |
| Dia 2 | Lançamento | Campanha no ar. Não mexer em nada. Monitorar aprovação dos anúncios. |
| Dia 3 | Leitura inicial | Primeiros dados. Verificar se há problema técnico. Não cortar nada ainda. |
| Dia 4 | Primeira decisão | Cortar o que ultrapassou critério de corte. Ajustar orçamento se necessário. |
| Dia 5 | Novas variações | Lançar criativos ou públicos alternativos para substituir o que foi cortado. |
| Dia 6 | Otimização | Analisar performance dos novos + manter os bons. Redistribuir budget. |
| Dia 7 | Decisão de escala ou pausa | Com 5 dias de dados: decidir escalar, pausar ou reiniciar ciclo. |

---

## Regras do plano

- Máximo 3 prioridades por semana — foco é obrigatório
- Cada dia tem no máximo 2 tarefas principais
- Dia 1 e 2: sem análise de dados (não há dados úteis ainda)
- Dia 3: leitura, não decisão
- Dia 4: primeira decisão real com dados de 48–72h
- Dia 7: decisão com 5 dias de dados — não adiar

---

## Processo passo a passo

1. Definir as 3 prioridades da semana com base no diagnóstico
2. Definir o critério de sucesso da semana — um número específico
3. Para cada dia, preencher: foco + tarefas concretas + métrica + critério de corte
4. Para cada teste ou decisão do plano, documentar: hipótese testada + métrica de validação + volume mínimo de dados + decisão possível + próxima ação
5. Não deixar nenhum dia sem tarefa definida — indefinição é paralisação
6. Dia 7 deve terminar com uma decisão documentada (escalar / pausar / reiniciar) e o próximo plano iniciado
7. Separar explicitamente o que é fato, estimativa e hipótese em cada item do plano

---

## Output obrigatório

```
## Plano de 7 Dias: [Produto] — [Data de início]

**Fase:** [Validação / Teste / Escala]
**Budget semanal:** R$ X
**CPA meta:** R$ X | **CPA de corte:** R$ X

### Prioridades da semana
1. ...
2. ...
3. ...

### Critério de sucesso da semana
[Um número ou evento específico que define a semana como bem-sucedida]
Ex: "Ao menos 1 criativo com CPA abaixo de R$X e 5+ vendas no período"

---

**Dia 1 — [Data] — PREPARAÇÃO**
Foco: garantir que tudo está funcionando antes de ligar o tráfego

- [ ] Tarefa: [o quê] | Como: [como fazer] | Métrica: [o que verificar]
- [ ] Tarefa: ...

**Dia 2 — [Data] — LANÇAMENTO**
Foco: campanha no ar, sem intervenção

- [ ] Tarefa: ligar a campanha às [horário] | Como: ... | Verificar: anúncios aprovados?
- [ ] Tarefa: monitorar aprovação dos criativos — se reprovado, acionar plano B

**Dia 3 — [Data] — LEITURA INICIAL**
Foco: observar, não decidir

- [ ] Tarefa: coletar CTR e CPM de cada criativo | Benchmark: CTR > 1%, CPM < R$X
- [ ] Tarefa: verificar se há problema técnico (pixel disparando? LP carregando?)
- Não cortar nada hoje — dados com menos de 48h são ruído.

**Dia 4 — [Data] — PRIMEIRA DECISÃO**
Foco: cortar o que ultrapassou critério de corte, realocar budget

- [ ] Tarefa: rodar skill `analisar-metricas` com dados de D2+D3
- [ ] Decisão obrigatória: [criativo X] → manter / pausar / iterar — justificativa: ...
- [ ] Tarefa: se pausou algum conjunto, redistribuir budget para os que estão ok

**Dia 5 — [Data] — NOVAS VARIAÇÕES**
Foco: substituir o que foi pausado com variação baseada em hipótese documentada

- [ ] Tarefa: lançar [criativo alternativo] com ângulo [X]
  - Hipótese testada: "Se [avatar] reage a [ângulo], então [métrica] deve [comportamento esperado]"
  - Métrica de validação: [CTR / Hook Rate / CVR / CPA]
  - Volume mínimo de dados: [impressões / dias / R$ gastos antes de decidir]
  - Decisão possível: [manter se X / pausar se Y]
  - Próxima ação se confirmado: [o que fazer quando a hipótese for validada]
- [ ] Tarefa: ajustar público se CPM > R$X | Ação: ...

**Dia 6 — [Data] — OTIMIZAÇÃO**
Foco: ajuste fino antes da decisão final

- [ ] Tarefa: comparar performance dos criativos novos vs. originais
- [ ] Tarefa: redistribuir budget para os 2 melhores conjuntos
- [ ] Verificar: CPA está convergindo para a meta ou se afastando?

**Dia 7 — [Data] — DECISÃO FINAL**
Foco: decidir o que acontece na semana 2

- [ ] Rodar skill `analisar-metricas` com dados completos da semana
- [ ] Decisão documentada: [ESCALAR / PAUSAR / REINICIAR CICLO] — justificativa com número
- [ ] Se escalar: acionar `advogado-do-diabo` antes de aumentar budget
- [ ] Se pausar: documentar o que foi aprendido e o que testar diferente
- [ ] Acionar skill `gerar-plano-7-dias` para a semana 2

### Retrospectiva (preencher no Dia 7)
- O que funcionou: ...
- O que não funcionou: ...
- Aprendizado principal: ...
- Hipótese para semana 2: ...
```

---

## Estrutura obrigatória de cada hipótese no plano

Todo item de teste ou decisão do plano deve conter:

```
- Hipótese testada: "Se [avatar/situação], então [ação/variável] deve gerar [resultado mensurável]"
- Métrica de validação: [métrica específica — CTR, CPA, CVR, Hook Rate etc.]
- Volume mínimo de dados: [X impressões OU X dias OU R$X gastos antes de decidir]
- Decisão possível: [manter se ≥X / pausar se <Y / iterar se entre X e Y]
- Próxima ação: [o que acontece imediatamente após confirmar ou refutar a hipótese]
```

Se um item do plano não tiver esses 5 campos preenchidos, o item está incompleto.

---

## Separação obrigatória por tipo de informação

Ao gerar o plano, usar os marcadores:
- `[DADO VALIDADO]` — vem de campanha real já rodada (pixel, Ads Manager, plataforma)
- `[ESTIMATIVA]` — baseado em benchmarks de mercado ou produtos similares
- `[HIPÓTESE]` — suposição lógica sem dado de suporte ainda
- `[DADO AUSENTE]` — informação necessária que não foi fornecida

Exemplo de uso correto:
> CPA meta: R$17 `[ESTIMATIVA baseada em LTV calculado]`
> CTR benchmark: 1–3% `[ESTIMATIVA de mercado]`
> Take rate de OB: 35% `[HIPÓTESE — sem dado validado neste produto]`

---

## Regras de qualidade

- Tarefa sem métrica = tarefa incompleta
- Hipótese sem volume mínimo de dados = hipótese não testável
- Dia 7 sem decisão documentada = plano não executado
- Decisão de escala sem passar pelo `advogado-do-diabo` = protocolo violado
- Plano que não gera o próximo plano = ciclo quebrado
- Estimativa apresentada como fato = erro de epistemologia — corrigir antes de entregar
