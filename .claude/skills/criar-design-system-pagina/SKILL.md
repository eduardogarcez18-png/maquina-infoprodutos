---
name: criar-design-system-pagina
description: Processo para criar um sistema de design simples e funcional para páginas de vendas de infoprodutos — paleta, tipografia, botões, cards, seções, espaçamento e estilo visual. Foco em consistência e velocidade de produção, não em originalidade estética.
---

# Skill: Criar Design System de Página de Vendas

## Quando usar

Acionar quando:
- A página de vendas está sendo construída do zero e não há identidade visual definida
- A página existe mas tem inconsistência visual que prejudica a percepção de valor
- Múltiplas páginas precisam de consistência visual (produto principal + upsell + downsell)

**Não acionar** para redesign completo de marca — este sistema é específico para páginas de vendas de infoprodutos.

---

## Input Necessário

| Campo | Obrigatório | Descrição |
|---|---|---|
| Produto e nicho | Sim | Para calibrar tom visual e paleta |
| Avatar principal | Sim | Para calibrar linguagem visual (jovem/formal, técnico/emocional) |
| Formato da página | Sim | Direta / VSL / quiz / advertorial |
| Referência visual | Não | URL de página de vendas no mesmo nicho que o usuário admira |
| Cor de marca existente | Não | Se já há identidade estabelecida |

---

## Processo

### Passo 1 — Definir o tom visual

Antes de definir cores, definir o tom visual baseado no nicho e avatar:

| Nicho | Tom recomendado | Evitar |
|---|---|---|
| Hobbies / entretenimento (anime, jogos, arte) | Energético, cores saturadas, informal | Corporativo, frio, monocromático |
| Saúde / bem-estar | Limpo, cores frias (verde/azul), confiável | Agressivo, vermelho intenso |
| Dinheiro / renda extra | Profissional mas acessível, verde escuro ou azul | Dourado excessivo, visual de "fica rico rápido" |
| Educação / habilidades profissionais | Neutro, tipografia clara, azul ou cinza | Infantil, fontes decorativas |
| Culinária / lifestyle | Quente, aconchegante, terracota/amarelo | Frio, industrial |

---

### Passo 2 — Definir a paleta

Um sistema de design de página de vendas precisa de exatamente 5 cores:

```
PALETA DE PÁGINA DE VENDAS

1. COR PRINCIPAL (Brand)
   Uso: headlines, elementos de identidade
   Frequência: média — não em todo elemento
   
2. COR DE CTA (Call to Action)
   Uso: SOMENTE nos botões de compra/ação
   Regra: não pode aparecer em nenhum outro elemento da página
   Frequência: máxima visibilidade, mínima ocorrência
   
3. COR DE FUNDO PRIMÁRIA
   Uso: fundo da maioria das seções
   Padrão: #FFFFFF (branco) ou #F8F8F8 (off-white)
   
4. COR DE FUNDO SECUNDÁRIA
   Uso: seções alternadas para criar respiração visual
   Padrão: #F0F0F0 ou variação da cor principal em 5% de opacidade
   
5. COR DE TEXTO
   Uso: corpo e headlines
   Padrão: #111111 (quase preto) para máxima legibilidade
```

**Regra do CTA:** a cor do CTA deve ter contraste de pelo menos 4.5:1 com o fundo do botão para acessibilidade e deve ser a cor mais chamativa da página.

---

### Passo 3 — Definir tipografia

**Regra: máximo 2 famílias tipográficas na mesma página.**

```
TIPOGRAFIA

FAMÍLIA 1 — Headlines
Família: [Sans-serif pesada]
Peso: Bold (700) ou ExtraBold (800)
Uso: H1, H2, subtítulos de seção
Tamanho mobile: H1=28–32px / H2=22–26px
Tamanho desktop: H1=40–48px / H2=30–36px
Sugestões: Inter, Montserrat, Raleway, Poppins

FAMÍLIA 2 — Corpo
Família: [Sans-serif regular de alta legibilidade]
Peso: Regular (400) e Bold (700) apenas
Uso: corpo de texto, bullets, FAQs, depoimentos
Tamanho mobile: 16px
Tamanho desktop: 17–18px
Sugestões: Inter, Open Sans, Lato

REGRA: se usar Inter para headlines, usar Inter para corpo também (mesma família, pesos diferentes). Duas famílias somente se há contraste de propósito visual claro.
```

---

### Passo 4 — Definir sistema de botões

```
SISTEMA DE BOTÕES

BOTÃO CTA (primário)
Cor de fundo: [COR DE CTA]
Cor do texto: [contraste máximo — geralmente branco ou preto]
Padding: 18px vertical / 32px horizontal
Border-radius: 6–8px
Tamanho de fonte: 16–18px, Bold
Texto: Title Case ou MAIÚSCULO
Estado hover: 10% mais escuro que a cor base
Largura mobile: 100% (largura total)
Largura desktop: automático com padding

BOTÃO SECUNDÁRIO (quando necessário)
Uso: ação menos importante ("ver mais depoimentos", "ver o que está incluído")
Estilo: outline com cor principal ou texto com seta →
Nunca competir visualmente com o CTA primário

MICRO-JUSTIFICATIVA (abaixo do CTA)
Texto: "[Ícone de cadeado] Pagamento seguro" ou "Garantia de [X] dias"
Tamanho: 12–14px
Cor: cinza médio (#666666)
```

