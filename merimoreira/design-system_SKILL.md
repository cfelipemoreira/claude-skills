---
name: meri-design-system
description: Sistema de design da Meri Moreira Correspondente. Use sempre que for criar, revisar ou avaliar qualquer material visual da marca — posts de Instagram, banners, stories, peças para WhatsApp, apresentações, materiais impressos, ou qualquer elemento gráfico. Também use quando alguém pedir para "criar um post", "fazer um banner", "montar um material", ou qualquer tarefa visual relacionada à marca.
---

# Design System — Meri Moreira Correspondente

> Referência visual completa da marca. Toda peça criada deve ser consistente com este documento.

---

## 1. Identidade Visual em Resumo

**Pilares:** Elegância · Modernidade · Confiança · Humanidade
**Estilo:** Clean, com respiração generosa — não é minimalismo vazio, é clareza com intenção.

---

## 2. Paleta de Cores

### Cores Primárias

| Nome | Hex | Uso |
|------|-----|-----|
| **Branco** | `#FFFFFF` | Fundo principal, espaço, clareza |
| **Preto** | `#0A0A0A` | Tipografia, autoridade, contraste máximo |
| **Azul Caixa** | `#1C60AB` | CTAs, destaques, elementos interativos, links |

### Cores de Suporte (derivadas)

| Nome | Hex | Uso |
|------|-----|-----|
| **Azul Claro** | `#EBF3FB` | Fundos de seção, backgrounds suaves, tags |
| **Azul Médio** | `#4A85C4` | Hover states, variações do azul principal |
| **Cinza Claro** | `#F5F5F5` | Fundos alternativos, divisores suaves |
| **Cinza Texto** | `#6B7280` | Textos secundários, legendas, placeholders |
| **Preto Suave** | `#1A1A1A` | Corpo de texto principal |

### Regras de Uso de Cor

- **Branco é o rei** — deve dominar a maioria das peças
- **Azul é o acento** — nunca use em mais de 20-30% de uma peça
- **Preto ancora** — use para textos e elementos de peso
- **Nunca use laranja, vermelho, verde ou amarelo** — remetem a concorrentes bancários
- **Gradientes:** se usar, somente branco → azul claro (`#FFFFFF` → `#EBF3FB`) ou azul claro → azul (`#EBF3FB` → `#1C60AB`)

### Variações de Fundo por Contexto

| Contexto | Fundo | Texto |
|----------|-------|-------|
| Peça principal | `#FFFFFF` | `#0A0A0A` |
| Seção destaque | `#1C60AB` | `#FFFFFF` |
| Seção suave | `#EBF3FB` | `#0A0A0A` |
| Peça escura (contraste) | `#0A0A0A` | `#FFFFFF` |

---

## 3. Tipografia

### Famílias

| Papel | Família | Pesos usados |
|-------|---------|-------------|
| **Display / Títulos** | Neue Gstaad | Bold (700), SemiBold (600) |
| **Corpo / UI** | Montserrat | Regular (400), Medium (500), SemiBold (600) |

### Hierarquia Tipográfica

| Nível | Fonte | Tamanho (web) | Tamanho (social) | Peso |
|-------|-------|---------------|------------------|------|
| H1 — Título principal | Neue Gstaad | 48–64px | 60–80px | Bold |
| H2 — Subtítulo | Neue Gstaad | 32–40px | 44–56px | SemiBold |
| H3 — Seção | Montserrat | 24–28px | 32–40px | SemiBold |
| Corpo | Montserrat | 16–18px | 24–28px | Regular |
| Caption / Legenda | Montserrat | 12–14px | 18–22px | Regular |
| CTA / Botão | Montserrat | 14–16px | — | SemiBold |
| Tag / Label | Montserrat | 11–13px | — | Medium, uppercase |

### Regras Tipográficas

- **Nunca** use mais de 2 famílias em uma peça
- **Nunca** use Neue Gstaad em corpo de texto longo
- **Kerning:** sempre tight em títulos grandes (tracking: -0.02em a -0.04em)
- **Line-height:** 1.1–1.2 para títulos, 1.5–1.7 para corpo
- **Alinhamento:** Preferir à esquerda. Centralizado apenas em títulos curtos e isolados

---

## 4. Grid e Espaçamento

### Sistema de Grid

- **Web:** 12 colunas, gutter 24px, max-width 1280px
- **Social (1:1):** grid de 3x3 implícito, margem mínima de 60px
- **Stories (9:16):** zona segura superior/inferior 120px, laterais 48px

### Escala de Espaçamento (múltiplos de 8)

| Token | Valor | Uso |
|-------|-------|-----|
| `--space-1` | 4px | Micro ajustes |
| `--space-2` | 8px | Interno de componentes |
| `--space-3` | 16px | Padding padrão |
| `--space-4` | 24px | Espaço entre elementos |
| `--space-5` | 32px | Espaço entre blocos |
| `--space-6` | 48px | Seções menores |
| `--space-7` | 64px | Seções principais |
| `--space-8` | 96px | Grandes respirações |

