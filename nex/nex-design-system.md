---
name: nex-design-system
description: Complete visual identity and design system for Nex Coworking. Use this skill whenever creating, reviewing, or generating any visual output for the Nex brand — UI components, landing pages, dashboards, presentations, banners, artifacts, HTML, CSS, React components, or any interface element. Must be consulted before writing any frontend code or visual layout for Nex. Trigger on requests like "crie uma página para o Nex", "faça um layout", "monte um dashboard", "design para o Nex", or any visual/interface task involving the brand.
---

# Nex — Design System

## Princípio Central

Todo output visual do Nex deve transmitir:
**limpeza, profissionalismo, contemporaneidade e hierarquia forte.**

Sem excessos. Sem gradientes. Sem cores aleatórias. Design serve a comunicação.

---

## Sistema de Cores

### Cores Primárias

| Token | Valor | Uso |
|---|---|---|
| `background-primary` | `#FFFFFF` | Fundo de todas as páginas e seções |
| `text-primary` | `#000000` | Texto principal em todo o sistema |

### Cor de Acento

| Token | Valor | Uso |
|---|---|---|
| `brand-yellow` | `#FFD400` | Destaques, ícones, CTAs, ênfase |

### Paleta Neutra

| Token | Valor | Uso |
|---|---|---|
| `white` | `#FFFFFF` | Fundos |
| `black` | `#000000` | Texto e elementos primários |
| `light-gray` | `#F5F5F5` | Fundos de seção alternados |
| `medium-gray` | `#E5E5E5` | Bordas, divisores, cards |
| `dark-gray` | `#2A2A2A` | Texto secundário, legendas |

### Regras de Uso de Cor

✅ Fundos sempre brancos  
✅ Texto primário sempre preto  
✅ Amarelo usado com parcimônia — apenas para ênfase, ícones e CTAs  
❌ Nunca usar grandes blocos amarelos como fundo  
❌ Nunca usar gradientes  
❌ Nunca usar variação excessiva de cores  

---

## Tipografia

### Fontes

| Uso | Fonte |
|---|---|
| Títulos e headings | **Proxima Nova** |
| Corpo de texto | **Arial** |

> Quando Proxima Nova não estiver disponível, usar **Inter** como fallback.

### Hierarquia Tipográfica

```css
h1 {
  font-family: 'Proxima Nova', Inter, sans-serif;
  font-weight: 700;
  font-size: clamp(48px, 6vw, 64px);
  line-height: 1.1;
}

h2 {
  font-family: 'Proxima Nova', Inter, sans-serif;
  font-weight: 600;
  font-size: clamp(32px, 4vw, 40px);
  line-height: 1.2;
}

h3 {
  font-family: 'Proxima Nova', Inter, sans-serif;
  font-weight: 600;
  font-size: clamp(24px, 3vw, 28px);
}

body {
  font-family: Arial, sans-serif;
  font-size: 16px;
  line-height: 1.6;
}

small {
  font-family: Arial, sans-serif;
  font-size: 14px;
}
```

---

## Grid e Espaçamento

| Elemento | Valor |
|---|---|
| Layout | 12 colunas |
| Container máximo | 1200px |
| Espaçamento entre seções | 80px |
| Espaçamento interno de conteúdo | 24px |
| Padding lateral mobile | 20px |

---

## Componentes UI

### Botões

```css
/* Botão Primário */
.btn-primary {
  background: #FFD400;
  color: #000000;
  border-radius: 6px;
  font-family: 'Proxima Nova', Inter, sans-serif;
  font-weight: 600;
  padding: 12px 24px;
  border: none;
}

/* Botão Secundário */
.btn-secondary {
  background: #000000;
  color: #FFFFFF;
  border-radius: 6px;
  font-weight: 600;
  padding: 12px 24px;
}

/* Botão Ghost */
.btn-ghost {
  border: 1px solid #000000;
  color: #000000;
  background: transparent;
  border-radius: 6px;
  padding: 12px 24px;
}
```

### Cards de Produto/Workspace

```css
.workspace-card {
  background: #FFFFFF;
  border: 1px solid #E5E5E5;
  border-radius: 8px;
  padding: 24px;
  transition: box-shadow 0.2s ease;
}

.workspace-card:hover {
  box-shadow: 0 4px 20px rgba(0,0,0,0.08);
}
```

### Navbar

```css
.navbar {
  background: #FFFFFF;
  color: #000000;
  font-family: 'Proxima Nova', Inter, sans-serif;
  position: fixed;
  top: 0;
  width: 100%;
  /* Logo: esquerda | Nav: centro | CTA: direita */
}
```

### Ícones

- Estilo: line icons (minimal)
- Cor padrão: `#000000`
- Variação com acento: `#FFD400`

---

## Estrutura de Seções

### Hero Section

```
background: #FFFFFF
título: Proxima Nova 700, 56px
subtítulo: Arial, 18px, #2A2A2A
CTA primário: botão amarelo
CTA secundário: botão ghost ou link
```

### Feature Section (3 colunas)

```
grid: 3 colunas
ícone: line icon, acento amarelo
título: Proxima Nova 600
texto: Arial 16px
```

### Testimonial Section

```
layout: blocos de citação
aspas: destaque em amarelo
nome: Proxima Nova 600
empresa: Arial, dark-gray
```

---

## Dashboards

```
background: #FFFFFF
texto: #000000
acento em dados: #FFD400
gráficos: minimal, gridlines em #E5E5E5
highlight de métrica: amarelo
cards de métrica: bordas sutis, sombra leve
```

---

## Regras Absolutas de Design

| Regra | Status |
|---|---|
| Fundo branco como base | Obrigatório |
| Texto primário preto | Obrigatório |
| Amarelo apenas como acento | Obrigatório |
| Títulos em Proxima Nova | Obrigatório |
| Corpo em Arial | Obrigatório |
| Layout limpo com espaço generoso | Obrigatório |
| Hierarquia tipográfica clara | Obrigatório |
| Sem gradientes | Proibido |
| Sem fundos amarelos grandes | Proibido |
| Sem excesso de variação de cores | Proibido |

---

## Filosofia Visual

O design do Nex é **arquitetônico**: limpo, funcional, com intenção clara em cada elemento. Cada componente existe para comunicar, não para decorar.

Palavras-chave do design: `clean` · `architectural` · `professional` · `modern` · `high contrast` · `generous whitespace`
