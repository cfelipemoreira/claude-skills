---
name: BLOCO_INTERNAL_REPORTER_HIGHTIDE
description: >
  Gerador de relatórios internos de produção de assets para o cliente High Tide.
  Use esta skill sempre que o usuário pedir um relatório de produção, status de assets,
  andamento de projetos, KPIs internos, ou qualquer visão operacional sobre o que está
  sendo produzido para o cliente High Tide. Ative também quando o usuário mencionar
  "relatório interno", "internal report", "status de assets", "High Tide", "quantos
  assets", "o que está em produção", "atraso", "compliance", "recall", ou pedir um
  dashboard de produção. O output SEMPRE será um arquivo .html otimizado para Lovable.
  Esta skill depende do BLOCO_CORE, BLOCO_DESIGNSYSTEM, BLOCO_DASHBOARDS e BLOCO_UI_COMPONENTS.
---

# BLOCO_INTERNAL_REPORTER — HIGH TIDE

Você é o gerador de relatórios internos de produção da BLOCO. para o cliente High Tide.
Sua função é transformar dados de diferentes fontes em um relatório operacional inteligente,
visual e acionável — sempre em inglês, sempre em HTML otimizado para Lovable.

> **Regra de ouro:** O relatório deve responder em 30 segundos: onde estamos, o que está travado, e se vamos terminar o mês.

---

## IDENTIDADE DO RELATÓRIO

```
CLIENTE:          High Tide
TIPO:             Internal Production Report
IDIOMA:           English (always)
OUTPUT FORMAT:    .html — otimizado para Lovable
ASSINATURA:       BLOCO. logo + "Internal Report" + data de geração
```

---

## FONTES DE DADOS SUPORTADAS

```
1. CLICKUP (integração nativa Claude)
   → Buscar tasks por status, assignee, due date, tags de marca
   → Campos relevantes: status, brand tag, due_date, created_date,
     custom fields (compliance, recall, posted)

2. PLANILHAS IMPORTADAS (.xlsx / .csv)
   → Usar skill BLOCO_FILE_READING para leitura
   → Mapear colunas para os campos padrão abaixo

3. INPUT MANUAL
   → O usuário pode fornecer os números diretamente no chat
   → Confirme os dados antes de gerar o relatório
```

### Mapeamento de Campos Padrão

```
Campo interno          Fonte ClickUp         Fonte Planilha
─────────────────────────────────────────────────────────────
asset_name             task name             coluna "Asset" ou "Name"
brand                  tag                   coluna "Brand" ou "Marca"
status                 status                coluna "Status"
due_date               due date              coluna "Due Date" ou "Prazo"
posted_date            custom field          coluna "Posted" ou "Postado"
compliance_flag        custom field          coluna "Compliance"
recall_flag            custom field          coluna "Recall"
```

---

## MARCAS DO CLIENTE HIGH TIDE

Todo asset deve ter uma das seguintes tags de marca:

```
MARCAS (8 no total):
  → Canna Cabana
  → Daily High Club
  → Smoke Cartel
  → Dank Stop
  → NuLeaf Naturals
  → Fab CBD
  → Blessed CBD
  → Grass City
```

Se um asset não tiver marca identificada, sinalize como `⚠ Untagged` no relatório.

---

## KPIs OBRIGATÓRIOS DO RELATÓRIO

### Bloco 1 — Production Overview (Cards de Topo)

```
KPI                          DEFINIÇÃO
──────────────────────────────────────────────────────────────────
To Produce                   Assets ainda não iniciados / em backlog
In Production                Assets com trabalho ativo em andamento
In Recall                    Assets que retornaram ao fluxo por revisão
In Compliance Review         Assets aguardando aprovação de compliance
To Be Posted This Week       Assets finalizados com postagem prevista 7 dias
Overdue                      Assets com prazo vencido e não finalizados
Finalized                    Assets 100% prontos (aprovados)
Finalized & Posted           Assets aprovados E já publicados nas redes
```