### Margens de Segurança em Peças Sociais

- **Instagram Post (1080x1080):** margem mínima 80px em todos os lados
- **Instagram Story (1080x1920):** margem lateral 72px, superior/inferior 160px
- **WhatsApp imagem:** margem mínima 48px

---

## 5. Iconografia

**Estilo:** Linha fina (stroke width: 1.5–2px), cantos ligeiramente arredondados, proporção 24x24px base

**Temas da marca:**
- 🏠 Casa / Lar / Chave
- 📄 Documento / Contrato
- 👨‍👩‍👧 Família
- ✅ Aprovado / Check
- 🔒 Segurança / Confiança
- 📍 Localização / Curitiba
- 📱 WhatsApp / Contato

**Nunca usar:** Ícones de outros bancos, logos de concorrentes, ícones de dinheiro/cifrão em excesso (pode gerar associação negativa de "caro")

---

## 6. Fotografia e Imagem

### O que usar

- Famílias reais em frente a casas reais
- Momento da entrega das chaves
- Assinatura do contrato (mãos, caneta, papel)
- Fachadas de imóveis residenciais em Curitiba
- Expressões genuínas de alegria e alívio

### Tom fotográfico

- **Temperatura:** Levemente quente (não fria/azulada)
- **Exposição:** Bem iluminado, claro, sem sombras pesadas
- **Composição:** Planos médios e próximos, pessoas como protagonistas
- **Filtro:** Se aplicar, levíssimo — realçar brilho/contraste sem filtro óbvio

### O que evitar

- Stock photos genéricos (aperto de mão em terno, família perfeita de banco de imagem)
- Imagens de agências bancárias
- Fotos escuras, pesadas ou com mood corporativo frio
- Imagens de dinheiro em espécie ou cofres

### Tratamento de fotos em peças

- **Sobreposição de cor:** overlay azul com opacidade 20-40% em fotos de fundo
- **Recorte:** bordas retas (sem arredondamento excessivo)
- **Posição:** foto sempre subordinada ao texto — nunca compete com a mensagem

---

## 7. Bordas, Sombras e Efeitos

### Border Radius

| Elemento | Raio |
|----------|------|
| Botões | 6–8px |
| Cards | 12–16px |
| Tags/Badges | 4px ou 100px (pill) |
| Imagens | 0px (padrão) ou 8px (suave) |
| Modais | 16–20px |

### Sombras

```css
--shadow-sm: 0 1px 3px rgba(0,0,0,0.08);
--shadow-md: 0 4px 12px rgba(0,0,0,0.10);
--shadow-lg: 0 8px 32px rgba(0,0,0,0.12);
--shadow-blue: 0 4px 20px rgba(28,96,171,0.20);
```

### Efeitos permitidos

- Sombra suave em cards (nunca pesada)
- Border sutil `1px solid #E5E7EB` em cards sobre fundo branco
- Azul com leve blur como elemento decorativo de fundo

---

## 8. CSS Variables — Referência Rápida

```css
:root {
  /* Cores */
  --color-white:       #FFFFFF;
  --color-black:       #0A0A0A;
  --color-blue:        #1C60AB;
  --color-blue-mid:    #4A85C4;
  --color-blue-light:  #EBF3FB;
  --color-gray-light:  #F5F5F5;
  --color-gray-text:   #6B7280;
  --color-text:        #1A1A1A;

  /* Tipografia */
  --font-display:  'Neue Gstaad', serif;
  --font-body:     'Montserrat', sans-serif;

  /* Espaçamento */
  --space-1: 4px;   --space-2: 8px;
  --space-3: 16px;  --space-4: 24px;
  --space-5: 32px;  --space-6: 48px;
  --space-7: 64px;  --space-8: 96px;

  /* Sombras */
  --shadow-sm: 0 1px 3px rgba(0,0,0,0.08);
  --shadow-md: 0 4px 12px rgba(0,0,0,0.10);
  --shadow-blue: 0 4px 20px rgba(28,96,171,0.20);

  /* Bordas */
  --radius-sm:  6px;
  --radius-md:  12px;
  --radius-lg:  20px;
  --radius-pill: 100px;
}
```

---

## 9. Checklist de Consistência Visual

Antes de finalizar qualquer peça, verificar:

- [ ] Usa apenas as cores da paleta oficial?
- [ ] Tipografia é Neue Gstaad (títulos) + Montserrat (corpo)?
- [ ] Há margem de segurança suficiente?
- [ ] O CTA de WhatsApp está presente e visível?
- [ ] A peça parece limpa e elegante (não poluída)?
- [ ] Nenhum elemento remete a concorrentes bancários?
- [ ] Logo ou nome da marca está presente?
- [ ] A hierarquia visual está clara (o que é mais importante chama mais atenção)?
