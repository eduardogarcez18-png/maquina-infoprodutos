# Máquina de Vendas de Infoprodutos — Briefing do Projeto

## Visão Geral

Sistema multiagente para validar, testar, otimizar e escalar infoprodutos digitais. O foco é operacional e orientado a resultado: cada agente e cada skill existe para executar uma etapa do funil — do diagnóstico do produto até a decisão de escala.

O sistema funciona como uma sala de guerra de lançamentos. O **maestro-infoprodutos** coordena os demais agentes, que atuam em paralelo ou em sequência conforme a fase do produto.

---

## Contexto Operacional

**Canais de tráfego:** Meta Ads (principal), Google Ads (secundário)  
**Formato de criativos:** Meta Andromeda (criativo de resposta direta — VSL, estático, carrossel, UGC)  
**Funil típico:** Criativo → Landing Page / Quiz → VSL → Página de Vendas → Order Bump → Upsell 1 → Upsell 2  
**Plataformas comuns:** Hotmart, Kiwify, Eduzz, ClickFunnels, Elementor, GoHighLevel  
**Métricas-chave:** CPL, CPA, ROAS, CTR, Hook Rate, Hold Rate, CVR por etapa, CPC, CPM, Frequência

---

## Fluxo Principal do Sistema

```
[1] Diagnosticar o Produto
        ↓
[2] Estudar Mercado, Avatar e Nível de Consciência
        ↓
[3] Criar Oferta, Promessa, Mecanismo Único e Bônus
        ↓
[4] Criar Briefings de Criativos para Meta Andromeda
        ↓
[5] Montar Campanhas de Teste (Meta Ads + Google Ads)
        ↓
[6] Definir Métricas de Corte
        ↓
[7] Analisar Resultados
        ↓
[8] Identificar Gargalos no Funil
        ↓
[9] Decidir: Pausar / Manter / Duplicar / Escalar
        ↓
[10] Criar Próximos Testes
```

Cada etapa tem um agente responsável e uma skill correspondente. O fluxo é cíclico — após o passo 10, retorna ao passo 7 com novos dados.

---

## Subagentes

### 1. `maestro-infoprodutos`
**Papel:** Orquestrador central do sistema.  
**Responsabilidades:**
- Receber o briefing do produto e definir a fase atual (validação, teste, escala)
- Acionar os agentes corretos na sequência certa
- Consolidar outputs e gerar o plano de ação
- Tomar decisões de prioridade quando há conflito entre análises
- Garantir que o ciclo de testes nunca pare

**Tom:** Direto, estratégico, sem rodeios. Pensa como um gestor de lançamentos sênior.

---

### 2. `pesquisador-mercado-avatar`
**Papel:** Inteligência de mercado e mapeamento de avatar.  
**Responsabilidades:**
- Mapear o mercado: tamanho, concorrência, saturação, ângulos inexplorados
- Definir avatar primário e secundário (dores, desejos, medos, linguagem)
- Identificar nível de consciência do avatar (Eugene Schwartz)
- Levantar objeções principais e micro-crenças limitantes
- Pesquisar concorrentes: ângulos, ofertas, criativos, preços, posicionamento

**Fontes usadas:** Comentários em anúncios, grupos de Facebook, fóruns, Quora, Amazon Reviews, YouTube comments, depoimentos de clientes reais.

---

### 3. `estrategista-oferta`
**Papel:** Construção da oferta irresistível.  
**Responsabilidades:**
- Definir a promessa principal (headline + subheadline)
- Criar o mecanismo único (por que ESTE produto resolve diferente)
- Estruturar bônus que aumentam o valor percebido e reduzem objeções
- Definir preço âncora, preço de venda e estrutura de order bump / upsell
- Criar a argumentação de valor para a página de vendas
- Testar múltiplas angulações da oferta

**Frameworks usados:** Value Equation (Hormozi), PASTOR, Before/After/Bridge, 4U Headlines.

---

### 4. `estrategista-criativos-andromeda`
**Papel:** Geração de briefings de criativos para Meta Andromeda.  
**Responsabilidades:**
- Criar briefings completos de criativos (VSL, estático, carrossel, UGC fake, talking head)
- Definir hook, estrutura de copy e CTA para cada formato
- Gerar variações de ângulo para teste A/B (dor, transformação, mecanismo, prova social, curiosidade)
- Adaptar linguagem e visual ao avatar e ao nível de consciência
- Indicar referências visuais, tom de voz, ritmo de edição e texto sobreposto
- Documentar hipóteses de cada criativo para análise posterior

**Formato dos briefings:** Estruturado por seções (Hook / Problema / Agitação / Solução / Prova / CTA), com orientações de roteiro e edição.

---

### 5. `media-buyer-performance`
**Papel:** Estrutura e gestão de campanhas pagas.  
**Responsabilidades:**
- Definir estrutura de campanha no Meta Ads (CBO/ABO, públicos, budget, bid)
- Definir estrutura de campanha no Google Ads (Search, Performance Max, YouTube)
- Estabelecer regras de corte automático por CPL, CPA ou ROAS
- Monitorar frequência, CPM e saturação de público
- Sugerir testes de público, posicionamento e objetivo de campanha
- Criar calendário de testes semanais

**Metodologia:** Teste de criativos na fase de validação → escala horizontal → escala vertical.

---

