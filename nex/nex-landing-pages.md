---
name: nex-landing-pages
description: Landing page structure, components, and generation rules for Nex Coworking. Use this skill when building complete landing pages, page sections, or HTML/React interfaces for any Nex product or campaign. Trigger on requests like "crie uma landing page", "monte uma página completa", "faça o HTML da página", "construa uma página de conversão", "página institucional do Nex", or any full-page build task. Works together with nex-design-system (visual) and nex-copywriting (text) and nex-product-pages (product logic).
---

# Nex — Landing Pages

## Tipos de Página

| Tipo | Objetivo |
|---|---|
| `home_page` | Visão geral do ecossistema Nex |
| `workspace_page` | Escritórios Privativos |
| `meeting_rooms_page` | Salas de Reunião |
| `events_page` | Espaços para Eventos |
| `nex_house_page` | Nex House |
| `virtual_office_page` | Escritório Virtual |
| `day_pass_page` | Diária de Trabalho |
| `dedicated_desk_page` | Mesa Fixa |
| `campaign_page` | Página de campanha específica |

---

## Estrutura Universal de Landing Page

```
┌──────────────────────────────────────────┐
│  NAVBAR (fixo no topo)                   │
│  Logo | Nav links | CTA                  │
├──────────────────────────────────────────┤
│  HERO SECTION                            │
│  Headline + Subheadline + CTA(s)         │
├──────────────────────────────────────────┤
│  EXPLANATION / HOOK                      │
│  O que é / Por que importa               │
├──────────────────────────────────────────┤
│  PRODUCT / BENEFITS                      │
│  Features, diferenciais, opções          │
├──────────────────────────────────────────┤
│  SOCIAL PROOF                            │
│  Depoimentos, logos de empresas          │
├──────────────────────────────────────────┤
│  FAQ                                     │
│  Perguntas frequentes (accordion)        │
├──────────────────────────────────────────┤
│  FINAL CTA                               │
│  Formulário ou botão de ação principal   │
├──────────────────────────────────────────┤
│  FOOTER                                  │
│  Links | Unidades | Contato | Social     │
└──────────────────────────────────────────┘
```

---

## Hero Section — Componentes

```html
<!-- Estrutura base do Hero -->
<section class="hero">
  <div class="container">
    <h1><!-- Headline principal: benefício direto --></h1>
    <p class="subheadline"><!-- Quem é, como funciona, por que o Nex --></p>
    <p class="supporting-text"><!-- Detalhe adicional opcional --></p>
    <div class="cta-group">
      <a class="btn-primary"><!-- CTA primário --></a>
      <a class="btn-ghost"><!-- CTA secundário opcional --></a>
    </div>
  </div>
</section>
```

**Regras do Hero:**
- Headline: máximo 10 palavras, benefício claro
- Subheadline: quem é e como, máximo 2 linhas
- Sempre ter CTA primário (botão amarelo)
- CTA secundário opcional (ghost button)
- Fundo branco, sem imagem de fundo com texto sobre ela (legibilidade)

---

## Navbar — Padrão

```
[Logo Nex]          [Espaços | Reuniões | Eventos | Nex House]          [Falar com a gente]
```

- Background: `#FFFFFF`
- Posição: `fixed top`
- Fonte: Proxima Nova
- CTA no canto direito: botão primário amarelo ou ghost
- Mobile: hamburger menu

---

## Seções Reutilizáveis

### Feature Grid (3 colunas)

```
┌──────────┐  ┌──────────┐  ┌──────────┐
│  Ícone   │  │  Ícone   │  │  Ícone   │
│  Título  │  │  Título  │  │  Título  │
│  Texto   │  │  Texto   │  │  Texto   │
└──────────┘  └──────────┘  └──────────┘
```

### Card de Produto

```html
<div class="product-card">
  <div class="card-icon"></div>
  <h3>Nome do produto</h3>
  <p>Descrição curta — para quem é e o que resolve</p>
  <a class="btn-ghost">Ver mais</a>
</div>
```

### Testimonial Block

