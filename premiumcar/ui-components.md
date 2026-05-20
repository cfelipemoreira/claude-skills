---
name: premiumcar-ui-components
description: >
  Biblioteca completa de componentes de UI da PremiumCAR — navbar, hero, cards de serviço, galeria, before/after,
  pilares de valor, processo, depoimentos, formulários, rodapé e todos os blocos reutilizáveis.
  Use SEMPRE que construir, revisar ou especificar componentes de interface da PremiumCAR: HTML, React, CSS, Figma,
  wireframes, especificações de design ou qualquer implementação de UI. Leia também a skill design-system para cores e tipografia.
---

# PremiumCAR — Biblioteca de Componentes UI

> Antes de implementar qualquer componente, consulte também `premiumcar-design-system` para cores, tipografia e espaçamento.

---

## NAVBAR

**Comportamento:** sticky discreto — aparecer com sombra leve ao scroll

```
Estrutura:
├── Logo (presença forte, esquerda)
├── Menu (enxuto — Home, Serviços, Projetos, Treinamentos, Contato)
└── CTA Principal → "Solicitar Orçamento" ou "Falar com Especialista"

Mobile: hamburger elegante, menu overlay premium
Desktop: navegação horizontal limpa
```

**Regras:**
- Fundo limpo (preto ou branco dependendo da página)
- Logo com presença, nunca pequeno demais
- Máximo 5 itens de menu
- CTA sempre visível — botão primário no canto direito

---

## HERO SECTION

**Objetivo:** Autoridade imediata + desejo + conversão

```
Estrutura:
├── Headline forte (56–80px, Display font)
├── Subheadline curta (18–20px, máx. 2 linhas)
├── CTA Primário → "Solicitar Orçamento"
├── CTA Secundário → "Ver Projetos" (texto com seta)
└── Imagem principal do veículo premium (protagonista absoluta)
```

**Variações de layout:**
- Imagem fullscreen com overlay escuro + texto centralizado
- Imagem à direita + texto à esquerda (split)
- Imagem background + texto no terço inferior esquerdo

**Regras:**
- Sensação: autoridade, proteção e alto padrão
- Headline deve impactar em menos de 3 segundos
- Nunca sobrecarregar com texto

---

## SERVICE CARDS

**Serviços core (5):** PPF · Vitrificação · Polimento Técnico · Lavagem Detalhada · Higienização Especial

```
Estrutura do card:
├── Imagem do serviço (ratio 16:9 ou 4:3)
├── Título do serviço (20–24px)
├── Descrição curta (2–3 linhas, body text)
├── Badge de benefício (ex: "Proteção Avançada", "Até 5 anos")
└── Link/CTA → "Saiba mais" (terciário)
```

**Grid:** 2 colunas desktop, 1 coluna mobile. 3 colunas aceitável para desktop wide.

**Regras:**
- Apresentar serviços como soluções premium, nunca como commodity
- Foco no benefício + proteção + acabamento
- Cards escuros com acento metálico sutil ou cards claros limpos

---

## PROJECT GALLERY

**Objetivo:** Prova visual de excelência e aspiração

```
Estrutura:
├── Grid premium (masonry ou grid uniforme)
├── Cards com imagem protagonista
├── Overlay discreto no hover: marca/modelo + tipo de serviço
├── Filtros opcionais (por serviço ou categoria)
└── Botão "Ver mais projetos"
```

**Regras:**
- Veículos aspiracionais (premium, esportivos, luxo)
- Mínimo de texto nos cards
- Destaque para a execução impecável
- Nunca usar imagens de baixa qualidade

---

## BEFORE/AFTER MODULE

**Objetivo:** Mostrar transformação com precisão técnica

```
Variação 1 — Slider:
├── Imagem before/after sobrepostas
├── Handle de drag elegante (linha fina + ícone sutil)
└── Labels discretos "Antes" / "Depois"

Variação 2 — Side by side:
├── Duas imagens lado a lado
├── Linha divisória central fina
└── Labels "Antes" e "Depois" acima ou abaixo
```

**Regras:**
- Nunca usar visual apelativo (cores chamativas, textos gritantes)
- A transformação deve falar por si
- Usar bordas finas e acabamento refinado

---

## VALUE PILLARS SECTION

**Blocos obrigatórios:**
1. Excelência
2. Confiança
3. Modernidade
4. Tecnologia
5. (Opcional) Detalhamento como Arte

```
Estrutura de cada pilar:
├── Ícone outline (24–32px, metallic silver)
├── Título (20–24px, uppercase controlado)
└── Descrição curta (2–3 linhas)

Layout: 4 colunas desktop / 2 colunas tablet / 1 coluna mobile
Fundo: escuro com acentos sutis ou claro clean
```

