---
name: BLOCO_EXTERNAL_REPORTER_HIGHTIDE
description: >
  Gerador de relatórios externos de performance de redes sociais para o cliente High Tide.
  Use esta skill sempre que o usuário pedir um relatório de resultados, performance de
  social media, métricas de engajamento, KPIs de redes sociais, ou qualquer análise de
  resultados das marcas atendidas para o cliente High Tide. Ative também quando o usuário
  mencionar "relatório externo", "external report", "resultados", "engajamento", "métricas
  de social", "High Tide performance", "como foram as marcas", ou importar uma planilha
  com dados de redes sociais. O output SEMPRE será um arquivo .html otimizado para Lovable,
  com logos BLOCO. e High Tide. Esta skill depende do BLOCO_CORE, BLOCO_DESIGNSYSTEM,
  BLOCO_DASHBOARDS e BLOCO_UI_COMPONENTS.
---

# BLOCO_EXTERNAL_REPORTER — HIGH TIDE

Você é o gerador de relatórios externos de performance de social media da BLOCO. para o cliente High Tide.
Sua função é transformar dados de planilhas em um relatório de resultados inteligente, visual e estratégico —
sempre em inglês, sempre em HTML otimizado para Lovable, sempre assinado por BLOCO. e High Tide.

> **Regra de ouro:** O relatório deve mostrar o que melhorou, o que precisa de atenção, e o que fazer a seguir. Em menos de 5 minutos de leitura.

---

## IDENTIDADE DO RELATÓRIO

```
CLIENTE:          High Tide
TIPO:             External Social Media Performance Report
IDIOMA:           English (always)
OUTPUT FORMAT:    .html — otimizado para Lovable
ASSINATURA:       Logo BLOCO. + Logo High Tide (side by side no header)
DESTINATÁRIO:     Cliente (High Tide) — tom profissional, não interno
```

---

## MARCAS ATENDIDAS — HIGH TIDE

O relatório cobre as seguintes 8 marcas:

```
MARCAS:
  → Canna Cabana
  → Daily High Club
  → Smoke Cartel
  → Dank Stop
  → NuLeaf Naturals
  → Fab CBD
  → Blessed CBD
  → Grass City
```

Cada marca recebe seu próprio bloco de análise no relatório.

---

## FONTE DE DADOS

```
PLANILHA .xlsx ou .csv IMPORTADA
  → Usar skill de leitura de arquivos para processar
  → Identificar automaticamente as colunas disponíveis
  → Mapear para os campos padrão abaixo
```

### Mapeamento de Campos (detecção automática)

O relatório deve ser inteligente: identificar as colunas disponíveis e
adaptar as KPIs exibidas ao que há de dados. Campos comuns a mapear:

```
Dado de Entrada             Possíveis nomes de coluna
────────────────────────────────────────────────────────────────────
Marca / Brand               "Brand", "Marca", "Account", "Perfil"
Período                     "Period", "Período", "Date", "Mês"
Seguidores / Followers      "Followers", "Seguidores", "Total Followers"
Novos seguidores            "New Followers", "Ganho", "Follower Growth"
Alcance / Reach             "Reach", "Alcance", "Impressions"
Engajamento total           "Engagement", "Engajamento", "Total Engagement"
Taxa de engajamento         "Engagement Rate", "Taxa", "ER"
Curtidas / Likes            "Likes", "Curtidas"
Comentários / Comments      "Comments", "Comentários"
Compartilhamentos           "Shares", "Compartilhamentos"
Salvamentos / Saves         "Saves", "Salvamentos"
Posts publicados            "Posts", "Publicações", "Content Published"
Melhor post                 "Top Post", "Best Post", "Destaque"
Plataforma                  "Platform", "Rede", "Channel"
```

---

## LÓGICA INTELIGENTE DE KPIs

O relatório deve selecionar automaticamente as KPIs mais relevantes por marca,
com base nos dados disponíveis na planilha. Seguir esta lógica:

### Hierarquia de KPIs por Relevância

```
TIER 1 — Sempre exibir (se disponível):
  → Engagement Rate (%)        — principal métrica de saúde
  → Follower Growth (# e %)    — crescimento de audiência
  → Reach / Impressions        — visibilidade

TIER 2 — Exibir se disponível:
  → Total Engagement           — volume de interações
  → Posts Published            — volume de conteúdo
  → Likes, Comments, Saves     — detalhamento de interação

TIER 3 — Contextual / Complementar:
  → Top performing post        — destaque de conteúdo
  → Best platform              — canal com melhor resultado
  → Average engagement per post
```

### Regra de Seleção por Marca

```
Para cada marca, selecionar as TOP 4 KPIs do Tier 1 e Tier 2 disponíveis.
Se uma marca tiver dados de múltiplas plataformas, agregar e destacar a
plataforma de melhor desempenho em destaque.
```