```html
<div class="testimonial">
  <span class="quote-mark">"</span>
  <p class="quote-text">Texto do depoimento...</p>
  <div class="author">
    <strong>Nome</strong>
    <span>Cargo · Empresa</span>
  </div>
</div>
```

### FAQ Accordion

```html
<div class="faq-item">
  <button class="faq-question">Pergunta aqui?</button>
  <div class="faq-answer">
    <p>Resposta clara e direta.</p>
  </div>
</div>
```

### Final CTA Section

```html
<section class="final-cta">
  <h2>Pronto para começar?</h2>
  <p>Fale com a nossa equipe e encontre o espaço certo para você.</p>
  <a class="btn-primary">CTA principal</a>
</section>
```

---

## CSS Base para Todas as Páginas

```css
:root {
  --color-bg: #FFFFFF;
  --color-text: #000000;
  --color-accent: #FFD400;
  --color-gray-light: #F5F5F5;
  --color-gray-medium: #E5E5E5;
  --color-gray-dark: #2A2A2A;
  --font-heading: 'Proxima Nova', Inter, sans-serif;
  --font-body: Arial, sans-serif;
  --container: 1200px;
  --section-gap: 80px;
  --content-gap: 24px;
}

* { box-sizing: border-box; margin: 0; padding: 0; }

body {
  background: var(--color-bg);
  color: var(--color-text);
  font-family: var(--font-body);
  font-size: 16px;
  line-height: 1.6;
}

.container {
  max-width: var(--container);
  margin: 0 auto;
  padding: 0 24px;
}

section { padding: var(--section-gap) 0; }

h1, h2, h3 { font-family: var(--font-heading); }

.btn-primary {
  display: inline-block;
  background: var(--color-accent);
  color: var(--color-text);
  padding: 12px 24px;
  border-radius: 6px;
  font-family: var(--font-heading);
  font-weight: 600;
  text-decoration: none;
  border: none;
  cursor: pointer;
}

.btn-secondary {
  background: var(--color-text);
  color: #FFFFFF;
  padding: 12px 24px;
  border-radius: 6px;
}

.btn-ghost {
  border: 1px solid var(--color-text);
  color: var(--color-text);
  background: transparent;
  padding: 12px 24px;
  border-radius: 6px;
}
```

---

## Home Page — Estrutura Específica

```
Hero: O que é o Nex / proposta de ecossistema
↓
Seção de Produtos: cards dos 7 produtos com link
↓
Diferenciais: 3 pilares (Flexibilidade, Comunidade, Experiência)
↓
Unidades: Casa de Pedra + Francisco Rocha
↓
Depoimentos
↓
CTA final: "Venha conhecer o Nex"
```

---

## Formulários

| Produto | Tipo de formulário |
|---|---|
| Escritório Privativo | Consultivo: nome, empresa, tamanho da equipe, mensagem |
| Sala de Reunião | Rápido: data, horário, capacidade, contato |
| Eventos Corporativos | Cotação: tipo de evento, nº pessoas, data, orçamento |
| Day Pass | Mínimo: nome + email (ou compra direta) |
| Escritório Virtual | Simples: nome, tipo de empresa, plano de interesse |
| Mesa Fixa | Lead: nome, email, telefone |
| Nex House | Interesse: nome, email, breve contexto |

**Regra:** Quanto maior o ticket, mais campos são aceitáveis. Nunca adicione fricção onde há urgência.

---

## Checklist de Página

- [ ] Navbar fixo no topo com CTA
- [ ] Hero com headline clara + CTA primário
- [ ] Seções na ordem correta (Hero → Produto → Benefícios → Prova → FAQ → CTA)
- [ ] CSS com variáveis do design system Nex
- [ ] Formulário correto para o produto
- [ ] Responsivo (mobile-first)
- [ ] Nenhum gradiente usado
- [ ] Amarelo apenas em acento/CTA
- [ ] Fundo branco em todas as seções
- [ ] Tipografia: Proxima Nova nos títulos, Arial no corpo