---

## PROCESS SECTION

**Etapas do processo:**
1. Diagnóstico
2. Preparação
3. Execução Técnica
4. Acabamento
5. Entrega e Orientação

```
Layout:
├── Numeração elegante (dourado ou prata sutil)
├── Título da etapa
├── Descrição curta
└── Linha conectora entre etapas (desktop: horizontal, mobile: vertical)
```

**Regras:**
- Aparência linear, premium e didática
- Reforça confiança e previsibilidade
- Sem exagero visual

---

## TESTIMONIALS

**Objetivo:** Reforçar confiança e resultado

```
Estrutura:
├── Citação curta (máx. 3 linhas, itálico sutil)
├── Nome do cliente
├── Tipo de veículo ou serviço realizado
└── Estrelas (opcional, discreta se usada)

Layout: carrossel elegante ou grid 2–3 colunas
```

**Regras:**
- Foco em confiança, resultado, atendimento e perfeição
- Nunca usar visual de review popular (sem avatares genéricos)
- Depoimentos curtos e selecionados

---

## TRAINING SECTION

**Objetivo:** Posicionar PremiumCAR como referência técnica

```
Estrutura:
├── Headline de autoridade
├── Subheadline: formação técnica premium
├── Bullets ou cards com módulos/benefícios
├── Depoimentos de alunos
└── CTA → "Saiba mais sobre treinamentos"
```

**Linguagem:** Autoridade, expertise, formação profissional real

---

## CONTACT SECTION

**Objetivo:** Maximizar conversão com mínimo de atrito

```
Estrutura:
├── Headline consultiva (ex: "Solicite uma avaliação")
├── Formulário premium (Nome, Telefone, Veículo, Serviço, Mensagem)
├── Botão WhatsApp em destaque
├── Endereço e contato claros
└── Mapa ou indicação de localização
```

**Regras:**
- Formulário refinado — labels claras, muito espaço interno, bordas sutis
- CTA deve soar consultivo, nunca urgente ou agressivo
- Sensação de atendimento exclusivo

---

## FOOTER

```
Estrutura:
├── Logo + tagline curta
├── Links essenciais (Serviços, Projetos, Treinamentos, Contato)
├── Contatos (telefone, email, WhatsApp)
├── Redes sociais (ícones outline discretos)
└── Copyright clean
```

**Regras:** Sofisticado, limpo e institucional. Nunca carregado.

---

## BADGES E SELOS

Usar com discrição — máximo 2–3 por página:

```
Exemplos:
- Proteção Avançada
- Alto Brilho
- Acabamento Premium
- Tecnologia Autoregenerativa
- Até 5 anos de proteção
- PPF Certified

Estilo: outline refinado ou fundo escuro com texto claro, borda fina dourada/prata
```

---

## FORM FIELDS

```css
/* Padrão de campo de formulário */
padding: 14px 20px;
border: 1px solid rgba(0,0,0,0.12);
border-radius: 10px;
font-size: 15px;
background: #FFFFFF ou #1A1A1A (dark mode);
transition: border-color 200ms ease;

/* Focus state */
border-color: #BFC3C9; /* Metallic Silver */
outline: none;
```

---

## CTA BAR (Conversion Bar)

**Posição:** Sticky bottom ou seção entre blocos

```
Estrutura:
├── Texto curto (ex: "Solicite uma avaliação gratuita para seu veículo")
└── Botão primário (ex: "Agendar Avaliação" ou "Falar com Especialista")
```

**Regras:** Discreta, não agressiva. Premium e direta.

---

## FAQ ACCORDION

```
Estrutura:
├── Pergunta (bold, 16px)
├── Ícone + / − (outline, sutil)
└── Resposta (body text, animação de expand suave)

Perguntas estratégicas sugeridas:
- Quanto tempo dura a vitrificação?
- PPF é adequado para qualquer veículo?
- Como funciona o processo de diagnóstico?
- O polimento remove riscos profundos?
- Qual a garantia dos serviços?
```

**Estilo:** Minimalista, sem separadores pesados. Borda fina inferior em cada item.

---

## Notas de Implementação

- Sempre priorizar `premiumcar-design-system` para tokens de cor e tipografia
- Componentes devem funcionar em dark mode (fundo escuro) e light mode (fundo claro)
- Motion padrão: `transition: all 200ms ease-out`
- Imagens sempre com `object-fit: cover` e proporções definidas
- Mobile-first, com breakpoints em 768px e 1200px
