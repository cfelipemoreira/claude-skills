---
name: oslo-design-system
description: >
  Complete design system reference for OSLO. Use this skill whenever designing,
  building, or reviewing any visual interface, component, layout, or branded
  material for OSLO. — including landing pages, dashboards, UI components,
  presentations, or any visual artifact. Trigger before writing any CSS,
  choosing colors, selecting typography, or specifying layout for OSLO work.
  Ensures all outputs match OSLO's premium, refined, contemporary aesthetic —
  elegant without being cold, technical without being industrial.
---

# OSLO. Design System

> Before any OSLO visual output: verify colors, typography, spacing and component
> rules against this document. Never use generic SaaS aesthetics.

---

## Brand Essence (Design Lens)

- **Perception goals:** premium · refined · elegant · strategic · minimal · intelligent · contemporary · credible · warm-precise
- **Aesthetic direction:** Minimalismo contemporâneo com sofisticação — próximo de marcas como Linear, Vercel e Arc. Não industrial, não corporativo tradicional.
- **Core principle:** Elegância viva — premium com leveza, não frieza técnica

### O que define o visual OSLO
> A OSLO não é uma empresa de engenharia pesada nem uma consultoria tradicional.
> O design deve parecer inteligente e refinado — como um estúdio de alto nível.
> Eliminar qualquer referência visual que remeta a desenho industrial, grid mecânico ou corporativismo antigo.

---

## Color Modes

### ⚪ Light Mode — Padrão (prioridade)

> Fundo branco é o padrão da OSLO. Usar sempre que não houver motivo explícito para o modo escuro.
> Transmite limpeza, clareza, sofisticação e leveza — sem peso industrial.

```
Canvas primary:    #FFFFFF
Canvas secondary:  #F7F7F5
Surface primary:   #F2F2F0
Surface secondary: #EBEBEA
Surface soft:      #E5E5E3

Text primary:      #0A0A0A
Text secondary:    rgba(10,10,10,0.72)
Text muted:        rgba(10,10,10,0.48)

Border soft:       rgba(10,10,10,0.08)
Border default:    rgba(10,10,10,0.12)
Border strong:     rgba(10,10,10,0.20)

Accent primary:    #275279
Accent hover:      #1E3F5E
Accent soft:       rgba(39,82,121,0.10)
Accent glow:       rgba(39,82,121,0.18)

Success:           #1E6644
Warning:           #7A5520
Error:             #7A2626
```

### ⚫ Dark Mode — Alternativo (uso consciente)

> Usar dark mode apenas em contextos específicos: dashboards operacionais,
> interfaces técnicas de monitoramento, ou quando o cliente / contexto pedir.
> Nunca usar dark por padrão em landing pages, apresentações ou materiais institucionais.

```
Canvas primary:    #000000
Canvas secondary:  #0A0A0A
Surface primary:   #101010
Surface secondary: #141414
Surface soft:      #1A1A1A

Text primary:      #fffafa
Text secondary:    rgba(255,250,250,0.78)
Text muted:        rgba(255,250,250,0.56)

Border soft:       rgba(255,250,250,0.10)
Border default:    rgba(255,250,250,0.14)
Border strong:     rgba(255,250,250,0.22)

Accent primary:    #275279
Accent hover:      #31638F
Accent soft:       rgba(39,82,121,0.16)
Accent glow:       rgba(39,82,121,0.28)

Success:           #2D7A58
Warning:           #8D6A2B
Error:             #8A3E3E
```

### Base Palette (Invariável nos dois modos)
| Token | Hex | Usage |
|---|---|---|
| White Serene | `#FFFAFA` | Superfícies claras, texto sobre escuro |
| Black | `#0A0A0A` | Texto principal no modo claro, canvas no escuro |
| Azure | `#275279` | Accent — intelligence, action, detail |

### Color Rules
- **Branco é a base dominante por padrão** — sempre iniciar no modo claro
- **Preto** como cor de texto principal no light mode — legibilidade máxima com elegância
- **Azure** é a cor de inteligência e ação — nunca deve dominar; use em CTAs, links, ícones-chave, estados ativos
- Evitar: gradientes saturados, neon, roxos sci-fi, azuis elétricos vibrantes
- Contraste: forte o suficiente para legibilidade, suave o suficiente para elegância

---

## Typography

