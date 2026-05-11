# FHIT PRO — Financial Health Intelligence Technology

> Demo version of FHITpro, its an web app to help with money and health management.
> Plataforma integrada de saúde financeira e física para indivíduos e organizações.

---

## Visão Geral

O **FHIT PRO** é uma plataforma digital completa que combina gestão financeira, avaliação de saúde física e ferramentas de RH organizacional em um único dashboard inteligente. Com recursos de IA, gamificação e análise de dados em tempo real, a plataforma ajuda usuários a tomarem decisões melhores sobre suas finanças e bem-estar.

---

## Funcionalidades Principais

### Financeiro
- **Dashboard de KPIs** — Indicadores financeiros em tempo real
- **Lançamentos** — Controle de receitas e despesas com categorização inteligente
- **Planejamento Mensal** — Orçamento mensal com metas e alertas
- **Histórico de Renda** — Análise temporal da evolução da renda
- **Balanço Patrimonial** — Patrimônio líquido, ativos e passivos
- **CFPB** — Avaliação de bem-estar financeiro baseada no Consumer Financial Protection Bureau
- **Ranking Financeiro** — Comparativo de saúde financeira com benchmarks
- **Simulador de Investimentos** — Projeções e cenários de investimento
- **Renda Passiva** — Rastreamento de fontes de renda passiva
- **Cofrinho** — Controle de metas de poupança
- **Cartão de Crédito** — Análise de gastos no cartão
- **Contas em Atraso** — Alertas de vencimentos e inadimplência
- **Faixa de Renda IBGE** — Posicionamento socioeconômico

### Saúde & Bem-estar
- **Avaliação de Saúde** — Métricas de performance física
- **Gamificação** — Sistema de badges, níveis e conquistas
- **Desafios Semanais** — Metas comportamentais e de saúde
- **Especialista FHIT** — Assistente virtual com IA para orientação financeira e de saúde

### RH & Organizacional
- **Gestão de RH** — Estrutura organizacional e colaboradores
- **Dashboard de Gestores** — Visão consolidada por setor, departamento e divisão
- **Controle de Turnos** — Gestão de escalas de trabalho
- **Multi-empresa** — Administração de múltiplas empresas

### IA & Tecnologia
- **OCR de Recibos** — Captura automática de despesas por foto
- **Análise de Gastos com IA** — Categorização inteligente de despesas
- **Comandos de Voz** — Entrada por áudio
- **Exportação** — Relatórios em PDF e Excel

---

### Lançamentos
<img width="1787" height="934" alt="image" src="https://github.com/user-attachments/assets/6f780f3d-ab58-40d6-9758-9666d7318031" />

> Controle de receitas e despesas com categorização inteligente e histórico detalhado.

<!-- Adicione aqui a foto da tela de lançamentos -->
| | |
|---|---|
| ![Lançamentos]() | ![Lançamentos - Detalhe]() |

---

### Especialista FHIT
<img width="1800" height="935" alt="image" src="https://github.com/user-attachments/assets/9e4558e8-77df-4094-8034-a031a416e704" />

> Assistente virtual com IA que oferece orientação personalizada sobre saúde financeira e física.

<!-- Adicione aqui a foto da tela do Especialista -->
| | |
|---|---|
| ![Especialista FHIT]() | ![Especialista FHIT - Chat]() |

---

### Planejamento Mensal
<img width="1846" height="934" alt="image" src="https://github.com/user-attachments/assets/1eb87330-babe-41ba-bc69-23cfae7971bc" />
<img width="1264" height="676" alt="image" src="https://github.com/user-attachments/assets/4c246be2-3ad6-42f2-8738-93c1b33cdea1" />


> Orçamento mensal inteligente com categorias personalizáveis, metas e alertas de desvio.

<!-- Adicione aqui a foto da tela de planejamento mensal -->
| | |
|---|---|
| ![Planejamento Mensal]() | ![Planejamento Mensal - Categorias]() |

---

### Histórico de Renda
<img width="1856" height="932" alt="image" src="https://github.com/user-attachments/assets/89f7e9dd-4c10-47b9-9452-7352f0c82a6b" />


