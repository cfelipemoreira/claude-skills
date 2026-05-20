---
name: oslo-ui-components
description: >
  Component library and UI patterns for OSLO. Use this skill whenever building
  UI components, buttons, cards, navbars, forms, tables, hero sections, or any
  interface element for OSLO. Trigger when writing HTML/CSS/React components,
  designing interaction states, specifying hover effects, or building any
  modular UI block. Always use alongside oslo-design-system for color and
  typography tokens. Ensures components look premium, technical, and consistent.
---

# OSLO. UI Components

> Read `oslo-design-system` first for color tokens and typography rules.
> These components build on top of that foundation.

---

## Component Principles

- Componentes devem parecer modulares, técnicos e premium
- Toda UI deve comunicar clareza estratégica
- Preferir poucos componentes fortes a muitos componentes medianos

---

## Buttons

### Primary
```css
background: #275279;
color: #fffafa;
border: 1px solid rgba(39,82,121,0.40);
border-radius: 999px;
padding: 14px 22px;
font: Inter 600;

/* Hover */
background: #31638F;
box-shadow: 0 10px 28px rgba(39,82,121,0.28);
```

### Secondary
```css
background: transparent;
color: #fffafa;
border: 1px solid rgba(255,250,250,0.16);
border-radius: 999px;

/* Hover */
background: rgba(255,250,250,0.04);
border: 1px solid rgba(255,250,250,0.26);
```

### Ghost
```css
background: transparent;
color: rgba(255,250,250,0.78);
border: none;

/* Hover */
color: #fffafa;
background: rgba(255,250,250,0.04);
```

**Rules:** CTA principal sempre com peso visual superior. Não usar muitos estilos diferentes na mesma tela.

---

## Navbar

**Structure:** logo left · links center/right · CTA right

```css
background: rgba(0,0,0,0.72);
backdrop-filter: blur(8px);
border-bottom: 1px solid rgba(255,250,250,0.08);
position: sticky;
top: 0;
```

- Compress on scroll
- Clean mobile menu
- Poucos links principais

---

## Hero

**Required:** strong headline · sharp subheadline · one core CTA

**Optional:** secondary CTA · credibility line · abstract system visual

**Rules:**
- Headline curta, forte e conceitual
- Subheadline explica com clareza o que a OSLO faz
- Não poluir com excesso de texto ou chips

---

## Cards

### Service Card
```css
background: #101010;
border: 1px solid rgba(255,250,250,0.12);
border-radius: 20px;
padding: 24px;
```
**Structure:** small label → title → short description → outcomes/bullets → CTA or link

### Metric Card
```css
background: #101010;
border: 1px solid rgba(255,250,250,0.10);
border-radius: 20px;
```
**Structure:** label → large value → context/delta

### Feature Card
- Accent top line: `#275279`
- Use cases: methodology · benefits · differentiators

**Rules:** Cards com borda suave e boa respiro interno. Usar Azure com moderação.

---

## Forms

### Inputs
```css
background: #0D0D0D;
color: #fffafa;
border: 1px solid rgba(255,250,250,0.12);
border-radius: 16px;
padding: 14px 16px;

/* Focus state */
border-color: rgba(39,82,121,0.60);
box-shadow: 0 0 0 3px rgba(39,82,121,0.16);
```

### Labels
```css
color: rgba(255,250,250,0.78);
font-family: Inter;
font-weight: 500;
```

**Rules:** Campos limpos. Focus state com Azure sutil. Formulários curtos e claros.

---

## Badges / Tags
```css
background: rgba(39,82,121,0.12);
color: #fffafa;
border: 1px solid rgba(39,82,121,0.26);
border-radius: 999px;
padding: 8px 12px;
font: Inter 500 12px;
```
**Usage:** tags de capability · status · service categories

---

## Accordions (FAQ / Service Breakdown)
```css
background: #101010;
border: 1px solid rgba(255,250,250,0.10);
border-radius: 16px;
```
- Animação discreta (220ms ease)
- Texto objetivo e profissional

---

## Tables
```css
background: #0D0D0D;
border: 1px solid rgba(255,250,250,0.12);
border-radius: 18px;

/* Header */
color: rgba(255,250,250,0.88);
font: Inter 600;

/* Row divider */
border-bottom: 1px solid rgba(255,250,250,0.08);
```
**Use cases:** comparativos · escopo · roadmaps · priorização

---

## Testimonials
**Structure:** quote → name → role/company

**Rules:**
- Minimal e credível, não emocional
- Preferir depoimentos sobre impacto, eficiência e clareza
- Evitar tom motivacional

---

## Diagrams
**Preferred styles:** workflow lines · system architecture · ecosystem map · process blocks

**Rules:**
- Fundo escuro, linhas suaves, Azure como destaque
- Devem parecer estratégicos e operacionais
- Evitar ilustrações infantis ou efeitos sci-fi

---

## Interaction States

| State | Treatment |
|---|---|
| Hover | slight lift · border strengthen · accent tint |
| Active | accent visible · clear hierarchy |
| Disabled | muted contrast · reduced opacity |
| Focus | visible outline with Azure tint |

---

## Sections Reference

| Section | Goal |
|---|---|
| Problem/Solution | pain → strategic reframing → OSLO solution |
| Methodology | Diagnóstico → Automação → Inovação |
| Deliverables | clear · structured · business-facing |
| Credibility | logos · proofs · case snapshots · operational outcomes |

---

## Reusable Patterns

- Hero + CTA
- Problem / Diagnosis / Solution
- Capabilities grid
- Methodology timeline
- Deliverables architecture
- System integration visual
- Case study strip
- FAQ block
- Contact conversion footer
