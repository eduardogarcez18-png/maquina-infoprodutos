---
name: diagnosticar-produto
description: Coleta informações sobre um infoproduto e gera diagnóstico completo com score por dimensão, pontos críticos e oportunidades imediatas de melhoria.
---

## Quando usar esta skill

Ao iniciar o trabalho com um produto novo, ou quando os resultados estagnaram e é necessário um novo ponto de partida.

## Input necessário

- Nome e descrição do produto
- Nicho e sub-nicho
- Preço atual
- Funil atual (quais etapas existem)
- Métricas disponíveis (pode ser "nenhuma" se produto novo)
- Histórico de testes (o que já foi testado e resultado)
- Budget mensal disponível para tráfego

## Processo passo a passo

1. Mapear o produto: o que entrega, para quem, qual transformação promete
2. Avaliar a oferta atual: existe mecanismo único? A promessa é específica? Os bônus fazem sentido?
3. Avaliar o funil: quais etapas existem, quais estão faltando (ex: sem order bump, sem upsell)
4. Avaliar os dados: se houver métricas, identificar qual etapa está abaixo do benchmark
5. Avaliar o posicionamento: como se compara com os 3 principais concorrentes
6. Gerar score por dimensão (0–10 cada): Produto / Oferta / Tráfego / Funil / Dados

## Output obrigatório

```
## Diagnóstico: [Nome do Produto]

### Scores
| Dimensão | Score | Situação |
|---|---|---|
| Produto | X/10 | ... |
| Oferta | X/10 | ... |
| Tráfego | X/10 | ... |
| Funil | X/10 | ... |
| Dados | X/10 | ... |

### Fase atual
[Validação / Teste / Escala] — justificativa

### Top 3 problemas críticos
1. ...
2. ...
3. ...

### Top 3 oportunidades imediatas
1. ...
2. ...
3. ...

### Próximo agente a acionar
[nome do agente] — motivo
```
