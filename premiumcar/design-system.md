---
name: premiumcar-design-system
description: >
  Sistema de design completo da PremiumCAR para criação de interfaces, componentes visuais, layouts e materiais gráficos.
  Use SEMPRE que criar ou revisar qualquer elemento visual da PremiumCAR: páginas web, landing pages, cards, banners,
  apresentações, mockups, interfaces de dashboard, posts para redes sociais, materiais impressos ou qualquer asset visual.
  Contém paleta de cores, tipografia, espaçamento, botões, superfícies, imagens, motion e princípios de design premium automotivo.
---

# PremiumCAR — Design System

## Identidade Visual

**Categoria:** Estética automotiva premium / proteção / detailing de alto padrão  
**Posicionamento visual:** Luxo técnico — sofisticação com precisão automotiva  

**Personalidade visual:**
- Sofisticada, precisa, técnica, elegante, moderna, confiável, apaixonada por carros

---

## Princípios de Design

1. **Elegância antes de excesso** — menos é mais, sempre
2. **Contraste forte e limpo** — nunca opaco ou confuso
3. **Poucos elementos, alto refinamento**
4. **Imagens com protagonismo**
5. **Sensação de precisão técnica**
6. **Conteúdo respirado** — hierarquia clara e generosa
7. **Interface silenciosa e sofisticada**

> Cada bloco deve parecer premium, automotivo e atual. Nunca popular, promocional demais ou genérico.

---

## Sistema de Cores

### Primárias
```
BLACK:       #0A0A0A   → uso principal de fundos e textos
DEEP_BLACK:  #000000   → contraste máximo
WHITE:       #FFFFFF   → espaço em branco, clareza
OFF_WHITE:   #F7F7F5   → fundos claros sofisticados
```

### Secundárias
```
GRAPHITE:    #1A1A1A   → superfícies escuras alternativas
DARK_GRAY:   #2B2B2B   → fundos de card dark
MID_GRAY:    #6F6F6F   → textos secundários, captions
LIGHT_GRAY:  #D9D9D9   → bordas, divisores, elementos neutros
```

### Acentos
```
METALLIC_SILVER:    #BFC3C9   → microdetalhes, ícones, linhas
WARM_SILVER:        #A8A8A3   → variação sofisticada do prata
PREMIUM_GOLD_SOFT:  #B89B5E   → selos, destaques premium, divisores especiais
```

### Feedback
```
SUCCESS:  #2E7D5A
WARNING:  #C28A2C
ERROR:    #B23B3B
```

### Regras de uso de cor
- Base principal: preta, branca ou grafite
- Dourado suave **apenas** para selos, divisores premium ou ícones de destaque
- Nunca usar: azul vibrante, vermelho saturado, verde neon, degradês chamativos
- A sensação deve remeter a luxo automotivo, pintura impecável e discrição

---

## Sistema Tipográfico

### Fontes por Função

| Função | Sugestão | Uso |
|---|---|---|
| **Display** | Cinzel, Playfair Display, Bodoni Moda | Hero titles, headlines, manifestos, frases de impacto |
| **UI Principal** | Montserrat, Inter, Helvetica Neue | Navegação, botões, subtítulos, formulários |
| **Corpo** | Inter, Arial, Helvetica | Parágrafos, descrições, tabelas, dashboards |

### Escala de Tamanhos
```
HERO_TITLE:     56–80px
SECTION_TITLE:  32–48px
CARD_TITLE:     20–28px
BODY_LARGE:     18–20px
BODY:           15–17px
CAPTION:        12–14px
LABEL:          11–13px
```

### Regras tipográficas
- Títulos: luxo, autoridade e presença
- Headlines podem usar caixa alta com espaçamento controlado (letter-spacing moderado)
- Subtítulos: contidos, objetivos, refinados
- Corpo: técnico, limpo, muito legível
- Evitar: fontes caricatas, esportivas demais, futuristas em excesso

---

## Sistema de Espaçamento

```
SECTION_VERTICAL:      80–140px
CONTAINER_HORIZONTAL:  24–48px
CARD_PADDING:          20–32px
GRID_GAP:              16–32px
```

### Border Radius
```
SMALL:   8px
MEDIUM:  14px
LARGE:   20px
XL:      28px
```

---

## Layout

- Grids amplos e bem organizados
- Hero sections: imagem forte + texto objetivo
- Grandes áreas de respiro
- Alternância entre blocos escuros e claros
- Páginas devem parecer **editoriais, premium e comerciais** ao mesmo tempo
- Priorizar modularidade

---

## Superfícies e Cards

- Superfícies: branco puro, preto profundo ou cinza muito claro
- Cards: sólidos, premium e discretos
- Bordas finas e sutis
- Sombras leves, nunca exageradas
- Glassmorphism: somente extremamente discreto e sofisticado
- Acabamento clean e automotivo, com sensação de materialidade refinada

**Regra de borda:**
```css
border: 1px solid rgba(0,0,0,0.08);      /* fundos claros */
border: 1px solid rgba(255,255,255,0.10); /* fundos escuros */
```

---

## Sistema de Botões

### Primário
```
background: #0A0A0A (BLACK)
color: #FFFFFF
border: subtle dark
border-radius: pill (9999px) ou 14px
```

### Secundário
```
background: transparent
color: BLACK ou WHITE (dependendo da seção)
border: 1px solid sutil
```

### Terciário
```
text-only com seta →
interação premium discreta
```

**Regras:**
- CTAs devem transmitir segurança e sofisticação
- Textos curtos e diretos
- Hover com microtransição elegante (180–350ms)
- Evitar botões agressivos ou muito publicitários

---

## Motion

```
Tipo:     fade, rise, scale (muito sutil)
Duração:  180ms a 350ms
Easing:   ease-out ou cubic-bezier suave
```
- Tudo deve parecer refinado e caro
- Evitar animações chamativas ou gimmicks

---

## Direção para Imagens

- Fotos são protagonistas — nunca decorativas
- Veículos em alta qualidade, brilho impecável, reflexos controlados
- Enquadramentos premium: close de pintura, textura, curvas, interiores
- Iluminação: limpa, refinada e luxuosa
- Nunca usar imagens genéricas de banco de imagens de baixa qualidade
- Estética editorial automotiva premium
- Antes/depois: exibir com elegância, nunca visual popular

---

## Iconografia

- Ícones minimalistas — outline ou solid refinado
- Traço limpo e técnico
- Temas: performance, proteção, precisão, acabamento, cuidado
- Nunca usar ícones divertidos ou infantis

---

## Texturas e Decoração

- Linhas finas, brilhos sutis, overlays suaves
- Referências visuais: película, reflexo, acabamento, metal escovado
- Decoração **sempre mínima**
- Jamais poluir a interface

---

## Sensação de Marca

> "Estúdio premium" · "Tecnologia aplicada ao detalhe" · "Proteção com sofisticação" · "Luxo técnico" · "O carro como obra de arte"