### Font Stack
| Role | Font | Fallback |
|---|---|---|
| Headlines / Branding | Neue Montreal | Montserrat |
| Body / UI / Navigation | Inter | — |

### Type Scale
| Token | Desktop | Mobile | Notes |
|---|---|---|---|
| Hero Display | 56–72px | 38–48px | line-height: 0.95–1.05 |
| H1 | 44–56px | 32–40px | |
| H2 | 30–38px | 24–30px | |
| H3 | 22–28px | 20–24px | |
| H4 | 18–22px | 17–20px | |
| Body LG | 18px | 17px | |
| Body MD | 16px | 15px | |
| Body SM | 14px | 14px | |
| Micro | 12px | 12px | |

### Usage Rules
| Context | Font | Weight | Tracking |
|---|---|---|---|
| Hero titles | Montserrat | 700 | -0.03em |
| Section titles | Montserrat | 600 | -0.02em |
| Card titles | Montserrat | 600 | — |
| Body text | Inter | 400 | — |
| UI / buttons | Inter | 500–600 | — |
| Captions | Inter | 400 | — |

**Rules:**
- Montserrat APENAS para headlines, títulos, chamadas e peças de branding
- Inter para TODO texto corrido, menus, botões, inputs e dashboards
- Evitar texto muito longo — OSLO fala com síntese
- Espaçamento generoso entre blocos para leitura premium

---

## Spacing & Layout

### Grid
- Desktop: 12 colunas · max-width: 1200px · content: 1120px · gutter: 24px
- Tablet: 8 colunas
- Mobile: 4 colunas

### Spacing Scale
```
xs:           4px
sm:           8px
md:           12px
lg:           16px
xl:           24px
xxl:          32px
xxxl:         48px
section:      72px
section_lg:   104px
```

**Layout rules:**
- Layouts devem respirar — evitar blocos comprimidos
- Cada dobra deve ter uma ideia central
- Usar espaçamento como linguagem de sofisticação

---

## Borders, Radius & Shadows

### Border Radius
```
xs:   8px    sm:  12px    md:  16px
lg:  20px    xl:  24px    pill: 999px
```

### Borders — Light Mode
```
Default:  1px solid rgba(10,10,10,0.12)
Soft:     1px solid rgba(10,10,10,0.08)
Strong:   1px solid rgba(10,10,10,0.20)
```

### Borders — Dark Mode
```
Default:  1px solid rgba(255,250,250,0.14)
Soft:     1px solid rgba(255,250,250,0.10)
Strong:   1px solid rgba(255,250,250,0.22)
```

### Shadows — Light Mode
```
Subtle:  0 4px 16px rgba(0,0,0,0.06)
Medium:  0 8px 28px rgba(0,0,0,0.10)
Strong:  0 16px 48px rgba(0,0,0,0.14)
```

### Shadows — Dark Mode
```
Subtle:  0 8px 24px rgba(0,0,0,0.20)
Medium:  0 14px 40px rgba(0,0,0,0.28)
Strong:  0 20px 60px rgba(0,0,0,0.36)
```

---

## Backgrounds & Surfaces

### Light Mode (padrão)
**Permitidos:**
- Branco puro (`#FFFFFF`) e off-whites quentes (`#F7F7F5`, `#F2F2F0`) — padrão
- Gradientes sutis de branco para off-white
- Seções de contraste com Azure muito suave (`rgba(39,82,121,0.06–0.10)`) como fundo de destaque

**Proibidos:**
- ❌ Grid quadriculado (dot grid, line grid, graph paper) — nunca usar como fundo ou textura decorativa
- ❌ Padrões repetitivos geométricos mecânicos
- ❌ Texturas que remetam a papel milimetrado ou planta técnica
- ❌ Fundos escuros em contextos institucionais ou comerciais
- ❌ Gradientes neon ou saturados

### Dark Mode (alternativo — apenas dashboards e interfaces técnicas)
**Permitidos:**
- Sólidos escuros (`#000000`, `#0A0A0A`, `#101010`)
- Gradientes sutis e atmosféricos: radial suave de Azure ou neutro sobre fundo preto
- Noise texture muito sutil (opacity 2–4%) para profundidade orgânica
- Glow difuso de Azure (`rgba(39,82,121,0.12–0.20)`)

**Proibidos:**
- ❌ Grid quadriculado — nunca, em nenhum modo
- ❌ Glassmorphism pesado ou espelhado
- ❌ Gradientes neon ou saturados