> Evolução temporal da renda com análise de tendências e comparativo com faixas do IBGE.

<!-- Adicione aqui a foto da tela de histórico de renda -->
| | |
|---|---|
| ![Histórico de Renda]() | ![Histórico de Renda - Gráfico]() |

---

### Balanço Patrimonial
<img width="1856" height="936" alt="image" src="https://github.com/user-attachments/assets/13425aba-0dbd-4493-8dcf-7b573dca66de" />


> Visão consolidada do patrimônio líquido, ativos, passivos e fundo de emergência.

<!-- Adicione aqui a foto da tela do balanço patrimonial -->
| | |
|---|---|
| ![Balanço Patrimonial]() | ![Balanço Patrimonial - Detalhe]() |

---

## Stack Tecnológica

| Camada | Tecnologia |
|---|---|
| Frontend | React 18, Vite, TailwindCSS, Radix UI |
| Animações | Framer Motion |
| Gráficos | Recharts |
| Backend | Node.js, Express, TypeScript |
| Banco de Dados | Supabase (PostgreSQL) |
| Autenticação | Supabase Auth |
| Deploy | Vercel |
| IA / OCR | Google Cloud Vision |
| Exportação | jsPDF, XLSX |

---

## Arquitetura

```
FHITPRO/
├── frontend/         
│   └── src/
│       ├── components/    # Componentes por feature
│       ├── pages/         # Páginas (Login, Dashboard, etc.)
│       ├── services/      # Camada de dados e API
│       ├── contexts/      # Gerenciamento de estado global
│       └── hooks/         # Hooks reutilizáveis
├── backend/           # Node.js + Express
│   └── src/
│       ├── routes/        # Endpoints da API
│       └── lib/           # Configuração do Supabase
├── api/               # Serverless functions (Vercel)
└── docs/              # Documentação técnica
```

---

## Controle de Acesso

O FHIT PRO implementa controle de acesso baseado em papéis (RBAC) com três níveis de acesso e Row Level Security (RLS) no banco de dados.

| Papel | Descrição |
|---|---|
| `user` | Usuário básico (B2C) |
| `b2c_1/2/3` | Tiers de cliente B2C |
| `b2b_1/2/3` | Tiers de cliente B2B |
| `gestor_setor` | Gestor de setor |
| `gestor_departamento` | Gestor de departamento |
| `gestor_divisao` | Gestor de divisão |
| `gestor_rh` | Gestor de RH |
| `adm_fhit` | Administrador FHIT |
| `adm_geral` | Administrador geral |

---

## Instalação e Desenvolvimento

### Pré-requisitos

- Node.js >= 20.19.1
- npm >= 9

### Configuração

```bash
# Clone o repositório
git clone <url-do-repositório>

# Instale as dependências (raiz, frontend e backend)
npm install
cd frontend && npm install
cd ../backend && npm install
```

### Variáveis de Ambiente

Copie os arquivos de exemplo e preencha com suas credenciais:

```bash
cp frontend/src/.env.example frontend/src/.env
```

Variáveis necessárias:

```env
VITE_SUPABASE_URL=
VITE_SUPABASE_ANON_KEY=
VITE_GOOGLE_CLOUD_API_KEY=
```

### Rodando em Desenvolvimento

```bash
# Inicia frontend (porta 3000) e backend simultaneamente
npm run dev
```

### Build para Produção

```bash
npm run build
```

---

## Deploy

O projeto é configurado para deploy na **Vercel** via `vercel.json`. O frontend é servido como SPA e o backend como serverless functions.

---

## Documentação

Documentação técnica adicional disponível em `/docs`:

- `SUPABASE_RLS_GUIDE.md` — Configuração de Row Level Security
- `GOOGLE_OAUTH_GUIDE.md` — Configuração do OAuth Google
- `DOMAIN_CONFIGURATION.md` — Configuração de domínio

---

## Licença

Propriedade da FHIT PRO. Todos os direitos reservados.
