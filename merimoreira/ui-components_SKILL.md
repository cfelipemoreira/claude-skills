---
name: meri-ui-components
description: Biblioteca de componentes de UI para a Meri Moreira Correspondente. Use sempre que for criar ou codificar elementos de interface — botões, cards, formulários, banners, headers, seções, badges, e qualquer componente HTML/CSS/React para o site ou materiais digitais da marca. Também use quando alguém pedir "criar um componente", "codificar uma seção", "fazer o botão de WhatsApp", ou qualquer tarefa de frontend para a marca.
---

# UI Components — Meri Moreira Correspondente

> Biblioteca de componentes prontos para uso. Todos usam as CSS variables do Design System.
> Importar sempre o Design System antes de usar estes componentes.

---

## 0. Setup Base

```html
<!-- Google Fonts -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&display=swap" rel="stylesheet">
<!-- Neue Gstaad deve ser importada via licença/CDN próprio -->

<style>
:root {
  --color-white:      #FFFFFF;
  --color-black:      #0A0A0A;
  --color-blue:       #1C60AB;
  --color-blue-mid:   #4A85C4;
  --color-blue-light: #EBF3FB;
  --color-gray-light: #F5F5F5;
  --color-gray-text:  #6B7280;
  --color-text:       #1A1A1A;
  --color-whatsapp:   #25D366;

  --font-display: 'Neue Gstaad', Georgia, serif;
  --font-body:    'Montserrat', sans-serif;

  --space-1: 4px;  --space-2: 8px;   --space-3: 16px;
  --space-4: 24px; --space-5: 32px;  --space-6: 48px;
  --space-7: 64px; --space-8: 96px;

  --shadow-sm:   0 1px 3px rgba(0,0,0,0.08);
  --shadow-md:   0 4px 12px rgba(0,0,0,0.10);
  --shadow-blue: 0 4px 20px rgba(28,96,171,0.20);

  --radius-sm:   6px;
  --radius-md:   12px;
  --radius-lg:   20px;
  --radius-pill: 100px;
}

* { box-sizing: border-box; margin: 0; padding: 0; }
body { font-family: var(--font-body); color: var(--color-text); }
</style>
```

---

## 1. Botões

### Botão Primário (Azul)

```html
<button class="btn btn-primary">Falar com a Meri</button>

<style>
.btn {
  display: inline-flex;
  align-items: center;
  gap: var(--space-2);
  padding: 14px 28px;
  font-family: var(--font-body);
  font-size: 15px;
  font-weight: 600;
  border: none;
  border-radius: var(--radius-sm);
  cursor: pointer;
  transition: all 0.2s ease;
  text-decoration: none;
}

.btn-primary {
  background: var(--color-blue);
  color: var(--color-white);
  box-shadow: var(--shadow-blue);
}

.btn-primary:hover {
  background: #1650A0;
  transform: translateY(-1px);
  box-shadow: 0 6px 24px rgba(28,96,171,0.30);
}
</style>
```

### Botão WhatsApp (CTA principal)

```html
<a href="wa.me/5541997381963" class="btn btn-whatsapp" target="_blank">
  <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
    <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/>
    <path d="M12 0C5.373 0 0 5.373 0 12c0 2.123.553 4.116 1.523 5.845L.057 23.492a.5.5 0 0 0 .614.61l5.79-1.516A11.95 11.95 0 0 0 12 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 22a9.955 9.955 0 0 1-5.085-1.392l-.364-.217-3.773.988.996-3.686-.238-.38A9.956 9.956 0 0 1 2 12C2 6.477 6.477 2 12 2s10 4.477 10 10-4.477 10-10 10z"/>
  </svg>
  Falar no WhatsApp
</a>

<style>
.btn-whatsapp {
  background: var(--color-whatsapp);
  color: var(--color-white);
  box-shadow: 0 4px 16px rgba(37,211,102,0.30);
}

.btn-whatsapp:hover {
  background: #1DA851;
  transform: translateY(-1px);
}
</style>
```

### Botão Outline

```html
<button class="btn btn-outline">Saiba mais</button>

<style>
.btn-outline {
  background: transparent;
  color: var(--color-blue);
  border: 2px solid var(--color-blue);
}

.btn-outline:hover {
  background: var(--color-blue);
  color: var(--color-white);
}
</style>
```

---

## 2. Cards

### Card de Serviço