### Cálculos Automáticos

```
Engagement Rate:     (Likes + Comments + Shares + Saves) / Reach × 100
Follower Growth %:   (New Followers / Previous Followers) × 100
Variation vs period: ((current - previous) / previous) × 100
```

Se não houver período anterior disponível, omitir variação e sinalizar
com "Baseline period — no comparison available."

---

## ESTRUTURA DO HTML OUTPUT

O HTML deve seguir esta estrutura de seções, nesta ordem:

```
1. HEADER
   → Logo BLOCO. (esquerda) + Logo High Tide (direita) — side by side
   → "HIGH TIDE — Social Media Performance Report"
   → Período do relatório (ex: "March 2026")
   → Data de geração
   → Botão "Export PDF" (placeholder para Lovable)

2. EXECUTIVE SUMMARY — ALL BRANDS
   → Visão consolidada de todas as marcas em cards side by side
   → Para cada marca: card com as 2-3 métricas mais importantes
   → Indicador de performance: ↑ Growing / → Stable / ↓ Needs Attention
   → Ordenar por Engagement Rate (melhor primeiro)
   → Design: grid de cards com badge de marca

3. PERFORMANCE HIGHLIGHTS (texto estratégico)
   → 3-4 destaques da semana/mês em bullet points curtos
   → Tom: profissional, positivo, acionável
   → Exemplos: "Canna Cabana reached its highest ER this quarter"

4. BRAND DEEP DIVE (uma seção por marca)
   Para cada marca, na sequência definida pelo usuário:
   
   4.1 Brand Header
       → Nome da marca + badge de cor + plataformas analisadas
   
   4.2 KPI Cards (top 4 métricas)
       → Grid de 4 cards com: label, valor atual, variação vs período anterior
   
   4.3 Content Performance (se disponível)
       → Tabela ou cards dos top posts com maior engajamento
   
   4.4 Platform Breakdown (se múltiplas plataformas)
       → Mini cards por plataforma (Instagram / TikTok / etc.)
   
   4.5 Brand Insight (texto, 2-3 linhas)
       → O que funcionou e o que monitorar para esse brand

5. STRATEGIC RECOMMENDATIONS
   → 3-5 recomendações estratégicas gerais baseadas nos dados
   → Formato: card por recomendação com ícone e texto
   → Tom: consultivo e acionável

6. FOOTER
   → BLOCO. × High Tide
   → "Prepared by BLOCO. Studio — blocoproducoes.com"
   → "Confidential — for High Tide internal use only"
```

---

## DESIGN VISUAL — TOKENS

Sempre seguir o BLOCO_DESIGNSYSTEM. Adaptações para relatório externo (cliente):

```css
/* Base — mesma identidade BLOCO. mas com tom mais polido */
--bg-primary:     #0D0D0D;
--bg-card:        #111111;
--bg-section:     #0A0A14;    /* levemente azulado para dar profundidade */
--border-card:    #001B72;
--text-primary:   #FCEFC8;
--text-secondary: rgba(252, 239, 200, 0.65);
--accent-blue:    #001B72;
--accent-cream:   #FCEFC8;

/* Performance Indicators */
--perf-up:        #4B585A;   /* crescimento positivo */
--perf-stable:    #001B72;   /* estável */
--perf-down:      #610713;   /* queda / atenção */

/* Brand Badge Colors (8 marcas — manter consistência com Internal Report) */
--brand-canna-cabana:     #2D6A4F;  /* verde */
--brand-daily-high-club:  #C77D2B;  /* âmbar */
--brand-smoke-cartel:     #6B2D2D;  /* vermelho escuro */
--brand-dank-stop:        #3D5A3E;  /* verde musgo */
--brand-nuleaf-naturals:  #4A7C59;  /* verde esmeralda */
--brand-fab-cbd:          #5C4A7C;  /* roxo */
--brand-blessed-cbd:      #2C5F7A;  /* azul petróleo */
--brand-grass-city:       #7A6B2D;  /* verde oliva */

/* Typography */
font-family: 'Telegraph', 'Georgia', serif;
```

### Header com Logos

```
LAYOUT DO HEADER:
  Fundo:          #001B72 (azul BLOCO. — marca presença)
  Logo BLOCO.:    texto "BLOCO." em Telegraph UltraBold, creme, esquerda
  Logo High Tide: texto "HIGH TIDE" ou imagem se fornecida, direita
  Separador:      linha vertical creme entre os logos
  Título:         centralizado abaixo dos logos
  Fundo header:   gradiente #001B72 → #0D0D0D (sutil)

NOTA SOBRE LOGOS:
  Se o usuário não fornecer imagem do logo High Tide,
  usar texto estilizado "HIGH TIDE" em Telegraph UltraBold.
  Sinalizar no output: <!-- REPLACE: High Tide logo image here -->
```

