---
name: estruturar-wireframe-vendas
description: Processo para transformar copy estruturada em wireframe de alta conversão — layout por seção, hierarquia visual, posicionamento de CTAs, mobile-first e anotações para o desenvolvedor ou page builder.
---

# Skill: Estruturar Wireframe de Página de Vendas

## Quando usar

Acionar após ter a copy completa da página definida (output de `criar-copy-pagina-vendas`).

**Não acionar** se a copy ainda não está escrita — o wireframe sem copy é estrutura sem argumento.

---

## Input Necessário

| Campo | Obrigatório | Descrição |
|---|---|---|
| Copy completa por seção | Sim | Todas as seções com texto e anotações |
| Produto e nicho | Sim | Para calibrar tom visual |
| Formato da página | Sim | Direta / VSL / quiz / advertorial |
| Elementos de prova disponíveis | Sim | Fotos de alunos, prints, selos, logos |
| Page builder | Não | WordPress/Elementor, Hotmart Pages, Leadpages, código custom — para calibrar anotações técnicas |

---

## Processo

### Passo 1 — Inventário de elementos

Antes de estruturar, listar todos os elementos visuais disponíveis:

| Tipo | Disponível? | Quantidade |
|---|---|---|
| Foto do criador | Sim/Não | |
| Fotos de alunos com resultados | Sim/Não | |
| Prints de depoimentos | Sim/Não | |
| Imagens de resultado do produto | Sim/Não | |
| Vídeo (VSL ou depoimento) | Sim/Não | |
| Selos de garantia | Sim/Não | |
| Logos de mídia ("como visto em") | Sim/Não | |
| Mockup do produto | Sim/Não | |

Elementos ausentes serão substituídos por alternativas no wireframe.

---

### Passo 2 — Estruturar mobile-first

Cada seção é desenhada primeiro para 375px de largura (iPhone padrão). Desktop é adaptação — não o ponto de partida.

**Regras mobile:**
- Um bloco por linha — sem colunas em mobile (exceto em comparações curtas 2×2)
- CTA visível sem scroll na hero
- Fonte mínima 16px no corpo
- Imagens de largura total (não flutuar texto ao redor de imagem em mobile)
- Botão de CTA com largura total em mobile (não botão pequeno centralizado)

---

### Passo 3 — Definir hierarquia por seção

Para cada seção, identificar:

1. **Elemento de entrada** — como o avatar chega nesta seção (lendo, scrollando, após CTA)
2. **Elemento principal** — o que o olho deve ver primeiro (H1, imagem de resultado, vídeo)
3. **Elemento de suporte** — o que reforça o elemento principal (bullets, subheadline, badge)
4. **Elemento de saída** — o que leva o avatar para a próxima seção (CTA, seta, pergunta)

---

### Passo 4 — Posicionar CTAs

Regra de posicionamento de CTA:

| Posição | Justificativa |
|---|---|
| Acima da dobra (hero) | Avatar que já decidiu — não precisa rolar |
| Após stack de valor | Avatar que precisou ver o conteúdo antes de clicar |
| Após prova social | Avatar cético que precisava de validação |
| Após garantia | Avatar com objeção de risco |
| CTA final | Último recurso para quem chegou até o fim |

Cada CTA deve ter texto diferente — não repetir o mesmo texto em todos os botões.

---

### Passo 5 — Anotar comportamento mobile/desktop

Para cada seção, especificar:
- Como os elementos se reorganizam em desktop (de empilhado para lado a lado)
- Qual elemento ganha destaque em desktop que não aparece em mobile
- Se há elemento que some em mobile para reduzir fricção visual

---

## Output — Wireframe por Seção

### Formato padrão de entrega

```
---

## SEÇÃO [N]: [Nome]

### Função na jornada
[O que esta seção faz para a conversão]

### Mobile (375px)
┌─────────────────────────────┐
│  [Elemento 1 — topo]        │
├─────────────────────────────┤
│  [Elemento 2 — corpo]       │
│  [Elemento 3 — suporte]     │
├─────────────────────────────┤
│  [CTA — se presente]        │
└─────────────────────────────┘

### Desktop (1200px)
┌──────────────┬──────────────┐
│  [Esquerda]  │  [Direita]   │
└──────────────┴──────────────┘

### Anotações de design
- Fundo: [cor ou código]
- Elemento principal: [tipo, peso visual]
- Espaçamento: [comprimido / normal / generoso]
- Elemento especial: [box, badge, seta, divisor]

### Anotações técnicas
- Componente: [Section / Hero / Testimonial / CTA Block / etc.]
- Comportamento: [fixo / scroll parallax / fade in / nenhum]
- Prioridade de produção: [alta / média / baixa]

---
```

---

## Mapa de CTAs

Ao final do wireframe, entregar tabela consolidada:

| # | Posição | Texto do botão | Cor | Justificativa |
|---|---|---|---|---|
| 1 | Hero — acima da dobra | "Quero aprender agora" | CTA principal | Avatar que já decidiu |
| 2 | Após stack de valor | "Ver detalhes e garantir minha vaga" | CTA principal | Avatar que precisou de contexto |
| 3 | Após garantia | "Começar com garantia de 7 dias" | CTA principal | Avatar com objeção de risco |
| 4 | CTA final | "Sim, quero [resultado da promessa]" | CTA principal | Último apelo |

---

## Checklist de Fricção

Antes de finalizar, listar elementos a remover:

- [ ] Menu de navegação no header
- [ ] Links externos na página
- [ ] Rodapé com links (manter somente links legais obrigatórios)
- [ ] Pop-ups que interrompem a leitura (exceto exit intent)
- [ ] Elementos animados que distraem do texto
- [ ] Formulários com muitos campos (acima de 3 campos = fricção alta)
- [ ] Contador de tempo falso (urgência não verificável)

---

## Prioridade de Produção

Ao final, entregar ranking de prioridade de produção:

| Prioridade | Seção | Justificativa |
|---|---|---|
| 1 | Hero | Maior impacto na taxa de permanência |
| 2 | CTA principal + stack de valor | Maior impacto na taxa de início de checkout |
| 3 | Prova social | Maior impacto na eliminação de ceticismo |
| 4 | Garantia | Maior impacto na taxa de conclusão de checkout |
| 5 | Demais seções | Completam o argumento |

---

## Regras de Qualidade

- Wireframe sem CTA acima da dobra = erro — corrigir antes de entregar
- Desktop desenhado antes do mobile = processo invertido — refazer
- Botão de CTA com cor que aparece em outro elemento = erro de contraste — corrigir
- Seção sem elemento de saída = risco de abandono — adicionar âncora visual