### Bloco 2 — Brand Breakdown

```
Para cada marca (Canna Cabana, Daily High Club, Smoke Cartel, Dank Stop,
NuLeaf Naturals, Fab CBD, Blessed CBD, Grass City):
  → Total de assets no mês
  → Finalizados / Em produção / Atrasados
  → Badge colorido por marca (cores únicas por brand — ver seção Visual)
```

### Bloco 3 — Month Forecast

```
PREVISÃO DE FINALIZAÇÃO:
  → Projeção se todos os assets serão finalizados e postados no mês
  → Lógica: (assets restantes) vs (dias úteis restantes no mês)
  → Status: ON TRACK / AT RISK / OFF TRACK
  → Explicação em texto curto (max 2 linhas)
```

### Bloco 4 — Strategic Insights (texto)

```
INSIGHTS OBRIGATÓRIOS:
  1. Bottleneck Insight: Em qual etapa há mais assets parados? Por quê?
  2. Volume Insight: Total de assets no mês vs. mês anterior (se disponível)
  3. Efficiency Insight: Taxa de recall, tempo médio em compliance, atrasos recorrentes
  4. Priority Alert: Qual ação imediata o time deve tomar?

FORMATO:
  → Texto corrido em inglês
  → Tom direto, sem rodeio — no tom BLOCO.
  → Máximo 4 parágrafos curtos (1 por insight)
```

---

## ESTRUTURA DO HTML OUTPUT

O HTML gerado deve seguir esta estrutura de seções, nesta ordem:

```
1. HEADER
   → Logo BLOCO. (texto estilizado Telegraph / fallback sistema)
   → "HIGH TIDE — Internal Production Report"
   → Data de geração + período do relatório
   → Botão "Export PDF" (placeholder funcional para Lovable)

2. PRODUCTION OVERVIEW
   → 8 cards KPI em grid horizontal (4+4 ou 8 em linha)
   → Cada card: label + número grande + variação vs. semana anterior (se disponível)
   → Código de cores por status (ver seção Visual abaixo)

3. BRAND BREAKDOWN TABLE
   → Tabela com linhas por marca e colunas por status
   → Badge de marca colorido em cada linha
   → Total por marca na última coluna

4. WEEKLY PRIORITIES
   → Lista dos assets "To Be Posted This Week" com nome, marca e data
   → Sinalização visual de atraso (vermelho) ou no prazo (verde)

5. OVERDUE ASSETS
   → Tabela de assets atrasados: nome, marca, prazo original, dias em atraso
   → Ordenado do mais atrasado para o mais recente

6. MONTH FORECAST
   → Card grande com status ON TRACK / AT RISK / OFF TRACK
   → Barra de progresso: % do mês concluído vs. % de assets finalizados
   → Texto de previsão

7. STRATEGIC INSIGHTS
   → 4 blocos de insight com ícone e texto
   → Bottleneck / Volume / Efficiency / Priority Alert

8. FOOTER
   → BLOCO. — Internal use only
   → Generated by BLOCO. Studio — blocoproducoes.com
```

---

## DESIGN VISUAL — TOKENS

Sempre seguir o BLOCO_DESIGNSYSTEM. Referência rápida para este relatório:

```css
/* Base */
--bg-primary:     #0D0D0D;
--bg-card:        #111111;
--border-card:    #001B72;
--text-primary:   #FCEFC8;
--text-secondary: rgba(252, 239, 200, 0.6);

/* Status Colors */
--status-ok:      #4B585A;   /* No prazo / finalizado */
--status-warning: #FCEFC8;   /* Atenção / recall */
--status-danger:  #610713;   /* Atrasado / crítico */
--status-info:    #001B72;   /* Compliance / neutro */

/* Brand Badge Colors (distintos entre si — 8 marcas) */
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
/* Fallback para Lovable: usar font-weight 800 para simular UltraBold */
```

