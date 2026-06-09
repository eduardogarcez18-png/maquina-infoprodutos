---
name: criar-oferta
description: Constrói a oferta completa com promessa, mecanismo único nomeado, stack de valor, bônus estratégicos, preço âncora e estrutura de upsell. Requer mapa de avatar pronto.
---

## Quando usar esta skill

Após ter o mapa de avatar. Ao lançar produto novo ou quando a oferta atual não está convertendo (CVR da página de vendas abaixo de 1%).

## Input necessário

- Mapa de avatar (output da skill criar-mapa-avatar)
- Descrição do produto e o que ele entrega
- Posicionamento desejado (premium, acessível, rápido resultado, método completo...)
- Concorrentes e seus preços
- O que diferencia este produto (mesmo que ainda não nomeado)

## Processo passo a passo

1. Definir a promessa principal: resultado específico + prazo + para quem + sem o quê (sem [objeção principal])
2. Nomear o mecanismo único: identificar o processo diferente, dar nome proprietário, explicar por que funciona quando outros falham
3. Construir o stack de valor: listar cada entrega com valor percebido individual
4. Criar os bônus: cada bônus deve resolver uma objeção específica (não bônus genérico)
5. Definir estrutura de preços: preço âncora → preço de venda → order bump → upsell 1 → upsell 2
6. Criar 3 variações de headline (4U: Útil, Urgente, Único, Ultra-específico)

## Output obrigatório

```
## Oferta: [Nome do Produto]

### Promessa principal
[resultado] + [prazo] + [para quem] + sem [objeção]

### Mecanismo único
Nome: [Nome Proprietário]
Como funciona: ...
Por que outros métodos falham e este não: ...

### Stack de valor
| Entrega | Valor percebido |
|---|---|
| Produto principal | R$ X |
| Bônus 1: [nome] (resolve objeção: ...) | R$ X |
| Bônus 2: [nome] | R$ X |
| **Total** | **R$ X** |
| **Preço de venda** | **R$ X** |

### Order Bump
Produto: ... | Preço: R$ X | Gatilho: ...

### Upsell 1
Produto: ... | Preço: R$ X | Gatilho: ...

### Headlines (3 variações)
1. ...
2. ...
3. ...
```