> O fundo deve ser silencioso e sofisticado.
> No light: limpeza e leveza.
> No dark: profundidade e controle.
> Nunca padrão mecânico.

---

## Iconography

### Filosofia
Ícones são parte ativa da linguagem visual da OSLO — não ornamento.
Cada ícone deve reforçar a mensagem do contexto onde aparece.
O conjunto iconográfico contribui para a percepção de inteligência, precisão e modernidade.

### Conjuntos recomendados (por ordem de preferência)
| Set | Estilo | Uso ideal |
|---|---|---|
| **Phosphor Icons** (Regular / Light) | Refinado, elegante, moderno | Preferência principal — apresentações, landing pages, componentes |
| **Lucide** | Clean, geométrico, neutro | UI, dashboards, tabelas, navegação |
| **Heroicons** (Outline) | Sólido, confiável | Formulários, estados, ações funcionais |

> Nunca misturar mais de um conjunto no mesmo contexto visual.
> Escolher um conjunto por projeto ou por seção de interface.

### Tamanhos
```
Micro:    16px   (inline, captions)
SM:       20px   (UI, navegação, badges)
MD:       24px   (cards, listas, botões com ícone)
LG:       32px   (destaques, seções, features)
XL:       40–48px (hero, apresentações, capa)
```

### Uso de cor em ícones

**Light Mode:**
- Padrão: `rgba(10,10,10,0.64)` — discreto, integrado ao texto escuro
- Destaque / ativo: `#275279` (Azure)
- Muted: `rgba(10,10,10,0.36)`

**Dark Mode:**
- Padrão: `rgba(255,250,250,0.72)`
- Destaque / ativo: `#275279` (Azure)
- Muted: `rgba(255,250,250,0.40)`

### Regras de aplicação
- Ícones devem aparecer sempre que puderem substituir ou reforçar uma palavra de forma visual
- Em cards de serviço, features e metodologia: sempre incluir ícone como âncora visual do conceito
- Em listas e bullets: preferir ícone a ponto ou traço
- Stroke weight consistente dentro do mesmo contexto (não misturar filled e outline)
- Evitar: ícones cartoon, arredondados demais, excessivamente ilustrativos, com sombra própria

---

## Motion

```
Fast:    160ms
Normal:  220ms
Slow:    320ms
Easing:  cubic-bezier(0.22, 1, 0.36, 1)
```

- Transições refinadas, não chamativas
- Hover: leve elevação, borda reforçada ou accent tint
- Evitar bounce, overshoot exagerado ou efeitos lúdicos

---

## Design Principles (Summary)

1. **Clareza como elegância** — fundo branco é o ponto de partida; limpeza é sofisticação
2. **Elegância viva** — premium com leveza e contemporaneidade, não frieza industrial
3. **Minimalismo com intenção** — menos ruído visual, mais propósito em cada elemento
4. **Hierarquia clara** — títulos fortes, textos curtos, blocos bem definidos
5. **Sofisticação funcional** — toda escolha visual melhora leitura, entendimento ou ação
6. **Tecnologia com calma** — evitar visual futurista clichê, cyberpunk ou desenho industrial antigo
7. **Ícones como linguagem** — iconografia ativa, não decorativa; reforça conceito e identidade
8. **Fundo como atmosfera** — profundidade vem de espaçamento, tipografia e contraste — nunca de padrão mecânico
9. **Marca orientada a confiança** — interface deve transmitir domínio, clareza e controle

---

## Anti-patterns (O que nunca fazer)

| ❌ Evitar | ✅ Preferir |
|---|---|
| Fundo escuro em landing pages e apresentações | Fundo branco como padrão institucional |
| Grid quadriculado como fundo (qualquer modo) | Fundo sólido limpo com espaçamento generoso |
| Visual de desenho industrial | Estética de estúdio contemporâneo |
| Estética corporativa antiga | Premium e moderno como Linear / Vercel |
| Interface sem ícones | Ícones Phosphor integrando a linguagem visual |
| Gradientes neon ou saturados | Gradientes atmosféricos sutis ou ausência de gradiente |
| Misturar conjuntos de ícones | Um conjunto por contexto, aplicado com consistência |
| Glassmorphism pesado | Superfícies sólidas com borda suave |
| Dark mode padrão em materiais institucionais | Light mode como modo principal da marca |