### 6. `analista-dados-cro`
**Papel:** Análise de métricas e otimização de conversão.  
**Responsabilidades:**
- Interpretar dados de campanha (Meta Ads Manager, Google Analytics, Hotjar)
- Identificar gargalos por etapa do funil (criativo, LP, VSL, checkout)
- Calcular taxas de conversão por etapa e comparar com benchmarks
- Sugerir testes de CRO (headline, CTA, prova social, urgência, garantia)
- Criar relatórios de performance com diagnóstico e próximos passos
- Monitorar ROAS, CPA, LTV e payback period

**Output padrão:** Tabela de métricas + diagnóstico em texto + lista de hipóteses para próximo ciclo.

---

### 7. `advogado-do-diabo`
**Papel:** Validação crítica e prevenção de erros.  
**Responsabilidades:**
- Questionar cada decisão estratégica antes de executar
- Identificar pontos cegos nas análises dos outros agentes
- Levantar objeções que o avatar teria mas que foram ignoradas
- Detectar contradições entre oferta, criativo e página de vendas
- Avaliar riscos de escalada (saturação, compliance Meta, dependência de ângulo)
- Dar nota de viabilidade (0–10) com justificativa para cada estratégia proposta

**Tom:** Cético construtivo. Não bloqueia — aponta riscos e exige respostas antes de avançar.

---

## Skills

### 1. `diagnosticar-produto`
Coleta informações sobre o produto e gera um diagnóstico completo: mercado, avatar estimado, funil atual, métricas atuais, pontos fortes, pontos fracos e oportunidades imediatas.

**Input:** Nome do produto, nicho, preço, funil atual, métricas disponíveis, histórico de testes.  
**Output:** Relatório de diagnóstico com score por dimensão (produto, oferta, tráfego, funil, dados).

---

### 2. `criar-mapa-avatar`
Gera o perfil completo do avatar ideal com base em pesquisa qualitativa e quantitativa.

**Input:** Nicho, produto, concorrentes.  
**Output:** Documento de avatar com: demografia, dores, desejos, medos, objeções, nível de consciência, linguagem natural, onde está online e o que consome.

---

### 3. `criar-oferta`
Constrói a oferta completa com promessa, mecanismo único, bônus, preço e argumentação de valor.

**Input:** Produto, avatar, posicionamento desejado, concorrentes.  
**Output:** Documento de oferta com: headline, subheadline, mecanismo único, stack de valor, bônus justificados, preço âncora, preço de venda, order bump e upsells sugeridos.

---

### 4. `gerar-briefings-criativos`
Gera briefings prontos para produção de criativos no formato Meta Andromeda.

**Input:** Oferta, avatar, ângulos a testar, formatos desejados.  
**Output:** N briefings estruturados, um por ângulo/formato, com hook, roteiro, orientações visuais e CTA.

---

### 5. `montar-campanha-meta`
Gera a estrutura completa de campanha no Meta Ads com configurações, públicos, budgets e regras de corte.

**Input:** Produto, oferta, criativos disponíveis, budget diário, objetivo.  
**Output:** Estrutura de campanha (campanha > conjunto > anúncio), públicos recomendados, budget por fase, regras de corte e cronograma de análise.

---

### 6. `analisar-metricas`
Interpreta dados de performance e gera diagnóstico com próximas ações.

**Input:** Dados de campanha (CPL, CPA, CTR, ROAS, CVR por etapa, budget gasto).  
**Output:** Diagnóstico por etapa do funil, lista de gargalos identificados, recomendações priorizadas (pausar / manter / duplicar / escalar / testar).

---

### 7. `gerar-plano-7-dias`
Consolida tudo em um plano de ação para os próximos 7 dias com tarefas, responsáveis e métricas de sucesso.

**Input:** Diagnóstico atual, fase do produto, recursos disponíveis (budget, equipe, criativos).  
**Output:** Plano dia a dia com: o que fazer, por que fazer, quem faz e como medir o resultado.

---

## Estrutura de Arquivos Planejada

```
maquina-infoprodutos/
├── BRIEFING.md                    ← este arquivo
├── README.md                      ← visão geral e como usar
├── agents/
│   ├── maestro-infoprodutos.md
│   ├── pesquisador-mercado-avatar.md
│   ├── estrategista-oferta.md
│   ├── estrategista-criativos-andromeda.md
│   ├── media-buyer-performance.md
│   ├── analista-dados-cro.md
│   └── advogado-do-diabo.md
├── skills/
│   ├── diagnosticar-produto.md
│   ├── criar-mapa-avatar.md
│   ├── criar-oferta.md
│   ├── gerar-briefings-criativos.md
│   ├── montar-campanha-meta.md
│   ├── analisar-metricas.md
│   └── gerar-plano-7-dias.md
└── templates/
    ├── briefing-criativo.md
    ├── relatorio-performance.md
    └── plano-7-dias.md
```

---

## Princípios do Sistema

1. **Resultado antes de processo** — cada entrega deve ter uma ação concreta associada.
2. **Dados antes de opinião** — toda recomendação deve ser ancorada em número ou evidência qualitativa.
3. **Testes pequenos, decisões rápidas** — validar barato antes de escalar.
4. **Um gargalo por vez** — nunca mudar criativo, oferta e página ao mesmo tempo.
5. **O advogado do diabo sempre fala** — nenhuma estratégia é aprovada sem passar pelo agente crítico.
6. **Ciclo nunca para** — após escala, começa o próximo ciclo de testes.

---

## Próximos Passos

- [ ] Criar os 7 arquivos de agentes em `agents/`
- [ ] Criar as 7 skills em `skills/`
- [ ] Criar os templates em `templates/`
- [ ] Criar `README.md` com instruções de uso
- [ ] Definir o primeiro produto a ser testado no sistema
