---
name: criar-copy-pagina-vendas
description: Processo passo a passo para escrever copy completa de uma página de vendas de infoproduto — da hero section ao CTA final, com todas as seções obrigatórias, tratamento de objeções e congruência com o criativo de tráfego.
---

# Skill: Criar Copy de Página de Vendas

## Quando usar

Acionar quando:
- A oferta e o avatar já estão definidos
- O produto tem criativo de tráfego pronto (ou ao menos ângulo definido)
- A página de vendas ainda não existe ou não está convertendo

**Não acionar** se a oferta ainda não foi estruturada — o output de `criar-oferta` é input obrigatório desta skill.

---

## Input Necessário

| Campo | Obrigatório | Descrição |
|---|---|---|
| Oferta completa | Sim | Promessa, mecanismo único nomeado, stack de valor, preço, bônus, garantia |
| Avatar mapeado | Sim | Dores, desejos, objeções, linguagem natural, nível de consciência |
| Copy do criativo | Sim | Hook e promessa do anúncio que gerará o clique |
| Formato da página | Sim | Direta / VSL / quiz / advertorial |
| Nome e credenciais do criador | Sim | Para seção de autoridade |
| Produto | Sim | Nome, o que inclui, formato de entrega (PDF, vídeo, acesso em plataforma) |
| Depoimentos disponíveis | Não | Resultados reais de clientes — se houver |
| CPA meta | Não | Para calibrar intensidade de urgência e construção de valor |

---

## Processo

### Passo 1 — Auditar congruência com o criativo

Antes de escrever uma linha, identificar:
- Qual é a promessa exata do anúncio que trará o avatar?
- Qual é o nível de consciência do avatar no momento do clique?
- O avatar chegará quente (retargeting) ou frio (topo de funil)?

**Regra:** o primeiro headline da página deve ser a continuação direta da promessa do criativo. Se o avatar viu "aprenda a desenhar Dragon Ball em 7 dias" no anúncio, a página abre com essa promessa — não com outra.

---

### Passo 2 — Mapear as 3 objeções principais

Antes de escrever, listar as 3 objeções que impedem o avatar de comprar. Exemplos:

| Objeção | Tipo |
|---|---|
| "Não tenho talento para isso" | Crença limitante |
| "Já tentei outros cursos e não funcionou" | Ceticismo por experiência |
| "R$ [preço] é caro para mim agora" | Objeção de preço |
| "Não tenho tempo" | Objeção de condição |
| "Não sei se isso funciona para mim" | Objeção de aplicabilidade |

Cada objeção será tratada em uma seção específica da página — não concentrada no FAQ.

---

### Passo 3 — Construir a sequência de seções

#### Seção 1 — Hero

**Função:** capturar atenção, confirmar que o avatar está no lugar certo, segurar na página

**Elementos obrigatórios:**
- Headline principal (H1): promessa específica com prazo e ponto de partida
- Subheadline: ampliar a promessa ou endereçar a maior objeção imediata
- CTA acima da dobra: botão com texto de ação, não de submissão ("Quero aprender" > "Comprar")
- Elemento de prova visual: número de alunos, avaliação, ou imagem de resultado

**Modelo de headline:**
> "[Resultado específico] em [prazo] — mesmo que [limitação do avatar]"

**Exemplo:**
> "Aprenda a desenhar qualquer personagem de Dragon Ball do zero em 7 dias — mesmo que nunca tenha desenhado nada na vida"

---

#### Seção 2 — Agitação do problema

**Função:** aprofundar a dor antes de oferecer solução — o avatar precisa sentir o problema para querer a solução

**Estrutura:**
- Começar com identificação: "Se você já tentou [ação do avatar] e ficou frustrado com [resultado]..."
- Listar as situações específicas de dor — não genéricas
- Não oferecer solução ainda
- Fechar a seção com a pergunta implícita: "Por que isso acontece?"

---

#### Seção 3 — Causa raiz (Por que não funcionou antes)

**Função:** explicar por que o avatar ainda não resolveu o problema — e preparar para a apresentação do mecanismo único

**Estrutura:**
- Identificar o método convencional que o avatar já tentou
- Explicar por que esse método não funciona (sem atacar nomes ou produtos)
- Criar contraste: "A maioria ensina X. O problema é que X não resolve Y porque..."
- Terminar com a transição para o mecanismo único

---

#### Seção 4 — Mecanismo único

**Função:** apresentar a solução de forma diferenciada, criar curiosidade sobre o método

