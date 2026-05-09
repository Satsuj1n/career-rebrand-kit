# Felipe Campello D'Albuquerque Lima

**AI Agent Engineer Pleno** · Sistemas LLM em produção & workflows autônomos · Fundação backend em Python

<felipenehz2003@gmail.com> · (61) 99286-4664 · Brasília, DF
[linkedin.com/in/felipecampellolima](https://www.linkedin.com/in/felipecampellolima/) · [github.com/Satsuj1n](https://github.com/Satsuj1n)

**Aberto a contratos remotos em USD.**

---

## Resumo

Construo agentes de IA e sistemas LLM em produção. Fundação backend — 4 anos em engenharia de software, incluindo 2+ anos entregando serviços distribuídos em produção, pipelines assíncronos e observabilidade — agora aplicando essa base em workflows autônomos rodando em produção, não demos. Atualmente operando um agente de trading de cripto ao vivo na AWS, além de tooling em torno de Claude Code, MCP servers e orquestração de agentes.

Minha posição: agentes são software. Precisam de arquitetura, testes, observabilidade e ops — não só de um prompt esperto. É essa lacuna que eu fecho.

---

## Projetos em Destaque

### Cosmic Trader — Agente de trading de cripto em produção

Rodando ao vivo em AWS EC2, deploy via Terraform. Execução multi-estratégia com arquitetura sinal → risco → ordem, integração com Binance Futures e gestão de risco em runtime. Python.

### Claude Code Toolkit — Tooling para desenvolvimento agentico

Slash commands customizados, configurações de MCP servers, padrões de plugin e scaffolds hierárquicos de contexto para workflows agenticos em monorepos grandes. Open-source em [github.com/Satsuj1n/claude-code-setup](https://github.com/Satsuj1n/claude-code-setup).

### Agent Memory Patterns — Infraestrutura de contexto para LLMs

Scaffolds hierárquicos de CLAUDE.md, contexto por pasta, padrões de observabilidade e harnesses de evals para sistemas LLM em produção.

---

## Experiência Profissional

### Backend Java Developer — SEA Tecnologia · *Abril 2026 – Atual*

- Desenvolvimento backend na plataforma Liferay 7.4 CE — Service Builder para camada de dados, REST Builder para contratos de API, módulos OSGi.
- Workflow doc-first: ADRs, design docs e contratos escritos antes da implementação.
- Processo de code review via GitLab MRs com Conventional Commits.

### Tech Lead — ArtRadar · *Abril 2026 – Atual*

- Arquitetei e construí o ArtRadar, SaaS de inteligência do mercado de arte (analytics de leilões, galerias e feiras) — Django 5.2, DRF, Celery, PostgreSQL, Redis.
- Clean Architecture (View → Use Case → Repository) com disciplina TDD (pytest, Factory Boy); gate de coverage enforced no CI.
- Integração com provider duplo de pagamento — Stripe principal, Pagar.me fallback — para compliance e disponibilidade.
- CI/CD no GitHub Actions (lint, test, Docker build para GHCR), gunicorn em produção. Liderança de time de 2 devs.

### Full Stack Developer (Backend & Automação) — iZJob (part-time) · *Março 2026 – Atual*

- Responsabilidade ponta a ponta em soluções Full Stack para automação e RPA: design, implementação, testes e monitoramento.
- Implementação de fluxos automatizados robustos com SeleniumBase, tratando edge cases (popups, timeouts, retries) e garantindo 95%+ taxa de sucesso em execuções.
- Integração entre sistemas legados e serviços web modernos através de APIs bem estruturadas em Python/Django, com logging estruturado e alertas de falha.
- Otimização de automações com cache distribuído, throttling e paralelização — 40% de redução em tempo operacional, liberando 10+ horas/semana de processamento manual.
- Monitoramento end-to-end com dashboards e observabilidade, permitindo rastreabilidade completa de execuções e rápida identificação de gargalos.

### Full Stack Developer (Backend & DevOps) — Coco Bambu Restaurante · *Agosto 2024 – Março 2026*

- Desenvolvimento de múltiplos microserviços independentes (Python/FastAPI e Node.js) para domínios críticos (pedidos, pagamentos, integrações), com responsabilidade ponta a ponta: planejamento, implementação, deploy e observabilidade.
- Implementação de APIs escaláveis com retry logic, circuit breaker, rate limiting e event streaming (Pub/Sub) — 10.000+ requisições/dia com 99.98% de sucesso.
- Modelagem de dados com TypeORM/SQLAlchemy, otimização de queries (índices, 60% de redução em query time), cache distribuído com Redis/ElastiCache e gerenciamento de múltiplos data stores (PostgreSQL, MongoDB, Firestore).
- Deploy de 20+ serviços containerizados em Kubernetes (GCP), auto-scaling baseado em métricas, IaC (Terraform, Helm) e CI/CD (GitHub Actions, Cloud Build).
- Instrumentação com New Relic / GCP Monitoring, alertas baseados em SLOs, testes automatizados (Jest) e code reviews rigorosos. Documentação de decisões arquiteturais elevando a régua técnica do time.

### Monitor de Programação (Python & Engenharia de Software) — Universidade de Brasília (UnB) · *Agosto 2022 – Atual*

- Mentoria de 50+ estudantes em programação Python, algoritmos, estruturas de dados e boas práticas de engenharia de software.
- Foco em resolução de problemas reais, code review colaborativo e padrões de design.
- Desenvolvimento de materiais didáticos cobrindo APIs, sistemas distribuídos, otimização e SOLID — preparando alunos para desafios técnicos em ambientes profissionais.

---

## Stack

**IA / Agentes**

`Anthropic` `OpenAI` `MCP` `Claude Code` `LangChain` `RAG` `prompt engineering` `agent evals`

**Backend**

`Python` `Django` `FastAPI` `Node.js` `TypeScript` `Java` `Spring Boot` `Liferay` `REST` `GraphQL` `async workers`

**Cloud & DevOps**

`AWS` `GCP` `Terraform` `Docker` `Kubernetes` `Helm` `GitHub Actions` `Cloud Build` `Linux`

**Dados**

`PostgreSQL` `MongoDB` `Redis` `pgvector` `Firestore` `Cloud SQL`

**Automação**

`Playwright` `SeleniumBase` `headless browsers`

**Mensageria & Observabilidade**

`Pub/Sub` `RabbitMQ` `Kafka` `New Relic` `Grafana` `Prometheus` `structured logging` `SLOs`

---

## Formação Acadêmica

### Licenciatura em Computação — Universidade de Brasília (UnB) · *Em andamento*

---

## O que estou buscando

Contratos remotos (USD) onde agentes de IA fazem trabalho real — sistemas em produção, não demos — e qualidade de engenharia é inegociável. Confortável como o engenheiro de IA em um time pequeno ou solo num projeto focado. Disponível part-time ou contrato full.