```html
<div class="service-card">
  <div class="service-card__icon">🏠</div>
  <h3 class="service-card__title">Financiamento Imobiliário</h3>
  <p class="service-card__desc">
    Cuidamos de toda a documentação e processo junto à Caixa. 
    Do início ao fim — sem filas, sem complicação.
  </p>
  <a href="wa.me/5541997381963" class="service-card__link">
    Saiba mais →
  </a>
</div>

<style>
.service-card {
  background: var(--color-white);
  border: 1px solid #E5E7EB;
  border-radius: var(--radius-md);
  padding: var(--space-6);
  transition: all 0.25s ease;
  display: flex;
  flex-direction: column;
  gap: var(--space-3);
}

.service-card:hover {
  border-color: var(--color-blue);
  box-shadow: var(--shadow-blue);
  transform: translateY(-3px);
}

.service-card__icon {
  font-size: 32px;
  line-height: 1;
}

.service-card__title {
  font-family: var(--font-display);
  font-size: 20px;
  font-weight: 700;
  color: var(--color-black);
}

.service-card__desc {
  font-size: 15px;
  line-height: 1.6;
  color: var(--color-gray-text);
  flex: 1;
}

.service-card__link {
  font-size: 14px;
  font-weight: 600;
  color: var(--color-blue);
  text-decoration: none;
  margin-top: auto;
}

.service-card__link:hover { text-decoration: underline; }
</style>
```

### Card de Depoimento

```html
<div class="testimonial-card">
  <div class="testimonial-card__stars">★★★★★</div>
  <blockquote class="testimonial-card__quote">
    "Não acreditava que ia conseguir. Em 40 dias as chaves estavam na minha mão."
  </blockquote>
  <div class="testimonial-card__author">
    <div class="testimonial-card__name">Carlos M.</div>
    <div class="testimonial-card__meta">Sítio Cercado · FGTS + MCMV</div>
  </div>
</div>

<style>
.testimonial-card {
  background: var(--color-blue-light);
  border-radius: var(--radius-md);
  padding: var(--space-6);
  display: flex;
  flex-direction: column;
  gap: var(--space-4);
  border-left: 4px solid var(--color-blue);
}

.testimonial-card__stars {
  color: #F59E0B;
  font-size: 18px;
  letter-spacing: 2px;
}

.testimonial-card__quote {
  font-family: var(--font-display);
  font-size: 18px;
  font-weight: 600;
  line-height: 1.5;
  color: var(--color-black);
  font-style: normal;
}

.testimonial-card__name {
  font-weight: 600;
  font-size: 14px;
  color: var(--color-black);
}

.testimonial-card__meta {
  font-size: 13px;
  color: var(--color-gray-text);
}
</style>
```

### Card de Credencial (Barra de Trust)

```html
<div class="trust-bar">
  <div class="trust-item">
    <span class="trust-item__icon">🏛️</span>
    <span class="trust-item__text">Correspondente Credenciada Caixa</span>
  </div>
  <div class="trust-item">
    <span class="trust-item__icon">📅</span>
    <span class="trust-item__text">+15 Anos de Experiência</span>
  </div>
  <div class="trust-item">
    <span class="trust-item__icon">✅</span>
    <span class="trust-item__text">Centenas de Aprovações</span>
  </div>
  <div class="trust-item">
    <span class="trust-item__icon">📍</span>
    <span class="trust-item__text">Curitiba e Região</span>
  </div>
</div>

<style>
.trust-bar {
  background: var(--color-gray-light);
  padding: var(--space-4) var(--space-7);
  display: flex;
  justify-content: center;
  gap: var(--space-7);
  flex-wrap: wrap;
}

.trust-item {
  display: flex;
  align-items: center;
  gap: var(--space-2);
}

.trust-item__icon { font-size: 20px; }

.trust-item__text {
  font-size: 14px;
  font-weight: 600;
  color: var(--color-black);
  white-space: nowrap;
}
</style>
```

---

## 3. Badge / Tag

```html
<span class="badge badge--blue">Minha Casa Minha Vida</span>
<span class="badge badge--outline">FGTS</span>
<span class="badge badge--dark">+15 Anos</span>

<style>
.badge {
  display: inline-block;
  padding: 4px 12px;
  border-radius: var(--radius-pill);
  font-size: 12px;
  font-weight: 600;
  font-family: var(--font-body);
  letter-spacing: 0.03em;
  text-transform: uppercase;
}

.badge--blue     { background: var(--color-blue); color: white; }
.badge--outline  { border: 1.5px solid var(--color-blue); color: var(--color-blue); }
.badge--dark     { background: var(--color-black); color: white; }
.badge--light    { background: var(--color-blue-light); color: var(--color-blue); }
</style>
```

---

## 4. Hero Section