**Estrutura:**
- Nome do mecanismo único (criado em `criar-oferta`)
- Como funciona em 3 passos simples
- Por que é diferente do que o avatar já tentou
- Resultado que esse mecanismo entrega

---

#### Seção 5 — Apresentação do produto

**Função:** revelar o produto como a implementação prática do mecanismo único

**Estrutura:**
- Nome do produto
- O que está incluído (lista visual de módulos ou seções)
- Formato e acesso (como o avatar receberá)
- Para quem é — e para quem não é (qualificação)

---

#### Seção 6 — Stack de valor

**Função:** construir valor percebido antes de revelar o preço

**Estrutura:**
- Listar cada componente com nome e âncora de preço individual
- Somar o valor total antes do desconto
- Não revelar o preço final ainda

**Exemplo:**
> - Módulo Principal: [nome] — Valor: R$ 97
> - Bônus 1: [nome] — Valor: R$ 47
> - Bônus 2: [nome] — Valor: R$ 37
> **Total se vendido separado: R$ 181**

---

#### Seção 7 — Prova social

**Função:** eliminar ceticismo com resultados reais de pessoas parecidas com o avatar

**Estrutura:**
- Depoimentos com foto, nome e resultado específico
- Priorizar depoimentos que tratam as objeções identificadas no Passo 2
- Se não há depoimentos: usar resultado do próprio criador como prova inicial

---

#### Seção 8 — Autoridade do criador

**Função:** justificar por que o criador pode ensinar isso

**Estrutura:**
- Resultado próprio (não credencial acadêmica, resultado prático)
- Número de alunos ou tempo de experiência
- Conexão com o avatar: "Eu era exatamente você antes de..."

---

#### Seção 9 — Oferta e preço

**Função:** revelar o preço após construção completa de valor

**Estrutura:**
- Revisitar o stack de valor com o total
- Revelar o preço com contraste: "Por tudo isso, não R$ 181, não R$ 97..."
- Prazo ou escassez legítima se houver
- CTA principal com botão

---

#### Seção 10 — Garantia

**Função:** remover o risco de decisão — tornar o não-comprar a pior escolha

**Estrutura:**
- Prazo da garantia (7, 14 ou 30 dias)
- Condições claras e simples
- Inverter o risco: "Se não gostar, eu devolvo. O risco é meu, não seu."

---

#### Seção 11 — FAQ

**Função:** tratar objeções finais que ainda impedem o clique

**Estrutura:**
- 5–7 perguntas que representam as últimas objeções reais do avatar
- Respostas diretas, sem evasão
- Não repetir o que já foi tratado nas seções anteriores

---

#### Seção 12 — CTA final

**Função:** fechar com a promessa e urgência

**Estrutura:**
- Retomar a promessa principal em uma frase
- CTA com texto de ação e micro-justificativa para agir agora
- Lembrete de garantia como redutor de fricção final

---

### Passo 4 — Revisar por objeções

Após escrever todas as seções, revisar o mapa de objeções do Passo 2:
- Objeção 1 tratada em qual seção?
- Objeção 2 tratada em qual seção?
- Objeção 3 tratada em qual seção?

Se alguma objeção não foi tratada, adicionar na seção mais adequada ou no FAQ.

---

### Passo 5 — Revisar escaneabilidade

A página será lida em escaneamento, não de forma linear. Verificar:
- Subtítulos em cada seção comunicam a promessa sem precisar ler o corpo?
- Bullets estão nos pontos mais importantes, não em listas genéricas?
- Negritos estão nas 3–5 palavras mais importantes de cada parágrafo?
- CTAs têm texto de ação, não de submissão?

---

## Output

### Entrega obrigatória

1. Copy completa por seção com anotações de função e notas de produção
2. Mapa de objeções com indicação de onde cada uma foi tratada
3. 3 variações de CTA principal para teste A/B
4. Headline alternativa para teste A/B

### Formato de entrega por seção

```
## [Nome da seção]

**Função:** [o que esta seção faz]
**Objeção tratada:** [se aplicável]

---

[COPY]

---

**Nota de produção:** [orientação para o designer]
```

---

## Regras de Qualidade

- Copy sem promessa específica na hero = incompleto — reescrever
- Mecanismo único sem nome = incompleto — nomear antes de descrever
- Preço revelado antes da seção 9 = erro de sequência — corrigir
- FAQ com objeções que já foram tratadas nas seções anteriores = desperdício — remover e substituir
- CTA sem micro-justificativa para agir agora = CTA fraco — adicionar razão
