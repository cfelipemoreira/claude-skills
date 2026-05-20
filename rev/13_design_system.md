# SKILL — Design System
**REV Strategy | Visual Identity & Output Standards**

---

## Propósito

Este documento define as diretrizes visuais completas da REV Strategy para todos os tipos de output — documentos entregáveis, PDFs, infográficos, interfaces digitais e apresentações.

Deve ser consultado sempre que qualquer material visual for produzido em nome da REV.

---

## Princípio Central

**Minimalismo funcional com autoridade.**

O design da REV comunica competência estratégica através de contenção — não de decoração. A organização visual é o design. Espaçamento, hierarquia tipográfica e uso restrito de cor fazem mais trabalho do que qualquer elemento decorativo.

> Excesso de cor é um erro estratégico de design. Um documento cheio de cores vibrantes transmite energia de agência criativa. Um documento contido, bem espaçado e estruturado transmite autoridade de consultoria.

**A regra de ouro:** cada decisão visual deve responder à pergunta — *"o que este elemento está comunicando?"* Se a resposta for "nada além de decoração", o elemento não deve existir.

---

## Contextos de Aplicação

O design system da REV opera em dois modos distintos, com critérios claros de quando usar cada um.

---

## Modo Claro — Documentos e Entregáveis ao Cliente

### Quando usar

**Obrigatório** em:
- PDFs entregáveis
- Infográficos
- Relatórios de diagnóstico
- Planos estratégicos
- Qualquer material enviado, impresso ou baixado pelo cliente

**Razão:** documentos são consumidos em ambientes variados (tela, impressão, projeção). Fundo claro garante legibilidade universal e transmite o registro visual de um documento profissional de alto nível.

---

### Paleta — Modo Claro

| Token | Uso | Valor Hex |
|---|---|---|
| `bg-page` | Background de página | `#F7F7F8` |
| `bg-surface` | Card / superfície primária | `#FFFFFF` |
| `bg-surface-2` | Superfície secundária / zebra | `#F0F0F2` |
| `bg-surface-3` | Header de tabela, tag muted | `#E8E8EC` |
| `text-primary` | Headings, rótulos fortes | `#18181F` |
| `text-body` | Texto corrido | `#3C3C4A` |
| `text-muted` | Legendas, notas, suporte | `#9A9AA8` |
| `border-default` | Bordas de card padrão | `#DCDCE4` |
| `border-subtle` | Divisores, separadores | `#E2E2E6` |
| `accent-dark` | Elemento de destaque único | `#18181F` (fundo de linha total, header) |

---

### Uso de Cor Funcional em Documentos

Cor é permitida **apenas para diferenciar categorias distintas** — nunca como decoração.

**Regras:**
- No máximo **2–3 cores funcionais** por documento, além do preto/branco/cinza
- Cores devem ser **dessaturadas e suaves** — tons de fundo leves com texto escuro da mesma família
- Nunca usar cores vibrantes (vermelho forte, verde saturado, azul vivo) como preenchimento de área
- Nunca usar múltiplas cores simultaneamente sem função semântica clara

**Paleta de cores funcionais permitidas em documentos:**

| Categoria | Background badge | Texto badge | Dot / indicador |
|---|---|---|---|
| Tipo A (ex: Online / Perpétuo) | `#E8EAF6` | `#3949AB` | `#3949AB` |
| Tipo B (ex: Presencial / Específica) | `#FFF8E8` | `#B26A00` | `#D4880A` |
| Tipo C (ex: Remarketing / Neutro) | `#F3F3F3` | `#444444` | `#888888` |

Esses valores são referências. O critério é: **fundo suave + texto escuro da mesma família de cor**.

---

### Tipografia — Modo Claro

Em documentos PDF gerados programaticamente, usar fontes do sistema para garantir fidelidade:

| Uso | Fonte | Peso |
|---|---|---|
| Headings principais | Helvetica-Bold | Bold |
| Subtítulos / rótulos | Helvetica-Bold | Bold |
| Corpo de texto | Helvetica | Regular |
| Notas, observações | Helvetica-Oblique | Italic |
| Dados numéricos em tabela | Helvetica | Regular |

**Tamanhos de referência (em documentos A4):**

| Hierarquia | Tamanho | Cor |
|---|---|---|
| Título principal | 14–16pt | `#18181F` |
| Título de seção | 9–10pt | `#18181F` |
| Corpo | 7–8pt | `#3C3C4A` |
| Suporte / muted | 6.5–7pt | `#9A9AA8` |
| Notas de rodapé | 6–6.5pt | `#9A9AA8` |

---

### Componentes — Modo Claro

#### Card padrão
```
background: #FFFFFF
border: 0.6px solid #DCDCE4
border-radius: 8px
padding: 10–14px
sem sombra
```

#### Card com header destacado
```
header background: #F0F0F2
border-bottom: 0.5px solid #DCDCE4
border-radius: 8px (apenas topo)
título: Helvetica-Bold, 7.5–8pt, #18181F
```

#### Linha de tabela
```
par: background #FFFFFF
ímpar: background #F0F0F2
border: 0.3–0.5px solid #DCDCE4
sem border-radius em linhas internas
```

#### Linha de total / destaque de tabela
```
background: #18181F
texto: #FFFFFF
Helvetica-Bold
único elemento escuro na tabela — uso exclusivo para linha totalizadora
```

