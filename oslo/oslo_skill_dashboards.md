---
name: oslo-dashboards
description: >
  Design and build guidelines for OSLO. dashboards and data interfaces. Use
  this skill whenever creating any dashboard, analytics view, monitoring panel,
  KPI board, operational interface, or data visualization for OSLO. Trigger
  when the user asks for a dashboard, metrics view, control panel, reporting
  interface, or any data-driven UI. Ensures all dashboards feel like strategic
  command centers — premium, minimal, analytically clear.
---

# OSLO. Dashboards

> Dependencies: `oslo-design-system` for tokens.
> Dashboards are the most data-dense OSLO interface — apply extra restraint.

---

## Dashboard Philosophy

- **Dashboard OSLO deve parecer sala de controle estratégica**
- Menos ornamentação, mais leitura e decisão
- Interface analítica, premium e silenciosa
- Todos os dashboards devem parecer ferramentas reais de decisão — não templates SaaS genéricos

---

## Visual Language

```
Background:         #000000
Surface:            #101010
Elevated surface:   #141414
Text primary:       #fffafa
Text secondary:     rgba(255,250,250,0.72)
Accent:             #275279
Grid lines:         rgba(255,250,250,0.06)
Dividers:           rgba(255,250,250,0.08)
```

---

## Layout Patterns

### Structure
1. Top summary row (KPIs / status)
2. Main analytical area (primary charts / tables)
3. Secondary cards (supporting metrics)
4. Filters and context tools

### Layout Options
| Pattern | Use When |
|---|---|
| 2-column executive | Strategic overview, leadership views |
| 3-column metrics | Dense data, operational monitoring |
| Single-focus operational | One critical workflow or process |

**Rules:**
- Não lotar tela com muitos widgets pequenos
- Priorizar leitura executiva
- No máximo 4 a 6 KPIs por linha

---

## Components

### KPI Cards
```css
background: #101010;
border: 1px solid rgba(255,250,250,0.10);
border-radius: 16px;
padding: 20px 24px;
```
**Structure:** small descriptor label → large value → delta or context

### Charts
**Preferred types:** line chart · bar chart · stacked bar · donut (only if necessary)

```css
/* Chart grid */
color: rgba(255,250,250,0.08);
stroke-width: 1px;

/* Primary line/bar */
color: #275279;

/* Secondary data */
color: rgba(255,250,250,0.40);
```

**Rules:**
- Linhas limpas, grids discretos, destaque em Azure
- Evitar visual colorido demais — charts devem parecer executivos
- Labels pequenos, Inter, muted color

### Filters
```css
background: #101010;
border: 1px solid rgba(255,250,250,0.10);
border-radius: 8px;
padding: 8px 12px;
font: Inter 500 13px;
```
- Filtros no topo ou lateral, nunca dominando a tela
- Compact, clear, high-legibility

### Tables
```css
background: #0D0D0D;
border: 1px solid rgba(255,250,250,0.10);
border-radius: 16px;

/* Header row */
background: #141414;
font: Inter 600 13px;
color: rgba(255,250,250,0.88);

/* Row divider */
border-bottom: 1px solid rgba(255,250,250,0.06);

/* Row padding */
padding: 12px 16px;
```
- Priorizar leitura rápida
- Alto espaçamento entre linhas
- Cabeçalhos claros e bem definidos

### Alerts / Status Indicators
**Style:** subtle · contextual · non-alarmist

```css
/* Status dot */
success: #2D7A58;
warning: #8D6A2B;
error: #8A3E3E;
info: #275279;
```
**Usage:** status changes · attention flags · process blockers

---

## Dashboard Types

### Executive Dashboard
- **Objective:** Visão estratégica de performance, operação e crescimento
- **Widgets:** core KPIs · trend overview · priority items · opportunities
- **Audience:** C-level, founders, directors

### Operational Dashboard
- **Objective:** Acompanhar fluxo, automações, eficiência e gargalos
- **Widgets:** workflow status · automation health · queue load · response times
- **Audience:** operations managers, team leads

### Sales & Growth Dashboard
- **Objective:** Ler aquisição, conversão, revenue e pipeline
- **Widgets:** leads · conversion rate · pipeline stages · revenue trend
- **Audience:** sales team, growth leads

### AI Systems Dashboard
- **Objective:** Monitorar agentes, integrações, inputs, outputs e performance
- **Widgets:** agent activity · task completion · error map · throughput · integration status
- **Audience:** technical team, AI operations

---

## Dashboard Quality Checklist

- [ ] Primary metric is immediately visible on load
- [ ] Maximum 6 KPIs in top summary row
- [ ] Charts use clean lines with minimal grid
- [ ] Azure used only for primary data series or key highlights
- [ ] No decorative elements that don't carry data
- [ ] Tables are scannable at a glance
- [ ] Filters are compact and don't dominate layout
- [ ] All text uses Inter, not Montserrat
- [ ] Alerts are contextual and non-alarmist
- [ ] Overall feels like a command center, not a report
