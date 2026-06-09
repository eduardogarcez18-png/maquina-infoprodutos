---
name: gerar-plano-7-dias
description: Consolida diagnóstico, análise de métricas e decisões em um plano de ação diário para os próximos 7 dias com tarefas específicas, responsáveis e métricas de sucesso.
---

## Quando usar esta skill

Ao final de cada ciclo de análise, para transformar insights em ação. Usar como última skill em qualquer sessão de trabalho.

## Input necessário

- Diagnóstico atual (output de diagnosticar-produto ou analisar-metricas)
- Fase do produto (validação / teste / escala)
- Recursos disponíveis: budget semanal, equipe (solo ou time), criativos prontos vs. a produzir

## Processo passo a passo

1. Listar as 3 prioridades da semana (máximo 3 — foco é obrigatório)
2. Para cada prioridade, quebrar em tarefas diárias concretas
3. Para cada tarefa, definir: o quê, por quê, como fazer, métrica de sucesso
4. Distribuir as tarefas nos 7 dias considerando dependências (ex: não analisar antes de ter dados)
5. Definir o critério de sucesso da semana: o que precisa acontecer para considerar a semana bem-sucedida

## Regras do plano

- Máximo 3 prioridades por semana
- Cada dia deve ter no máximo 2 tarefas principais
- Dias 1–2: configuração / produção (não há dados ainda)
- Dias 3–4: primeira análise e ajustes
- Dias 5–6: segunda análise e decisão de escala ou novo teste
- Dia 7: retrospectiva e planejamento do próximo ciclo

## Output obrigatório

```
## Plano de 7 Dias: [Produto] — [Data de início]

### Fase atual
[Validação / Teste / Escala]

### Prioridades da semana
1. ...
2. ...
3. ...

### Critério de sucesso da semana
Se [X acontecer], a semana foi bem-sucedida.

---

**Dia 1 — [Data]**
- [ ] Tarefa: ... | Por quê: ... | Como: ... | Métrica: ...

**Dia 2 — [Data]**
- [ ] ...

**Dia 3 — [Data] (Primeira análise)**
- [ ] Analisar métricas com skill analisar-metricas
- [ ] ...

**Dia 4 — [Data]**
- [ ] ...

**Dia 5 — [Data] (Segunda análise)**
- [ ] ...

**Dia 6 — [Data]**
- [ ] ...

**Dia 7 — [Data] (Retrospectiva)**
- [ ] O que funcionou:
- [ ] O que não funcionou:
- [ ] O que testar na próxima semana:
- [ ] Próximo plano: acionar skill gerar-plano-7-dias
```