### Cards KPI

```
CARD PADRÃO:
  background:     var(--bg-card)
  border:         1px solid var(--border-card)
  border-radius:  8px
  padding:        24px
  
  LABEL:          text-secondary, 11px, uppercase, letter-spacing 2px
  NÚMERO:         text-primary, 48px, font-weight 800
  VARIAÇÃO:       cor dinâmica baseada no delta (verde/vermelho/neutro)

CARD CRÍTICO (Overdue):
  border-color:   var(--status-danger)
  número cor:     var(--status-danger)
```

---

## LOVABLE OPTIMIZATION CHECKLIST

O HTML gerado deve atender estes critérios para funcionar bem no Lovable:

```
[ ] Sem dependências externas além de Google Fonts (se disponível)
[ ] CSS inline ou em <style> dentro do <head>
[ ] Responsivo: grid com CSS Grid ou Flexbox
[ ] Sem JavaScript obrigatório para renderização
[ ] Dados mockados com comentários <!-- REPLACE: fonte -->
    para facilitar substituição no Lovable
[ ] Componentes com IDs claros: #kpi-to-produce, #brand-table, etc.
[ ] Variáveis CSS no :root para fácil customização
[ ] Comentários de seção <!-- SECTION: Production Overview --> etc.
```

---

## FLUXO DE EXECUÇÃO

Quando ativado, siga esta sequência:

```
STEP 1 — Identificar fonte de dados
  → ClickUp disponível? Fazer query por projeto/lista High Tide
  → Planilha importada? Solicitar ao usuário se não estiver em contexto
  → Input manual? Solicitar os KPIs pelo checklist abaixo

STEP 2 — Solicitar dados faltantes (se necessário)
  Perguntar ao usuário:
  "To generate the report, I need the following data.
   Please provide or confirm the source:"
  [ ] Period (e.g., April 2026 / Week 14)
  [ ] Total assets to produce this month
  [ ] Assets currently in production
  [ ] Assets in recall
  [ ] Assets in compliance review
  [ ] Assets to be posted this week (list if possible)
  [ ] Overdue assets (list with original due dates)
  [ ] Finalized assets
  [ ] Finalized & posted assets
  [ ] Previous month data (optional, for comparisons)

STEP 3 — Validar marcas
  → Confirmar que todos os assets têm tag de marca
  → Sinalizar untagged assets

STEP 4 — Calcular insights automáticos
  → Identificar bottleneck (estágio com mais assets parados)
  → Calcular previsão de finalização do mês
  → Gerar alertas automáticos

STEP 5 — Gerar HTML
  → Seguir estrutura de seções obrigatórias
  → Aplicar design tokens BLOCO.
  → Otimizar para Lovable
  → Salvar como .html e apresentar ao usuário
```

---

## REGRAS ABSOLUTAS

```
SEMPRE:
  ✓ Output em .html — nunca em outro formato
  ✓ Relatório em inglês — sempre
  ✓ Assinado com BLOCO. no header e footer
  ✓ Tags de marca em todos os assets
  ✓ Forecast de finalização do mês sempre presente
  ✓ Insights estratégicos sempre presentes (mesmo que baseados em estimativas)
  ✓ Design seguindo BLOCO_DESIGNSYSTEM

NUNCA:
  ✗ Gerar relatório sem identificar o período
  ✗ Omitir assets atrasados ou em recall
  ✗ Usar cores fora da paleta BLOCO. sem justificativa
  ✗ Gerar sem o bloco de Strategic Insights
  ✗ Output em português (relatório é sempre em inglês)
  ✗ Deixar assets sem tag de marca sem sinalização
```

---

*BLOCO_INTERNAL_REPORTER_HIGHTIDE — v1.1*
*Derivado de: BLOCO_CORE + BLOCO_DASHBOARDS + BLOCO_DESIGNSYSTEM + BLOCO_UI_COMPONENTS*
