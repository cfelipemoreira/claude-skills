---
name: premiumcar-dashboards
description: >
  Padrões visuais e especificações para dashboards da PremiumCAR — comercial, operacional, experiência do cliente e treinamentos.
  Use SEMPRE que criar, projetar ou implementar painéis de dados, relatórios interativos, KPIs, gráficos ou qualquer
  interface de visualização de dados da PremiumCAR. Inclui estilo visual, KPIs recomendados por área, regras de gráficos,
  tabelas, filtros e estados vazios no padrão premium da marca.
---

# PremiumCAR — Dashboards

> Leia também `premiumcar-design-system` para cores, tipografia e tokens visuais.

---

## Filosofia de Dashboard

**Estilo:** Interface premium, limpa e técnica  
**Paleta:** Preto, branco, grafite e acentos metálicos suaves  
**Nunca:** Aparência de software genérico ou ERP antiquado  
**Sempre:** Estética de painel executivo de marca premium automotiva

---

## Componentes Base

### KPI Cards

```
Estrutura:
├── Valor principal (grande, bold — 32–48px)
├── Label descritiva (pequena, uppercase — 11–13px, MID_GRAY)
├── Variação percentual (12–14px — verde para positivo, vermelho para negativo)
├── Ícone sutil (24px, outline, METALLIC_SILVER)
└── Fundo: #1A1A1A (dark) ou #F7F7F5 (light)
```

**Regra:** Um KPI card = uma métrica. Sem sobrecarga.

### Charts

**Tipos preferidos:**
- Bar chart (comparativo simples)
- Line chart (tendência temporal)
- Donut chart (composição de segmentos — máx. 4 fatias)
- Area chart (volume ao longo do tempo)

**Regras:**
- Máximo 3–4 cores por gráfico
- Preferir tons neutros: grafite, prata, off-white
- Acento dourado/prata apenas para destaque de série principal
- Gridlines suaves (rgba(255,255,255,0.06) em dark)
- Sem excesso de informação — clareza acima de estética decorativa
- Labels diretas, sem truncamentos

### Tabelas

```css
/* Estilo de tabela */
th: font-size 11–12px, uppercase, letter-spacing 0.08em, MID_GRAY
td: font-size 14–15px, LINE_HEIGHT 1.5
border-bottom: 1px solid rgba(255,255,255,0.06)
hover: background rgba(255,255,255,0.03)
```

**Regras:**
- Linhas limpas, sem zebra agressiva
- Cabeçalhos discretos
- Colunas bem espaçadas
- Hover muito sutil

### Filtros

Filtros padrão disponíveis:
- Período (semana, mês, trimestre, ano)
- Tipo de serviço
- Origem do lead
- Tipo de cliente
- Consultor / vendedor
- Categoria de projeto

```
Estilo: dropdown limpo, seleção com chip refinado
Posição: topo da seção ou coluna lateral
```

### Status Badges

```
Cores por status:
- Em execução:  #BFC3C9 (Metallic Silver)
- Concluído:    #2E7D5A (Success)
- Pendente:     #C28A2C (Warning)
- Cancelado:    #B23B3B (Error)
- Agendado:     #6F6F6F (Mid Gray)

Estilo: pill, fundo sutil (10% opacidade), texto pequeno
```

---

## Dashboard Comercial

**Objetivo:** Visão de performance de vendas e leads

**KPIs principais:**
| Métrica | Descrição |
|---|---|
| Leads Gerados | Total de novos contatos no período |
| Taxa de Conversão | % leads → orçamentos fechados |
| Orçamentos Enviados | Volume de propostas no período |
| Ticket Médio | Valor médio por serviço fechado |
| Faturamento | Total realizado no período |
| Serviços Mais Vendidos | Ranking por tipo de serviço |
| Origem de Leads | Canal (Instagram, WhatsApp, Google, indicação) |

**Gráficos sugeridos:**
- Linha: faturamento mensal (12 meses)
- Barra: serviços mais vendidos
- Donut: origem de leads
- Barra empilhada: orçamentos enviados vs fechados

---

## Dashboard Operacional

**Objetivo:** Controle de produção e agenda

**KPIs principais:**
| Métrica | Descrição |
|---|---|
| Veículos em Execução | Quantos carros estão em processo agora |
| Etapa do Serviço | Status por etapa do processo |
| Prazo Médio de Execução | Tempo médio por tipo de serviço |
| Capacidade da Agenda | % da agenda ocupada |
| Gargalos | Etapas com maior tempo ou backlog |

**Gráficos sugeridos:**
- Kanban ou pipeline de status de veículos
- Barra: capacidade semanal de agenda
- Linha: prazo médio por serviço (histórico)

---

## Dashboard de Experiência do Cliente

**Objetivo:** Monitorar satisfação, fidelização e indicações

**KPIs principais:**
| Métrica | Descrição |
|---|---|
| NPS | Net Promoter Score |
| Satisfação Média | Nota média nas avaliações |
| Taxa de Recorrência | % clientes com 2+ serviços |
| Indicações | Clientes novos via indicação |
| Avaliações Recentes | Comentários e estrelas recentes |

**Gráficos sugeridos:**
- Gauge: NPS atual
- Barra: distribuição de notas (1–5)
- Linha: NPS ao longo do tempo
- KPI card: taxa de recorrência mensal

---

## Dashboard de Treinamentos

**Objetivo:** Acompanhar resultados do programa de formação

**KPIs principais:**
| Métrica | Descrição |
|---|---|
| Alunos Inscritos | Total no período |
| Turmas Abertas | Quantidade de turmas ativas |
| Taxa de Ocupação | % de vagas preenchidas |
| Origem dos Alunos | Canal de captação |
| Faturamento por Curso | Receita por tipo de treinamento |

---

## Empty States

Quando não há dados para exibir:

```
Estrutura:
├── Ícone outline (48px, MID_GRAY)
├── Título: "Nenhum dado encontrado"
├── Descrição orientativa: "Ajuste os filtros ou aguarde novos registros"
└── (Opcional) CTA para ação relevante

Nunca:
- Mostrar erro técnico visível ao usuário
- Deixar espaço em branco sem contexto
```

---

## Breakpoints

```
Desktop wide:   1400px+  → grid 4 colunas, sidebar fixa
Desktop:        1200px   → grid 3 colunas
Tablet:         768px    → grid 2 colunas
Mobile:         < 768px  → 1 coluna, KPIs empilhados
```

---

## Checklist de Dashboard

Antes de entregar qualquer dashboard:

- [ ] KPI cards visíveis no primeiro fold?
- [ ] Gráficos com máximo 4 cores?
- [ ] Filtros de período presentes?
- [ ] Empty states definidos?
- [ ] Consistência com design system (cores, tipografia, bordas)?
- [ ] Hover states em tabelas e gráficos?
- [ ] Status badges usando a paleta correta?
- [ ] Responsivo para tablet?