---

### Passo 5 — Definir cards e boxes

```
SISTEMA DE CARDS

CARD DE DEPOIMENTO
Fundo: #FFFFFF com borda #E0E0E0 (1px)
Sombra: 0 2px 8px rgba(0,0,0,0.08)
Padding: 24px
Border-radius: 8–12px
Foto do avatar: 60–80px, circular
Nome: Bold, cor de texto principal
Cargo/localização: Regular, cinza médio
Texto do depoimento: Regular, itálico, tamanho normal
Aspas: elemento decorativo, cor principal em 20% opacidade

CARD DE BÔNUS / COMPONENTE DO PRODUTO
Fundo: fundo secundário ou cor principal em 5% opacidade
Borda esquerda: 4px sólida na cor principal (acento)
Padding: 20px 24px
Ícone: 32px, cor principal
Título: Bold, cor principal
Descrição: Regular, cor de texto
Valor: negrito, cor principal, com "De: R$ X" riscado

BOX DE DESTAQUE (mecanismo único, garantia, urgência)
Fundo: cor principal em 10% opacidade ou fundo secundário
Borda: 2px sólida na cor principal
Border-radius: 8px
Padding: 24–32px
Ícone grande: 48px centralizado (opcional)
```

---

### Passo 6 — Definir espaçamento e ritmo

```
SISTEMA DE ESPAÇAMENTO

Entre seções: 64–80px (mobile) / 96–120px (desktop)
Dentro de seção — elementos: 24–32px
Entre bullets: 12–16px
Entre headline e subheadline: 16px
Entre subheadline e corpo: 24px
Entre corpo e CTA: 32–40px

LARGURA MÁXIMA DE CONTEÚDO
Mobile: 100% com 16–20px de padding lateral
Desktop: 760–900px centralizado (não esticar copy para 1200px)

REGRA: text-align center em mobile para heroes e CTAs. Text-align left para corpos longos de texto (acima de 3 linhas).
```

---

### Passo 7 — Definir estilo visual de seções

```
ALTERNÂNCIA DE SEÇÕES

Seção clara → Seção escura (ou fundo alternado)
Evitar 3 seções com o mesmo fundo em sequência — cria monotonia

PADRÃO RECOMENDADO:
1. Hero: fundo branco ou gradiente leve
2. Problema: fundo branco
3. Causa raiz: fundo secundário (#F5F5F5)
4. Mecanismo: fundo com cor principal em 8% opacidade
5. Produto: fundo branco
6. Stack de valor: fundo secundário
7. Prova social: fundo branco
8. Autoridade: fundo escuro (cor principal em versão escura) com texto branco
9. Oferta e preço: fundo branco com box de destaque
10. Garantia: fundo verde claro ou cor de confiança
11. FAQ: fundo branco com acordeão
12. CTA final: fundo cor principal com texto branco
```

---

## Output

### Entrega — Design System Completo

```
## Design System — [Nome do produto]

---

### 1. Tom visual
[Descrição em 1 parágrafo]

---

### 2. Paleta

| Token | Cor | Hex | Uso |
|---|---|---|---|
| brand-primary | [nome] | #XXXXXX | Headlines, identidade |
| cta | [nome] | #XXXXXX | SOMENTE botões de ação |
| bg-primary | Branco | #FFFFFF | Fundo principal |
| bg-secondary | Off-white | #F5F5F5 | Seções alternadas |
| text-primary | Quase preto | #111111 | Corpo e títulos |

---

### 3. Tipografia

| Elemento | Família | Peso | Mobile | Desktop |
|---|---|---|---|---|
| H1 | [família] | Bold 700 | 28px | 40px |
| H2 | [família] | Bold 700 | 22px | 30px |
| Corpo | [família] | Regular 400 | 16px | 17px |
| CTA | [família] | Bold 700 | 16px | 16px |

---

### 4. Botão CTA

Cor: #XXXXXX
Texto: #XXXXXX
Padding: 18px 32px
Border-radius: 8px
Largura mobile: 100%

---

### 5. Cards

[Especificações de cada card — depoimento, bônus, box de destaque]

---

### 6. Espaçamento

[Tabela de espaçamento entre elementos e seções]

---

### 7. Sequência de seções

[Ordem das seções com fundo de cada uma]

---
```

---

## Regras de Qualidade

- Cor de CTA repetida em outro elemento = erro — o CTA precisa ser único na página
- Mais de 2 famílias tipográficas = poluição visual — reduzir para 2 máximo
- Seções sem alternância de fundo = página monótona — adicionar variação a cada 2 seções
- Fonte menor que 16px no corpo mobile = problema de leitura — corrigir
- Botão de CTA com largura pequena em mobile = baixa taxa de clique — usar 100% de largura