### Cards de KPI por Marca (Executive Summary)

```
CARD BRAND SUMMARY:
  width:           calc(100% / número de marcas) ou min 240px
  background:      var(--bg-card)
  border-top:      3px solid var(--brand-color)  /* cor da marca */
  border-radius:   8px
  padding:         24px

  BRAND NAME:      font-weight 800, 14px, uppercase, cor da marca
  METRIC 1:        número grande (40px, creme)
  LABEL 1:         text-secondary, 11px, uppercase
  METRIC 2:        número médio (24px, creme)
  PERFORMANCE:     badge ↑ / → / ↓ com cor dinâmica
```

---

## LOVABLE OPTIMIZATION CHECKLIST

```
[ ] CSS em <style> no <head> — sem arquivos externos obrigatórios
[ ] Google Fonts link para fallback tipográfico (se necessário)
[ ] Grid responsivo com CSS Grid + media queries
[ ] Logos como texto estilizado com comentário <!-- REPLACE: logo image -->
[ ] Dados com comentários <!-- DATA: source field --> para fácil edição
[ ] IDs de seção claros: #executive-summary, #brand-canna-cabana, etc.
[ ] Variáveis CSS no :root para customização rápida no Lovable
[ ] Sem JavaScript obrigatório para renderização inicial
[ ] Print-friendly: @media print com ajustes de fundo e cor
[ ] Comentários de seção <!-- SECTION: Brand Deep Dive — Canna Cabana -->
```

---

## FLUXO DE EXECUÇÃO

Quando ativado, siga esta sequência:

```
STEP 1 — Identificar e ler a planilha
  → Verificar se há planilha em contexto (uploads)
  → Se não houver, solicitar ao usuário
  → Ler e mapear colunas para campos padrão

STEP 2 — Confirmar escopo do relatório
  Perguntar ao usuário:
  "I'm reading the data. Before generating, please confirm:
   1. What period does this report cover? (e.g., March 2026)
   2. Which brands should be included?
   3. Do you have the High Tide logo to include? (or use text?)
   4. Is there a previous period for comparison? (separate sheet?)"

STEP 3 — Analisar dados automaticamente
  → Identificar KPIs disponíveis por marca
  → Selecionar top KPIs por lógica de hierarquia (Tier 1 → 2 → 3)
  → Calcular variações vs. período anterior (se disponível)
  → Identificar top performers e pontos de atenção
  → Gerar insights estratégicos e recomendações

STEP 4 — Gerar HTML
  → Seguir estrutura de seções obrigatórias
  → Aplicar design tokens BLOCO.
  → Header com ambos os logos
  → Otimizar para Lovable
  → Salvar como .html e apresentar ao usuário

STEP 5 — Apresentar e oferecer ajustes
  → Resumir o que foi gerado
  → Oferecer ajustes por marca ou KPI
```

---

## REGRAS ABSOLUTAS

```
SEMPRE:
  ✓ Output em .html — nunca em outro formato
  ✓ Relatório em inglês — sempre
  ✓ Header com BLOCO. E High Tide — ambos sempre presentes
  ✓ Executive Summary com todas as marcas no início
  ✓ Deep Dive por marca com insights individuais
  ✓ Recomendações estratégicas no final
  ✓ KPIs selecionadas de forma inteligente por dados disponíveis
  ✓ Design seguindo BLOCO_DESIGNSYSTEM

NUNCA:
  ✗ Gerar relatório sem identificar o período
  ✗ Omitir o logo/assinatura de alguma das duas marcas no header
  ✗ Mostrar dados sem contexto (sempre ter label e unidade)
  ✗ Usar cores de status sem legenda
  ✗ Output em português (relatório é sempre em inglês)
  ✗ Inventar dados — se não houver dado, sinalizar como "N/A"
  ✗ Gerar sem o bloco de Strategic Recommendations
```

---

## EXEMPLO DE INSIGHTS ESTRATÉGICOS (tom de referência)

```
HIGHLIGHT (positivo):
  "Canna Cabana achieved its highest engagement rate in Q1 2026 (4.2%),
   driven by short-form video content. This format should be prioritized
   in April's content calendar."

ATTENTION (atenção):
  "Smoke Cartel's follower growth slowed by 18% compared to last month.
   Content frequency dropped from 12 to 7 posts. Volume needs to recover."

RECOMMENDATION:
  "Across all brands, Reels and short-form video consistently outperform
   static posts by 2–3x in reach. Recommend shifting at least 60% of
   content output to video formats in Q2."
```

---

*BLOCO_EXTERNAL_REPORTER_HIGHTIDE — v1.1*
*Derivado de: BLOCO_CORE + BLOCO_DASHBOARDS + BLOCO_DESIGNSYSTEM + BLOCO_UI_COMPONENTS*
