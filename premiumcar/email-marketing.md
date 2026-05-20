---
name: premiumcar-email-marketing
description: >
  Sistema completo de email marketing para a PremiumCAR: fluxos de automação, sequências de nutrição,
  templates de campanhas, emails de pós-venda e jornadas de cliente.
  Use SEMPRE que criar fluxos de automação de email, sequências de CRM, campanhas de email, newsletters,
  comunicações de pós-venda ou qualquer estratégia de relacionamento por email para a PremiumCAR.
---

# PremiumCAR — Email Marketing

> Todo email da PremiumCAR deve parecer comunicação de uma marca premium automotiva, não newsletter genérica.
> Leia `premiumcar-language` para manter voz e tom corretos.

---

## Princípios de Email Marketing PremiumCAR

1. **Qualidade > Quantidade** — menos emails, mais relevantes
2. **Tom consultivo** — nunca parecer panfleto
3. **Valor em cada envio** — informação útil ou resultado visual
4. **CTA único** — um objetivo por email
5. **Personalização básica** — nome + veículo quando disponível

---

## Fluxos de Automação

### Fluxo 01 — Boas-Vindas (Lead Novo)

**Trigger:** Lead preencheu formulário ou entrou em contato

```
Email 1 — Imediato: Confirmação + próximos passos
Email 2 — Dia 2:    O que nos diferencia (processo + materiais)
Email 3 — Dia 5:    Serviços e casos de uso para o perfil do lead
Email 4 — Dia 10:   CTA para agendar avaliação
```

**Email 1 — Confirmação:**
```
Assunto: Recebemos seu contato, [Nome]

Olá, [Nome]!

Recebemos seu interesse e nossa equipe está pronto para te atender.

Em breve um de nossos especialistas vai entrar em contato para entender
melhor seu veículo e recomendar a solução ideal.

Enquanto isso, você pode conhecer nossos projetos recentes:
→ [Ver Projetos]

Até logo,
Equipe PremiumCAR
```

**Email 2 — Diferencial:**
```
Assunto: Por que o processo faz toda a diferença

[Nome], o cuidado com um veículo premium começa muito antes da execução.

Na PremiumCAR, cada projeto passa por diagnóstico detalhado, seleção
de materiais específicos e execução técnica por especialistas.

É a diferença entre um resultado bom e um resultado impecável.

→ [Conheça nosso processo]
```

---

### Fluxo 02 — Pós-Serviço

**Trigger:** Serviço concluído e entregue

```
Email 1 — Dia 1:   Pós-venda + instruções de manutenção
Email 2 — Dia 7:   Como está o resultado? Pesquisa de satisfação
Email 3 — Dia 30:  Dicas de cuidado para o serviço realizado
Email 4 — Dia 90:  Próximo serviço recomendado / revisita
```

**Email 1 — Pós-venda:**
```
Assunto: Cuidados para manter seu [serviço] impecável

[Nome], foi um prazer cuidar do seu [veículo]!

Para preservar o resultado pelo maior tempo possível, seguem
as principais recomendações de manutenção:

• [Cuidado 1 específico do serviço]
• [Cuidado 2]
• [Cuidado 3]

Qualquer dúvida, estamos à disposição.

→ [Fale conosco no WhatsApp]
```

---

### Fluxo 03 — Reengajamento

**Trigger:** Lead inativo há 60+ dias sem conversão

```
Email 1 — Dia 60:   Resultado visual impactante + CTA suave
Email 2 — Dia 75:   Conteúdo educativo relevante
Email 3 — Dia 90:   Último contato com CTA direto
```

---

### Fluxo 04 — Renovação / Recorrência

**Trigger:** 6–12 meses após último serviço (dependendo do serviço)

```
Email 1:  "Seu [serviço] pode estar precisando de atenção"
Email 2:  Dicas de quando revisar cada tipo de proteção
Email 3:  CTA para agendamento de revisão
```

---

## Templates de Campanha

### Campanha de Novo Serviço
```
Assunto: Conheça [novo serviço] — [benefício principal]

[Nome],

Apresentamos [nome do serviço]: [descrição em 1 linha].

[Parágrafo de benefício principal — 3 linhas]

[Parágrafo de diferencial técnico — 2 linhas]

→ [Saiba mais] ou [Agendar avaliação]
```

### Campanha de Galeria / Projeto
```
Assunto: [Marca do veículo] transformado — veja o resultado

[Nome],

Acabamos de concluir mais um projeto que vale a pena você ver.

[Descrição do projeto em 2 linhas]

O processo durou X dias e envolveu [serviços realizados].

→ [Ver o projeto completo]
```

### Newsletter Mensal
```
Assunto: PremiumCAR em [Mês] — projetos, dicas e novidades

[Nome],

Confira o que aconteceu no estúdio este mês:

🔹 Projeto em destaque: [Veículo + Serviço]
🔹 Dica técnica: [Tema do mês]
🔹 No blog: [Título do artigo]

→ [Ver tudo]
```

---

## Regras de Design para Emails

**Layout:**
- Largura máxima: 600px
- Fundo: branco (#FFFFFF) ou grafite profundo (#0A0A0A)
- Tipografia: sistema (Arial, Helvetica) — segurança de renderização
- Font size: mínimo 15px para body, 24px+ para headlines

**Imagens:**
- Sempre incluir alt text
- Máximo 1–2 imagens por email
- Veículo de alta qualidade quando usar imagem

**CTA:**
- Botão único por email
- Fundo preto, texto branco
- Texto curto: máx. 5 palavras
- Borda-radius: 8–12px

**Rodapé obrigatório:**
- Link de descadastro
- Endereço da empresa
- Copyright PremiumCAR

---

## Métricas e Benchmarks

| Métrica | Benchmark Saudável |
|---|---|
| Taxa de abertura | 25–40% |
| Taxa de clique (CTR) | 3–8% |
| Taxa de conversão | 1–3% |
| Taxa de descadastro | < 0.5% |
| Taxa de spam | < 0.1% |

---

## Segmentação de Lista

**Segmentos recomendados:**
- Leads novos (< 30 dias)
- Leads antigos sem conversão (> 60 dias)
- Clientes ativos (serviço nos últimos 6 meses)
- Clientes inativos (> 12 meses sem serviço)
- Por tipo de serviço (PPF, vitrificação, polimento)
- Por tipo de veículo (premium, luxo, esportivo)
- Interessados em treinamentos

**Personalização possível:**
- `[Nome]` — obrigatório em todos os emails
- `[Veículo]` — quando disponível no CRM
- `[Último serviço]` — para fluxos de recorrência
- `[Especialista responsável]` — para humanizar follow-ups
