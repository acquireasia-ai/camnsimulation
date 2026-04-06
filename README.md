# CAMN Simulation — Powered by MiroFish

> **Customer Acquisition Multi-agent Network (CAMN) Simulation Engine**
> Built on [MiroFish](https://github.com/666ghj/MiroFish) — A Simple and Universal Swarm Intelligence Engine

---

## Overview

This repository adapts MiroFish's swarm intelligence engine for **CAMN (Customer Acquisition Multi-agent Network) simulation** use cases. MiroFish was originally designed to construct high-fidelity parallel digital worlds where thousands of agents with independent personalities, long-term memory, and behavioral logic freely interact to forecast real-world outcomes.

CAMN Simulation repurposes this engine to model, rehearse, and optimize **customer acquisition funnels, agent-driven outreach networks, and market penetration strategies** — before a single real dollar or message is spent.

---

## What is CAMN?

A **Customer Acquisition Multi-agent Network** is a distributed system of AI agents, each representing a participant in the acquisition ecosystem:

| Agent Role | Real-world Analogue |
|---|---|
| Prospect Agent | Potential customer with modeled psychographic traits |
| Outreach Agent | Sales rep, affiliate, or AI-driven messenger |
| Channel Agent | Platform (LinkedIn, WhatsApp, email, social) |
| Qualifier Agent | Lead scoring and intent signal detector |
| Conversion Agent | Closer, onboarding flow, or demo handler |
| Retention Agent | Post-sale success, upsell, and churn prevention |

MiroFish provides the **runtime infrastructure** — agent memory, interaction logic, temporal evolution, and emergent behavior reporting — that makes a CAMN simulation tractable and high-fidelity.

---

## How MiroFish Maps to CAMN

### 1. Graph Building → Prospect Universe Construction

MiroFish's **Graph Building** stage extracts seed information and constructs a GraphRAG (graph-based retrieval-augmented generation) memory layer.

In CAMN, this translates to:
- Ingesting ICP (Ideal Customer Profile) documents, LinkedIn exports, or CRM dumps as **seed materials**
- Extracting entity relationships (company → decision maker → pain point → buying signal)
- Building a **prospect graph** where edges represent influence, referral likelihood, or co-buying signals

```
Seed Input: ICP report + product pitch deck + competitor analysis
→ MiroFish Graph Builder
→ Output: Interconnected prospect universe with persona nodes and relationship edges
```

### 2. Environment Setup → Acquisition Channel Configuration

MiroFish's **Environment Setup** stage generates agent personas and configures behavioral parameters.

In CAMN, this maps to:
- Generating **prospect personas** from ICP data (role, seniority, industry, objections, preferred channels)
- Configuring **outreach agent behavior** (tone, cadence, channel preference, follow-up thresholds)
- Setting **channel environment rules** (LinkedIn message limits, email deliverability, WhatsApp opt-in constraints)

Each simulated prospect agent carries:
- Long-term memory of prior touchpoints
- Personality parameters (skepticism index, urgency, budget authority)
- Behavioral rules (when to engage, when to ghost, when to refer)

### 3. Simulation → Acquisition Funnel Rehearsal

MiroFish's **Dual-platform Parallel Simulation** runs thousands of agent interactions simultaneously with dynamic temporal memory updates.

In CAMN, this is the **acquisition funnel playbook rehearsal**:
- Run N simulation rounds, each representing a campaign cycle (e.g., 30-day outreach sprint)
- Inject variables mid-simulation: "What if we add a free trial?" or "What if we reduce price by 20%?"
- Observe emergent outcomes: conversion clusters, churn patterns, referral cascades, objection hotspots
- Compare simulation variants (A/B test different messaging, sequences, or channel mixes)

```
Simulation Input: Outreach sequence v1 vs v2, with 500 prospect agents
→ MiroFish Simulation Engine (OASIS-powered)
→ Output: Predicted conversion rates, drop-off points, optimal follow-up timing
```

### 4. Report Generation → Campaign Intelligence Reports

MiroFish's **ReportAgent** generates deep interaction reports after simulation completes.

In CAMN, the ReportAgent produces:
- **Funnel analytics**: Stage-by-stage conversion breakdown across all agent interactions
- **Persona heat maps**: Which prospect archetypes converted, which ghosted, which referred
- **Objection clustering**: Most common rejection reasons and counter-messaging recommendations
- **Channel attribution**: Which outreach channels drove the highest-quality engagement
- **Revenue projection**: Extrapolated pipeline value based on simulation outcomes

### 5. Deep Interaction → Live Strategy Iteration

MiroFish's **Deep Interaction** layer lets you chat with any agent in the simulated world post-run.

In CAMN, this enables:
- Interviewing a **simulated prospect** to understand why they didn't convert
- Querying the **ReportAgent** for what-if analysis ("What if we targeted CFOs instead of CMOs?")
- Injecting new market events mid-conversation ("A competitor just dropped pricing — how does the funnel change?")
- Iterating messaging live without re-running a full simulation

---

## CAMN-Specific Use Cases

### Market Entry Simulation (Singapore / Philippines)
Upload a market research report and product brief as seed material. Configure prospect agents representing local SME owners, enterprise procurement teams, or consumer segments. Simulate 60 days of outreach across LinkedIn, email, and WhatsApp channels. Receive a predicted conversion curve and recommended go-to-market sequence before launch.

### Affiliate Network Optimization
Model a multi-tier affiliate structure as a CAMN. Each affiliate is an Outreach Agent with configurable performance traits (reach, conversion rate, niche audience). Simulate referral cascades and identify which affiliate archetypes drive the highest downstream acquisition at lowest cost.

### SaaS Onboarding Funnel Testing
Seed the engine with product onboarding documentation and user personas. Simulate the first 30 days post-signup across cohorts. Identify drop-off points, feature adoption blockers, and upsell trigger moments before rolling out to real users.

### Competitive Displacement Campaign
Inject a competitor's public pricing and feature sheet as a market event. Simulate how prospect agents re-evaluate their current vendor. Identify which segments are most displaceable and what messaging accelerates switching behavior.

---

## Architecture

```
acquireasia-ai/camnsimulation
│
├── backend/
│   ├── app/api/              # REST endpoints: graph, simulation, report
│   ├── app/services/         # Core engine services
│   │   ├── graph_builder.py          # Prospect universe graph construction
│   │   ├── oasis_profile_generator.py # Agent persona generation
│   │   ├── simulation_manager.py     # Funnel simulation orchestration
│   │   ├── simulation_runner.py      # CAMN agent interaction runtime
│   │   ├── report_agent.py           # Campaign intelligence report generation
│   │   └── zep_graph_memory_updater.py # Long-term agent memory (Zep Cloud)
│   └── scripts/
│       ├── run_parallel_simulation.py  # Multi-variant A/B simulation
│       ├── run_twitter_simulation.py   # Social channel simulation
│       └── run_reddit_simulation.py    # Community/forum channel simulation
│
├── frontend/
│   └── src/components/
│       ├── Step1GraphBuild.vue     # Prospect universe upload & build
│       ├── Step2EnvSetup.vue       # Channel & persona configuration
│       ├── Step3Simulation.vue     # Funnel simulation run panel
│       ├── Step4Report.vue         # Campaign intelligence dashboard
│       └── Step5Interaction.vue    # Live agent query interface
│
└── locales/                # i18n support (en, zh)
```

---

## Quick Start

### Prerequisites

| Tool | Version |
|---|---|
| Node.js | 18+ |
| Python | ≥3.11, ≤3.12 |
| uv | Latest |

### 1. Configure Environment

```bash
cp .env.example .env
```

```env
# LLM API (OpenAI-compatible — recommended: Alibaba Qwen-plus or GPT-4o)
LLM_API_KEY=your_api_key
LLM_BASE_URL=https://dashscope.aliyuncs.com/compatible-mode/v1
LLM_MODEL_NAME=qwen-plus

# Zep Cloud — long-term agent memory
ZEP_API_KEY=your_zep_api_key
```

### 2. Install & Run

```bash
npm run setup:all   # Install all dependencies (frontend + backend)
npm run dev         # Start both services
```

| Service | URL |
|---|---|
| Frontend UI | http://localhost:3000 |
| Backend API | http://localhost:5001 |

### Docker

```bash
cp .env.example .env
docker compose up -d
```

---

## Upstream

This repository is a fork of [666ghj/MiroFish](https://github.com/666ghj/MiroFish), maintained by [AcquireAsia AI](https://github.com/acquireasia-ai). The simulation engine is powered by [OASIS (Open Agent Social Interaction Simulations)](https://github.com/camel-ai/oasis) by the CAMEL-AI team.

---

## License

Inherits upstream license from MiroFish. See [LICENSE](./LICENSE).