#### Badge / tag de categoria
```
background: cor funcional suave (ver paleta funcional)
border-radius: altura/2 (pill)
padding: 4–6px horizontal, 2–3px vertical
texto: Helvetica-Bold, 6.5–7pt
```

#### Separador de seção
```
line: 0.5px solid #DCDCE4
margin vertical: 12–16px
sem ornamentos
```

#### Indicador de categoria (dot)
```
círculo: 3px raio
cor: da paleta funcional correspondente
posição: inline antes do título de seção
```

---

### Regras de Layout — Documentos

1. **Margens:** mínimo 28px em todos os lados em A4
2. **Espaçamento entre seções:** 20–28px mínimo
3. **Duas colunas:** gap mínimo de 8px entre colunas
4. **Não comprimir** — se o conteúdo não cabe com espaçamento adequado, usar segunda página
5. **Hierarquia visual por espaçamento:** seções principais têm mais espaço acima do que subseções
6. **Rodapé:** sempre presente em documentos entregáveis, com identificação REV Strategy + cliente, fonte 6–6.5pt, `#9A9AA8`

---

## Modo Escuro — Interfaces Digitais

### Quando usar

**Aplicável apenas em:**
- Site da REV Strategy
- Dashboards e ferramentas digitais próprias
- Apresentações projetadas em tela (não impressas)
- Interfaces de produto digital

**Nunca usar** em documentos para download, PDFs ou materiais impressos.

---

### Paleta — Modo Escuro

| Token | Uso | Valor |
|---|---|---|
| `bg-primary` | Background de página | `#0B0B0F` |
| `bg-secondary` | Superfície de card | `#111218` |
| `bg-tertiary` | Superfície interna | `#171923` |
| `text-primary` | Texto principal | `#FFFFFF` / `rgba(255,255,255,0.92)` |
| `text-secondary` | Texto suporte | `rgba(255,255,255,0.72)` |
| `text-muted` | Texto auxiliar | `rgba(255,255,255,0.52)` |
| `accent-1` | Accent principal | `#4F7CFF` |
| `accent-2` | Accent suave | `#8AA4FF` |
| `border-subtle` | Borda sutil | `rgba(255,255,255,0.08)` |
| `border-default` | Borda padrão | `rgba(255,255,255,0.12)` |

**Regra do accent em modo escuro:** apenas em ícones, micro-destaques, frases-chave, elementos pequenos de UI e hover states. Nunca em backgrounds de área grande.

---

### Tipografia — Modo Escuro / Digital

| Uso | Fonte | Peso |
|---|---|---|
| Headings / Display | Sora | 600–700 |
| Body / UI | Inter | 400–500 |

---

## Regras Universais — Aplicam-se a Ambos os Modos

### O que nunca fazer

- Usar gradientes decorativos (gradiente só para propriedade física/estado, nunca estético)
- Usar sombras expressivas (box-shadow com blur > 0 é proibido em documentos)
- Usar mais de 3 cores funcionais simultaneamente
- Usar cor sem função semântica definida
- Usar fontes decorativas ou display
- Criar hierarquia por cor quando pode ser criada por peso tipográfico
- Usar ALL CAPS em textos corridos
- Deixar elementos sem respiro — padding e margin são tão importantes quanto o conteúdo

### O que sempre fazer

- Hierarquia clara: o olho deve saber onde ir primeiro
- Espaçamento generoso como sinal de organização
- Alinhamento consistente (grid mental sempre presente)
- Bordas sutis em vez de sombras
- Tipografia como principal vetor de diferenciação visual
- Elementos de destaque únicos por seção — nunca competindo

---

## Identidade Visual — Direção

### O que a REV DEVE parecer

- Consultoria premium de estratégia
- Documento executivo de alto nível
- Autoridade visual silenciosa
- Elegância estrutural — onde a organização é o design
- Clareza antes de estética

### O que a REV NUNCA deve parecer

- Startup playful
- Coaching motivacional
- Agência criativa colorida
- Dashboard de BI neon
- Infográfico com múltiplas cores vibrantes sem função
- Template genérico de apresentação
- Relatório de marketing com excesso de elementos gráficos

---

## Checklist de Qualidade Visual

Antes de finalizar qualquer output visual, verificar:

- [ ] Fundo claro para documentos / fundo escuro apenas para interfaces digitais?
- [ ] Número de cores funcionais ≤ 3?
- [ ] Cada cor tem função semântica definida?
- [ ] Espaçamento entre seções é generoso?
- [ ] Hierarquia tipográfica clara (heading → subtítulo → corpo → muted)?
- [ ] Ausência de gradientes, sombras ou ornamentos desnecessários?
- [ ] Elemento de destaque único por seção?
- [ ] Rodapé com identificação presente?
- [ ] O documento comunica autoridade ou energia?

---

## Histórico de Decisões

| Data | Decisão | Contexto |
|---|---|---|
| 2026-03 | Modo claro como padrão obrigatório para documentos entregáveis | Infográfico PremiumCAR: versão dark foi rejeitada por excesso de cor e fundo escuro inadequado para documento de cliente |
| 2026-03 | Uso de cor funcional restrito e dessaturado em documentos | Primeira versão do infográfico usou múltiplas cores vibrantes; diretriz de minimalismo elegante foi reforçada |