```html
<section class="hero">
  <div class="hero__content">
    <span class="badge badge--light">Correspondente Credenciada Caixa</span>
    <h1 class="hero__title">Sua casa própria<br>começa aqui.</h1>
    <p class="hero__subtitle">
      Cuidamos de todo o processo de financiamento Caixa — do FGTS ao 
      Minha Casa Minha Vida. Mais de 15 anos realizando sonhos em Curitiba.
    </p>
    <div class="hero__actions">
      <a href="https://wa.me/5541997381963?text=Olá%20Meri!%20Vim%20pelo%20site." 
         class="btn btn-whatsapp" target="_blank">
        💬 Falar no WhatsApp
      </a>
      <a href="#servicos" class="btn btn-outline">Ver serviços</a>
    </div>
  </div>
</section>

<style>
.hero {
  min-height: 90vh;
  display: flex;
  align-items: center;
  background: var(--color-white);
  padding: var(--space-8) var(--space-7);
}

.hero__content {
  max-width: 640px;
  display: flex;
  flex-direction: column;
  gap: var(--space-4);
}

.hero__title {
  font-family: var(--font-display);
  font-size: clamp(48px, 6vw, 80px);
  font-weight: 700;
  line-height: 1.05;
  letter-spacing: -0.03em;
  color: var(--color-black);
}

.hero__subtitle {
  font-size: 18px;
  line-height: 1.6;
  color: var(--color-gray-text);
  max-width: 520px;
}

.hero__actions {
  display: flex;
  gap: var(--space-3);
  flex-wrap: wrap;
  margin-top: var(--space-2);
}
</style>
```

---

## 5. WhatsApp Floating Button (Mobile)

```html
<a href="https://wa.me/5541997381963" class="whatsapp-float" target="_blank" aria-label="WhatsApp">
  <svg width="28" height="28" viewBox="0 0 24 24" fill="white">
    <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413z"/>
  </svg>
</a>

<style>
.whatsapp-float {
  position: fixed;
  bottom: 24px;
  right: 24px;
  width: 60px;
  height: 60px;
  background: var(--color-whatsapp);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 4px 20px rgba(37,211,102,0.4);
  z-index: 999;
  transition: transform 0.2s ease;
}

.whatsapp-float:hover { transform: scale(1.08); }
</style>
```

---

## 6. FAQ Accordion

```html
<div class="faq">
  <div class="faq__item">
    <button class="faq__question" onclick="toggleFaq(this)">
      O serviço tem custo para o cliente?
      <span class="faq__icon">+</span>
    </button>
    <div class="faq__answer">
      <p>Não. O correspondente é remunerado pela Caixa Econômica Federal. 
      Os únicos custos são os de cartório e documentação, que existem em 
      qualquer financiamento independente de onde você faça.</p>
    </div>
  </div>
</div>

<style>
.faq { max-width: 720px; margin: 0 auto; }

.faq__item {
  border-bottom: 1px solid #E5E7EB;
  padding: var(--space-2) 0;
}

.faq__question {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: var(--space-4) 0;
  background: none;
  border: none;
  font-family: var(--font-body);
  font-size: 16px;
  font-weight: 600;
  color: var(--color-black);
  cursor: pointer;
  text-align: left;
  gap: var(--space-4);
}

.faq__question:hover { color: var(--color-blue); }

.faq__icon {
  font-size: 22px;
  font-weight: 300;
  color: var(--color-blue);
  flex-shrink: 0;
  transition: transform 0.2s;
}

.faq__answer {
  display: none;
  padding-bottom: var(--space-4);
  color: var(--color-gray-text);
  line-height: 1.7;
  font-size: 15px;
}

.faq__item.open .faq__answer { display: block; }
.faq__item.open .faq__icon { transform: rotate(45deg); }
</style>

<script>
function toggleFaq(btn) {
  const item = btn.parentElement;
  item.classList.toggle('open');
}
</script>
```

---

## 7. Process Steps (Como Funciona)

```html
<div class="steps">
  <div class="step">
    <div class="step__number">01</div>
    <div class="step__content">
      <h3 class="step__title">Análise Gratuita</h3>
      <p class="step__desc">Nos conte sua situação: renda, FGTS, imóvel. 
      A gente vê o que é possível — sem compromisso.</p>
    </div>
  </div>
  <!-- repetir para cada passo -->
</div>

<style>
.steps { display: flex; flex-direction: column; gap: var(--space-6); }

.step {
  display: flex;
  gap: var(--space-5);
  align-items: flex-start;
}

.step__number {
  font-family: var(--font-display);
  font-size: 48px;
  font-weight: 700;
  color: var(--color-blue-light);
  line-height: 1;
  min-width: 64px;
  /* border trick for elegance */
  -webkit-text-stroke: 2px var(--color-blue);
  color: transparent;
}

.step__title {
  font-family: var(--font-display);
  font-size: 20px;
  font-weight: 700;
  color: var(--color-black);
  margin-bottom: var(--space-2);
}

.step__desc {
  font-size: 15px;
  line-height: 1.6;
  color: var(--color-gray-text);
}
</style>
```

---

## 8. Responsividade — Breakpoints

```css
/* Mobile first */
/* SM  */ @media (min-width: 640px)  { ... }
/* MD  */ @media (min-width: 768px)  { ... }
/* LG  */ @media (min-width: 1024px) { ... }
/* XL  */ @media (min-width: 1280px) { ... }

/* Utilitários mobile */
.hide-mobile { display: none; }
@media (min-width: 768px) { .hide-mobile { display: unset; } }
```
